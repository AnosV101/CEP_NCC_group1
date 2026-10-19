# AI coding agents: impact on productivity and jobs

Research file for the AI Coding Agents project. It covers the impact side only (productivity and jobs) and gives the evidence on both sides. Compiled October 19, 2026. Nearly all the hard data is from the US. I didn't gather Canadian numbers.

## Short version

The productivity gains are real, but they're smaller and messier than the marketing suggests. The better studies put the lift at roughly 10% to 26% on output measures like pull requests and completed tasks. Self-reports run much higher, with a median of 3x speed in one 2026 survey. The best randomized trial on experienced developers found them 19% slower with early-2025 tools, and the follow-up couldn't produce a clean number. More code is getting written. Evidence that more finished software is shipping is thin.

On jobs, the damage so far sits at the entry level. Employment for software developers aged 22 to 25 is down roughly 20% from its late-2022 peak, while older developers held steady or grew. Overall postings have recovered some but are still well under 2020 levels, and most of the recovery is in senior and AI-titled roles.

Whether AI caused any of this is still being argued. Yale's Budget Lab and the Chicago Fed see no clear AI-driven disruption across the economy. Interest rates, pandemic-era overhiring and a US tax rule change all compete as explanations for weak junior hiring. AI is also the most-cited layoff reason in 2026, though some analysts think companies are using it as cover for other problems.

## Productivity

### Evidence that AI coding tools raise output

| Study | What it measured | Result | How far to trust it |
|---|---|---|---|
| Microsoft rollout of Claude Code and Copilot CLI, early 2026 (tens of thousands of engineers) | Merged PRs per engineer per day, synthetic-control estimate | +24.0% (95% CI +14.5% to +33.7%) | Large, real-world, causal-style design. It counts PRs, which says nothing about business value. |
| Cui, Demirer et al. (three field RCTs at Microsoft, Accenture and a Fortune 100 firm; 4,867 developers) | Completed tasks (weekly PRs) | +26.08% (SE 10.3%), with bigger gains for junior and short-tenured developers | Randomized, but the tool was Copilot-style autocomplete (2022 to 2024), not agents. Each single experiment was noisy. |
| Peng et al. (GitHub Copilot lab experiment; 95 developers) | Time to build an HTTP server in JavaScript | 55.8% faster (95% CI 21% to 89%) | One well-scoped greenfield task, and the authors include GitHub and Microsoft staff. Not a good guide to mature codebases. |
| Google RCT (96 engineers) | Time on a complex enterprise-grade task | About 21% faster | Only seen secondhand on a vendor blog. Check the original before citing. |
| Harvard-linked study of 700+ firms (reported Oct 2026) | Output at firms adopting agents | About +30% code, +20% commits, +23% PRs, with no significant change in Jira issues or epics resolved | Unverified. I only found it in an aggregator article, not the paper. Treat it as a lead. |
| METR survey of 349 technical workers (Feb to Apr 2026) | Self-reported change | Median 1.4x to 2x in value of work, 3x in speed | Self-report. METR itself says to be skeptical, and its own staff reported the lowest gains. |

Adoption is close to universal. DORA 2025 found about 90% of respondents using AI at work. A JetBrains 2026 survey, as relayed by Uvik (a secondary compilation), has 90% of professionals using it weekly and 68% daily. DX's data on about 4.2 million developers (Nov 2025 to Feb 2026) puts AI-authored code at 26.9% of production code, up from 22% the quarter before.

### Evidence of limited, zero or negative effect

METR ran a randomized trial in 2025 with 16 experienced open-source developers on 246 real tasks in repos they knew well. With early-2025 tools they took 19% longer (CI +2% to +39%). They had predicted a 24% speedup, and afterward they still believed AI had made them about 20% faster. They accepted fewer than 44% of the code the tools generated.

DX and Laura Tacho studied 121,000 developers across 450+ companies. Usage was around 93%, yet measured productivity gains plateaued near 10%.

Faros AI's 2025 telemetry (10,000+ developers, 1,255 teams) found AI users completed 21% more tasks and merged 98% more PRs, but company-level delivery metrics didn't move. Review time rose 91%, PR size rose 154% and bugs per developer rose 9%. Faros is a vendor, so weigh it accordingly. Its 2026 report (22,000 developers, 4,000+ teams) says PRs merged with no review at all, human or agent, were up 31.3%, and that production-incident probability per merged PR more than tripled. Those are also vendor-published figures.

DORA 2025 (about 5,000 respondents) found AI adoption now correlates with higher delivery throughput, reversing 2024's slightly negative result, but still correlates with lower delivery stability.

Two 2026 papers raise a different worry. One reports that coding agents improve productivity while hurting developers' understanding of the code. The other argues AI assistance can lower experienced developers' productivity by adding to the maintenance load. I haven't read either in full.

### Why the studies disagree

Part of it is what gets counted. PRs, commits and tasks rise easily. Lead time, change failure rate and resolved business issues rise much less. Part of it is who gets studied: the gains look biggest for juniors and newer hires, while the 2025 METR slowdown was in senior people working in codebases they knew deeply. Tool generations differ too. METR's slowdown used February to June 2025 tools, and agentic CLI tools like Claude Code, Codex and Copilot CLI only spread widely from late 2025 into 2026.

The bottleneck also moves. Agents speed up writing, but review, testing and deployment stay the same size, so queues grow. That's the Faros and GitLab "paradox" story. And developers consistently overestimate their own speedup. METR measured an average overestimate of 40 percentage points in 2025.

### The measurement problem: METR's 2026 follow-up

METR's own update (Feb 24, 2026) is the clearest statement of how hard this has become. The new study started in August 2025 with 57 developers across 143 repos and 800+ tasks, paid $50/hr instead of the original $150/hr. In METR's convention, a negative number means tasks got faster. Returning developers showed -18% (CI -38% to +9%) and newly recruited developers showed -4% (CI -15% to +9%).

METR called this an unreliable signal. Developers who value AI most declined to participate rather than work without it, and 30% to 50% said they held back tasks they didn't want to do without AI. Time tracking also broke down when people ran several agents in parallel. METR's stated belief is that developers are probably more sped up in early 2026 than in early 2025, but this data is only very weak evidence of how much.

So the hardest method to fool, a randomized trial on real work, is the one that stopped working, because the tools became too embedded to withhold.

## Jobs

### Evidence of harm, concentrated at the entry level

The central source is the Stanford Digital Economy Lab paper "Canaries in the Coal Mine?" (Brynjolfsson, Chandar and Chen), built on ADP payroll data covering about 4.6 million workers. For workers aged 22 to 25 in the most AI-exposed occupations, the relative employment decline was 13% in the first draft, 16% in the November 2025 revision (after controlling for firm-level shocks) and about 19% in the August 2026 update. Software developers aged 22 to 25 are down nearly 20% from their late-2022 peak, while older developers' employment grew or held. The 2026 AI Index repeats that figure. The 16% and 19% numbers are relative gaps against less-exposed jobs, so they don't mean that many jobs vanished in absolute terms.

Indeed Hiring Lab data shows US software development postings up about 15% to 18% year over year (sources differ), but still roughly 24% to 27.5% below February 2020. Senior roles accounted for 71% of the May 2025 to May 2026 increase, and AI-titled roles for 37%. A separate July 2026 Indeed reading has senior postings up 13.5% since January 2025 and entry-level postings down 6.3%.

Some secondary sources add more. SignalFire (June 2026) reportedly has new-grad hiring at major tech firms down 50% to 65% versus 2019. IEEE Spectrum, via a blog, has junior postings about 28% below their 2022 peak and the junior share of IT employment falling from about 15% to 7% in three years. I didn't check either against the original. On pay, Lightcast puts the premium for AI skills at about 28% (roughly $18,000) and PwC at 62%. They measure different things, so don't average them.

### Evidence against a large AI-driven jobs effect

Yale's Budget Lab updates its tracker monthly. Its September 2026 update still finds no clear evidence of disruption tied to AI: the occupational mix isn't shifting in line with exposure, and AI-usage measures show no link to employment or unemployment changes. The team points out that earlier technology shifts played out over decades. The Federal Reserve Bank of Chicago (July 2026) found employment in the most AI-exposed occupations rose about 4% from 2019 to 2024 while less-exposed ones shrank, and said exposure doesn't map mechanically onto job loss. A secondary source says Stanford's own SIEPR brief found unemployment rose slightly more for the least AI-exposed workers. Treat that one as a lead.

The aggregate outlook is fine. BLS projects about 10% software developer employment growth from 2025 to 2035 (per CNBC, Oct 2026), while older sources cite 15% for 2024 to 2034. Those come from different projection cycles. TrueUp counts about 67,000 open software engineering roles at tech companies, up about 30% in 2026 and the highest in three years. That's a narrower sample than Indeed's, so the two don't conflict.

Junior hiring also has other suspects: post-pandemic overhiring, higher interest rates, and the end of Section 174 R&D tax expensing (raised by LeadDev). None of these can be cleanly separated from AI.

### Layoffs and the AI label

Challenger, Gray & Christmas tracks announced US job cuts, which are announcements and not realized unemployment.

| Period | Total cuts | Cuts citing AI | Notes |
|---|---|---|---|
| Full year 2025 | not gathered | 54,836 (about 5%) | Secondary source |
| Jan to Aug 2026 | 529,914 | 116,175 (about 22%) | AI was the top cited reason for most of the year |
| Jan to Sep 2026 | 573,195 (down 39% vs. same period 2025) | 120,136 (about 21%) | AI was only fifth for September (3,961 cuts) |
| Tech sector, Jan to Sep 2026 | 165,925 (up 54% vs. 2025) | not broken out | Tech led all industries |

Overall announced cuts are down sharply from last year, so the AI share went up partly because other reasons fell. The director of Yale's Budget Lab has suggested some companies cite AI to avoid talking about tariffs, policy uncertainty or earlier overhiring, and Amazon has said its cuts weren't AI-driven. An announced cut also isn't the same thing as a role AI actually replaced.

### How the two sides fit together

Total developer demand is partly recovering while the entry rung shrinks and employers ask for more experience. Indeed has the share of tech postings requiring five or more years rising from 37% to 42% between mid-2022 and mid-2025. Entry-level work leans on tasks agents do well, like boilerplate, scaffolding and small fixes, and an AI-skilled senior can now absorb more of it. The data still can't separate AI from the macro factors. Stanford (payroll data, firm-level controls) and Yale (aggregate mix, unemployment duration) are both credible, and they look at different populations.

## Key numbers

| Metric | Number | Source quality |
|---|---|---|
| PR lift at Microsoft after agent rollout | +24.0% (CI +14.5 to +33.7) | Primary (arXiv) |
| Completed tasks, three field RCTs | +26.08% | Primary (SSRN / MIT draft) |
| METR RCT 2025 | 19% slower (CI +2 to +39) | Primary (METR) |
| METR follow-up 2026 | 4% to 18% faster, flagged unreliable | Primary (METR) |
| METR survey, self-reported | 1.4x to 2x value, 3x speed | Primary (METR) |
| Plateau in measured gains (DX) | About 10% | Secondary (ShiftMag) |
| Faros: PRs / review time | +98% / +91% | Vendor, via secondary |
| Developers aged 22 to 25 | About -20% from late-2022 peak | Stanford, via multiple outlets |
| Relative decline, AI-exposed, aged 22 to 25 | -16% (Nov 2025), about -19% (Aug 2026) | Stanford, via secondary |
| Postings vs. Feb 2020 | About -24% to -27.5% | Indeed, via secondary |
| Senior share of 2025 to 2026 postings rebound | 71% | Indeed, via CNBC and others |
| AI-cited announced cuts, Jan to Sep 2026 | 120,136 (about 21%) | Challenger, via secondary |

## Gaps to close before publishing

Several figures come from secondary or vendor sources: Faros, Uvik, DX via ShiftMag, SignalFire, IEEE via blogs, and the Harvard 700-firm item. Pull the originals for anything you plan to feature.

A few numbers disagree between outlets. Stanford's 20% is "since late 2022" in some places and "from 2024" in others. Indeed's year-over-year posting rise shows up as 15%, 18% and 30% depending on dataset and date.

Many of the productivity results predate agentic tools. Only the Microsoft rollout study and METR's 2026 work cover agents directly.

There's no Canada-specific evidence here. If the project needs a Canadian angle, Statistics Canada and Canadian job-board data are the next place to look.

I left out code quality, security, cost and capability benchmarks on purpose. Those belong in other research files.

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
