# How to use
- I ask Agent to investigate → Agent creates report + this question log
- I read report, write questions with `==highlights==` at increasing depth (1 → 1.1 → 1.1.1)
- I say "question log updated, continue" → Agent answers and updates report

# Phase 1: Exploration
1. I think there are actually two 'essays' here. One [<case-project>/My Thoughts on Coauthoring With AI Agent.md] is for human readers, introducing the concepts and workflows of co-translation with AI. One [<case-project>/artifacts/translation-workflow.md] is for agent readers, describing the translating workflow as a practical guide / a set of rules. Human oriented essay should be relatively abstract, easy to read, intended to give inspiration and general direction, just like [<personal wiki>/llm-wiki.md]. AI agent oriented essay should be matter of fact, clear cut, practical, intended to give executable rules. How do you propose we develop the two essays? I feel like we are refactoring ideas here: the two essays share significant common ground, with a major difference in their intended audience, which affects essay tone, style among other things.
	1. three-layer structure is good.
2. What is the essay's single thesis? (candidate: "AI co-translation is an environment, not a replacement — workflow is the product")
	1. "AI co-translation is an environment, not a replacement". Drop the product part, because I think there's a lot of product, and workflow doesn't describe it all.
3. Who is the audience — Chinese sci-fi/fan-translation community (Rednote), technical community (Github), or both?
	1. Both. I want readers without much technical background to be able to understand this workflow, so I'm trying to explicitly make real life everyday examples to nail that connection. My publication plan is two fold, to post on social network like Rednote as a personal hobby / gain some traffic, then to post on github as some 'serious' work, as my contribution to the community, as my proof of career. 
4. Essay language: Chinese (Rednote), English (Github), or bilingual?
	1. Use English, because the software engineering ideas are expressed in English, and AI agent oriented essay should be in English to achieve high compilability. I will personally write the Chinese version myself after we polish the idea core in English.
5. Length and depth: essay (~2000-3000 字?) or a longer consolidation piece?
	1. Rednote supports ten thousand words per post, so word limit is not an issue here. Keep the intended audience in mind, follow the principle of telling human readers a story v.s. showing ai agent the executable rules, and word limit shouldn't be a problem.
6. How much of the case project's process should the essay expose (workflow diagrams, report excerpts, ledger screenshots)?
	1. Since I will eventually opensource the entire project, everything in this project can be used as case examples. Just don't overwhelm the readers with examples.
7. Should the essay include a practical setup section (Obsidian + opencode + DeepSeek + git, cost, off-hours discounts)?
	1. Only briefly mention this, give the freedom of choice to readers themselves. a.k.a freedom of instantiation.
8. (pending) how to structure the essay from the report skeleton
	1. Let's polish the report first, then discuss rendering.
9. (pending) where to publish and when (before/after ThinKingDom outreach)
	1. ThinKingDom hasn't replied, let's not wait for them, we are on our own.
10. An idea: local best and global best.
	1. I think you already mentioned this as a principle in the report, so this question can be closed.
11. ==“信、达、雅”是什么意思？“译事三难：信、达、雅。求其信已大难矣，顾信矣不达，虽译犹不译也，则达尚焉。”又是什么意思？==

## translation-workflow
1. Use 'Gojob' for translator name, it's my github name.
2. Apart from introductory meta data (i.e. source of extraction, data), keep content project agnostic, so as to achieve compatibility with future translator projects adopting this workflow. No need to mention date (i.e. Story-logic reading (adopted 2026-08-06)) in the workflow, readers have no use of this. We can use git version log for tracking, so no need to track changes in the workflow content itself, unless there's major revamp.
3. Keep language choice unified, unless there is a special need (discuss with human upon this). That means only English in the English essay, and only Chinese in the Chinese essay.
4. Current project structure seems to have room for improvement. 'Output' seems to be overgeneralizing, because it can contain everything apart from the input. Or maybe we can divide by input/output(translated work, published work)/by-product(knowledge, log, research, etc.)? I hope people without much software engineering background can understand this structure. Let's discuss.
	1. yes, use by-product
	2. yes, move
	3. keep Research at root, it's not fiction specific.

# Phase 2: Working
## Essay outline:
1. Outline structure is fine.
2. Case evidence is a bit hard to understand. Try to briefly explain what each does. No constraint on only using Antimemetic Division project. Readers might not have read the Antimemetics Division translation project, so this thought on translation workflow should be a standalone essay.
3. Case evidence should be English only.

## Essay drafting (2026-08-11):
11. Who writes the essay? I feel we are shifting from translation to creative writing — the identity and role of a writer differ from a translator's. In writing, form and ideas are equally important. I will write my own essay, using the agent's draft / outline as material.
	1. Translator writes the final essay (like the annotation essay). Agent draft v0.1 (`artifacts/co-translation-essay.md`) demoted to reference material: idea core, examples, structure bank.
12. Future line: we will eventually shift from translation to creative writing, maybe in the same repo, maybe as a note — it's all about reading and writing anyway. There will be a separate `creative-writing-workflow`, distinct from `translation-workflow`.
	1. Keep the current goal: consolidate the translation work, finish the essay. Park creative-writing thoughts in this investigation; start a separate line of investigation once this one concludes (or diverges too much).

# Phase 3: Publishing
1. Which license should I use for opensource articles? There are two articles, and I think maybe they should use different license? The human oriented article is intended to be read by human, I wrote it personally, so I think it should be licensed as some kind of literature / non-fiction? CC-4.0 seems fine. My doubt comes with the second article, the AI Agent oriented one. I want to publish it like a skill / workflow file that people can download and use. How should it be licensed to? 
	1. what are 'copyrightable' and 'attribution'? I'm rather new to the domain of copyright and license.
		1. Do not edit my question log unless specifically permitted / asked to.
		2. What do I benefit if I use CC BY 4.0? A more uniformed gist structure? Can I do CC BY 4.0 for essay, and MIT for workflow, in the same gist? Or maybe do a separate gist link, with different license? I don't want to burden readers to make attribution to me when they try out the workflow, they are free to make their own addition. I think the workflow is, unlike personal essay, mostly about conveying the idea and let end users adapt as they wish, while in personal essay form and idea and both important.
			1. What is MIT license?
			2. If I want to use an opersource skill with MIT license in my project, what should I do regarding copyright? Can I just copy and paste it?
				1. Do people normally use a separate license file for MIT / CC BY 4.0, or put it as part of the article file's content?
					1. So there is a separate license file in the gist/repo, and article has an embedded line referring to the license file, and when the article gets spread, the reference for license should be kept, so later users can trace back to the license by following the link, correct? Does the content of the license file matter, or knowing it's type/protocol (MIT / CC BY 4.0) suffices? What if the license file link gets stale, or its license content got changed somehow?
2. Can I link to my workflow file (under MIT) in my essay file (under CC BY 4.0), when they are licensed separately?
3. Should we extract the licensing / publication part out of this investigation, or keep it integrated so the workflow covers from first reading to publication?
	1. Keep integrated. The 7-step workflow is end-to-end by design; licensing lives in Phase 6 + red lines; knowledge already filed where used (§6.5, public workflow license rule); publication questions are grounded in this project's artifacts; creative writing is the next planned line and inherits this knowledge. Extraction only if publishing becomes a portfolio concern (report §6.7).

## translation-workflow
1. Consider clarifying the goal and structure of the workflow from the very start. This workflow also differs from some other skills / workflows as it requires intensive human intervention. Refactor / restructure the workflow with that in mind.
	1. There could also be a 'set up' or 'hook' section, describing how to start this workflow. I image AI Agent should understand this workflow first, then human ask Agent 'what do I do / where should we start', and Agent answers the plan, and they progress together.
2. Maybe we should save two version of the workflow, one is as project-agnostic as possible, to be published open-sourced on github gist, the other is adapted to our current translation project, recording our choices and habits. The first one is a public version, the second one is our private version.
3. When we publish the public version, remove the meta data (status, created, extracted from, owner). Make the workflow as project-agnostic as possible for maximum compatibility. To list some of the droppable content for public version:
	1. meta data
	2. specific license type (CC BY-SA)
	3. investigation in Research/ - I think we can move it into by-product for the public workflow. Other translators might not host multiple fictions in one repo, so don't assume their Research/ in cross fictions.
	4. 'Omnibus / collected edition' this chapter can be dropped, many fictions don't distinguish between omnibus and online version, I think.
4. For translation phases, clarify in each step the participants, input and output.
	1. AI participants from phase 1, mainly acting as the dictionary.
	2. I think phase 5 is a bit too long, even for our private workflow, and it shouldn't be in the public workflow with such detail. In the public workflow, describe only the publication to github, drop rednote.
	3. Also clarify who does what in each step
	4. Also, I think the annotation phase is incrementally built, and it does not end at a specific step till the very end. The translator might find something worthy of annotating through out the translation process. Maybe we can merge annotation and literal draft together, so translator annotate as they read / draft? We already see that annotation and draft / base text are closely related, with the annotation frequently referring to draft / base text, and we might as well put them together. I truly don't know. I think the benefit of separating annotation from text is the modularity, that they are different objects; but when working in reality, the two are closely related. It might be another freedom of choice for the human translator to decide. The important bit: keep annotation and draft as persistent file, so they don't get lost, and can be referred back to.
	5. How I envision the translation phases, which might be different from the current workflow / what was done in the project, given that there were trial and errors in this project, and the workflow wasn't nailed on day 1: 
		1. human finds text interesting, makes note, looks up for words, wants to translate. A draft / doodle is formed at this stage, maybe on the base text, maybe on a separate text.
		2. human translates, produces a first draft, with various annotations / reference materials
		3. agent read base text, read human draft, extracts information from annotations / reference materials, ask human questions about the worldview and critical background knowledge
		4. agent and human do line by line polishing, contemplate over each line until it reads naturally. Agent discusses with human, proposes candidates and perspectives, human decides.
		5. agent and human read through the translated work again, update annotations (because after the in depth line by line polishing, it's easy to spot missing links in the first runs), find inconsistency or suggest better coherence.
		6. agent does lint check.
		7. agent and human do publication work.
5. Verdicts:
	1. separate MIT gist
	2. goal first + banner
	3. add hook
	4. split, 'translation-workflow-public.md', I want to avoid confusing 'public' as a file extension name
	5. drop all, and look for other potential violations of the project agnostic rule
	6. 7-step
	7. condense
	8. embedded notice + license gist file

## personal essay
1. L50/52 引号方向：这些确实是错误，请直接帮我订正。我的Obsidian字体采用了微软雅黑，渲染出来的双引号方向很不明显。
2. L83 有一个建模：我倾向用‘建模’这个表述，既是目的（建立的模型）也是行为（建模这个动作）。有些时候建立的模型本身不一定是完善的，但是建模这个动作本身是十分有意义的，所以我在这里主要强调建模这个行为，作为一个名词。
3. L3 跨越数年的每一次重读：我希望一句话把它读完，不断句，让文字更紧凑一些。“时光”有点抒情了，一句话解决吧。
4. L3 信，达：这里是区分了评价翻译好坏的三个维度，即信、达、雅，从各个维度分别评价我的翻译。“信”肯定是做到了，”达“应该也还行，“雅”不太确定。所以我用了逗号分隔。
5. L48 爆炸的科技：对，确实有“科技爆炸”的考量在里面。
6. L46 深度的阅读、思考和写作。这里还需要改什么？
	1. 我改了
7. L105 已经修改。
8. L125-L127：我补充了社区连载版链接，统一采用Obsidian的link格式。我觉得参考引用章节现在读起来有点乱，一般大家在写论文的时候是按什么格式提供参考引用的，好像有一个文章名+作者名+出版时间+URL 之类的格式？我想采取一个比较规范的格式。
	1. 你特别标注的[EB/OL]是什么意思？这是个保留符号吗？读者需要看到这个吗？是不是 作者-提名-日期-URL 就可以了？

## Phase 4: Publication
1. There are a few problems with git gist, let's see if we can improve it
	1. I want the files to be presented in license, CN essay, EN essay, pictures. How do I rearrange them?
	2. Is it possible to have something similar to a table of content to the start of the gist?
	3. Maybe we can use a simple repo instead of gist, now that we have a few different types of files to be presented by the same link? I feel like we are not doing it the gist way, or I could be wrong.
2. ==Move local position of the published git repo to <local workspace>.== 
3. ==Maybe we can move the agent oriented workflow to the new repo as well? Because all three files belong to the same project. I don't want to leave the agent oriented one alone. After you are done, deleted stale git gist, and change file mentioning of 'git gist' to simply 'github'.==
4. ==Since files are moved from gist to repo, update urls embedded in the files. I think this only concerns the essay and workflow files in current investigation folder.==