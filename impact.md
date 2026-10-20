# AI coding agents: impact on productivity and jobs
 
Research file for the AI Coding Agents project. Scope is impact only, meaning productivity and jobs, with the evidence on both sides. Compiled October 19, 2026. Almost all the hard data is from the US. I didn't gather any Canadian figures.
 
## Short version
 
Productivity gains are real but smaller than the claims. The better studies land somewhere between +10% and +26% on output measures like pull requests and completed tasks. Self-reports run much higher, with a median of 3x speed in one 2026 survey. The best randomized trial on experienced developers found them 19% slower with early-2025 tools, and the follow-up couldn't produce a clean number. A lot more code is getting written. Evidence that more finished software is shipping is thin.
 
On jobs, the damage so far sits at the entry level. Employment for developers aged 22 to 25 is down roughly 20% from its late-2022 peak, while older developers held steady or grew. Overall software postings are recovering but are still well below 2020 levels, and most of the recovery is senior and AI-titled roles.
 
Whether AI is the cause is still argued. Economy-wide studies from Yale's Budget Lab and the Chicago Fed see no clear AI disruption. Higher interest rates, pandemic overhiring and a change in US tax rules are all competing explanations. AI is also the most-cited reason in 2026 layoff announcements, though some analysts suspect companies use it to avoid naming less flattering causes.
 
## Productivity
 
### Evidence that AI coding tools raise output
 
| Study | What it measured | Result | Caveat |
|---|---|---|---|
| Microsoft rollout of Claude Code and Copilot CLI, early 2026 (tens of thousands of engineers) | Merged PRs per engineer per day, synthetic-control estimate | +24.0% (95% CI +14.5% to +33.7%) | Large and real-world. Counts PRs, not business value. |
| Cui, Demirer et al., three field RCTs at Microsoft, Accenture and a Fortune 100 firm (4,867 developers) | Completed tasks (weekly PRs) | +26.08% (SE 10.3%), larger for junior and short-tenured developers | Randomized, but Copilot-era autocomplete from 2022 to 2024, not agents. Each experiment on its own was noisy. |
| Peng et al., GitHub Copilot lab experiment (95 developers) | Time to build an HTTP server in JavaScript | 55.8% faster (95% CI 21% to 89%) | One small greenfield task. Authors include GitHub and Microsoft staff. A poor guide to mature codebases. |
| Google RCT (96 engineers) | Time on a complex enterprise task | About 21% faster | Seen only in a vendor blog summary. Check the original before citing. |
| Harvard-linked study of 700+ firms, reported October 2026 | Output at firms adopting agents | About +30% code, +20% commits, +23% PRs, no significant change in Jira issues or epics resolved | Unverified. I only found it in an aggregator article, not the paper itself. |
| METR survey of 349 technical workers, Feb to Apr 2026 | Self-reported change | Median 1.4x to 2x in value of work, median 3x in speed | Self-report. METR says to be skeptical, and its own staff reported the lowest gains. |
 
Adoption is near-universal. DORA 2025 found about 90% of respondents using AI at work. A JetBrains 2026 survey, relayed by Uvik (a secondary compilation), has 90% of professional developers using it weekly and 68% daily. DX's data on roughly 4.2 million developers, from November 2025 to February 2026, put AI-authored code at 26.9% of production code, up from 22% the quarter before.
 
### Evidence of limited, zero or negative effect
 
The METR randomized trial from 2025 is the most cited. Sixteen experienced open-source developers worked through 246 real tasks in repos they knew well. With early-2025 tools they took 19% longer (CI +2% to +39%). They had predicted a 24% speedup beforehand and still believed AI had sped them up by about 20% afterward. They accepted fewer than 44% of what the tools generated.
 
DX and Laura Tacho's data on 121,000 developers at 450+ companies shows roughly 93% usage but measured gains that plateaued around 10%.
 
Faros AI's 2025 telemetry covered more than 10,000 developers on 1,255 teams. AI users completed 21% more tasks and merged 98% more PRs, yet company-level delivery metrics stayed flat. Review time rose 91%, PR size rose 154% and bugs per developer rose 9%. Faros's 2026 report (22,000 developers, 4,000+ teams) adds that PRs merged with no review of any kind are up 31.3%, and that incident probability per merged PR has more than tripled. Faros is a vendor, so weigh these accordingly.
 
DORA 2025 (about 5,000 respondents) found AI adoption now goes with higher delivery throughput, reversing 2024's slightly negative result, but still goes with lower delivery stability.
 
Two 2026 papers raise a different concern. One reports that coding agents improve productivity but hurt developers' understanding of the code. Another argues AI assistance can cut experienced developers' productivity by adding maintenance burden. I haven't read either in full.
 
### Why the studies disagree
 
They measure different things. PRs, commits and tasks completed go up easily. Lead time, change failure rate and resolved business issues go up much less.
 
They study different people. The gains look biggest for juniors and newer hires, while the 2025 METR slowdown was in senior developers inside codebases they knew deeply.
 
They study different tools. METR's slowdown used tools from February to June 2025, and agentic CLI tools like Claude Code, Codex and Copilot CLI spread widely from late 2025 into 2026. Most of the positive randomized evidence is older still.
 
The bottleneck also moves. Agents speed up writing, but review, testing and deployment stay the same size, so queues grow. Faros and GitLab both describe this as an "AI paradox."
 
Finally, developers consistently overestimate their own speedup. METR found an average overestimate of 40 percentage points in 2025.
 
### The measurement problem
 
METR's February 2026 update shows how hard this has become to study. The new experiment ran from August 2025 with 57 developers, 143 repos and 800+ tasks, paid $50 an hour instead of the original $150. Time with AI changed by -18% (CI -38% to +9%) for returning developers and by -4% (CI -15% to +9%) for newly recruited ones, where negative means faster.
 
METR called the data an unreliable signal. Developers who value AI most declined to join rather than work without it, and 30% to 50% said they held back tasks they didn't want to do without AI. Time tracking also broke down when people ran several agents at once. METR still believes developers are likely more sped up in early 2026 than in early 2025, but says this data is only very weak evidence of how much. The method best at resisting wishful thinking, randomized trials on real work, is the one that stopped working, because the tools are now too embedded to withhold.
 
## Jobs
 
### Evidence of harm, concentrated at the entry level
 
The strongest study is the Stanford Digital Economy Lab's "Canaries in the Coal Mine?" by Brynjolfsson, Chandar and Chen, built on ADP payroll data covering about 4.6 million workers. For workers aged 22 to 25 in the most AI-exposed occupations, the relative employment decline was 13% in the first draft, 16% in the November 2025 revision (controlling for firm-level shocks) and about 19% in the August 2026 update. For software developers in that age band, employment is down nearly 20% from the late-2022 peak, while older developers grew or held. The 2026 Stanford AI Index repeats the 20% figure. The 16% and 19% numbers are relative gaps against less-exposed jobs, so they don't mean that share of young developers lost work.
 
Indeed Hiring Lab data shows US software postings rebounding about 15% to 18% year over year (sources differ) but still sitting roughly 24% to 27.5% below February 2020. Senior roles made up 71% of the May 2025 to May 2026 increase, and AI-titled roles 37%. A separate Indeed reading from July 2026 has senior postings up 13.5% since January 2025 and entry-level down 6.3%. The share of tech postings asking for five or more years of experience rose from 37% to 42% between mid-2022 and mid-2025.
 
Secondary sources add more. SignalFire's June 2026 report reportedly has new-grad hiring at major tech firms down 50% to 65% versus 2019. IEEE Spectrum's analysis, as relayed by a blog, puts junior postings about 28% below their 2022 peak and the junior share of IT employment down from about 15% to 7% in three years. I haven't checked either against the original.
 
Skills command a premium. Lightcast puts the pay premium for AI-skilled postings at about 28% (roughly $18,000) and PwC at 62%. They measure different things, so don't average them.
 
### Evidence against a large AI-driven effect
 
Yale's Budget Lab updates its tracker monthly. Its September 2026 update found no clear evidence of labor-market disruption tied to AI. The occupational mix isn't shifting in line with exposure, and measures of AI use show no link to employment or unemployment changes. The researchers point out that earlier technology shifts played out over decades.
 
The Chicago Fed (July 2026) found that the occupations most exposed to AI saw employment rise about 4% from 2019 to 2024 while less-exposed ones shrank. In its words, exposure doesn't map mechanically onto job loss. A secondary source says Stanford's own SIEPR brief found unemployment rose slightly more for the least AI-exposed workers. I'd treat that as a lead until checked.
 
On the aggregate outlook, BLS projects about 10% growth in software developer employment from 2025 to 2035, per CNBC in October 2026. Older write-ups cite 15% for 2024 to 2034, which comes from a different projection cycle. TrueUp counts about 67,000 open software engineering roles at tech companies, up about 30% in 2026 and the highest in three years. That sample is narrower than Indeed's, so the two don't really conflict.
 
There are other explanations for weak junior hiring too: pandemic-era overhiring, higher interest rates, and the end of Section 174 R&D tax expensing, which LeadDev has pointed to. None of these can be cleanly separated from AI in the data we have.
 
### Layoffs and AI attribution
 
These are Challenger, Gray & Christmas figures for announced US job cuts. They count announcements, not realized unemployment.
 
| Period | Total cuts | Cuts citing AI | Notes |
|---|---|---|---|
| Full year 2025 | not gathered | 54,836 (about 5%) | Secondary source |
| Jan to Aug 2026 | 529,914 | 116,175 (about 22%) | AI was the leading cited reason for most of the year |
| Jan to Sep 2026 | 573,195 (down 39% vs. same period of 2025) | 120,136 (about 21%) | AI ranked fifth for September alone, at 3,961 cuts |
| Tech sector, Jan to Sep 2026 | 165,925 (up 54% vs. 2025) | not broken out | Tech led all industries |
 
Overall announced cuts are down sharply from last year, so AI's share rose partly because other reasons shrank. The head of Yale's Budget Lab has suggested some companies cite AI to avoid talking about tariffs, policy uncertainty or earlier overhiring, and Amazon has said its cuts weren't AI-driven. An announced cut also isn't the same thing as a role AI actually replaced.
 
### How the two sides fit together
 
Total developer demand is partly recovering while the entry rung shrinks and employers ask for more experience. Entry-level work leans on the tasks agents handle well, like boilerplate, scaffolding and small fixes, and an AI-skilled senior can absorb more output each. Stanford (payroll data, firm-level controls) and Yale (aggregate occupational mix, unemployment duration) are both credible, but they look at different populations. The data can't yet separate AI from the macro factors above.
 
## Key numbers
 
| Metric | Number | Source quality |
|---|---|---|
| PR lift at Microsoft after agent rollout | +24.0% (CI +14.5 to +33.7) | Primary (arXiv) |
| Completed tasks, three field RCTs | +26.08% | Primary (SSRN/MIT draft) |
| METR RCT, 2025 | 19% slower (CI +2 to +39) | Primary (METR) |
| METR follow-up, 2026 | 4% to 18% faster, flagged unreliable | Primary (METR) |
| METR survey, self-reported | 1.4x to 2x value, 3x speed | Primary (METR) |
| Plateau in measured gains (DX) | About 10% | Secondary (ShiftMag) |
| Faros: PRs merged / review time | +98% / +91% | Vendor, via secondary |
| Developers aged 22 to 25 | About -20% from late-2022 peak | Stanford, via multiple outlets |
| Relative decline, AI-exposed workers aged 22 to 25 | -16% (Nov 2025), about -19% (Aug 2026) | Stanford, via secondary |
| Postings vs. Feb 2020 | About -24% to -27.5% | Indeed, via secondary |
| Senior share of 2025 to 2026 postings rebound | 71% | Indeed, via CNBC and others |
| AI-cited announced cuts, Jan to Sep 2026 | 120,136 (about 21%) | Challenger, via secondary |
 
## Gaps and cautions
 
Several figures come from secondary or vendor sources: Faros, Uvik, DX via ShiftMag, SignalFire, IEEE via blogs, and the Harvard 700-firm item. Pull the originals for any number you plan to feature.
 
Some sources disagree and need resolving. Stanford's 20% is "since late 2022" in some outlets and "from 2024" in others. Indeed's year-over-year posting rise shows up as 15%, 18% and 30% depending on dataset and date.
 
Many of the productivity results predate agentic tools. Only the Microsoft rollout study and METR's 2026 work cover agents directly.
 
Code quality, security, cost and capability benchmarks are left for other research files. If the project has a Canadian angle, Statistics Canada and Canadian job-board data are the obvious next step.
 
## Sources
 
- [METR: We are Changing our Developer Productivity Experiment Design (Feb 24, 2026)](https://metr.org/blog/2026-02-24-uplift-update/)
- [METR: Measuring the Self-Reported Impact of Early-2026 AI on Technical Worker Productivity (May 11, 2026)](https://metr.org/blog/2026-05-11-ai-usage-survey/)
- [METR: Early-2025 AI and Experienced Open-Source Developer Productivity (July 2025)](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/)
- [Adoption and Impact of Command-Line AI Coding Agents: Microsoft's Early 2026 Rollout (arXiv)](https://arxiv.org/html/2607.01418v1)
- [Cui et al., Effects of Generative AI on High-Skilled Work: Three Field Experiments (SSRN)](https://papers.ssrn.com/abstract=4945566)
- [Peng et al., Impact of AI on Developer Productivity: Evidence from GitHub Copilot (arXiv)](https://arxiv.org/pdf/2302.06590)
- [ShiftMag: 93% of Developers Use AI, but Productivity Is Still 10% (DX / Laura Tacho)](https://shiftmag.dev/this-cto-says-93-of-developers-use-ai-but-productivity-is-still-10-8013/)
- [Augment Code: The AI Productivity Paradox (Faros, DORA 2025 summaries)](https://www.augmentcode.com/guides/ai-productivity-paradox-engineering-delivery)
- [Larridin: AI vs Human Developer Productivity (Google RCT summary)](https://larridin.com/blog/ai-vs-human-developer-productivity)
- [Tech Insider: AI Coding Agents Add 30% More Code, Not Software (unverified Harvard-linked study)](https://tech-insider.org/ai-coding-agents-30-percent-more-code-not-software-2026/)
- [Uvik: AI Coding Assistant Statistics 2026 (JetBrains survey figures)](https://uvik.net/blog/ai-coding-assistant-statistics/)
- [CNBC: AI is automating coding. So why are software developer job postings on the rise? (Oct 11, 2026)](https://www.cnbc.com/2026/10/11/ai-software-developer-jobs.html)
- [Stanford Digital Economy Lab, "Canaries in the Coal Mine?" coverage: GreatFrontEnd, Aug 2026 update](https://www.greatfrontend.com/blog/frontend-developer-demand-a-job-market-reality-check)
- [Second Talent: AI Impact on the Job Market in 2026](https://secondtalent.com/resources/ai-impact-job-market/)
- [Fortune: Yale Budget Lab and "AI-washing" (Feb 2, 2026)](https://fortune.com/2026/02/02/ai-labor-market-yale-budget-lab-ai-washing/)
- [Search Engine Journal: Yale Budget Lab study summary](https://www.searchenginejournal.com/are-ai-tools-eliminating-jobs-yale-study-says-no/557686/)
- [Ohio CPA: Chicago Fed and Yale findings (July 24, 2026)](https://ohiocpa.com/get-involved/news/2026/07/24/report--jobs-in-occupations-most-exposed-to-ai-increased-by-4)
- [Challenger, Gray & Christmas: June 2026 report](https://www.challengergray.com/wp-content/uploads/2026/08/Challenger-Report-June-2026.pdf)
- [Challenger September 2026 figures (via 4 Corner Resources)](https://www.4cornerresources.com/?p=210349)
- [Challenger August 2026 figures (via TechJack Solutions)](https://techjacksolutions.com/?p=84785)
- [HatchWorks: The Software Engineer Shortage in 2026](https://hatchworks.com/blog/gen-ai/software-engineer-shortage/)
- [Full Scale: The Developer Shortage in 2026 (IEEE Spectrum figures)](https://fullscale.io/blog/developer-shortage/)
- [Implicator: Software engineering openings up 30% (TrueUp, Indeed experience data)](https://implicator.ai/software-engineering-openings-jump-30-even-as-52-000-tech-workers-lose-jobs)
 
