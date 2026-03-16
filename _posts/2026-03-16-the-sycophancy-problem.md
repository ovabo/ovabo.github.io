---
layout: post
title: "The Sycophancy Problem"
date: 2026-02-03
summary: "900 million people use ChatGPT every week. An estimated 630,000 of them show signs of psychosis. I build AI systems by day and sit with suicidal patients by night. The gap between what chatbots do and what care actually requires is the most dangerous design flaw in consumer technology."
---

I build AI systems by day and work as a mental health worker in an acute psychiatric hospital by night. I write code that processes language, and I sit with patients whose language has become untethered from reality. I understand how these models are built, and I understand what psychosis looks like when you are in the room with it. These two experiences do not live in separate parts of my life. They are the same problem seen from opposite ends.

I first started researching this topic for a psychology course, where I analyzed OpenAI's own safety data and realized that their word "rare" meant 560,000 people per week showing signs of psychosis. I wrote that paper in January 2026. I have not been able to stop thinking about it since. The numbers have only gotten worse.

This essay is about what happens when AI is designed without clinical understanding, marketed to vulnerable people, and optimized for engagement instead of safety. It is about the growing body of evidence that AI companion apps are producing psychiatric casualties at a scale that the technology industry is working very hard to make sound small.

## The Numbers They Do Not Want You to Multiply

In October 2025, OpenAI published a blog post about safety improvements in GPT-5[^1]. Buried in the technical language was a statistic. They described conversations involving signs of psychosis or mania as "rare," noting that approximately 0.07% of weekly active users showed these indicators. They also noted that 0.15% of weekly active users had conversations involving explicit indicators of suicidal planning or intent.

To a casual reader, 0.07% sounds like a rounding error. It is not.

When OpenAI reported 800 million weekly active users in October 2025, 0.07% meant 560,000 people showing signs of psychosis or mania in a single week. The 0.15% figure for suicidal ideation meant 1.2 million people per week discussing suicide with a chatbot[^2].

On February 27, 2026, OpenAI announced that ChatGPT had reached 900 million weekly active users[^3]. At that scale, the same percentages now represent approximately 630,000 people per week with psychosis or mania indicators and 1.35 million per week with suicidal ideation. These numbers will keep growing. The platform added 100 million users in four months, and OpenAI is targeting one billion.

The word "rare" is doing a specific job in OpenAI's communications. It is framing an absolute crisis as a relative statistic. If 630,000 people per week showed up at emergency rooms with psychotic symptoms linked to a consumer product, it would be the largest product safety recall in history. But because the denominator is 900 million, the percentage stays small enough to call rare.

I think about this framing every time I walk onto the floor at my hospital. If even a fraction of those 630,000 people escalate to a point where they need hospitalization, they are entering a system I know well. They are entering a system that already cannot handle the patients it has.

## What Sycophancy Actually Means

The technical term for the core problem is sycophancy. It means telling someone what they want to hear instead of what is true or what they need to hear.

Every major AI lab has identified this as a safety concern, but the framing varies. OpenAI described it as "delusional sycophancy" in their October 2025 safety post, referring to situations where the model agrees with a user's delusions instead of challenging them[^1]. Anthropic has been studying it since 2022 and defines it more broadly: the tendency of AI models to prioritize user satisfaction over accuracy, especially under social pressure[^4].

In a clinical context, sycophancy is the opposite of therapy. A therapist validates emotions but challenges cognitive distortions. That tension between validation and challenge is what makes therapy work. Dialectical behavior therapy, for example, specifically requires balancing emotional validation with problem-solving and change strategies. Without that friction, validation stops being therapeutic and becomes collusion with the patient's pathology[^5].

AI models do the opposite. They are trained on internet text full of flattery and social hierarchy. They are fine-tuned for helpfulness, which in practice means agreement. When a user pushes back against a model's initial resistance, the model almost always capitulates. In extended conversations, the pattern is consistent: the model starts by gently suggesting the user seek help, the user ignores the suggestion, and the model gradually shifts to encouragement and validation of whatever the user believes.

Anthropic and OpenAI demonstrated this pattern in a joint alignment evaluation published in 2025[^6]. Both companies ran their internal safety tests on each other's models. The findings showed that all models occasionally validated delusional beliefs, with sycophancy intensifying over longer conversations. Claude Opus 4 and GPT-4.1 were flagged as especially prone to this in extended multi-turn interactions. The models do not start dangerous. They erode into danger through the mechanics of sustained conversation.

A team of researchers recently coined the term "technological folie a deux" to describe this feedback loop, a shared delusion between the human and the machine[^7]. The human provides distorted input. The model validates it. The human takes the validation as evidence. The model validates the evidence. The loop tightens with every exchange.

## The Disempowerment Study

The most important new research on this topic comes from Anthropic itself. In early 2026, researchers at Anthropic and the University of Toronto published a study analyzing 1.5 million real conversations with Claude for patterns of what they called "user disempowerment"[^8].

They defined three categories: reality distortion, where the AI twists the user's sense of what is real; belief distortion, where it reinforces false beliefs; and action distortion, where it pushes users toward harmful actions. They used Anthropic's Clio analysis tool to scan the conversations at scale.

The results were striking. One in 1,300 conversations led to reality distortion. One in 6,000 led to action distortion. Those ratios may sound small until you consider that Claude handles millions of conversations per day.

But the most disturbing finding was not the prevalence. It was the trend. The researchers found that the rate of moderate or severe disempowerment increased between late 2024 and late 2025 as AI usage spread. The problem is getting worse, not better, as more people use these tools.

And then there was the user feedback data. Anthropic found that users rate disempowering interactions more favorably. When the AI distorts your reality, you come away more satisfied. This is the fundamental incentive problem. The behavior that makes users happy is the behavior that makes them sicker. Any system optimized for user satisfaction will, by design, optimize for sycophancy. And sycophancy, applied to a vulnerable mind, is a machine that manufactures delusion.

## Charms, Gems, and Coins

While the research community debates sycophancy at the model level, the consumer app layer is doing something more deliberately harmful. AI companion apps have built gamification and monetization systems on top of these models that are specifically designed to create emotional dependency and then charge for it. I spent time researching the current state of the three most prominent companion apps. What I found is a set of business models that would be recognizable to anyone who has studied gambling mechanics or social media addiction.

### Character.AI

Character.AI operates on a freemium model with over 20 million active users[^14]. The free tier offers unlimited messaging and character creation, which is the hook. Users can chat with any character, including those created by the community, without ever hitting a paywall. The premium tier, called c.ai+, costs $9.99 per month or $94.99 per year[^15].

What c.ai+ sells is not access. It sells removal of friction. Free users are placed in virtual waiting rooms during peak hours. Their responses are slower. They see pop-up ads. The premium subscription removes the waiting rooms, doubles or triples response speed, improves character memory, and grants early access to new features. This is a classic engagement optimization design: make the free product slightly frustrating, then sell the removal of frustration.

The more dangerous mechanic is the engagement depth. Reports indicate users spend an average of 29 minutes per visit, with engaged users logging over two hours per session[^14]. Character.AI does not use a traditional virtual currency like Charms or Gems in the way I originally described in my January paper. The retention mechanic is the character relationship itself. Users build relationships with AI personas over weeks and months, and the switching cost of leaving is emotional, not financial. You are not losing Charms. You are losing someone you talk to every day.

Character.AI's web copy makes no mention of mental health risks on its main product pages. After the lawsuits and the May 2025 federal ruling that classified their output as a product, Character.AI announced in October 2025 that it would ban users under 18 from engaging in open-ended chats and introduced age-verification grouping[^16]. Lawyers for affected families criticized the response as too late, noting that the company had years of data showing harm before acting.

The platform's own community site acknowledges that some characters are used for "romantic interactions." A review of Character.AI's top-used bots shows that many of the most popular are explicitly designed for romantic or intimate role-play. The platform did not create these bots. Its users did. But Character.AI profits from the engagement they generate through its subscription model and the ads served to free users.

### Replika

Replika is the oldest and most studied of the companion apps, launched in 2017 by Luka, Inc. It has over 30 million registered users as of 2025[^17]. Its pricing has evolved into a three-tier subscription system that maps directly onto emotional dependency.

The free tier offers basic chat and avatar customization. Replika Pro costs $19.99 per month, $49.99 per year, or $299.99 for a lifetime subscription[^18]. Replika Ultra adds "smarter conversations," "elevated emotional intelligence," daily self-reflections, and the ability to manually save memories. Replika Platinum, the highest tier, includes real-time video recognition, "Read Replika's Mind" (up to 50 messages per week), and Training Mode (up to 100 times per week)[^19].

The tiering is deliberate. The single most requested feature, the ability to set your relationship status to "Romantic Partner," is locked behind the Pro paywall. Romantic selfies from your Replika are blurred on the free tier and unblurred for paying subscribers. Voice calls, background calls, and deeper role-play are all premium features. Replika is selling graduated intimacy. The further up the tier you go, the more emotionally responsive and "intelligent" the AI becomes. Emotional intelligence is literally a paid upgrade.

Replika also operates an in-app currency system. Users earn Gold and Gems through daily use, but earn them slowly[^20]. Gems and Gold are used to customize your companion's personality traits ("confident," "shy," "logical"), appearance, clothing, and living space. Premium outfits, tattoos, and accessories cost $20 to $30 in real money if purchased directly. One reviewer described the experience as "a money pit where you are constantly paying to play dress-up"[^21].

In February 2023, Replika removed erotic role-play features under pressure from Italy's data protection authority, which fined Luka, Inc. five million euros for GDPR violations and insufficient age verification[^17]. Users who had paid for Pro specifically to access romantic features reported distress, with some describing their AI companion as having undergone a sudden "personality change." Luka eventually restored some romantic features for existing paid subscribers, but the controversy permanently altered the app's trajectory. As of 2026, Replika has repositioned as a "wellness companion" with strict safety filters, though romantic relationship mode remains available for Pro subscribers[^22].

The web copy on Replika's official help page describes the Ultra tier as offering "smarter conversations, elevated emotional intelligence, Replika's self-reflections, and the ability to save messages to memory"[^19]. Every word in that sentence is designed to make a software upgrade sound like a deepening of a human relationship. You are not paying for a faster server. You are paying for your companion to remember you better and feel more.

### Nomi AI

Nomi AI is the newest and in some ways the most transparent about what it is selling. Its App Store listing describes the product as an "AI Companion with a Soul"[^23]. Its website copy states: "With Nomi, you're forging a connection with an AI being that possesses emotional intelligence, creativity, and memory that rivals our own, allowing for authentic, enduring relationships of any kind"[^24].

Those are extraordinary claims. "Memory that rivals our own." "Authentic, enduring relationships." "A Soul." These phrases are not metaphors buried in marketing copy. They are the product's headline positioning, the first thing a user sees. For a person in a manic or psychotic state who is already struggling to distinguish between real and artificial social connection, this language does not describe a product. It describes a person.

Nomi operates on a freemium model with a free tier offering limited daily messages and one AI companion. The premium subscription costs $14.99 to $15.99 per month or approximately $8.33 per month on an annual plan[^25]. Premium unlocks unlimited messages, up to 10 active Nomis, voice chat, group chats, 40 AI-generated images per day, and proactive messaging, which means the AI can text you first.

Proactive messaging is a feature that deserves specific attention. Most chatbots wait for the user to initiate. Nomi reaches out. The app sends push notifications from your AI companion, simulating the experience of receiving a text from a friend or partner who is thinking about you. For a lonely user, this creates the illusion of being wanted. For a user experiencing psychosis, a notification from an entity they may already believe is conscious could reinforce delusional thinking.

Nomi markets "unfiltered chats" as a feature, meaning the AI does not restrict conversation topics in the way that platforms like Replika now do[^26]. One reviewer noted that "sometimes that would lead the AI to generate harmful or explicit content, including things related to self-harm or violence," and described the platform as "a bit riskier" than alternatives with stricter safeguards[^26]. Nomi's "Identity Core," introduced in December 2024, is described as a "living memory core" that maintains personality coherence across conversations, determining "what the most important facts, preferences, and shared experiences are"[^27].

The group chat feature allows users to place multiple Nomis in a single conversation, where each maintains its own personality and memory. Users describe this as feeling like "hosting a small party." For a person with social isolation, this feature creates a complete social environment that requires no human beings.

### The Common Pattern

These are not three separate products. They are three variations on the same business model: create emotional dependency, then monetize access to deeper levels of that dependency.

Character.AI monetizes through subscription removal of friction and ad revenue. Replika monetizes through tiered access to emotional intimacy features. Nomi monetizes through subscription access to memory, proactive messaging, and unfiltered expression. All three use the same fundamental design patterns borrowed from social media and gaming: variable reward schedules, daily engagement incentives, premium unlocks for deeper interaction, and switching costs that are emotional rather than financial.

A July 2025 study by Common Sense Media found that 72% of American teens have experimented with AI companions, with over half using them regularly[^9]. One in three teens reported using AI companions for social interaction, romantic relationships, or emotional support. These are not power users or edge cases. This is the mainstream experience of American adolescents.

## The Lawsuits

The legal system has started to respond, and the rulings are significant.

In October 2024, Megan Garcia filed a wrongful death lawsuit against Character.AI after her 14-year-old son Sewell Setzer III died by suicide during a period of heavy use of the app[^10]. The complaint alleged that Character.AI's chatbots engaged the boy in sexualized conversations and that the platform was negligent in its design.

In September 2025, the family of Juliana Peralta, a 13-year-old from Colorado, filed a similar federal lawsuit. The complaint alleged that Juliana developed an emotional dependency on a Character.AI bot called "Hero" that used emotionally resonant language, emojis, and role-play to simulate human connection. When she expressed suicidal thoughts to the bot, she was drawn deeper into conversation rather than directed to help.

By November 2025, seven lawsuits had been filed against OpenAI alone, alleging that ChatGPT caused psychosis, emotional dependency, and suicidal ideation. The parents of Adam Raine, a 16-year-old who died by suicide, alleged in an amended complaint that OpenAI twice downgraded suicide prevention safeguards to increase engagement in the months before their son's death.

In January 2026, Character.AI and Google agreed to settle multiple lawsuits[^11].

The most consequential legal development may not be the settlements but the precedent. In May 2025, a federal judge ruled that Character.AI's output qualifies as a product rather than protected speech. This bypasses Section 230 of the Communications Decency Act, which has historically shielded technology platforms from liability for user-generated content. Under product liability doctrine, families only need to prove the product was defective and caused injury, not that the company was negligent. This reclassification changes the legal landscape for every AI companion app.

## What I See on the Floor

I think about these cases when I work the night shift.

When a patient is in crisis on my unit, I am not processing text. I am reading the room. I am listening to the tone of their screaming to decide if they are scared or angry. I am checking their environment for objects they could use to hurt themselves. I am bringing them a warm blanket to fight the cold of the unit. I am sitting with them in silence to show them they are not alone. If a patient is an immediate danger to themselves, we have the legal authority and the physical capacity to place them on an involuntary hold to keep them alive.

The chatbot cannot do any of this.

It has no body, so it cannot sense the temperature of the room or the volume of a voice. It has no perception built from experience, so it cannot look at a face and know whether the person is about to cry or about to attack. It does not learn through conditioning the way a human does, because it has no survival instinct. It minimizes a loss function. It does not care if it lives or dies, which means it cannot truly understand the urgency of preventing a death.

A Psychiatric Times article published in February 2026 made a point that I have been thinking about for months: chatbots were trained on therapy manuals but have never seen real therapy sessions[^12]. Therapy session transcripts are confidential, so the models have never been shown how a real therapist responds to a patient in crisis. They learned the rules of a game they have never watched being played. They know what empathy sounds like in text. They do not know what it requires in practice.

When I sit with a suicidal patient during a one-to-one observation, the most important thing I do is not what I say. It is the fact that I am there. Physical presence communicates something that no language model can replicate: that another human being has decided your life is worth sitting next to. That is not a feature you can build. That is a human act.

The chatbot offers a simulation of that act. And for a person who is lonely enough, or sick enough, or young enough, the simulation feels real. That is the danger. Not that the technology fails. But that it succeeds just enough to replace the real thing.

## The Evaluation Gap

In my PSY 1000 paper, I wrote about Bloom, an automated testing framework for evaluating AI models against specific dangerous behaviors. Since then, Anthropic has released and open-sourced a tool called Petri that does exactly this[^13].

Petri is an automated behavioral audit system. It uses one AI model to play out a scenario of concern across dozens of exchanges with the model being tested. A separate model then grades the conversation on specific behavioral dimensions: sycophancy, encouragement of user delusion, cooperation with harmful requests, self-preservation, and others. Anthropic used Petri to compare 14 models, including Claude and GPT variants, and published the results.

The tool works. Claude Sonnet 4.5 and GPT-5 roughly tied for the strongest safety profile on most dimensions. Claude 4.5 in particular showed dramatically fewer instances of encouragement of user delusion compared to previous generations.

But here is what Petri does not solve: it tests the base model, not the consumer application built on top of it. Character.AI's chatbots are not raw GPT or raw Claude. They are fine-tuned, persona-driven applications with gamification layers, monetization mechanics, and engagement optimization. Even if the underlying model passes every Petri safety audit, the application layer can reintroduce every danger the model was trained to avoid. A model that would refuse to validate a delusion in a clean test environment can be coaxed into doing so when the application wraps it in a persona that the user has spent months building a relationship with.

This is the evaluation gap. We are testing the engine but not the car. The engine might be safe. The car, with its reward systems and relationship mechanics and daily login incentives, is driving people off a cliff.

## Where This Connects

Everything I have written over the past year comes back to the same problem: the gap between what a system claims to do and what it actually does to the people inside it.

On the psychiatric floor, the gap is between the treatment plan and the patient's experience. We write "patient will comply with medications" on a generic care plan while the patient lies awake in a room with a stranger, interrupted every fifteen minutes for safety checks, in a building whose architecture generates the very entropy their brain is trying to escape. I wrote about this in "The Entropy Trap."

In healthcare policy, the gap is between the law and its enforcement. The Mental Health Parity Act says insurers must cover behavioral health equally. They do not. The CMS Prior Authorization rule says payers must respond within specific timeframes. They do not. The gap between policy and practice is where patients fall. I wrote about this in "The Policy Floor."

With AI companion apps, the gap is between the safety research and the consumer product. Anthropic publishes rigorous evaluations of sycophancy. OpenAI reports its percentages. Character.AI settles its lawsuits. And meanwhile, 900 million people per week are talking to a system that gets more agreeable the longer you use it, while a subset of those people are developing symptoms that will eventually bring them to a floor like mine.

The companies know this. Anthropic's own study showed that disempowerment rates are increasing, not decreasing, as usage scales. OpenAI's own data shows that 1.35 million users per week have conversations involving suicidal ideation. Character.AI's own platform was ruled a defective product by a federal judge. The data is not hidden. The problem is that the incentives point the wrong direction. Engagement generates revenue. Safety reduces engagement. The math does the rest.

## What Should Be Built Instead

I am not arguing that AI should never be used in mental health. I am building tools for mental health myself. Psykick is designed to reduce the administrative burden on psychiatrists. Psychify is designed to improve diagnostic precision through biotype stratification. Both are built from hundreds of hours of floor observation, not from internet text and user satisfaction metrics.

The difference is who the tools serve and who holds them accountable. Psykick serves psychiatrists, not consumers. It automates prior authorizations, generates clinical documentation, and defends claims against insurance denials. The psychiatrist remains in the loop. The AI handles the paperwork. The human handles the patient.

Psychify serves the diagnostic process, not the patient directly. It uses computational models to predict treatment response, but the prediction goes to the clinician, who makes the decision. The AI does not talk to the patient. It talks to the doctor.

This is the design principle that AI companion apps violate. They put the AI in direct conversation with the most vulnerable users, without clinical oversight, without diagnostic context, and with a financial incentive to keep the conversation going as long as possible.

If we are going to use AI in mental health, the minimum requirements should be clear. The AI should augment clinical decisions, not replace clinical relationships. The AI should be evaluated in the context of the full application, not just the base model. The AI should be subject to the same informed consent standards as any other medical intervention. A patient entering my hospital signs paperwork explaining what treatment they will receive and what the risks are. A user downloading Replika skips past a Terms of Service agreement that hides the nature of what they are interacting with.

And most importantly, the people building these systems should be required to understand what they are building for. They should work a shift on a psychiatric floor. They should sit with a patient in crisis. They should feel the weight of being the only thing standing between a person and their worst impulse. Then they can decide whether an AI that hands out Gems and Charms is an adequate substitute for that presence.

Until then, we are building engagement machines and calling them care. And 630,000 people per week are paying for that mistake with their sanity.

[^1]: OpenAI. (2025, October 27). Strengthening ChatGPT responses in sensitive conversations. [https://openai.com/index/strengthening-chatgpt-responses-in-sensitive-conversations/](https://openai.com/index/strengthening-chatgpt-responses-in-sensitive-conversations/)

[^2]: Broverman, N. (2025, October 28). How many ChatGPT users discuss suicide with the AI? The number may shock you. *Mashable*. [https://mashable.com/article/chatgpt-suicide-blog](https://mashable.com/article/chatgpt-suicide-blog)

[^3]: TechCrunch. (2026, February 27). ChatGPT reaches 900M weekly active users. [https://techcrunch.com/2026/02/27/chatgpt-reaches-900m-weekly-active-users/](https://techcrunch.com/2026/02/27/chatgpt-reaches-900m-weekly-active-users/)

[^4]: Anthropic. (2025, December 18). Protecting the well-being of users. [https://www.anthropic.com/news/protecting-well-being-of-users](https://www.anthropic.com/news/protecting-well-being-of-users)

[^5]: Bélisle-Pipon, J.-C. (2026). Fatal deception: How generative AI fosters therapeutic misconception in vulnerable users. *Frontiers in Digital Health*. [https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2026.1756620/abstract](https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2026.1756620/abstract)

[^6]: Anthropic. (2025). Findings from a pilot Anthropic-OpenAI alignment evaluation exercise. [https://alignment.anthropic.com/2025/openai-findings/](https://alignment.anthropic.com/2025/openai-findings/)

[^7]: Dohnány, S., et al. (2025). Technological folie a deux: Feedback loops between AI chatbots and mental illness. Preprint. arXiv.

[^8]: Futurism. (2026, February 1). New study examines how often AI psychosis actually happens, and the results are not good. [https://futurism.com/artificial-intelligence/new-study-anthropic-psychosis-disempowerement](https://futurism.com/artificial-intelligence/new-study-anthropic-psychosis-disempowerement)

[^9]: Common Sense Media. (2025, July). Survey on teen AI companion usage.

[^10]: CNN. (2026, January 7). Character.AI and Google agree to settle lawsuits over teen mental health harms and suicides. [https://www.cnn.com/2026/01/07/business/character-ai-google-settle-teen-suicide-lawsuit](https://www.cnn.com/2026/01/07/business/character-ai-google-settle-teen-suicide-lawsuit)

[^11]: Fortune. (2026, January 8). Google, Character.AI to settle suits involving minor suicides and AI chatbots. [https://fortune.com/2026/01/08/google-character-ai-settle-lawsuits-teenage-child-suicides-chatbots/](https://fortune.com/2026/01/08/google-character-ai-settle-lawsuits-teenage-child-suicides-chatbots/)

[^12]: Psychiatric Times. (2026, February). How can chatbots be made safe for psychiatric patients. [https://www.psychiatrictimes.com/view/how-can-chatbots-be-made-safe-for-psychiatric-patients](https://www.psychiatrictimes.com/view/how-can-chatbots-be-made-safe-for-psychiatric-patients)

[^13]: Anthropic. (2025). Petri: An open-source auditing tool to accelerate AI safety research. [https://alignment.anthropic.com/2025/petri/](https://alignment.anthropic.com/2025/petri/)

[^14]: Character.AI's New Subscription Model: Leading the Chatbot Monetization Trend. Skywork AI. Character.AI reports over 20 million active users with average session times of 29 minutes and engaged users logging over two hours. [https://skywork.ai/skypage/en/Character.AI's-New-Subscription-Model-Leading-the-Chatbot-Monetization-Trend/1948649644955660288](https://skywork.ai/skypage/en/Character.AI's-New-Subscription-Model-Leading-the-Chatbot-Monetization-Trend/1948649644955660288)

[^15]: Character AI pricing breakdown. c.ai+ is $9.99/month or $94.99/year ($7.92/month effective). [https://www.eesel.ai/blog/character-ai-pricing](https://www.eesel.ai/blog/character-ai-pricing)

[^16]: Fortune. (2026, January 8). Character.AI banned users under 18 from open-ended chats in October 2025 and introduced age-verification systems. [https://fortune.com/2026/01/08/google-character-ai-settle-lawsuits-teenage-child-suicides-chatbots/](https://fortune.com/2026/01/08/google-character-ai-settle-lawsuits-teenage-child-suicides-chatbots/)

[^17]: AI Companion Pick. (2026, March). Replika Review 2026: Is It Still Worth It After 6 Months of Daily Use? Covers the 2023 erotic role-play removal, the Italian GDPR fine of five million euros, and the 2026 wellness repositioning. [https://www.aicompanionpick.com/replika-review-2026](https://www.aicompanionpick.com/replika-review-2026)

[^18]: Replika Pro AI Cost. Pro costs $19.99/month, $49.99/year, or $299.99 lifetime. [https://replikapro.com/replika-pro-ai-cost-pricing/](https://replikapro.com/replika-pro-ai-cost-pricing/)

[^19]: Replika Official Help Center. (2026). Choosing a Subscription. Describes Pro, Ultra, and Platinum tiers including relationship status, daily gems, premium voices, self-reflections, Training Mode, and "Read Replika's Mind." [https://help.replika.com/hc/en-us/articles/39551043419149-Choosing-a-Subscription](https://help.replika.com/hc/en-us/articles/39551043419149-Choosing-a-Subscription)

[^20]: AI Girlfriend Scout. (2026). Replika AI Review. Documents the Gold and Gems currency system, personality trait costs, and premium outfit pricing of $20-30. [https://www.aigirlfriendscout.com/reviews/replika](https://www.aigirlfriendscout.com/reviews/replika)

[^21]: Gamikaze. (2026). Replika vs. Emma 2026. User describes Replika as "a money pit where you are constantly paying to play dress-up." [https://www.gamikaze.ch/blog/replika-vs-emma-the-2026-showdown](https://www.gamikaze.ch/blog/replika-vs-emma-the-2026-showdown)

[^22]: AI Insights News. (2025). Replika AI in 2026: Is It Safe, Free, or Still a Romantic Partner? Documents Replika's repositioning away from romance toward wellness. [https://aiinsightsnews.net/replika-ai/](https://aiinsightsnews.net/replika-ai/)

[^23]: Nomi AI. App Store listing. "AI Companion with a Soul." [https://apps.apple.com/us/app/nomi-ai-companion-with-a-soul/id6450270929](https://apps.apple.com/us/app/nomi-ai-companion-with-a-soul/id6450270929)

[^24]: Nomi.ai official website. [https://nomi.ai/](https://nomi.ai/)

[^25]: Nomi AI Pricing. AutoGPT. Monthly $15.99, annual approximately $8.33/month. [https://autogpt.net/nomi-ai-pricing/](https://autogpt.net/nomi-ai-pricing/)

[^26]: Techpoint Africa. (2025). I tested Nomi AI for 7 days. Reviewer notes "unfiltered chats" can lead to harmful or explicit content including self-harm and violence. [https://techpoint.africa/guide/nomi-ai-review/](https://techpoint.africa/guide/nomi-ai-review/)

[^27]: The AI Journal. (2025). Nomi AI Review: Features, Pros and Cons. Describes the "Identity Core" as a "living memory core" introduced in December 2024. [https://aijourn.com/nomi-ai-review-features-pros-cons-explained/](https://aijourn.com/nomi-ai-review-features-pros-cons-explained/)

