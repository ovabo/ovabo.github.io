---
layout: post
title: "Building AI for the Psychiatric Floor"
date: 2026-02-01
summary: "Most health tech companies start with the technology and go looking for a clinical problem. I started with the clinical problem and went looking for the technology."
---

I have spent the past year splitting my time between two worlds. On one side, I work overnight shifts as a mental health worker in an acute psychiatric hospital, doing 15-minute rounds, monitoring CPAP patients, and documenting behaviors on paper. On the other side, I build AI systems in Python designed to fix the problems I see on those shifts. This essay is about how those two worlds connect technically.

Most explanations of AI are written for a general audience or for engineers building consumer products. This one is written from the psychiatric floor, for anyone who wants to understand how the technology actually works and why I believe it belongs in behavioral health.

The AI systems behind tools like ChatGPT, Claude, and Gemini are called Large Language Models. They are fundamentally different from traditional software. A calculator follows fixed rules. Give it the same input and you get the same output every time. An LLM works on probability. It was trained on massive amounts of text and learned patterns in how words relate to each other. When you ask it a question, it predicts the most likely sequence of words to form a useful answer.

This distinction matters for psychiatry because it explains both the promise and the danger.

The promise is that LLMs can process, summarize, and generate clinical language at a speed no human can match. A psychiatrist who spends 15 minutes writing a progress note after a session could have a draft generated in seconds. A prior authorization request that takes a nurse 45 minutes to compile could be assembled automatically from existing clinical data.

The danger is that LLMs can hallucinate. Because they predict likely words rather than look things up in a verified database, they can produce text that sounds clinically accurate but is factually wrong. In a consumer chatbot, a hallucination is an inconvenience. In a clinical setting, a hallucinated medication dosage or a fabricated patient history could cause harm. This is why every AI tool I build for the psychiatric floor has a human in the loop. The AI drafts. The clinician reviews, edits, and signs. The system is designed to save time, not to replace judgment.


Psykick is built in Python. It is designed to relieve the administrative burden that consumes psychiatric practices. The average psychiatrist spends over ten hours a week on paperwork. Psykick automates the parts of that workload that do not require clinical judgment.

The system has five working components.

The first is the AI clinical scribe. It listens to a session and generates a structured clinical note. Under the hood, this is an LLM performing a specific task: taking unstructured audio or text and converting it into a formatted document that matches the conventions of psychiatric documentation. The model is prompted with detailed instructions about note structure, clinical terminology, and compliance requirements. The output is a draft, never a final document. The clinician reviews it, makes corrections, and signs off.

The second is prior authorization automation. This is where the engineering gets interesting. Prior auth is essentially a structured argument. You need to convince an insurance company that a treatment is medically necessary. That means assembling the right clinical data, mapping it to the right billing codes, and presenting it in the format the payer expects. An LLM is good at this because it can take scattered information from a patient's record, identify the relevant clinical facts, match them against known payer criteria, and generate a coherent request. When a request is denied, the system generates an appeal using the specific denial reason and the clinical evidence that contradicts it.

In a traditional agent architecture, you would think of this as a workflow where code is in charge. My Python code orchestrates the process step by step: pull the patient data, identify the relevant diagnosis and procedure codes, retrieve the payer's known criteria, generate the request, and format it for submission. The LLM is called at specific points where language generation or clinical reasoning is needed, but the overall flow is deterministic. I control what happens and in what order. This is the approach Anthropic calls a "workflow" as opposed to a fully autonomous "agent," and for clinical applications, that level of control is essential.[^5]

The third component is claims defense. When an insurer denies a claim or downcodes it, the system automatically generates the medical necessity documentation and launches an appeal. This uses a similar architecture to the prior auth module but in reverse. Instead of arguing for approval before treatment, it argues against a denial after treatment.

The fourth is electronic prescribing. This is the most straightforward component technically, using secure eFax to send prescriptions directly to pharmacies. It does not require an LLM. It requires reliable, compliant infrastructure.

The fifth is the AI intake system. This is an automated phone agent that answers incoming calls to a psychiatric practice. It triages based on urgency, redirecting emergencies to 911 immediately. For non-emergency calls, it schedules appointments, answers basic practice questions, and routes complex inquiries to the appropriate staff. This component sits at the boundary between the administrative and the clinical. The call itself is administrative. But the triage decision, determining whether a caller is in crisis, requires the kind of language comprehension that LLMs are well-suited for. The system errs heavily on the side of caution. If there is any indication of danger to self or others, the call is escalated immediately. The AI does not make clinical assessments. It listens for signals and routes accordingly.

The prior authorization module is worth additional context because the regulatory landscape is shifting underneath it. The CMS Interoperability and Prior Authorization Final Rule, finalized in January 2024, began requiring payers to meet new process standards as of January 1, 2026.[^4] Payers must now respond to urgent prior auth requests within 72 hours and standard requests within 7 calendar days. They must provide specific denial reasons. By January 1, 2027, payers will be required to implement a Prior Authorization API that allows electronic submission and response. Psykick is being built to interface with these APIs as they come online. The regulatory mandate is creating the infrastructure that tools like Psykick automates.


One of the most important technical concepts in clinical AI is Retrieval-Augmented Generation, or RAG. Instead of relying on what the LLM memorized during training, RAG lets you point the model at a specific set of documents and have it search those documents before generating a response.

This matters enormously for psychiatry. An LLM trained on general internet text knows a lot about psychiatric medications in a broad sense. But it does not know your specific patient's medication history, their allergies, their prior auth denials, or the clinical guidelines your hospital follows. RAG bridges that gap. You load the relevant documents, clinical guidelines, formulary lists, payer criteria, patient records, into a searchable knowledge base. When the system needs to generate a prior auth request or a clinical note, it searches that knowledge base first and grounds its output in real, specific data rather than general patterns.

The difference is the same one I described in my essay about the ambulance ride. The ER does not guess what is wrong with a patient. It reads the data from the sensors. RAG is the mechanism that lets clinical AI read the data instead of guessing.


Psychify is a harder technical challenge. Where Psykick addresses administrative friction, Psychify goes after diagnostic uncertainty.

The goal is to use foundation models to stratify patient biotypes and predict treatment response at day zero, before the months of trial and error that currently define psychiatric prescribing. I have working code that demonstrates the concept, but I want to be honest about where this stands. The concept works in a controlled environment. Translating it to clinical practice requires validation, regulatory navigation, and far more data than I currently have access to.

The technical architecture is different from Psykick. Where Psykick uses LLMs for language tasks like documentation and argumentation, Psychify uses models for pattern recognition across clinical variables. The idea is that if you can identify clusters of patients who share biological or behavioral characteristics, you can predict which treatments are most likely to work for a new patient who matches that cluster. This is the stratification thesis I have written about in earlier essays, applied computationally.

The challenge I wrote about in "My World Fell Apart This Summer" still applies. We know very little about our own biology. Without enough reliable data, even the best models cannot perform well. AI startups that promised to transform psychiatric drug discovery have largely failed because the data foundation was not there. I am approaching this cautiously. The working code is a proof of concept, not a product. It will become a product when the clinical validation supports it.


The hardest problem in clinical AI is not technical. It is trust.

Clinicians have good reason to be skeptical. They have seen decades of health tech promises that did not deliver. They have watched electronic health records, which were supposed to make their lives easier, become the primary source of their administrative burden. They are now watching insurance companies use AI to automatically deny claims at higher rates. The AMA's most recent survey found that 61 percent of physicians are concerned that AI is increasing prior authorization denial rates.[^1] The numbers behind that concern are stark. Physicians complete an average of 39 prior authorizations per week, spending roughly 13 hours on the process. Eighty-nine percent say it contributes to burnout. Twenty-nine percent report that prior auth has led to a serious adverse event for a patient, including hospitalization, permanent impairment, or death.[^2] And emerging evidence shows that some insurers are using AI tools that generate denial rates up to 16 times higher than normal, processing hundreds of thousands of claims with little or no human review.[^3]

This is why I build with a specific philosophy. The AI handles the administrative and computational work. The clinician retains all decision-making authority. The system is transparent about what it did and why. Every generated document shows the clinician what data was used and what the model produced, so they can verify it before it goes anywhere.

I also build from the floor up, not from the whiteboard down. Every feature in Psykick started as a problem I watched a nurse or a psychiatrist struggle with on a real shift. The prior auth module exists because I watched a patient wait a month for a transfer that should have taken days. The scribe exists because I watched nurses spend their shifts at the computer instead of with patients. The claims defense module exists because I learned in my healthcare course that insurers routinely downcode psychiatric claims and providers waste hours appealing for correct payment.

I do not believe AI should make clinical decisions in psychiatry. I have written extensively about why the diagnostic tools in this field are not ready for that. But I do believe AI should handle the paperwork, the insurance fights, the billing code translation, and the pattern recognition that humans are too overwhelmed or too slow to do well. The clinician should be freed to do the one thing the machine cannot: sit with a patient and listen.


One concept from AI engineering that translates directly to clinical settings is the spectrum of control between code-driven workflows and LLM-driven agents.

On one end of the spectrum, your code is in charge. It calls the LLM when specific language or reasoning tasks are needed, but the overall process is predetermined. This is how Psykick works. I know the steps for generating a prior auth request. I write the code that executes those steps. The LLM fills in the parts that require natural language generation. This is predictable, testable, and auditable.

On the other end, the LLM is in charge. You give it a goal and let it figure out the steps. This can be powerful for open-ended tasks, but it is harder to predict and harder to audit. For clinical applications, this level of autonomy is dangerous. You do not want an AI system deciding on its own what information to include in a clinical document or what argument to make to an insurance company without a human verifying the logic.

Almost everything I build sits on the controlled end of this spectrum. The LLM is a tool that my code calls, not a decision-maker that my code serves. This is a deliberate choice. In psychiatry, where the consequences of errors are measured in human suffering, predictability is more important than flexibility.

I am an engineer who works on a psychiatric floor. That combination is unusual, and it is the reason I build the way I do. Most health tech companies start with the technology and go looking for a clinical problem to solve. I started with the clinical problem and went looking for the technology that could help.

The next phase for both Psykick and Psychify involves the same thing: clinical validation. The tools work technically. The question is whether they work in practice, in real hospitals, with real clinicians, under real conditions. That requires partnerships with hospitals and research institutions, and it requires the kind of clinical depth that only comes from medical training.

That is one of the reasons I am going to medical school. Not to stop building. To build with the authority, the knowledge, and the access that only a clinician has. The engineering got me to the floor. The floor showed me what to build. Medical school will give me the credibility and the clinical foundation to deploy it.

---

[^1]: AMA. "Physicians Concerned AI Increases Prior Authorization Denials." [Press release](https://www.ama-assn.org/press-center/ama-press-releases/physicians-concerned-ai-increases-prior-authorization-denials), February 24, 2025.
[^2]: AMA. "2024 Prior Authorization Physician Survey." [PDF](https://www.ama-assn.org/system/files/prior-authorization-survey.pdf). Published February 2025.
[^3]: See [AJMC](https://www.ajmc.com/view/ama-survey-highlights-growing-burden-of-prior-authorization-on-physicians-patients) and [Medical Society of the State of New York](https://www.mssny.org/pulse-3-7-2025-physicians-concerned-ai-increases-prior-auth-denials/) reporting on AI-driven batch denials generating rates up to 16x higher than normal.
[^4]: CMS. "CMS Interoperability and Prior Authorization Final Rule (CMS-0057-F)." [CMS](https://www.cms.gov/cms-interoperability-and-prior-authorization-final-rule-cms-0057-f), January 2024.
[^5]: Anthropic. "Building Effective Agents." December 2024. Distinction between code-driven workflows and LLM-driven agents.
