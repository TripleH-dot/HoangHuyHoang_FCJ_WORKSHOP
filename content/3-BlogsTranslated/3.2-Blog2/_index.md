---
title: "Blog 2"
date: "2025-10-02"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---


# Rocket Simplifies the Homebuying Experience with Amazon Bedrock Agents

*by Manali Sapre, Seshidhar Raghupathi, Axel Larsson, and Sajjan AVS | on 10 MAY 2025 | in Amazon Bedrock Agents, Amazon Bedrock Knowledge Bases, Artificial Intelligence, Customer Solutions, Generative AI, Responsible AI*

---

Rocket Companies is a Detroit-based FinTech company with the mission to **“Help Everyone Home.”** While best known as a mortgage lender, Rocket's mission spans the entire homeownership journey, from finding the perfect home, purchasing, financing, to leveraging home equity. Rocket has thrived by taking complexity and making it simple, empowering clients to navigate the homeownership journey through intuitive technology solutions. Rocket’s website and mobile apps combine home search, financing, and servicing into a seamless experience. By combining data analytics and 11PB of data with cutting-edge automation, Rocket accelerates every process from loan approval to post-closing service, all while maintaining personalization at scale.

Rocket's client-first approach is central to everything they do. With customizable digital tools and expert guidance from seasoned mortgage professionals, Rocket aims to match every client with the right product and support, quickly, accurately, and securely.

With the advent of **generative AI**, Rocket saw an opportunity to go further. The homebuying process can still feel overwhelming for many. This led Rocket to ask: How can we provide the trusted guidance clients expect at any time, on any channel? The result is the **Rocket AI Agent**, a conversational AI assistant designed to transform how clients interact with Rocket’s digital platforms. Built on **Amazon Bedrock Agents**, the Rocket AI Agent combines deep domain knowledge, personalized guidance, and the ability to execute meaningful actions on the client’s behalf. Since its launch, it has become a central part of Rocket’s client experience. Clients who interact with the Rocket AI Agent are **three times more likely to close on a loan** than those who do not.

Because it is embedded directly within Rocket’s web and mobile services, it delivers precise support when and where clients need it. This article explores how Rocket realized that vision using Amazon Bedrock Agents, ushering in a new era of always-on, deeply personalized, and action-capable AI-powered support.

## Introducing the Rocket AI Agent: Personalized AI Guidance for Homeownership

The Rocket AI Agent is now available across the majority of Rocket’s websites and mobile applications. It is assisting clients through the loan origination process, servicing, and even within Rocket’s third-party broker system (**Rocket Pro**), essentially meeting clients wherever they digitally interact with Rocket. The Rocket AI Agent is designed to be more than just an answer bot. It delivers real-time personalized guidance and takes action when necessary. It provides:

* **24/7 multi-language support** through Rocket’s web and mobile services.
* **Contextual awareness**. The Rocket AI Agent knows which page a client is viewing and tailors its response based on that context.
* **Real-time answers** on mortgage options, interest rates, documentation, and processes.
* **Guided self-service actions**, such as filling out a pre-approval form or scheduling a payment.
* **Personalized experiences** utilizing Rocket’s proprietary data and user context.
* **Seamless hand-off** to Rocket Mortgage professionals when human assistance is required.

Whether someone wants to know why their escrow changed or how to qualify for a refinance, the Rocket AI Agent is designed to respond with clarity, confidence, and action.

---

## Amazon Bedrock Agents

**Amazon Bedrock Agents** is a fully managed, cloud-based capability that enables customers to quickly build, test, and scale agentic AI applications on Amazon Web Services (AWS). With built-in integration and security, customers like Rocket use Amazon Bedrock Agents to safely and reliably accelerate from initial experimentation to production.

These agents extend **foundation models (FMs)** by using the **Reasoning and Acting (ReAct) framework**, allowing them to interpret user intent, plan and execute tasks, and seamlessly integrate with enterprise data and APIs just like a knowledgeable digital assistant.

The agents use the FM to analyze the user request, break it down into actionable steps, retrieve relevant data, and trigger underlying APIs to complete the task. This allows the Rocket AI Agent to move beyond passive support into **proactive assistance**, helping clients navigate complex financial processes in real time.

Key Amazon Bedrock Agents capabilities utilized in the Rocket AI Agent include:

* **Agent instructions** – sets the agent’s goal and persona (e.g., mortgage servicing expert), enabling goal-driven behavior.
* **Amazon Bedrock Knowledge Bases** – provides rapid, accurate information retrieval from Rocket’s Learning Center and other internal documents.
* **Action groups** – defines secure operations, like submitting a lead or scheduling a payment, that the agent can execute via Rocket’s backend services.
* **Agent memory** – the ability to remember allows the Rocket AI Agent to maintain contextual awareness across multiple turns of conversation, enhancing the user experience with more natural and personalized interactions.
* **Amazon Bedrock Guardrails** – supports Rocket’s responsible AI goals by ensuring the agent stays within appropriate topical boundaries.

By combining structured reasoning with the ability to act across multiple systems, Amazon Bedrock Agents helps the Rocket AI Agent deliver **outcomes, not just answers**.

---

## How the Rocket AI Agent Works: Architecture Overview

The Rocket AI Agent is a centralized capability deployed across Rocket’s digital platforms, designed for scalability, flexibility, and per-task accuracy. At the core of the architecture is a growing network of **domain-specific agents**, currently numbering eight, each focusing on discrete functions like loan origination, servicing, or broker support. These agents coordinate through a unified interface to deliver seamless, context-aware support.

The three foundational elements that make up the Rocket AI Agent architecture are:

1.  **Client initiation:** A client uses the chat functionality in the Rocket mobile app or website.
2.  **Rocket AI Agent API:** Provides a unified API interface for the agents powering the chat functionality.
3.  **Agent routing:** The AI Agent API routes the request to the correct Amazon Bedrock agent based on static criteria (e.g., web or mobile) or LLM-powered intent identification.
4.  **Agent processing:** The agent breaks down the task, determines the appropriate sequence, and executes actions and knowledge retrieval.
5.  **Task execution:** The agent utilizes data within Rocket’s knowledge base to find information, sends results to the client, and performs actions.
6.  **Guardrails:** Enforces Rocket’s responsible AI policies by blocking out-of-scope topics or language.
7.  **Prompt management:** Helps Rocket manage the library of prompts for the agents and optimize for specific FMs.

This modular and scalable design allows Rocket to serve diverse client needs effectively and consistently across the entire homeownership journey.

---

## Impact and Results

Since the launch of the Rocket AI Agent, we have seen transformative improvements across the client journey and internal operations:

* **Threefold increase** in conversion rates from web traffic to closed loans, as the Rocket AI Agent captures leads 24/7, even outside of normal business hours.
* **Increased operational efficiency**, particularly through chat containment. With the AI assistant deployed to help prospects explore Rocket’s offerings, Rocket has seen an **85% decrease** in hand-offs to the care desk and a **45% reduction** in hand-offs to servicing specialists. This reduction in human agent hand-offs has freed up team capacity to focus on more complex and high-impact client needs.
* **Higher Customer Satisfaction (CSAT)** scores, with 68% of clients giving high satisfaction ratings on servicing and origination-related chat interactions. Key drivers include fast response times, clear communication, and accurate information, all contributing to increased client trust and reduced friction in the experience.
* **Increased client engagement**, as users complete more tasks on their own, driven by the intuitive and personalized self-service capabilities.
* **Greater personalization and flexibility**. The Rocket AI Agents adapt to each client’s stage in the homeownership journey and their preferences, providing the ability to escalate to a banker based on the client’s condition. This personalized support reflects Rocket’s core mission — “Help Everyone Home,” by meeting clients right where they are and giving them the confidence to move forward.
* **Expanded language support**, including Spanish language assistance, to better serve a diverse and growing client base.

The Rocket AI Agent is not only making it easier for clients to understand and navigate financial processes, but is also helping Rocket employees be more effective, freeing up their time for high-value conversations with clients.

---

## Lessons Learned

Throughout the development and deployment of the Rocket AI Agent, the Rocket team learned several key lessons that shaped both the technical strategy and the overall client experience. These insights can serve as valuable guidance for other organizations building generative AI applications at scale:

* **Curate your data carefully**: The quality of generative AI-produced responses is directly tied to the quality and structure of the source data. Rocket built its enterprise knowledge base using **Amazon Bedrock Knowledge Bases**, which internally uses **Amazon Kendra** to retrieve data from Rocket’s content libraries, including FAQs, compliance documents, and servicing workflows.
* **Limit the agent’s scope per task**: Rocket found that limiting each agent's scope to **3–5 actions** makes them easier to maintain, test, and perform more efficiently. For example, the payment agent focuses only on tasks like scheduling payments and providing due dates, while the refinance agent handles rate simulations and lead capture. Each agent capability uses **Amazon Bedrock action groups** with well-documented interfaces and independently monitored task completion rates.
* **Prioritize graceful escalation**: Escalation is not failure; it’s a critical part of building user trust. Rocket implemented **uncertainty thresholds** using confidence scores and specific keyword triggers to detect when an interaction might require human assistance. In those cases, the Rocket AI Agent proactively transfers the chat session to a live support agent or gives the user the option to escalate. This approach avoids frustrating conversational loops and ensures that complex or sensitive situations are handled with the appropriate level of human care.
* **Expect user behavior to evolve**: Real-world user behavior is constantly changing. Clients will interact with the system in unexpected ways, and behavioral patterns also change over time. Investing in **observability** and user feedback loops is essential for rapid adaptation.
* **Using cross-Region inference from the start**: To deliver scalable model performance and high stability, Rocket enabled **cross-Region inference** from the start of development. This allows inference requests to be routed to the optimal AWS Region within the supported area, improving model latency and availability by automatically distributing the load based on capacity. During high-traffic periods, such as product launches or interest rate fluctuations, this architecture helps Rocket avoid Regional service quota limits, maintain responsiveness, and increase throughput by leveraging compute capacity from multiple AWS Regions. The result is a smoother and more consistent user experience, even during unpredictable load spikes.

These lessons reinforce that while generative AI can unlock powerful possibilities, careful implementation is key to delivering sustainable value and a trustworthy experience.

---

## Next Steps: Moving Toward Multi-Agent Collaboration

Rocket is just beginning to realize the potential of agentic AI. Building on the success of the domain-specific agents, the next phase focuses on extending these capabilities through **multi-agent collaboration** powered by Amazon Bedrock Agents. This evolution will allow Rocket to orchestrate agents across multiple domains and deliver intelligent, **end-to-end experiences** that truly reflect the complexity of the real client journey.

By enabling agents to seamlessly work together, Rocket is laying the groundwork for a future where AI not only responds to questions but proactively navigates entire workflows, from discovery and qualification to servicing and beyond.

### Benefits for Rocket

Multi-agent collaboration marks a transformative step in Rocket’s journey to build agentic AI-powered experiences, redefining homeownership, from the first question to the final signature. By allowing multiple **specialized agents** to coordinate within a single conversation, Rocket can unlock a new level of intelligence, automation, and personalization across all its digital services.

* **End-to-end personalization**: By allowing multiple domain-specific agents (like refinance, servicing, and loan options) to share context and coordinate, Rocket can deliver smarter and more relevant responses that evolve in real time with the client's homeownership journey.
* **Back-office integration**: With the ability to invoke secure backend APIs and workflows, agents allow Rocket to begin automating parts of back-office operations, such as document verification, progress tracking, and lead routing, improving speed, accuracy, and operational efficiency.
* **Context switching**: Seamlessly switching between servicing, origination, and refinancing within the same chat session.
* **Orchestration**: Handling multi-step tasks that span various Rocket business units.

With multi-agent orchestration, Rocket is building the foundation for an always-on, deeply personalized assistant that doesn't just answer questions, but delivers tangible outcomes—from finding a home to closing a loan. This is the next chapter in Rocket’s mission: **“Help Everyone Home.”**

---

## Conclusion

The Rocket AI Agent is more than a digital assistant—it’s an entirely new approach to client engagement, powered by agentic AI. By combining **Amazon Bedrock Agents** with Rocket’s proprietary data and backend systems, the company has created a smarter, highly scalable, and more human experience that’s available 24/7, without the wait.

To dive deeper into building intelligent multi-agent applications with Amazon Bedrock Agents, you can explore the AWS workshop **Unified User Experiences with Hierarchical Multi-Agent Collaboration**. This hands-on workshop includes open-source code and best practices drawn from real-world financial services implementations, illustrating how multi-agent systems can automate complex workflows to deliver next-generation client experiences.

Rocket sums it up simply: “Together with AWS, we are just getting started. Our goal is to empower every client to move forward with confidence, and ultimately, to **Help Everyone Home**.”

---

## About the Authors

#### Manali Sapre

Senior Director at Rocket Mortgage, with over 20 years of experience leading transformative technology initiatives across the company. Her passion lies in solving complex challenges through collaboration, mentoring the next generation of technology leaders, and creating intuitive, high-impact experiences.

#### Seshidhar Raghupathi

Software architect at Rocket, with over 12 years of experience driving innovation, scalability, and system resiliency across AI and client communication platforms. He plays a key role in developing Rocket's first cloud-native digital mortgage application and has since led numerous critical initiatives to enhance intelligent and personalized client experiences.

*Seshidhar Raghupathi is a Principal Engineer at Rocket, focused on generative AI and enterprise automation solutions.*

#### Venkata Santosh Sajjan Alla

Senior Solution Architect at AWS Financial Services, where he drives AI-powered digital transformation in the North America FinTech sector. He specializes in AI/ML, Generative AI, and cloud-native architectures. You can connect with him on LinkedIn.

#### Axel Larsson

Senior Solution Architect at AWS, working in the greater New York City area. He supports clients in the FinTech space and has a passion for helping them transform their business models through cloud technology and AI.
