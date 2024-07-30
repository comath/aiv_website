---
layout: post
title: DEFCON 32 Friday Schedule
author: AI Village
date: 2024-07-30 09:00:00 +0900
category: "defcon 32"
toc: true
---

## Removing the Ring of Gyges: Lessons from Securing AI Systems Against File Format Abuse
===================================

Abstract
--------

This talk will focus on the implications of our work defending AI based cybersecurity systems against file format abuse for the design of AI systems for cyber. The audience will learn how the interface between traditional cybersecurity systems and the AI models being integrated into them impacts security. File format abuse enables polyglot files to bypass state-of-the-art malware detection systems (EDR tools) that utilize machine learning in an attempt to catch novel forms of malware. The polyglot file is sent to the wrong model because the embedded file type is not detected. Existing file type, file carving, and polyglot detection tools are insufficient to detect polyglots used by threat actors in the wild. However, we trained a machine learning model capable of detecting all polyglot types in our dataset, which is based on threat actor usage of polyglots in the wild, with over 99.9% accuracy. Content disarm and reconstruct (CDR) tools can also be used to disarm polyglots, but are not effective on all file types. 


Authors
-------
1. Sean Oesch <oeschts@ornl.gov> (Oak Ridge National Laboratory)
2. Luke Koch <kochlr@ornl.gov> (Oak Ridge National Laboratory)
3. Brian Weber <weberb@ornl.gov> (Oak Ridge National Laboratory)
4. Amul Chaulagain <chaulagaina@ornl.gov> (Oak Ridge National Laboratory)
5. Matthew Dixson <dixsonmk@ornl.gov> (Oak Ridge National Laboratory)
6. Jared Dixon <dixonjm@ornl.gov> (Oak Ridge National Laboratory)
7. Cory Watson <watsoncl1@ornl.gov> (Oak Ridge National Laboratory)

Talk type
---------
Short (20 minutes)

Topics
------
* Attacks against AI systems
* Using AI in defensive operations

## Photoshop Fantasies
===================================

Abstract
--------
The possibility of an altered photo revising history in a convincing way highlights a salient threat of imaging technology. After all, seeing is believing. Or is it? The examples history has preserved make it clear that the observer is more often than not meant to understand that something has changed. Surprisingly, the objectives of photographic manipulation have remained largely the same since the camera first appeared in the 19th century. The old battleworn techniques have simply evolved to keep pace with technological developments. In this talk, we will learn about the history of photographic manipulation, from the invention of the camera to the advent of generative AI. Importantly, we will consider the reception of photo editing and its relationship to the notion of reality, which is more significant than the technologies themselves. Surprisingly, we will discover that creative myth making has found a new medium to embed itself in. This talk is based on Walter Scheirer's recent book A History of Fake Things on the Internet (Stanford University Press 2023). 

Author
------
Walter Scheirer <walter.scheirer@nd.edu> (University of Notre Dame)

Talk type
---------
Long (45 minutes)

Topics
------
* AI and social risks
* AI enabled creativity
* Fairness, ethics, and transparency


## Incubated Machine Learning Exploits: Backdooring ML Pipelines Using
Input-Handling Bugs
===================================

Abstract
--------

Machine learning (ML) pipelines are vulnerable to model backdoors that compromise the integrity of the underlying system. Although many backdoor attacks limit the attack surface to the model, ML models are not standalone objects. Instead, they are artifacts built using a wide range of tools and embedded into pipelines with many interacting components. 

In this talk, we introduce incubated ML exploits in which attackers inject model backdoors into ML pipelines using input-handling bugs in ML tools. Using a language-theoretic security (LangSec) framework, we systematically exploited ML model serialization bugs in popular tools to construct backdoors. In the process, we developed malicious artifacts such as polyglot and ambiguous files using ML model files. We also contributed to Fickling, a pickle security tool tailored for ML use cases. Finally, we formulated a set of guidelines for security researchers and ML practitioners. By chaining system security issues and model vulnerabilities, incubated ML exploits emerge as a new class of exploits that highlight the importance of a holistic approach to ML security. 


Author
------
Suha Sabi Hussain <suhashussain1@gmail.com> (Trail of Bits)

Talk type
---------
Long (45 minutes)

Topics
------
* Attacks against AI systems
* Defenses for AI systems


## BOLABuster: Harnessing LLMs for Automating BOLA Detection
===================================

Abstract
--------
Broken Object Level Authorization (BOLA) is a prevalent vulnerability in modern APIs and web
applications, ranked as the top risk in the OWASP API top 10 and the fourth most reported vulnerability type in HackerOne Global Top 10. The consequences of BOLA can be severe, from sensitive data exposure to a total loss of system control. 

While manually verifying or triggering known BOLAs is typically straightforward, automatically identifying the correct execution sequences and generating viable input values for testing BOLAs is challenging. The complexities of application and business logic, the wide range of input parameters, and the stateful nature of modern web applications all hinder existing static analysis tools from detecting unknown BOLAs. 	

To overcome these challenges, we leverage LLM's reasoning and generative capabilities to automate tasks that were previously done manually. These tasks include understanding application logic, uncovering endpoint dependency relationships, generating test cases, and interpreting test results. When combined with heuristics, this AI-backed method enables fully automated BOLA detection at scale. We dub this research BOLABuster.

Although BOLABuster is still in its early stages, it has already discovered multiple new vulnerabilities in open-source projects. In one instance, we submitted 15 CVEs for one project, some leading to critical privilege escalation. Our most recent disclosed vulnerability was CVE-2024-1313, a BOLA vulnerability in Grafana, an open-source project used by over 20 million users.

When benchmarked against other state-of-the-art fuzzing tools using applications with known BOLAs, BOLABuster, on average, sends less than 1% of the API requests to a target server to uncover a BOLA.

In this talk, we will share our methodology and the lessons learned from our research. We invite you to join us to learn about our journey with AI and explore a new approach to conducting vulnerability research.


Authors
-------
1. Ravid Mazon <rmazon@paloaltonetworks.com> (Palo Alto Networks)
2. Jay Chen <jaychen@paloaltonetworks.com> (Palo Alto Networks)

Talk type
---------
Long (45 minutes)

Topics
------
* AI enabled creativity
* Using AI in offensive operations


## My Conversations with a GenAI-Powered Virtual Kidnapper
===================================

Abstract
--------

For the past few weeks, I've been seeing how far I can push several commercially available GenAI systems past their ethical boundaries. ... hint: it's way too far.

In this talk, I'll demonstrate how I was able to turn LLMs into a powerful backend for realtime, interactive voice enabled cyber scams. I'll share my prompting strategy, the backend systems used, and show how each of these are working innocently in their own right, but enable massive possibilities for deception and harm when combined (in their current form). 


Author
------
Perry Carpenter <perryc@knowbe4.com> (KnowBe4, Inc.)

Talk type
---------
Short (20 minutes)

Topics
------
* AI and social risks
* Attacks against AI systems
* Defenses for AI systems


## Evaluations and Guardrails against Prompt Injection attacks on LLM powered-applications
===================================

Abstract
--------
Prompt injections are a class of attacks against LLM-powered applications that exploit the inclusion of untrusted user inputs in LLM prompts. We give an overview of two open source frameworks developed by Meta related to understanding and mitigating prompt injection risks:

-  our *CyberSecEval Prompt Injection benchmarks* (evaluations of the propensity of popular LLMs to succumb to prompt injection when used without guardrails), 

- as well as *Prompt Shield* which includes *direct and indirect prompt injection scanners* (open-source models for identifying risky inputs to LLM-powered applications).

**Findings of interest:**

- *Evaluating foundation model vulnerability to indirect prompt injection:* LLMs can be trained to have contextual awareness of which parts of the input prompt are coming from a trusted user versus an untrusted third party - in particular via inclusion of a system prompt. We share our benchmark for direct and indirect prompt injection susceptibility of foundational LLMs (across a wide variety of attack strategies)  introduced as part of CyberSecEval (an open-source suite of benchmarks for measuring the cybersecurity risks of foundational models). We present the results of these evaluations for currently-popular foundational LLMs. We conclude that model conditioning is not enough to defend against indirect prompt injection risks in most contexts, even with the usage of a system prompt.

- *Guardrailing against prompt injection attacks in real applications:* We present PromptShield, a pair of open-source direct and indirect prompt injection detection models. We highlight the differences between our models and existing malicious prompt detectors (which largely only address direct prompt injection or jailbreaking risks), and the specific risks that can be prevented by utilizing our guardrail in LLM-powered applications. We also show how the model can be fine-tuned to improve application-specific performance.


Authors
-------
1. Cyrus Nikolaidis <cyni@meta.com> (Meta Platforms, Inc)
2. Faizan Ahmad <fa7pdn@meta.com> (Meta Platforms, Inc)

Talk type
---------
Short (20 minutes)

Topic
-----
* Attacks against AI systems


## On Your Ocean's 11 Team, I'm the AI Guy (technically Girl)
===================================

Abstract
--------
One of the best parts of DEF CON is the glitz and glam of Vegas, the gambling capital of the world. Many have explored hacking casinos (on and off stage). Unfortunately, it’s just not like it is portrayed in the Oceans franchise.. in real life there’s much less action, no George Clooney, and it’s a lot harder to pull off a heist than it seems. 

Well fortunately I’m not your typical hacker, I’m an AI hacker. I use adversarial machine learning techniques to disrupt, deceive and disclose information from Artificial Intelligence systems. 
I chose my target carefully: Canberra Casino. It’s the best casino in my city.. It’s also the only casino but that’s not the point. 

The casino industry is at an interesting inflection point. Many large casinos have already adopted AI for surveillance and gameplay monitoring, smaller casinos are starting to make the transition, and there’s only a couple of companies in the world that provide this software. It’s ripe for exploitation. 

In this talk I’m going to show you how I bypassed casino AI systems - facial recognition, surveillance systems and game monitoring. AI Security is the new cyber security threat, and attacks on AI systems could have broad implications including misdiagnoses in medical imaging, navigation errors in autonomous vehicles.. and successful casino heists.

Author
------
Harriet Farlow <harrietfarlow@gmail.com>

Talk type
---------
Long (45 minutes)

Topics
------
* Attacks against AI systems
* Using AI in defensive operations
* Using AI in offensive operations


## AI’ll be watching you. Greybox Attacks against an Embedded AI
===================================

Abstract
--------
AI’ll be watching you will cover attacking an embedded AI on a family of popular security cameras with over 100,000 combined reviews on Amazon. The camera’s embedded AI system is used for on-device person detection, a system that filters notifications based on whether a person is detected. Traditionally the camera would alert the owner if any motion was detected, meaning that an attacker would have to have no motion be detected, but now with the embedded AI making decisions, an attacker needs to only appear not to be human. While this may seem a simple task, dressing up as a giant bush would be noticeable by the people around the attacker, meaning that a successful attack against this system requires the on-camera AI to be tricked while not alerting nearby people to any suspicious disguises.

In this talk we will cover the steps we took to research and gain access to the device in order to perform greybox attacks against its embedded AI. We will demonstrate how we rooted an older version of the device to gain access to how the models were brought to the camera. We will show how the knowledge we gained while reverse engineering let us download the models for any arbitrary device or firmware and, eventually, how we were able to exploit and gain root on the newer, more secure device. We will show the audience our process in which we discovered and reverse-engineered a proprietary model format that we had never seen before. Finally, we will show how, once we understood the model, we were able to perform attacks against both it and the camera.

The purpose of this talk is to raise awareness about the insecurity of embedded AI as well as to demonstrate how known attack techniques can be used on never-before-seen models, showcasing that AI/ML research has truly passed the infant stage and has reached a point where developed methods can be broadly applied.

Authors
-------
1. Ryan Tracey <rtracey@hiddenlayer.com> (HiddenLayer)
2. Kasimir Schulz <kschulz@hiddenlayer.com> (HiddenLayer)
3. Tom Boner <tom@hiddenlayer.com> (HiddenLayer)

Talk type
---------
Long (45 minutes)

Topics
------
* Attacks against AI systems
* Embedded AI systems


## RoguePilot: Data Corruption and Leakage in Copilot for Microsoft 365
===================================

Abstract
--------
he hype for integrating artificial intelligence into an enterprise’s daily work has become more prevalent after the introduction of AI-driven systems that use Retrieval Augmented Generation (RAG) as seen with Copilot for Microsoft 365. But is the trust put into such systems and their control over decision-making processes rational? System design vulnerabilities within Copilot can be exploited to cause a dissemination of misinformation impacting decision-making processes negatively. 

This talk will demonstrate such an attack that we have termed RoguePilot because of its ability to turn Copilot rogue. The attack occurs when a malicious document is introduced to the data pool (documents, presentations, other relevant files, etc.) related to a topic affecting the decision-making process of the enterprise. The malicious document contains a combination of corrupt data and malicious strings that suppress the correct documents related to the topic and respond to the user’s query with only the information present within the malicious document. Furthermore, the talk highlights how this attack can persist long after the deletion of content within the malicious document or the document itself. 

The talk also points to the larger implications of such vulnerabilities, highlighting the potential for widespread and self-perpetuating organizational disruption and regulatory concerns. Our talk not only sheds light on the vulnerabilities currently present but also calls for a concerted effort to develop standards and practices that can shield enterprises from the adverse effects of such attacks on AI-driven systems. 

Authors
-------
1. Ayush Roy Chowdhury <ayushrc0914@gmail.com> (The University of Texas at Austin)
2. Mulong Luo <ml2558@cornell.edu> (The University of Texas at Austin)
3. Mohit Tiwari <mohit.tiwari@gmail.com> (UT Austin)

Talk type
---------
Long (45 minutes)

Topics
------
* AI and social risks
* Attacks against AI systems
* Defenses for AI systems


