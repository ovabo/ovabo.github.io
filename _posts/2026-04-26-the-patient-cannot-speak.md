---
layout: post
title: "The Patient Cannot Speak"
date: 2026-04-26
summary: "An honest response to the medical student who skipped residency because AI is automating clinical medicine. He is right about parts of it. He is wrong about the parts I am entering."
---

In Aditya Jain's example, the patient walks in with diarrhea. The AI takes the history, conducts the interview, reviews the literature, generates the differential, orders the tests, drafts the note. The physician's job is to click approve. The patient gets tinidazole and goes home satisfied. Jain calls this the trajectory of clinical medicine. He is finishing Harvard Medical School and has decided not to apply to residency. The cognitive core of medicine, he writes, is being automated, and the economic value of physician training is depreciating. He is keeping his MD because it gives him standing with regulators and payers. He is skipping the residency because four more years of executing existing protocols would close the window for building anything new.[^1]

He is right about a lot of things. He is right that AI capability is improving exponentially while human expertise plateaus. He is right that residency is largely endurance with learning attached, not deliberate practice with feedback loops. He is right that the "physician and" track produces risk-averse 35-year-olds who recommend faster horses instead of cars. And he is right that the academic medical establishment is too slow on AI, publishing model evaluations on generalist models from two years ago while Google runs nationwide randomized trials of its own diagnostic AI in real telehealth settings.[^2]

I read his essay carefully. I agreed with most of it. And then I went to work that night and watched the patient I was assigned to one-to-one accuse me of being the FBI for the third time, apologize, accuse me again, ask me to take off my glasses I had not told him I was wearing, and then ask if his mother was dead. He had been admitted four days earlier. The chart said active psychosis with disorganized features. The chart did not say what was happening in the room.

On the unit where I work, the patient does not walk in with diarrhea.

The patient is brought in restrained because they broke their parents' window with a kitchen knife. The patient cannot tell you what they took. The patient says they have not slept in twelve days but the timeline is wrong by a factor of four. The patient says the FBI is in the walls, that I am evil, that I am their cousin, that I am their mother, that I am God. The patient cannot remember whether they have eaten. The patient says they have been shot when they have not been shot. The patient is admitted for mania and is in hepatic encephalopathy. The patient is admitted for psychosis and has just had a stroke. The patient is admitted for substance-induced psychosis and is post-ictal. The patient is admitted with the wrong chief complaint because the patient cannot speak in the way the system needs them to speak.

This is the part of medicine Jain's argument does not reach.

---

The Counsel Health workflow he describes works because the patient with diarrhea is a competent narrator. They know when the symptom started. They know what they ate. They can describe the stool. They can answer follow-up questions. The history is structured because the patient is structured. The AI's task is to organize the structured input into a structured output. The physician's job is to confirm.

The patients I sit with are not competent narrators of their own conditions. That is why they are on a locked unit. The mental health worker's job, my job, is to assemble a usable picture from twelve hours of fragmentary, contradictory, hallucinated, withheld, and confabulated information. Some of it comes from what the patient says. Most of it comes from what the patient does. The patient who tells me they have been sleeping all night while I have been documenting their wakefulness on rounds sheets every fifteen minutes. The patient who tells me they have not eaten while I have watched them eat. The patient who tells me they are calm while standing two inches from my face with their fists clenched. The data is not in the chart because the data cannot be reduced to language the patient is capable of producing.

This is the same problem Dawn Zuidgeest-Craft describes in her piece on becoming a physician at 73 after 45 years as a neonatal nurse practitioner. The neonate cannot speak. The bedside person learns to read feeding intolerance, subtle changes in clinical response, the precursors to necrotizing enterocolitis that do not show up in vitals until it is too late. She writes that medical school and residency do not teach this. It is experiential. The current neonatologists depend on the nurses to alert them to further investigate.[^3]

A neonate and a person in active psychosis have almost nothing in common, except that neither one of them can give a usable history. They are different versions of the same clinical problem. The patient cannot speak. Someone has to assemble the picture from what the patient does, from how the patient changes across hours of observation, from the subtle signals that the patient cannot or will not produce on demand.

This is the part of medicine where AI is least likely to replace the human role. Not because the AI is not smart enough. Because the data does not exist in the format the AI consumes.

---

Jain's strongest example is radiology. On the Radiology's Last Exam benchmark, board-certified radiologists score 83 percent. Radiology residents score 45 percent. Google's Gemini 3.0 Pro, a generalist AI model not trained on radiology, scored 51 percent as of January 2026. AI capability is improving roughly 27 percentage points per year. Human residents improve roughly 8 to 10 percentage points per year, at the cost of 80-hour weeks and delayed life milestones. The trajectories cross before the resident finishes training.[^4]

This is a real argument. The benchmark is well-designed. The math is right. If I were planning to enter radiology, I would take Jain's piece very seriously and probably reconsider.

But radiology is unusually well-suited to AI in ways that most of medicine is not. The input is a structured image. The output is a structured interpretation. The ground truth is verifiable on follow-up imaging or pathology. The benchmark exists because the data exists and the task is bounded. The same is true of dermatology, which is increasingly diagnosed from photographs. The same is true of pathology, which is increasingly diagnosed from slides. The same is true of significant portions of internal medicine, where the patient can produce a structured history and the labs can produce structured numbers and the differential is finite.

The specialties where this is least true are the specialties where the patient cannot speak. Pediatric subspecialties, especially neonatology. Geriatrics, where the patient may not remember when the symptom started or whether they took their medications. Palliative care, where the patient is dying and the medical question is no longer what is wrong but how the person wants to spend the time they have. Addiction medicine, where the patient lies about consumption and the chart cannot distinguish current use from withdrawal from a third unrelated condition. And psychiatry, especially the inpatient and consultation-liaison varieties, where the patient's account of reality is part of what is being assessed.

There is no Psychiatry's Last Exam benchmark because there cannot be one in the same form. The ground truth in psychiatry is not a follow-up scan that resolves the question. The ground truth is what happens over the next six months, and even then it is contested. Two trained psychiatrists evaluating the same patient at the same time produce different diagnoses with disturbing frequency. The diagnostic categories themselves are revised every few years because the field is still arguing about what the categories should be. An AI trained on the existing literature will be trained on the existing disagreement. It will not resolve it.

This is not an argument that AI has no role in psychiatry. AI will write the notes. AI will manage the documentation. AI will flag medication interactions and suggest differential diagnoses and run the screening tools and handle the prior authorizations. I am building several of these tools myself. But the work of sitting with a patient on the second night of one-to-one observation, watching them apologize and accuse and apologize and accuse, deciding whether the apology is metacognitive or reflexive, deciding whether to call the on-call psychiatrist because the patient just said something that does not fit the working diagnosis, that work is not in the chart and it cannot be approved.

---

Consultation-liaison psychiatry, the specialty I am entering, is the test case for this distinction. The C-L psychiatrist sees the cancer patient who is refusing chemotherapy. The oncologist has tried to convince them. The nurses have tried to convince them. The social worker has documented capacity and decisional impairment. The chart says the patient is depressed and noncompliant. The C-L psychiatrist's job is to figure out why the patient is actually refusing, which may be depression, or may be a previously undiagnosed delusion that the chemotherapy is poison, or may be a competent and rational decision to stop treatment that the oncology team is not ready to accept, or may be a family pressure the patient has not disclosed, or may be a religious commitment that has not been asked about, or may be a financial calculation about leaving something for the spouse, or may be all of these at once.

The cognitive task is not differential diagnosis. The cognitive task is producing a usable formulation in a system where every actor has assumed they understand what is happening and none of them does. The C-L psychiatrist is the person who is allowed to spend an hour asking questions nobody else has time to ask. The output is not a diagnosis. The output is a recommendation that the oncology team, the nurses, the family, and the patient can all live with. That is not a chart-approve workflow. That is the part of medicine that requires the human in the room.

If AI replaces this work, it will do so by also replacing the oncologist's bedside conversation, the nurse's daily check-ins, the social worker's family meetings, and the entire structure of integrated medical care. That is possible. It is not imminent.

---

The honest part of Jain's argument that I have to engage with is the timing. He is right that the building window for AI in healthcare is now. He is right that the people writing the policy will not have time for those of us still in training. He is right that academic medicine is structurally too slow. He is right that the "physician and" model produces risk-averse 35-year-olds.

I am running my own response to this in parallel. I am building Psykick and Psychify at Stratification Labs while I take pre-medical prerequisites at Cypress College and work overnight shifts on the psychiatric unit. I am not waiting for the credential to start the building. The credential, when I have it, will let me do the clinical work that the building is in service of. The building, while I am pursuing the credential, will let me ship products that change how psychiatric care is delivered before the credential is finished.

This is not a hedge. It is a recognition that Jain is right about which window is closing and wrong about which specialties are durable. The specialties that will survive AI automation are the ones where the patient cannot speak. The specialties that will be transformed by AI tooling are most of them. The right move, for me specifically, is to build the tooling while training for the practice. Not one or the other. Both.

If I were entering radiology, I would not be writing this essay. I would be writing the one Jain wrote.

But I am not entering radiology. I am entering the specialty where the patient is brought in restrained, where they cannot remember whether they have eaten, where they say the FBI is in the walls, where they apologize for hitting a staff member they could not see. That specialty is not being automated by 2030. Or by 2040. Or by the time I would finish residency. It is the specialty that exists because the chart cannot see what the person in the room sees, and Aditya Jain's essay does not change that. It just confirms which parts of medicine the chart can finally see, and which parts it cannot.

The parts it cannot see are the parts I am going into. I am going into them because that is where the work still needs a person. And because the person who builds the tools for a system has to know the system from the inside. I am doing both for the same reason.

---

[^1]: Aditya Jain, "Why I Didn't Apply to Residency … and What I'm Doing Instead," Doximity Op-Med, March 16, 2026.

[^2]: Google Research, "Collaborating on a nationwide randomized study of AI in real-world virtual care." See also METR, "Measuring AI Ability to Complete Long Tasks," 2025.

[^3]: Dawn Zuidgeest-Craft, "I started medical school at 69 and will begin residency at 72. Here's what I learned," STAT First Opinion, April 24, 2026.

[^4]: Radiology's Last Exam benchmark, arxiv:2509.25559, cited in Jain (2026).
