---
title: "Blog 1"
date: "2025-10-02"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---


# Arctic: Automated Desktop Application Testing

*by Elif Aslan and David Alvarez | on 10 MAY 2025 | in AWS Java Development, Developer Tools, Java, Open Source, Technical How-to*

---

The Amazon Corretto team delivers more than 75 OpenJDK bundles for various platforms and Java versions. These builds include the **AWT** and **Swing** UI libraries. Since a button needs to look like a button after a Java update, and even the smallest change can have a significant impact on how graphical elements are rendered, we need to validate each release to ensure we do not introduce regressions.

Validating interactive desktop applications as part of an automated build pipeline is **difficult**. Although solutions exist, they are limited in scope and usually require tests to be specifically written to support the automation. Adapting existing tests can be a time consuming process, and in some scenarios may not be possible. Falling back to manual verification is slow and does not scale.

> **Arctic** supports existing tests intended to be run manually, and is agnostic about how tests were written. It relies on the operating system to capture all required events at recording time and then reproduce them during replay time. Arctic can thus operate with older tests that were not written with automation in mind, **without the need to modify them**.

Arctic runs on Linux, Windows, and macOS on x86\_64 systems and on Linux and macOS on aarch64 systems.

---

## How does Arctic work?

First, a test is run manually with Arctic in **“recording mode”** to capture a baseline set of screenshots. During recording, all keyboard and mouse events, as well as screenshots, are saved whenever instructed. Later, the recording is used to replay the original sequence of mouse and keyboard events while recording a new set of screenshots. Arctic then compares the two sets of screenshots to validate that they are the same.

A distinguishing Arctic feature is support for scenarios where a **perfect pixel match is not possible**.

* **“The workbench”**: A special window drawn in the background by Arctic at recording time, which determines the area of the screen Arctic will pay attention to.
* **“Shades”**: Other windows that can be used to hide parts of the test that are not relevant or may appear randomly.
* Arctic supports **multiple image comparison mechanisms** to differentiate between minor fluctuations (like a single isolated pixel or a slight color deviation) and material differences.

Even with these features, Arctic may report a test failure that a human would consider acceptable. Arctic includes a way to review failed image comparisons, and those that are considered valid can be added as **approved alternatives** to be used in the next iteration of tests.

### Other Arctic features are:

* Configurable image comparators for screenshots
* Session persistence and restoration to review results later on a different platform
* Automatic removal of redundant events for test playback
* Test playback speed control to run tests faster than originally recorded
* Configurable logging
* Overlays to help humans locate differences between two images

---

## How do I start using Arctic?

### Arctic configuration

Arctic is a Java application, requiring at least **JDK 11** to run, but **JDK 21 is recommended**.

Configuration is done using the **`recorder.properties`** and **`player.properties`** files, read from the current working directory.

### Test environment configuration

As Arctic relies on **pixel comparison**, changes to the test environment may cause **false positives**. Common problematic settings include:

* Desktop background
* Screen resolution
* UI theme
* Installed fonts

NOTE: The demo app was prepared on **MacOS**.

### Download Arctic

* [Arctic binaries](https://github.com/amazon-corretto/arctic)
* [Arctic source code](https://github.com/amazon-corretto/arctic)

### Arctic control keys

Control is achieved by pressing specific key combinations (modifier keys like `ctrl` or `alt` followed by an instruction).

* You can check keycodes by running: `java -jar arctic-<VERSION>.jar -k`.
* By default: `ctrl+alt+z` (starts/stops a recording) and `ctrl+alt+x` (captures a screenshot).

### Recording a test

1.  Start Arctic in **recording mode**: `java -jar arctic-<VERSION>.jar -r`.
2.  Adjust the **Workbench** and **Shade** windows.
3.  Tell Arctic which test is running: `java -jar arctic-<VERSION>.jar -c test start <testName> <testCase>`.
4.  Start the recording, manually interact with the application, and **take a screenshot** every time a relevant UI change occurs.
5.  Stop recording.

Screenshots and recordings are saved in the `tests` folder (configured via `arctic.common.testPath = ../tests`).

### Replay a test

1.  Launch Arctic in **player mode**: `java -jar arctic-<VERSION>.jar -p`.
2.  Instruct Arctic to run the test: `java -jar arctic-<VERSION>.jar -c test start <testName> <testCase>`.
3.  Inform Arctic when the test is finished: `java -jar arctic-<VERSION>.jar test finish <testName> <testCase> <result>`.

> If `result` is **true** and all screenshots are considered good enough, Arctic will mark the test as **ok**. Otherwise, it will be marked as **failed**.

---

## Getting Arctic results

Results can be exported using the command: `java -jar arctic-<VERSION>.jar <format> save <filename>`.

| Format (`<format>`) | Description |
| :--- | :--- |
| `xml` | JUnit XML report |
| `tap` | TAP version 13 |
| `jtx` | **jtHarness** exclusion file (for failed tests) |

### Review screenshot comparisons

Failed comparisons can be reviewed using the Arctic command `sc`. For example, `java -jar arctic-<VERSION>.jar -c sc all` will start a review of all failed screenshots in the current session, allowing you to add the current screenshot as an alternative.

---

## What’s next? Where can I learn more and how can I get involved?

The Amazon Corretto team appreciates any feedback and questions.

* Please visit the GitHub repository at [Arctic github repository](https://github.com/amazon-corretto/arctic) to learn more, report problems, and contribute.
* **Demo video:** [https://youtu.be/diA0IPl-bEU](https://youtu.be/diA0IPl-bEU)

---

### Acknowledgement

We would like to acknowledge the following open source projects that made Arctic possible:

* jNativeHook
* Apache Commons Configuration
* Google Gson
* Google Guice
* Junit
* Mockito
* Slf4j
* Lombok
* Checkstyle
* Gradle

---

### Author Bios

#### Elif Aslan

Software Engineer at AWS specializing in JDK projects, release engineering, and system design.

#### David Alvarez

David has been a Software Development Engineer in Amazon for over ten years, focusing on different aspects of OpenJDK. You can find him on GitHub as **@alvdavi**.
