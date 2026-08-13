# Translate with AI Agent
Recently I translated a novel-length story with the help of an AI Agent (you can read my workflow [here](https://gist.github.com/Gojob2987/c60efcef24b47e18b1c9bdabf12d4381)). The original story was written by [qntm](https://qntm.org/) in English. I retold the story in Chinese (my mother language). I'm moderately confident that my translation was done properly, that the story I told in Chinese is faithful to the original story; I'm absolutely sure that the original story is a masterpiece of science fiction, and it is a great joy to witness the publication of such a story.

I am a software engineer. I started the translation project as a hobby, one seeded at an early stage of life, lying dormant for quite some years, waiting to be activated. This past month I had more free time than before, and I attempted to seriously incorporate AI Agent into my daily workflow, not for the first time. Previously I failed, mostly because I didn't know what to do with the Agent once I set it up.

I was thrilled to learn about the [Karpathy LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) concept during this time, and I wanted to adopt its principles to build something real, something that matters to me, not just a demo. What can I do? What am I interested in? 

Then I heard that *There Is No Antimemetic Division* had been published as a physical book. I first came upon this story as an undergrad, almost 10 years ago. It was mind-blowing. It was a series of stories about ideas went wrong -- ideas that can't be described, ideas that can't be remembered, ideas that 'kill' everyone who comes up with them. It was horrific, scary not by visual or sound, but by the very idea itself.

My study on LLM Wiki and AI Agent somehow brings me back to the story of Antimemetic Division. I read it again, 10 years later, thunderstruck just like the first time. Connections between my AI study and the story quickly manifested themselves. Warning: I'm not professional AI researcher, and I might have mixed 'LLM' with 'AI Agent', please forgive me.
- In the story, there's a memory-erasing anomaly that 'hunts' its victim by isolating them from history, so nothing the victim says or does could be perceived by other people. It's just like the 'unlink' function in Obsidian. Once an article is 'unlinked' with every other article, it becomes isolated and is considered an anomaly, waiting to be linted.
- In the story, operatives proactively flush their own memories to avoid being poisoned by harmful ideas, just like starting a new session in AI Agent workflow to avoid context overflowing, or the 'one session, one topic' principle to avoid context pollution.
- In the story, operatives are trained to restore their memories and knowledge from scratch in case their memories are accidentally flushed. It's like having the AI Agent resume an ongoing work in a new session, by reading the log and progress report.
- In the story, operatives adopt a non-linear research strategy to investigate containment procedures for dangerous anomalies. Studying with the help of AI Agent naturally suits non-linear research, because AI Agent can provide tons of information in each round of conversation, and it's a waste to restrict the conversation to one question per round. I usually run a question log document to record my questions. I would update the log with multiple questions in every round, let AI Agent answer them all. It's batch work.
- ...

At that moment I realized a few things:
- I really like this story!
- The story is valuable, especially in this age of flourishing AI industry.
- I want to translate it into my mother language, so more people can read it.
- This is the project that glues my knowledge on AI and passion on story together. I will practice using AI Agent in my translation work, and see what I can do.

It turns out I could do a lot, apart from the translation text itself:
- I found multiple questions, each with its own merits and forming into individual lines of investigation, ranging from tool use to publication strategy.
- I extracted a translation workflow, which was what I wanted to share in this article originally (this foreword is too lengthy, maybe I will do a separate post / article).
- Discussion with AI Agent greatly enhanced my understanding of the original story. I found that having a peer to discuss my thoughts with was really helpful, and kept my sanity in check.

Without further ado, next I will share my experience on co-working with AI during this translation project.

# What (text) translation needs
Translation is essentially intensive reading and writing, with a lot of thinking involved. There's also translation by listening and speaking, but it's **not** in the scope of this article.

The workflow in this article places the translator at center, with AI agent as an assistant. If you are looking for fully autonomous AI translation, with minimal human intervention, it's **beyond** the scope of this article. 

Translator receives information, understands it, and retells the information in another language / manner.

A few things that facilitate this process, from real life perspective:
- **Quiet room**: When the house is noisy with kids, with dishes and laundry to be done, it's hard to concentrate on reading, writing, listening, or thinking at all in general. Great inventions of the century, vacuum cleaner and washing machine, saved much time from housework. 
- **Discussion peer**: The translator has a base text to work on. Faithful capture of the base text's meaning is top priority. Natural language is ambiguous. A reader never perceives 100% what the author intends (unless under special form of language, like math formula, or programming code), so reader essentially does guesswork. Translator is a reader. Translator at best makes educated guesses on what the author means in the base text. Guesswork needs a second opinion, validation and cross-examination. Doing this alone is risky. Someone to discuss with is reassuring and necessary. Think of a friend, a pen pal, a colleague, an editor.
- **Dictionary**: It is necessary. Expect to encounter unfamiliar words upon reading foreign text. I even need to look up words in my own mother language from time to time.
- **Paper and pen**: Better come in handy, cheap and abundant. There are annotations to be written, and sprawling ideas. What could the author possibly mean here? Would it be a better way to convey X if we do Y? Untracked ideas evaporate fast. Write them down often.

# The agent as environment
AI Agent gives you, the translator, a cozy environment to work in.

Following the analogies:
- **Quiet room**: Physically, you still need to look for the room yourself. But AI Agent does two things for you to smoothen the experience:
	- AI Agent is good at doing linting, grammar check and archiving, the dirty work that disrupts you from working on the juicy parts of creative thinking. Refer to [Karpathy LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) for this idea.
	- AI Agent provides tons of information, fast, almost overwhelmingly, for you to absorb. You might find it easier to get soaked in the information, as everything you read is related to your work, thereby creating the metaphoric 'room' for you to concentrate (a room of information, related to your work, secluding you from information irrelevant to your work). You might find some information distracting, diverging from your goal, arousing your curiosity to chase hares. In the second case, AI Agent is also especially capable of tracking fleeting thoughts for later investigation. It's double-edged really. 
- **Discussion peer**: Agent is not only Chatbot pro max, it can also record and read from conversation history, annotations and various reference material. The more you discuss with Agent, the better it learns about your style, your expectation, your understanding of the base text, and the base text itself.
- **Dictionary**: AI Agent is a highly customizable dictionary, with a flexible answer format. I usually ask it to provide meaning in original text, pronunciation (i.e. IPA or Pinyin), example sentences, translation candidates. Improvise your own.
- **Paper and pen**: I use Obsidian (a sleek text editor + viewer), OpenCode (AI Agent), DeepSeek (LLM, the brain behind the agent) and Git (version control, remote file storage) in my project. They are highly customizable and the experience is smooth. I read and write the documents in Obsidian. I have a terminal window opened chatting with AI Agent. I ask the Agent to read from / write into persistent text documents most of the time (unless it's chitchat).
	- About price: Thanks to the community and companies such as DeepSeek, AI Agent is very affordable. I use Obsidian, OpenCode and Git for free. DeepSeek is incredibly cheap (though they might raise the price in the near future, according to their website). In my most intensive translation days I spent less than 2 CNY (about 1/3 of 1 USD) a day. The entire translation project took around 3 USD regarding token usage.
	- About freedom of instantiation: All these tools are easily swappable; the choices are yours. One thing to consider regarding LLM selection for translation: look for an LLM trained to understand source/target languages. For instance, if you want to translate something into Chinese, chances are Chinese LLM have used more training materials written in Chinese, making them more capable of performing Chinese translation tasks. There should be a tier list or scoreboard somewhere on the Internet that rates each LLM's performance on a given language.

Also, I find the greatest strength of AI Agent in this project to be its ability to materialize ideas into text. This has two critical benefits:
- I ask AI Agent to capture my fleeting ideas into text files, such as investigation report or session logs. When I later want to dig into a line of investigation, or to resume working, all the AI Agent needs to do is to read the text file and catch up.
- I ask AI Agent to capture routines and workflows as persistent text files. AI Agent uses them as guides. The guides get continuously polished during the process. It's a self-reinforcement loop.

# Translation as an engineering project
I'm a software engineer who happens to love science fiction. I realized from the very start that translation is a process of continuous polish and refinement, just like coding. 

A translation project can benefit from a software engineering perspective by borrowing the following practices:
- **Start small, build incrementally**. A translation project is a really nice starting point for trying out AI Agent. It's pure text processing work. It doesn't require all the fancy AI abilities marketed on social media. It doesn't require numerous dependencies on foreign packages. Everything is text, and the project can literally start from scribbling a few annotations, then asking the AI Agent what they think about it. That's how I started the project. I didn't have the current layered project structure or workflow nailed down until the very end of the project, and that's to say I kept making adjustments to them, tested out how they work, till the very end.
- **Persistent storage**. All ideas, background, questions and progress are saved in text files. This avoids overflowing the Agent's context window when translating large volume of text, because the Agent doesn't need to store everything in running memory. I also explain the rationale of my decisions to Agents, recorded in the text files, so Agents can learn and preserve their knowledge. Also, save routines as workflow for AI Agent to follow, so you don't need to spend time on explaining how to get things done multiple times.
- **Version control / Logging**. A version control system such as Git makes file changes easily tracked, as well as making cross-environment (i.e. workplace, home) work and multi-person cooperation effortless. I also ask the AI Agent to keep a log file for almost every process, so the Agent can automatically resume work by reading its own log, or understand the project's history by reading the log.
- **Structural design**. Returning to what a translator really does: read original text, think, retell in another language. We immediately see the input and output of this process, and everything in between can be addressed as the by-product. So I structure my translation project as follows. It's nice to have files structured and classified into corresponding folders, so as to keep the house clean.
	- **Input**: the original text (base text)
	- **Output**: the translated work, and publication-related work (i.e. Carousel cards suited for social media posts, scripts to produce the cards)
	- **By-product**:
		- annotation
		- logs (to track questions and answers, the process of polish and review)
		- reference (this could arguably move into 'Input', but in my case the reference was extracted by AI Agent from my annotations, so it's sort of in the middle ground. Freedom of instantiation is the reader's')

# The value of the human
In my humble opinion: AI is stochastic, which is to say it does guesswork based on probability. When you ask it to write something for a given prompt, it answers a combination of words most likely to occur in the given circumstance.

AI is good at doing measurable things, following well-documented steps, under clearly written rules.

Think of AI Agent as a junior engineer joining the project. They were taught this and that at school and first-day lectures, mostly rules, regulations and outdated knowledge in school textbooks. What they lack is the hidden, unspoken context: knowledge about the project, value model of how the company runs, the team's style of cooperation and operation -- everything that's not explicitly written down. AI can make up for some of these by deducing, but often it misses something, from a lack of context. Some of the context is not learnt, but experienced, and might be difficult for even humans to perceive.

But to perceive it human will, especially when something goes wrong, which happens often. To make the human - AI Agent pair more productive, I see human contributing in follow aspects, wherein lies the value:
- **Hidden context**: From the author's biography to latent jokes / references, the human translator knows a lot more about the text than their AI Agent (that is, if the only input AI Agent receives is the base text). By annotating the base text, human can introduce a significant amount of background knowledge into the translation project.
- **Feeling**: AI Agent can provide multiple translation candidates, based on guess. More often than not they are 'off a bit', and the human translator should trust their gut instinct to pick a wording that looks most comfortable to them. Human translator is able to perceive caveats in the text, which are hard to identify by deduction.
- **The common tongue / cultural norm**: Human translator knows how people speak in today's language. AI Agent learns from training materials that are by nature outdated. Especially for languages with less or little training materials, AI Agent is not trained to learn that language so well, and could perform badly at translating alone. Human intervention is most helpful in such cases. 
- **Passion and commitment**: Humans have passion and commitment, the willingness to polish the work they love, to see it done, sometimes without considering the cost-effectiveness. AI Agent does as told. This is why the translation project should be led by the human translator.

# The end
This turns out to be longer than I expected.

I drafted a list of ideas at first, and used AI Agent to provide an outline as reference. Then I hand-typed the above article, asking Agent to do a final lint check.

I realized writing an article is different from translating. In translation there's a base text, and both human translator and Agent work towards making the guesswork that's most natural. The important part is to keep the idea right, faithful to the base text, then express it in a natural-sounding way. article writing is different. There's no base text to follow, and I think form and ideas are equally important here. I would start a new line of investigation on the creative-writing-workflow later, and that's beyond the scope of this article.

# Reference
- qntm - author of "There Is No Antimemetic Division": https://qntm.org/
- Karpathy LLM Wiki: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- my translation workflow: https://gist.github.com/Gojob2987/c60efcef24b47e18b1c9bdabf12d4381
---

© 2026 Gojob. This article is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — you are free to share and adapt it, with attribution to the author.

Originally published at: https://github.com/Gojob2987/translate-with-ai-agent
Simplified Chinese version: https://github.com/Gojob2987/translate-with-ai-agent/blob/main/与人工智能体一起翻译.md