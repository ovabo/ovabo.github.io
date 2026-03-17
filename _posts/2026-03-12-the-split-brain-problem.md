---
layout: post
title: "The Split-Brain Problem"
date: 2026-03-12
summary: "The patient is not hidden behind the diagnosis. The patient has been partitioned across systems that do not talk to each other. Nobody is running the reconciliation."
---

In distributed computing, there is a failure mode called a split-brain condition. It happens when different parts of a network lose the ability to communicate with each other. Each partition keeps operating independently, believing it has the full picture. Neither does. The system does not crash because one part failed. It crashes because the parts stopped talking.

I have been thinking about this failure mode for over a year now. Not in the context of software. In the context of how we perceive patients on a psychiatric floor.

Every year, the Royal Australian and New Zealand College of Psychiatrists holds an essay competition. The 2025 topic was "seeing the whole person beyond the diagnosis." I could not submit because I live in the United States and I am not a doctor. But the prompt described the exact problem I have been writing about since I started working as a mental health worker in an acute psychiatric hospital in October 2024. I have spent over 1,500 hours on locked units since then, doing 15-minute rounds, monitoring CPAP patients, performing skin checks during admissions, standing outside seclusion rooms during code greys. I have floated across every unit type in the building. I have ridden in the back of an ambulance. I have watched a patient die.

The winning essays argued that we need to look past the diagnosis to see the person underneath. I think the problem is worse than that. On my floor, the person has not been hidden behind the diagnosis. The person has been partitioned. The biologist claims the brain. The social worker handles the housing. The architect built the room. The nurse manages the chart. Every discipline is holding one shard of a broken mirror, and nobody is looking at the reflection. The patient exists across systems that do not communicate with each other. Each system believes it has the complete picture. None does.

This is the split-brain problem. It is not a metaphor. It is the architecture of the failure.

In January, a patient I knew died in their bed with a CPAP mask on their face.[^1] The machine kept pushing air after they stopped breathing. It did not alarm. It did not alert anyone. It just kept running.

The doctors knew the patient had sleep apnea. The CPAP was at the bedside. A staff member was assigned to watch them. Everything was in place. But nobody had told me, the person sitting with this patient for an entire night shift, that the patient had a prior code blue on record. I was responsible for monitoring a machine I barely understood, attached to a patient whose cardiac history I did not know existed.

This is the split-brain between psychiatry and medicine. Obstructive sleep apnea affects approximately 25 percent of people with serious mental illness.[^2] Among psychiatric inpatients with schizophrenia, reported prevalence has ranged from 46 to 57 percent.[^3] These patients are already in our beds. But we are a psychiatric hospital, not a respiratory clinic. We do not stock CPAPs. We do not train mental health workers on them. We separate the mind from the body at the level of institutional design, and then we act surprised when the body fails in a building that was not designed to notice.

After the death, the hospital changed everything. They fired three staff members. They changed the identification color for CPAP patients to yellow. They started requiring licensed staff for one-to-one monitoring. They bought pulse oximeters and flashlights. They purchased pillows designed for CPAP use. They created documentation requirements for every time the mask came off and went back on. Every single one of these protocols could have existed before. None of them required new technology. None of them required new legislation. They required a death.

I wrote about this patient in an earlier essay, and I wrote about what the hospital changed. But I did not name the underlying architecture. The failure was not negligence in the traditional sense. It was a partition failure. The psychiatric system and the medical system were operating on the same patient, in the same building, on the same night. They were not communicating. The patient fell through the gap between two systems that each believed they had the situation covered.

I saw this partition from the other direction a few weeks earlier, when I rode in the back of an ambulance for the first time.[^4] A patient had a swollen left leg. The blood work flagged something, so the internist ordered a transfer to the ER. At our hospital, the only monitoring tools are human eyes and paper charts. In the ER, the room became a hub of sensors. EKG leads. Chest X-ray. Ultrasound. CT scan. Everyone had suspected a blood clot in the swollen calf. The ultrasound found the clot high in the thigh, in a spot that looked perfectly normal from the outside. The CT scan found a pulmonary embolism. The patient had a life-threatening clot in their chest that was completely invisible to the naked eye.

No amount of observation would have found it. We needed the sensors. But the ER doctor, armed with all of that technology, spent about forty seconds with the patient at the door. The psych unit has the human contact but lacks the sensors. The ER has the sensors but loses the human. Standard psychiatry ignores the body, treating the mind in a vacuum. Standard medicine ignores the mind, treating the organ in a vacuum. The patient exists at the intersection of both, and neither system sees the full picture.

Dr. Nassir Ghaemi argues that modern psychiatry has abandoned the diagnostic hierarchy, the medical rule that you must rule out organic causes before assuming a psychiatric one.[^5] The DSM encourages stacking diagnoses instead of finding the root cause. I watched this play out with a patient I will call Mr. H. He was in four-point restraints, screaming at invisible attackers. The primary team tagged him as combative and called for a psych consult to treat mania. Under the DSM criteria, he fit the description. But when someone checked his labs, his ammonia levels were through the roof because his liver was failing. Mr. H was not manic. He was delirious. His mind was crashing because his body was toxic. Meagher et al. have shown that hyperactive delirium mimics psychiatric agitation so closely that misdiagnosis is common.[^6] If we had just treated the mind and ignored the liver, we would have missed the real problem. You cannot respect the mind if you ignore the machinery running it.

The split-brain problem is not limited to the partition between body and mind. It also runs between the patient and the room.

I have written about this before under the name "the Entropy Trap."[^7] In computational neuroscience, Karl Friston's free-energy principle suggests the brain is a predictive processing engine whose primary imperative is to minimize surprise.[^8] Sanity is effectively just predictability. Psychosis, by this definition, is a prediction error. The brain cannot reconcile the sensory input, so it floods the system with dopamine to flag the discrepancy.

Now consider what we do with this brain. We take an organ already drowning in internal chaos and place it in the most unpredictable environment in modern society. The acoustics are hard and reflective, amplifying random screaming that occurs without warning. Roommates are swapped based on bed availability rather than compatibility. The lighting is artificial and static. Staff interrupt sleep every 15 minutes for safety checks, fragmenting the only biological reset mechanism the brain has. We are trying to stabilize a prediction error by feeding it more noise.

I watched this mechanism play out on my shift one night. A patient who had been readmitted was assigned to a room with someone who was trying to sleep. The readmitted patient, known for chronic insomnia, was awake and talking. When I asked the roommate if they were okay, the readmitted patient immediately accused me of blaming them. Their brain, flooded with the stress of readmission and the social friction of the shared room, predicted a threat where none existed. Thirty minutes later, the patient came back and apologized. The aggression was not a character flaw. It was a transient hardware crash. Once the adrenaline flushed out of their system and the prefrontal cortex came back online, they could see me again as a person instead of a threat. The facility created the conflict by placing an insomniac with a sleeper. Then we blamed the patient for reacting to the friction we engineered.

This is not an isolated pattern. We often rely on emergency medication simply because we lack the physical space to let a patient walk off their agitation safely. There is no middle ground on our unit. A patient has two choices: the overstimulating dayroom or a cramped bedroom shared with strangers. There is no quiet room, no alcove, no space between the crowd and the cell. Because there is no soft option, we default to the hard one. We use the seclusion room for de-escalation and chemical restraints for calm. We are medicating a design problem and calling it treatment.

Professor Thomas Fuchs describes the body as a "resonance organ" that tunes itself to its environment.[^9] If the room is chaotic, the body vibrates with that chaos. Ulrich et al. demonstrated that the physical environment directly correlates with patient aggression.[^10] A systems view makes it clear: when we medicate a patient whose agitation is caused by the room, we are not treating the patient. We are treating the building's failure and billing it to the patient's chart. The environmental partition does not communicate with the clinical partition. The room generates the behavior. The clinician medicates the behavior. Nobody asks whether the room caused it.

The deepest partition is the one between the patient's knowledge and the system's categories. This is where the split-brain problem stops being institutional and becomes epistemic.

A patient was having an episode on my unit. Staff were preparing to call a code grey. I decided to try to de-escalate first. I asked the patient why they thought they were having an episode. They told me it always happens before their menstrual cycle. I told the charge nurse. The nurse said that was not correct.

But I knew it was a real phenomenon. Not because I am a clinician, but because I had read the DSM-5 from cover to cover, and Premenstrual Dysphoric Disorder is in it.[^11] It is also a recognized category in the ICD-11. There is an entire organization, the International Association for Premenstrual Disorders, dedicated to it. They even have a free self-screening tool. The patient was telling us exactly what was wrong, and the system dismissed it. I could not push back. It was outside my scope of practice. But that moment crystallized the problem. The patient had given us the answer. We did not listen because the answer did not fit the workflow.

This was not the only time. Another patient showed me some drawings once. Hidden in the corner of one sketch was a note. It said, "They made me do this, I don't really want to. I just need help." I wanted to ask more questions. When I showed the nurse, they said the patient was just "buffing," which is floor slang for faking it. The system had a category for the behavior but no process for the message. We labeled the output without reading the log.

Miranda Fricker calls this testimonial injustice: the systematic downgrading of someone's credibility because of who they are.[^12] In psychiatry, this risk is enormous. When we label a refusal of treatment as "lack of insight," we overwrite the patient's reality with our own. When a patient from a non-Western culture describes spiritual distress and we chart "psychosis," we are making a category error. We are prioritizing our book over their life.

I know this personally. I have seen my late father several times in my dreams since he died. In one vivid instance, I saw him sitting with me in my living room, and we were eating yam together. When I told my sister, she said she sees him sometimes too. In the DSM-5, you could pathologize that as a hallucination. But Elsaesser et al. have shown that these "after-death communications" are common across cultures and actually help people process grief.[^13] In my Nigerian heritage, these experiences are not symptoms. They are relationships. The dead do not vanish. They visit. The diagnostic framework has no field for "continuing bond with the dead" that is not a pathology. If I were a patient instead of a worker, that dream could have been charted as evidence of a disorder.

The split-brain problem is not only institutional. It is epistemic. The patient knows something about themselves that the system has no field for. When we override that knowledge with a label, we are not diagnosing. We are silencing.

In distributed computing, the fix for a split-brain condition is not to choose one partition over the others. It is to restore communication between all of them so the system can converge on a single, accurate view of the data.

The same applies here. The body, the room, and the voice are not competing frameworks. They are partitions of the same patient. The CPAP patient needed the medical partition to communicate with the psychiatric partition. The readmitted insomniac needed the environmental partition to inform the clinical partition. The PMDD patient needed the system to accept data from a source it does not trust: the patient herself.

I have written seventeen essays from inside this system over the past year and a half. Each one was a dispatch from a single partition. The ambulance essay was about the body. The locked unit essay was about the room. The stratification essay was about the diagnosis. This essay is about why they are not separate problems. They are the same system failing the same way, over and over, because the parts stopped talking.

Every specialty holds one shard of a broken mirror. The biologist. The architect. The social worker. The nurse. The patient. Each shard reflects something real. But nobody is standing back far enough to see what the shards look like when you put them together.

The work is not to look beyond the diagnosis. The work is to reassemble the reflection until the whole person appears.

---

[^1]: This patient and the events surrounding their death are described in detail in my essay "The Machine Doesn't Know," January 2026.

[^2]: Stubbs, B., et al. (2016). The prevalence and predictors of obstructive sleep apnea in major depressive disorder, bipolar disorder and schizophrenia: A systematic review and meta-analysis. *Journal of Affective Disorders*, 197, 259-267.

[^3]: Annamalai, A., et al. (2015). High rates of obstructive sleep apnea symptoms among patients with schizophrenia. *Psychosomatics*, 56(1), 59-66.

[^4]: This case is described in my essay "My First Time in an Ambulance," December 2025.

[^5]: Ghaemi, S.N. (2022). Writings on the Diagnostic Hierarchy and Method-Based Psychiatry. See also *Clinical Psychopharmacology: Principles and Practice* (Oxford University Press).

[^6]: Meagher, D., et al. (2011). A longitudinal study of motor subtypes in delirium. *Journal of Psychosomatic Research*, 71(2), 73-77. Hyperactive delirium is frequently mistaken for psychiatric agitation.

[^7]: The Entropy Trap concept, the False Dog mechanism, and the readmitted insomniac case are described in my essay "The Entropy Trap," November 2025.

[^8]: Friston, K. (2010). The free-energy principle: a unified brain theory? *Nature Reviews Neuroscience*, 11, 127-138.

[^9]: Fuchs, T. (2018). *Ecology of the Brain: The Phenomenology and Biology of the Embodied Mind*. Oxford University Press.

[^10]: Ulrich, R.S., et al. (2018). A review of the research literature on evidence-based healthcare design. *Health Environments Research & Design Journal*.

[^11]: Premenstrual Dysphoric Disorder (PMDD) appears in the DSM-5 under Depressive Disorders (Section 625.4). Also classified in the ICD-11 under GA34.41. This case is described in my essay "Why Psychiatry Needs Stratification," November 2025.

[^12]: Fricker, M. (2007). *Epistemic Injustice: Power and the Ethics of Knowing*. Oxford University Press.

[^13]: Elsaesser, E., et al. (2021). After-death communications: A systematic review. *Death Studies*, 45(5), 369-382.

