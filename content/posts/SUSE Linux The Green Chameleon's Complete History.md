---
title: " SUSE Linux: The Green Chameleon's Complete History"
draft: true
tags:
  - مقال
  - لينكس
date: 2026-03-27
---


## From a Small German Office to the Global Stage — The Unsparing, Full Account

---

# Prologue: The Questions Nobody Asks

There is a version of the SUSE story that has been told many times. It is the version that appears on corporate timelines and conference keynotes — a clean arc of founding, growth, acquisition, and resilience. Four Germans start a company. They build a Linux distribution. They get bought. They survive. The end.

But the clean version leaves out the most interesting parts. It leaves out the geopolitics — the quiet ways in which American national security interests shaped the enterprise Linux market. It leaves out the human cost — what it actually felt like to be an engineer in Nuremberg watching your company get sold to strangers for the fourth time. It leaves out the power struggles — the invisible negotiations between a community that believed in openness and a corporation that needed revenue. It leaves out the founders themselves — four men who built something extraordinary and then, one by one, walked away from it, largely forgotten.

This is an attempt to tell the fuller story. Not the clean version, but the true one — or as close to true as the available evidence allows. Where the record is clear, it follows it. Where it is ambiguous, it says so. Where it is silent, it explains what the silence itself reveals.

---

# Part I: The World That Made SUSE Necessary

## The Operating System Wars and Their Wreckage

To understand SUSE, you must first understand the world into which it was born. And that world was a battlefield.

Unix had been born beautiful. Created at Bell Labs in 1969 by Ken Thompson and Dennis Ritchie, it was elegant, portable, and philosophically coherent. Its design principles — small tools that do one thing well, text as a universal interface, programs that compose — were so compelling that they still underpin modern computing half a century later. When AT&T was forbidden from commercializing Unix by a consent decree, the operating system spread through universities almost like samizdat literature, passed from department to department, shared freely. The University of California at Berkeley created its own branch, BSD, and for a decade Unix flourished in an atmosphere of academic collaboration that presaged the open-source movement by twenty years.

Then the consent decree was lifted, and everything went wrong.

AT&T began charging for Unix licenses. Companies forked the code, added proprietary extensions, and locked customers in. Sun had SunOS and later Solaris. IBM had AIX. HP had HP-UX. Digital had Ultrix, then Tru64. SGI had IRIX. Each was incompatible with the others. Each cost tens or hundreds of thousands of dollars. A Sun workstation might cost $10,000 or more. A site license for a commercial Unix could run into six figures. The Open Software Foundation was created to counter AT&T's Unix International, and what followed was years of political maneuvering, competing standards, and lawsuits that drained the industry's energy and customers' patience.

Meanwhile, AT&T sued the University of California over BSD, creating legal uncertainty that would hang over the free-software world for years. The BSD lawsuit, filed in 1992 and not fully resolved until 1994, had consequences that are still underappreciated. Had the lawsuit been resolved quickly in BSD's favor, the free Unix world might have rallied around FreeBSD or NetBSD rather than Linux. But the legal cloud over BSD created an opening — and Linux walked through it.

By 1991, if you wanted to run a Unix-like system on your personal computer, your options were bleak. You could buy a commercial Unix — SCO Xenix, Coherent, Minix — at significant cost. Or you could wait for the GNU Project, Richard Stallman's audacious plan to create a complete free Unix-like system. The GNU Project had produced excellent tools (GCC, Emacs, Bash, the GNU coreutils) but whose kernel, GNU Hurd, was perpetually in development and perpetually not ready.

Into this gap stepped Linus Torvalds, a 21-year-old Finnish student who wanted to run Unix on his 386 PC and couldn't afford to buy it. On August 25, 1991, Torvalds posted his now-famous message to the comp.os.minix newsgroup:

> "Hello everybody out there using minix — I'm doing a (free) operating system (just a hobby, won't be big and professional like gnu) for 386(AT) clones..."

His kernel was not technically superior to BSD or Hurd. But it was available, it was free, it was unencumbered by lawsuits, and — crucially — Torvalds was willing to accept contributions from anyone. Within months, a global community of developers had begun building on his kernel, combining it with the GNU tools to create a complete, free operating system. Linux was not the most elegant kernel ever written. Tanenbaum himself publicly criticized its monolithic architecture in a famous Usenet flame war. But it worked, it was free, and it was improving at a ferocious pace.

But this operating system, in 1992, was not usable by ordinary people. It had no installer. It had no package manager. Configuration required editing cryptic text files by hand. Installing it on a PC was a multi-day adventure involving dozens of floppy disks, arcane boot parameters, and the constant risk of bricking your hardware. Someone needed to take this raw material and turn it into something that a professional could use in a production environment.

In the United States, Patrick Volkerding created Slackware and Ian Murdock started Debian. In Germany, four men decided they could do better.

---

# Part II: Four Men in Nuremberg

## Who They Were

The founding story of SUSE is typically reduced to a single sentence: four Germans started a company in 1992. But who these men were — their backgrounds, their motivations, their personalities — matters enormously, because the company they built was an expression of who they were.

**Roland Dyroff** was the businessman of the group. He had a background in mathematics and business, and he understood something that pure technologists often miss: that great technology, without a viable business model, is just a hobby. Dyroff would eventually become the managing director (Geschäftsführer) of S.u.S.E. GmbH, the one who handled the contracts, the finances, the partnerships. He was not the most visible of the founders, but he was the one who kept the lights on.

**Thomas Fehr** was the systems expert, deeply knowledgeable about Unix administration and networking. He brought practical expertise in the kind of corporate Unix environments that S.u.S.E. would need to understand if it wanted to sell Linux to businesses.

**Burchard Steinbild** brought additional technical depth. Like the others, he was a product of the German technical education system — rigorous, practical, detail-oriented.

**Hubert Mantel** was, by many accounts, the deepest technical mind of the group. He would eventually become SUSE's chief technology officer and was instrumental in shaping the distribution's kernel and low-level architecture. Mantel was the kind of engineer who understood operating systems at the level of interrupts and page tables, and his fingerprints were on SUSE's kernel customizations for years.

What united them was not a grand vision but a practical observation. Unix was powerful but expensive. Linux was free but unusable. The gap between the two was an opportunity.

They founded **S.u.S.E.** — **Software und Systementwicklung** (Software and Systems Development) — on **September 2, 1992**, in Nuremberg, Bavaria. The company was registered as a GmbH, the standard German form for a limited-liability company, with minimal capital. There was no venture capital, no angel investment, no Silicon Valley pitch meeting. Just four men, a small office, and a conviction that Linux could be made to work for professionals.

The name itself carried a resonance they may or may not have intended. **Konrad Zuse** — pronounced roughly "Tsoo-zeh," phonetically close to "S.u.S.E." — was the German engineer who built the Z3 in 1941, the world's first programmable, fully automatic digital computer. The founders have given varying accounts about whether the name was a deliberate tribute. Fehr once acknowledged the connection in a magazine interview; others have been more ambiguous. But the phonetic echo was unmistakable to German ears, and it lent the young company an air of historical weight — a link to a tradition of German engineering innovation.

Their early business centered on Unix consulting, software services, and eventually Linux distribution and support. SUSE did not spring from ideological purity or from a single technical invention. It sprang from market recognition: Linux was arriving, and there would be demand for people who could make it usable. The founders were not celebrity founders in the modern style. Their legitimacy came less from charisma than from competence.

## The Early Days: From Consulting to Translating Slackware

S.u.S.E.'s first product was not, strictly speaking, its own. In 1993, the company began selling a localized version of **Slackware**, the American Linux distribution created by Patrick Volkerding. S.u.S.E. took Slackware, translated it into German, added documentation, fixed bugs, and packaged it in a boxed set that could be sold through bookstores and mail order.

This was not plagiarism. It was how the open-source ecosystem worked. Slackware was freely available under open-source licenses, and adding value through translation, documentation, and packaging was entirely legitimate. What S.u.S.E. brought was accessibility. In 1993, a German system administrator who wanted to run Linux faced a double barrier: the technical complexity of the system and the linguistic barrier of English-only documentation. S.u.S.E. removed the second barrier and significantly lowered the first.

That is how SUSE first earned loyalty — not with ideology, but by making Linux livable.

In those years, distributions were less about inventing from zero than about integrating, packaging, documenting, localizing, and supporting a fast-moving software ecosystem. The kernel, GNU tools, X11, compilers, boot systems, networking, libraries, desktop components — these existed in pieces. A distribution made them a coherent operating system. SUSE excelled at that curation and integration work from the very beginning.

Over the next two years, the founders gradually replaced Slackware's components with their own, and by 1996, they had created something that was unmistakably theirs: **S.u.S.E. Linux**, later simplified to **SuSE Linux** and eventually **SUSE Linux**. It was, from the beginning, distinctly European in character — methodical, well-documented, engineering-driven, and focused on reliability over flash.

## The Boxed Set: A Civilizing Force

To understand how SUSE built loyalty, picture a computer shop or mail-order catalog in the mid-to-late 1990s. There are software boxes on shelves. Windows products dominate, of course. But for a technically inclined user, there is a Linux distribution in an actual box — CDs, thick printed manuals, supplementary documentation on networking, security, and system administration. SUSE's packaging projected seriousness.

The boxed set was critical in ways that go beyond mere distribution mechanics. In Germany, internet connections in the mid-1990s were typically ISDN lines (128 Kbps at best) or dialup connections charged by the minute. Downloading a 600 MB CD image was impractical for most users. Physical distribution was the only practical way to obtain software. SUSE's boxed sets appeared in German bookstores — Thalia, Hugendubel, the local Buchhandlung — alongside programming textbooks and computer magazines.

The bookstore channel was also culturally significant. In Germany, bookstores are trusted institutions. The _Buchpreisbindung_ — fixed book pricing, mandated by law — has helped sustain a dense network of bookstores throughout the country. When SUSE appeared there, it gained a legitimacy that a download from an American website could not provide. It was a real product, in a real store, with a real manual. Your boss would take it seriously.

The manuals were, for many users, the real product. They were written in clear, precise German, sometimes running to a thousand pages or more, and reflected the _Gründlichkeit_ — the thoroughness, the meticulousness — that is central to German technical culture. An American Linux distribution might ship with a README file and a FAQ. SUSE shipped with a manual that could serve as a university textbook. Buying a SUSE boxed set was an act of intention — you were choosing to invest time and money in learning a new operating system. Many SUSE users of the 1990s and 2000s describe those manuals as transformative, the resource that took them from curiosity to competence.

SUSE sold hundreds of thousands of these boxed sets throughout the 1990s and early 2000s. They were the company's primary revenue source and built a loyal customer base that would sustain SUSE through multiple corporate upheavals.

---

# Part III: YaST — The Crown Jewel

Between 1993 and 1996, S.u.S.E. gradually replaced Slackware's components with their own. The centerpiece of this transformation was **YaST — Yet another Setup Tool** — first introduced in 1994.

YaST was not just an installer. It was a complete system administration framework — a unified interface for managing every aspect of a Linux system, from initial installation through ongoing configuration and maintenance. To appreciate why this mattered, you need to understand what configuring Linux was like without it.

In the mid-1990s, configuring a Linux system meant editing dozens of text files scattered across the filesystem, each with its own syntax and its own potential for catastrophic misconfiguration:

- `/etc/fstab` for disk mounts — one wrong entry and the system won't boot
- `/etc/XF86Config` for display settings — wrong refresh rate could physically damage a CRT monitor
- `/etc/lilo.conf` or `/etc/grub.conf` for the boot loader
- `/etc/sysconfig/network` for networking
- `/etc/passwd` and `/etc/shadow` for user management
- `/etc/printcap` for printers
- Dozens more for mail servers, DNS, NFS, SAMBA, firewalls...

Each file had its own format, its own conventions, its own error modes. There was no validation, no error checking, no undo. A misplaced comma could render a service inoperable. System administration was an exercise in meticulous attention to detail, and mistakes were punished harshly.

YaST changed all of this. It provided a menu-driven interface — text-based initially, later graphical — that abstracted away this complexity. Instead of editing `/etc/fstab` by hand, you used YaST's partitioning module. Instead of manually editing X configuration files, you used **SaX** (SUSE Advanced X Configuration), which probed your hardware, detected your monitor's capabilities, and generated a correct configuration. YaST's architecture was modular — each administrative function was handled by a separate module. New modules could be added without modifying the core. The modules were initially written in YCP (YaST Control Panel language), a domain-specific language developed specifically for system configuration. In later years, YaST modules were migrated to Ruby, which lowered the barrier to contribution.

What made YaST philosophically remarkable was its underlying idea: **an operating system is not finished when it boots. It is finished when it can be administered sanely.** This is one of SUSE's deepest contributions to Linux history. There are companies that innovate by creating entirely new categories. And there are companies that elevate a category by making it practical. SUSE belongs strongly to the second kind. It made Linux manageable for institutions.

There is a story, possibly apocryphal but widely told in SUSE circles, about an early demonstration of YaST at a Linux trade show in Germany. A skeptical system administrator challenged the S.u.S.E. team to install Linux on his laptop — a notoriously difficult task in the mid-1990s, when laptop hardware was exotic and poorly supported. YaST probed the hardware, configured the display, set up networking over a PCMCIA modem card, and had the system running in under an hour. The administrator became a SUSE customer on the spot. Whether or not this specific incident occurred exactly as described, it captures something true about YaST's impact: it turned Linux from a hobby for hackers into a viable operating system for professionals.

### The YaST Licensing Controversy

S.u.S.E. initially released YaST under a proprietary license — the **YaST License**, which allowed use only with S.u.S.E. Linux. This was a deliberate business decision: YaST was SUSE's primary competitive differentiator, and the founders were concerned that if they released it under an open-source license, competitors could simply take it and strip away SUSE's advantage.

The free-software community was not pleased. Richard Stallman's Free Software Foundation argued that YaST was a critical system component and that making it proprietary violated the spirit of free software. Debian refused to include YaST on philosophical grounds. The proprietary license created a philosophical tension that would persist for years: SUSE was built on free software, profited from free software, and contributed extensively to free software — but it kept its crown jewel locked up.

The tension was resolved in **2004**, after Novell's acquisition, when YaST was relicensed under the **GNU General Public License (GPL)**. The relicensing was welcomed by the community, but by that point, other distributions had developed their own administration tools, and YaST's proprietary period had prevented it from becoming a cross-distribution standard. This was a missed opportunity: had YaST been open source from the beginning, it might have become the universal Linux administration framework, much as RPM became the near-universal package format.

---

# Part IV: The European Crucible

## Why Germany Was Different

SUSE's emergence in Germany was not a coincidence. Europe in general — and Germany in particular — provided uniquely fertile ground for Linux and open-source software, for reasons that were cultural, economic, political, philosophical, and historical.

### The Economic Pressure

Germany's economy in the early 1990s was under extraordinary strain. Reunification, formally completed in October 1990, required massive investment. The _Solidaritätszuschlag_ (solidarity surcharge), levied to fund reunification, was introduced in 1991 and remained in place for three decades. In this environment, every mark mattered. German businesses, particularly the small and medium enterprises that form the backbone of the German economy — the _Mittelstand_ — were intensely cost-conscious. Microsoft's per-seat licensing fees, while manageable for large American corporations, were a significant burden for a German manufacturer with 200 employees.

Linux offered an alternative: no per-seat licensing fees, modest hardware requirements, and a genuine substitute for expensive proprietary Unix. This economic argument was particularly compelling in post-reunification Germany, where cost discipline was a survival strategy.

### The Privacy Imperative

Germany's relationship with surveillance is shaped by a historical experience that has no parallel in the Anglophone world. Germans lived under two of the most pervasive surveillance states in history: the Gestapo during the Nazi era and the Stasi during the East German era. The Stasi alone employed an estimated 91,000 full-time agents and maintained files on approximately 5.6 million people — roughly one-third of the East German population. When the files were opened after reunification, they revealed a society in which neighbors had spied on neighbors, spouses on spouses, children on parents. The trauma of this experience is woven into the fabric of German culture and German law.

Germany's federal data protection laws — the _Bundesdatenschutzgesetz_, first enacted in 1977 and repeatedly strengthened — are among the most stringent in the world. The country was a driving force behind the EU's General Data Protection Regulation (GDPR). Open-source software aligned naturally with these values. When you run open-source software, you can inspect the source code. You can verify what it does, what data it collects, and where it sends that data. When you run proprietary software, you are trusting the vendor. For German organizations — particularly government agencies, financial institutions, and companies handling sensitive data — this transparency was not a philosophical nicety but a practical requirement.

### The Academic Pipeline

German universities were early adopters of Linux, and the pipeline from academia to industry was a crucial factor in SUSE's success. Many computer science departments used Unix workstations for teaching and research, and when Linux became available as a free alternative, they adopted it enthusiastically. Students who learned Linux in university — often on SUSE, since it was the most accessible German-language distribution — carried that expertise into the workforce. When they became system administrators, they recommended SUSE. When they became IT managers, they purchased SUSE. This created a self-reinforcing cycle that was particularly strong in Germany and the German-speaking world. Several of Germany's Fraunhofer Institutes — the applied research organizations that bridge academia and industry — used SUSE Linux extensively, serving as both customer and reference.

### The Political and Cultural Factors

European governments were increasingly concerned about dependence on American technology companies. This concern was partly economic — billions of euros flowing to Redmond, Washington — but also strategic. The idea that critical national infrastructure might depend on software controlled by a foreign corporation, whose source code could not be inspected, was troubling to European policymakers. Germany's Federal Office for Information Security (BSI) began recommending open-source software for government use as early as the late 1990s.

Germany's computing culture also had a broader sensibility: _Gründlichkeit_ — thoroughness, meticulousness, attention to detail. SUSE Linux reflected this sensibility. Where American distributions were often rough around the edges, optimized for speed of development, SUSE was polished, well-documented, and carefully tested. This resonated deeply with German engineers and system administrators who valued reliability and comprehensibility over novelty.

In summary, Europe shaped SUSE in five major ways: language and localization that built trust in German-speaking markets; public-sector and institutional orientation that suited Europe's stable, standards-conscious organizations; an engineering-first culture that valued depth over marketing theater; less venture-capital-driven growth that preserved technical seriousness but limited aggressive expansion; and openness to heterogeneity in IT environments that taught SUSE to live in a plural world rather than assuming one universal commercial script.

---

# Part V: The Rivals — A Deeper Look

## Red Hat: Strategy, Capital, and the American Advantage

Red Hat was founded in March 1993 by **Bob Young** and **Marc Ewing** in Durham, North Carolina — barely months after S.u.S.E. The two companies were almost exact contemporaries, but they diverged rapidly in strategy, culture, and scale.

Bob Young was a salesman at heart. He had previously run a computer supply business, and he understood something that the S.u.S.E. founders, who were engineers, did not: that the value of a Linux distribution was not in the software — which was freely available — but in the brand, the support, and the trust. He set out to build Red Hat into the brand that enterprises trusted for Linux, and he succeeded.

### The IPO and Its Consequences

Red Hat went public on **August 11, 1999**, at the peak of the dot-com bubble. The stock opened at $14 and closed the day at $52, giving the company a market capitalization of approximately $3.6 billion. By comparison, SUSE Linux AG — still a privately held GmbH — had annual revenues estimated at perhaps $30-40 million.

The IPO was transformative. It gave Red Hat hundreds of millions of dollars in cash, made employees wealthy through stock options, attracted top talent, gave Red Hat enormous visibility with CIOs and executives who had never heard of Linux, and created a currency — Red Hat stock — for acquisitions.

Why didn't SUSE pursue an IPO of its own? The question has several answers:

**The German capital market.** The Frankfurt Stock Exchange did not have the same appetite for technology IPOs that NASDAQ did in 1999. Germany had its own technology stock market, the _Neuer Markt_, created in 1997 to emulate NASDAQ — but it was smaller, less liquid, and collapsed spectacularly when the dot-com bubble burst. It was closed entirely in 2003.

**The venture capital gap.** The United States had a mature, aggressive venture capital industry eager to fund technology companies and push them toward IPOs. Europe's venture capital industry was smaller, more conservative. S.u.S.E. was self-funded, bootstrapped, grown organically. This was a source of pride — the founders had built something real without diluting their ownership — but it also meant they lacked powerful backers who could navigate the IPO process.

**Cultural factors.** German business culture, particularly in the 1990s, valued stability, profitability, and prudent growth over the aggressive, loss-funded expansion that characterized American technology companies. The idea of going public before your company was solidly profitable — standard practice in Silicon Valley — was alien to the German business mentality.

**Ownership structure.** For long stretches, SUSE was owned by larger parent companies. A subsidiary does not simply decide to IPO itself.

**Narrative complexity.** Public markets like stories they can understand. Red Hat's story was clean: enterprise open source leader, subscription model, growing strategic importance. SUSE's story was often messier: a Linux jewel inside a larger, strategically searching parent.

By the time SUSE finally went public — in **May 2021**, on the Frankfurt Stock Exchange, at a valuation of approximately €5 billion — Red Hat had been generating billions in annual revenue for years and had already been acquired by IBM for $34 billion. The window that opened in 1999 never opened quite the same way again.

### Other Red Hat Strategic Advantages

Beyond the IPO, several specific decisions gave Red Hat compounding advantages:

**RPM.** Red Hat developed RPM (Red Hat Package Manager), which became a de facto standard. SUSE eventually adopted RPM as well (while adding their own layer of tools), but Red Hat's early-mover advantage in defining the package format gave it significant ecosystem influence.

**Red Hat Enterprise Linux (RHEL).** Introduced in 2002, RHEL created a clear separation between its free community distribution (which became Fedora) and its commercial, supported product with long-term support commitments. This was exactly what enterprise customers wanted: not just software, but a guarantee that someone would fix problems, release patches, and ensure compatibility for up to a decade.

**The certification ecosystem.** Red Hat invested heavily in building certifications. **Red Hat Certified Engineer (RHCE)** became the most recognized Linux certification in the industry. Employers hired for RHCE. Job postings specified RHEL experience. This created a self-reinforcing cycle: more certified engineers meant more companies comfortable with RHEL, attracting more software vendors, attracting more customers. SUSE had its own certification program — **SUSE Certified Administrator (SCA)** and **SUSE Certified Engineer (SCE)** — but it never achieved the same market penetration.

**The enterprise sales machine.** Red Hat invested early in an enterprise sales organization — account managers, solution architects, pre-sales engineers, partner managers — capable of selling to Fortune 500 companies. It made itself the safe choice. Its hardware partnerships with Dell, HP, IBM ensured RHEL was pre-installed and certified on the most popular enterprise servers. SUSE had all of these elements but at smaller scale, particularly thin in North America and Asia.

**The CentOS effect.** In 2004, the **CentOS** community began producing a free distribution binary-compatible with RHEL. CentOS paradoxically expanded the installed base of RHEL-compatible systems, which expanded the ecosystem of software certified for RHEL, making RHEL the default choice when organizations wanted supported Linux. Red Hat eventually acquired CentOS in 2014. SUSE had no equivalent: openSUSE served a similar role in some respects, but was not binary-compatible with SUSE Linux Enterprise in the way CentOS was with RHEL.

**The IBM partnership.** IBM announced a $1 billion investment in Linux development in 2000, much directed at Red Hat. When IBM eventually acquired Red Hat in 2019 for $34 billion — the largest software acquisition in history at the time — it was the culmination of a relationship built over nearly two decades.

**Consistency of purpose.** Perhaps most fundamentally, Red Hat was an independent company with single-minded focus for most of its history. It had one CEO (Matthew Szulik) for a critical decade (1999-2008), followed by another (Jim Whitehurst) for another decade (2008-2019). SUSE, by contrast, was bounced from owner to owner, each transition bringing new leadership, new strategies, new priorities. Every time a new owner arrived, there was disruption: employees left, customers worried, competitors pounced.

## Debian: The Ideological Counterpoint

Debian was founded in 1993 by Ian Murdock (the name combining his name with that of his then-girlfriend, Debra). Unlike SUSE and Red Hat, Debian was not a company. It was a community project, run by volunteers, governed by a constitution and elected leadership, and committed to free software with an almost religious fervor. The **Debian Free Software Guidelines** — later generalized as the **Open Source Definition** — were the philosophical backbone of the free software movement.

Debian was technically excellent but notoriously slow to release. It had no corporate backing, no marketing budget, and no sales team. It was the purest expression of the open-source ideal: software made by the community, for the community.

SUSE occupied a middle ground between Red Hat's corporate ambition and Debian's ideological purity. It was a commercial company, but one that valued engineering over marketing. This middle position was both a strength and a weakness — it gave SUSE credibility with both businesses and communities, but it also meant that SUSE was never quite aggressive enough to dominate commercially or quite pure enough to command the loyalty of the most committed free-software advocates.

---

# Part VI: The U.S. Government's Role — Structural, Indirect, and Underestimated

This is where most corporate histories become too polite.

Enterprise dominance in the U.S. is not shaped by private-sector buying alone. Government standards, certifications, contracts, and the gravitational effect of federal procurement all matter enormously. The United States federal government is the largest buyer of information technology in the world. The Department of Defense alone spends tens of billions of dollars annually on IT. And there are structural factors that give American companies significant advantages in this market.

**Federal procurement preferences.** The Buy American Act of 1933 and the Trade Agreements Act require federal agencies to give preference to domestic products and services. While open-source software complicates the "country of origin" analysis, the practical effect is that American companies with American sales teams, American addresses, and American security clearances have significant advantages in selling to the federal government. A German company based in Nuremberg could not easily obtain the clearances needed to participate in classified programs.

**Certification programs.** The federal government maintains a complex web of certification and accreditation programs — Common Criteria evaluations, FIPS (Federal Information Processing Standards) validations, DISA STIGs (Defense Information Systems Agency Security Technical Implementation Guides), FedRAMP — that software must pass before it can be used in government environments. These certifications are time-consuming and expensive to obtain, and the testing bodies and processes are predominantly American. Red Hat invested early and heavily in obtaining these; SUSE did as well, but with fewer resources and less familiarity with American government requirements.

**DISA STIGs.** The Defense Information Systems Agency publishes Security Technical Implementation Guides — detailed security configuration standards — for approved software. Red Hat Enterprise Linux received a DISA STIG early in its history, giving it a head start in the DoD market that created long-term entrenchment.

**Ecosystem gravity.** Government purchasing is not just direct revenue — it is validation. Once a technology is trusted by federal agencies, major enterprises notice. They infer seriousness. If a Linux vendor becomes common in federal and defense-adjacent deployments, integrators certify around it, security teams become familiar with it, procurement templates mention it, and skills accumulate around it. Red Hat benefited from being inside that ecosystem in ways SUSE simply could not replicate from Nuremberg.

To be precise: this is not a claim that the U.S. government deliberately chose Red Hat over SUSE to promote American interests, or that there was a conspiracy to exclude European Linux vendors. The structural features of American federal procurement were designed for entirely legitimate purposes — security, domestic economic support, reliability. But those features had the effect of advantaging American vendors over European ones. Red Hat benefited from these structures. SUSE was disadvantaged by them.

---

# Part VII: SELinux, AppArmor, and the Geopolitics of Security

This is perhaps the most sensitive and underexplored aspect of the SUSE-Red Hat competition.

**SELinux** (Security-Enhanced Linux) was developed by the **National Security Agency** — the NSA — and released as open-source software in 2000. SELinux implements **mandatory access control (MAC)**, constraining what individual programs and users can do even if they have root privileges. It is technically sophisticated and powerful.

Red Hat adopted SELinux and integrated it deeply into Red Hat Enterprise Linux, making it enabled by default. This was a technically defensible decision, but it also aligned Red Hat closely with the U.S. government's preferred security technology.

SUSE took a different path. SUSE adopted **AppArmor**, developed by **Immunix** (later acquired by Novell). AppArmor and SELinux address the same problem — constraining program behavior — but through fundamentally different approaches:

**SELinux** uses labels. Every file, process, socket, and device on the system is assigned a security context, and policies define which contexts can interact with which others. This is extremely powerful but also notoriously complex. Writing and maintaining SELinux policies is difficult, and misconfigured policies can break applications in subtle ways. Many system administrators, confronted with a SELinux denial, resort to running `setenforce 0` — disabling SELinux entirely — rather than debugging the policy.

**AppArmor** uses paths. It defines profiles for individual programs, specifying which files and capabilities each can access. This is simpler to understand and configure — an AppArmor profile reads like a list of permissions — but less comprehensive than SELinux's label-based approach.

The technical merits of each have been debated exhaustively, and reasonable people disagree. But the choice between them was never purely technical. There were at least three additional dimensions:

**The NSA factor.** SELinux was developed by the NSA, whose mission is signals intelligence. The idea that the NSA developed security software and gave it away for free raised questions. Was SELinux genuinely intended to improve security? Were there intentional vulnerabilities hidden in the code? The open-source community's official position was that these concerns were unfounded — the code was public, anyone could inspect it, and no evidence of backdoors had been found. But the concerns were not irrational, particularly in Germany, where historical experience with surveillance made people more skeptical of government-developed security tools.

After the **Snowden revelations in June 2013** — which exposed that the NSA had deliberately weakened encryption standards, subverted security software, and specifically targeted German government communications including Chancellor Merkel's personal mobile phone — these concerns seemed less paranoid and more prescient. In Germany, this was not merely a scandal; it was a betrayal by a supposed ally. It strengthened the case for European technological sovereignty and, implicitly, for European alternatives to American-controlled security frameworks.

**The certification alignment.** By adopting SELinux, Red Hat aligned itself with the security framework preferred by the U.S. government. Government security policies were written around SELinux. Government training programs taught SELinux. Government certifications required SELinux. If you were deploying Linux in a U.S. government environment, SELinux was not optional — it was mandatory. This created a self-reinforcing dynamic: Red Hat had the most mature SELinux implementation, so Red Hat became the default government Linux.

**The European dimension.** SUSE's choice of AppArmor can plausibly be read as an expression of European technological independence. Using a security framework developed by the NSA, deeply integrated by an American company, and mandated by the American government would have meant adopting a critical security component over which SUSE had minimal influence. AppArmor, after being acquired through Novell, became effectively a SUSE-controlled project. SUSE could develop it, modify it, and guarantee its integrity in a way it could not with SELinux.

In practical administration terms, many users considered AppArmor easier to deploy and maintain than SELinux, especially in environments without highly specialized security expertise. In parts of Europe, and especially in German-speaking environments shaped by long historical memories of surveillance, an NSA pedigree was a psychological liability as much as a technical asset.

This distinction represents two different civilizational answers to Linux security:

- **Red Hat/SELinux:** rigorous, policy-heavy, institutionally legible, state-adjacent.
- **SUSE/AppArmor:** practical, lighter-weight, admin-friendly, culturally easier to trust in certain environments.

Did SELinux help Red Hat win? Absolutely, in certain markets. Deep SELinux integration gave Red Hat stronger standing in security-conscious enterprise and U.S. government contexts. It also came with tradeoffs — AppArmor often had a better human-factors story. But in high-assurance markets, difficult but powerful often beats easier but less symbolically authoritative.

To emphasize: this analysis is interpretive, not documentary. Internal SUSE documents explicitly stating they chose AppArmor because they distrusted the NSA have not been publicly disclosed. But the circumstantial evidence is suggestive, and the geopolitical context makes the interpretation plausible.

---

# Part VIII: Technical Innovations

## Package Management and Zypper

While SUSE adopted the RPM package format, it built its own package management tools on top. The most significant was **Zypper**, a command-line package manager that used a dependency resolver called **libzypp** based on a SAT solver algorithm — arguably more sophisticated than the equivalent tools in other distributions. Where Red Hat's yum sometimes struggled with complex dependency chains, Zypper's SAT-based solver could handle them elegantly. This was a technical advantage largely invisible to end users but deeply appreciated by system administrators managing hundreds of systems.

## Btrfs and Filesystem Innovation

SUSE was an early adopter and champion of the **Btrfs** filesystem, a next-generation Linux filesystem offering snapshots, checksumming, and dynamic volume management. SUSE began shipping Btrfs as the default root filesystem in **SUSE Linux Enterprise Server 12** (2014), making it the first major enterprise Linux distribution to do so. Red Hat took a more cautious approach — it included Btrfs as a technology preview in RHEL 7 but never promoted it to full support, eventually removing it entirely in RHEL 8.

SUSE's Btrfs implementation was paired with **Snapper**, a tool for managing Btrfs snapshots integrated with YaST and the package management system. Before every system update, Snapper automatically created a snapshot. If the update caused problems, the administrator could roll back to the pre-update state with a single command. This turned system updates from anxiety-inducing operations into routine, reversible actions.

The Btrfs/Snapper combination also enabled **transactional updates** — system changes applied atomically. Either the entire update succeeded, or the system rolled back. This concept, pioneered by SUSE, would later become central to the design of immutable operating systems and container-optimized platforms.

SUSE invested significantly in Btrfs development, employing several of the filesystem's core developers. This mitigated the risk of being an early adopter, but required sustained commitment that Red Hat was not willing to make.

## The Open Build Service

One of SUSE's most important and least appreciated contributions to the broader open-source ecosystem is the **Open Build Service (OBS)**, originally developed as the openSUSE Build Service. OBS automates the compilation and packaging of software: a developer submits source code, and OBS compiles it for multiple distributions, architectures, and versions, producing ready-to-install packages.

The decision to make OBS a cross-distribution tool — rather than limiting it to openSUSE — was deliberate and reflected SUSE's upstream philosophy. By making OBS useful to the entire ecosystem, SUSE created goodwill, attracted contributors, and established itself as a good citizen of the open-source community. Thousands of projects across the entire Linux ecosystem now use it.

## KIWI, AppArmor, and Other Contributions

**KIWI** was a system for creating operating system images — complete, bootable system images for virtual machines, cloud platforms, USB drives, and more. It was ahead of its time, anticipating the shift toward image-based deployment that would later dominate with containers and cloud computing.

SUSE was also one of the most prolific contributors to the **Linux kernel** itself. SUSE engineers made fundamental contributions to memory management, filesystem development (particularly Btrfs and XFS), kernel testing, and hardware support. **Greg Kroah-Hartman**, who worked for SUSE before moving to the Linux Foundation, is one of the most prolific kernel contributors in history. **Jeff Mahoney**, **Takashi Iwai** (the primary maintainer of the ALSA sound subsystem), and many other SUSE engineers made lasting contributions to the kernel. SUSE has also been a major contributor to systemd, GCC, glibc, and QEMU/KVM.

## The KDE Connection

SUSE's relationship with the **KDE** desktop environment deserves special mention. While Red Hat aligned itself with GNOME, SUSE became the spiritual home of KDE. KDE was itself a European project, started in 1996 by Matthias Ettrich, a German computer science student at the University of Tübingen. KDE's design sensibility — feature-rich, configurable, thorough — aligned closely with SUSE's engineering culture.

SUSE hired numerous KDE developers, contributed extensively to KDE development, and made KDE the default desktop. The KDE/GNOME split was, in many ways, a proxy for a deeper cultural divide. GNOME embodied a philosophy of simplification — removing features, reducing options. KDE embodied a philosophy of empowerment — providing as many options as possible, trusting users to configure things to their liking. That SUSE aligned with KDE and Red Hat with GNOME reflected fundamentally different ideas about the relationship between software and its users.

---

# Part IX: The Corporate Odyssey — What It Actually Felt Like

## Act I: Novell (2003-2010)

On **November 4, 2003**, Novell announced the acquisition of SUSE Linux AG for approximately $210 million. For SUSE's employees, this was a moment of mingled hope and anxiety.

The hope was real. Novell, despite its declining NetWare business, was a large company with significant resources, a global sales organization, and deep relationships with enterprise customers. Novell's CEO, **Jack Messman**, spoke enthusiastically about transforming Novell into a Linux company.

But the anxiety was real too. SUSE employees in Nuremberg had built something they were proud of. Now they were being absorbed into an American corporation headquartered in Provo, Utah — a city with a strong Mormon cultural influence (home of Brigham Young University) and a hierarchical management structure profoundly different from their own. Novell also had a history of acquiring companies and failing to integrate them successfully.

There is an anecdote, told by multiple SUSE veterans, about the first all-hands meeting after the acquisition. Novell executives flew to Nuremberg, spoke in English, and talked about "synergies" and "market opportunities" and "strategic alignment." The SUSE engineers listened politely, then went back to their desks. The unspoken sentiment was: "The Americans can talk about strategy all they want. We'll keep doing what we've always done — building good software."

This pattern — corporate owners arriving with grand strategies, SUSE engineers keeping their heads down and building software — would repeat with each subsequent acquisition. It was both a survival mechanism and a source of frustration.

### The openSUSE Project (2005)

One of the most significant decisions of the Novell era was the creation of the **openSUSE** community project in **August 2005**, modeled loosely on Red Hat's Fedora project. openSUSE formalized the separation between a free community distribution (governed by a community board) and SUSE Linux Enterprise (the commercial product with additional testing, certification, and long-term support).

openSUSE was more than a marketing exercise. SUSE genuinely opened its development processes, moved code to public repositories, and invited community participation. The **Open Build Service** was a particularly generous contribution, designed from the beginning to be useful to the entire Linux ecosystem.

openSUSE also pioneered **Tumbleweed**, a rolling-release distribution that continuously updated to the latest software versions without requiring periodic reinstallation — originally the brainchild of **Greg Kroah-Hartman**. The combination of openSUSE **Leap** (a regular-release distribution aligned with SUSE Linux Enterprise) and openSUSE **Tumbleweed** (a rolling-release distribution) gave users a unique choice between stability and currency.

Tumbleweed is especially revealing of SUSE's philosophy. It is not chaotic bleeding-edge for its own sake. It is rolling release with engineering controls — progress, but managed progress.

### The Microsoft Deal: The Day the Community Turned

On **November 2, 2006**, Novell and Microsoft jointly announced a partnership that sent shockwaves through the Linux community. The deal had three components: technical collaboration on interoperability, mutual patent covenants, and sales collaboration where Microsoft sales representatives would recommend SUSE Linux Enterprise to customers.

The technical and sales collaboration was relatively uncontroversial. The patent agreement was explosive.

The covenant protected only Novell's customers — not users of other Linux distributions. This created what critics called a "protection racket": use SUSE, and you're safe from Microsoft patent claims; use anything else, and you're on your own. It appeared to validate Microsoft CEO Steve Ballmer's earlier claims that Linux infringed more than 200 Microsoft patents.

The reaction from the open-source community was volcanic. **Richard Stallman** began working on revisions to the GNU General Public License (GPLv3) that would prevent similar arrangements in the future. Section 11 of GPLv3 — explicitly designed to close the loophole the Novell-Microsoft deal had exploited — ensures that anyone distributing GPL-licensed software who enters a patent licensing arrangement must extend the patent protection to all recipients of the software, not just their own customers.

**The internal SUSE reaction** was, by most accounts, somewhere between dismay and fury. The deal was negotiated at the highest levels of Novell — with minimal input from SUSE's engineering organization. Most SUSE engineers learned about the deal from the press, or at most hours before the public announcement. This created an immediate sense of betrayal: the people who had built SUSE's technology and maintained its community relationships had been excluded from a decision that would fundamentally affect both.

SUSE engineers found themselves confronted by angry community members — on mailing lists, in IRC channels, at conferences — who demanded to know whether SUSE believed that Linux infringed Microsoft patents. The engineers were in an impossible position: they could not speak against their employer's decision, but many personally disagreed with it. Some remained silent. Some offered carefully worded defenses. A few quietly began updating their résumés.

Did engineers resign over the deal? Some did, though the exact number is difficult to determine. Particularly those most active in the community and most committed to free-software principles left in the months following the announcement — some to Red Hat, some to other open-source companies. German labor law, which provides strong protections for employees through _Betriebsräte_ (works councils), would have provided mechanisms for collective action, but using them would have been a dramatic escalation most employees were unwilling to undertake. What happened instead was more diffuse: private conversations, quiet criticism, a palpable shift in morale.

Several former employees have described the post-Microsoft-deal period as the most difficult of their careers — not because of the work itself, but because of the constant tension between loyalty to their employer and loyalty to their community. Linus Torvalds, characteristically, took a more pragmatic view, describing the deal as distasteful but not technically important. But Torvalds' equanimity was not shared by much of the community, and SUSE spent years rebuilding trust.

A telling anecdote from the 2006 Linux Kernel Summit: several kernel developers confronted Novell employees, demanding to know whether Novell believed that Linux infringed Microsoft patents. One reportedly said: "We're engineers. We write code. We didn't make this deal, and if you ask us privately, we'll tell you what we think of it."

From a purely business perspective, the deal did bring some benefits — interoperability improvements, some sales from Microsoft recommendations, financial payments to Novell. But the strategic cost — damage to community trust — was high, and it took years to repair.

## Act II: Attachmate (2010-2014)

On **November 22, 2010**, the Attachmate Group, a private equity-backed technology company, announced the acquisition of Novell for approximately $2.2 billion. The acquisition was completed in April 2011.

Attachmate immediately reorganized Novell into four business units, one of which was **SUSE**. This gave SUSE more autonomy than it had under Novell, with its own leadership, budget, and strategic direction. **Nils Brauckmann**, a German executive, was appointed as SUSE's president and led the company through the next several years of transformation.

But the transition was also painful. Attachmate laid off a significant number of Novell employees. The **Mono** project — an open-source implementation of Microsoft's .NET framework developed under Miguel de Icaza — was effectively abandoned when its entire team was laid off. (De Icaza and several colleagues went on to found **Xamarin**, later acquired by Microsoft.)

The layoffs were hard on the SUSE community because some of the people let go were well-known contributors to open-source projects. But Brauckmann's leadership steadied the ship. He focused SUSE on its core competencies — enterprise Linux and system management — and began rebuilding relationships strained during the Novell era.

## Act III: Micro Focus (2014-2018)

In **September 2014**, Attachmate merged with the **Micro Focus Group**, a British technology company specializing in legacy software and IT infrastructure management. SUSE became a division of Micro Focus.

The Micro Focus era was, by most accounts, a period of relative stability and quiet growth. Micro Focus was a financially disciplined company focused on profitability and cash flow, and SUSE benefited from this discipline. Revenue grew. The customer base expanded. SUSE Linux Enterprise Server gained ground particularly in SAP environments — SAP, the German enterprise software giant, certified SLES as a preferred platform for its applications.

But Micro Focus derived most of its revenue from maintaining legacy software, and it was not a natural home for an open-source Linux company. SUSE's engineering culture — innovative, community-oriented — was not always aligned with Micro Focus's conservative, efficiency-focused corporate culture.

## Act IV: EQT Partners (2018-Present)

In **March 2018**, Micro Focus announced the sale of SUSE to **EQT Partners**, a Swedish private equity firm, for $2.535 billion — at the time, the largest private equity acquisition of an open-source company in history.

The EQT acquisition was transformative. For the first time in years, SUSE was an independent company — not a division of a larger corporation, but a standalone entity with its own board, strategy, and identity. EQT's thesis was straightforward: SUSE was an undervalued asset with strong technology, loyal customers, and significant growth potential in cloud and container markets.

**Melissa Di Donato** was appointed as SUSE's CEO in 2019 — the first woman to lead a major open-source company. Under her leadership, SUSE accelerated product development in Kubernetes and container management, and prepared for its public listing.

On **May 19, 2021**, SUSE went public on the **Frankfurt Stock Exchange**, with an initial valuation of approximately €5 billion — the largest European technology IPO in years. However, the public listing was relatively short-lived. In **August 2023**, EQT took SUSE private again in a transaction valuing the company at approximately €2.7 billion, reflecting both the broader tech market downturn and SUSE's challenges in accelerating revenue growth.

Through all these ownership changes — Novell, Attachmate, Micro Focus, EQT, public listing, private again — the remarkable thing is that SUSE's engineering team and product quality remained largely intact. The Nuremberg office continued to produce excellent software. The core values endured.

### The Emotional Toll of Serial Acquisitions

Most corporate histories discuss acquisitions strategically. Employees experience them existentially.

Imagine you are a software engineer in Nuremberg. You love the technology, your colleagues, and the community. You have a spouse, children, an apartment. Your life is anchored here. Now imagine that every three to five years, your employer is sold to a new company. Each time: Will the new owners keep the Nuremberg office? Will there be layoffs? Will your job still exist in six months?

Multiple former employees describe a pattern that repeated with each acquisition: the announcement, weeks of uncertainty, the arrival of new management, restructuring and layoffs, a settling period — then rumors of the next sale, and the cycle repeating. Some engineers left, burned out by the uncertainty, attracted by the stability of Red Hat. Others stayed, anchored by personal ties to Nuremberg and a stubborn commitment to the product.

A recurring theme is that employees clung to product quality as a source of continuity. When ownership changed, the engineering mission became the emotional homeland. "We still know how to build a good Linux." That professional pride can hold a company together through years of strategic turbulence — but survival is not the same as serenity. Serial acquisitions produce fatigue, caution, and a learned distrust of grand corporate language.

One stabilizing factor was Germany's system of _Betriebsräte_ (works councils). Under German labor law, companies above a certain size must allow employees to elect a works council with significant rights: to be consulted on major business decisions, to negotiate on working conditions, and to be involved in decisions about layoffs. SUSE's works council played an important role during acquisitions, particularly in negotiating severance terms and ensuring fair treatment — a significant difference from the American corporate environment, where layoffs can be executed quickly and with minimal employee input.

---

# Part X: The openSUSE Question — Who Really Held Power?

The relationship between the **openSUSE community** and **SUSE the corporation** is one of the most complex and underexplored aspects of the SUSE story. When the interests of the community and the corporation conflicted, who won?

openSUSE was governed by a **Board** of both community-elected members and SUSE-appointed members. A Chairman was appointed by SUSE — a significant detail, because it meant SUSE retained ultimate authority over the project's governance structure. In practice, the relationship worked well during periods of stability: SUSE provided infrastructure (build servers, hosting, bandwidth), employed key contributors, and funded travel; the community contributed code, testing, and documentation.

But tensions emerged periodically:

**The Evergreen controversy.** When SUSE announced that certain openSUSE releases would reach end-of-life, community members organized **Project Evergreen** to extend support. SUSE did not actively oppose it but did not provide resources, and the project struggled because community volunteers alone could not maintain the volume of security patching required.

**The Leap/Enterprise alignment.** When openSUSE **Leap** was introduced in 2015, explicitly aligned with SUSE Linux Enterprise, community members who wanted faster release cadences were constrained by the need to stay synchronized with the enterprise product.

**The ALP transition.** SUSE's development of the **Adaptive Linux Platform (ALP)** raised significant questions about openSUSE's future. The development model was different, and some community members worried that ALP would reduce community influence and consolidate control within SUSE's engineering team.

The unspoken truth about corporate-sponsored open-source projects is that they are, in the end, corporate projects. The community has voice but not control. When corporate and community interests align — which they usually do — the arrangement works well. When they conflict, the corporation wins, because the corporation controls the resources. Most openSUSE community members understood this and accepted it pragmatically. But the acceptance was tinged with awareness that their project's future depended on decisions made in boardrooms where they had no seat.

This dynamic was not unique to openSUSE — Fedora operates under similar constraints with Red Hat. But openSUSE's situation was complicated by the serial ownership changes, each new corporate owner bringing new priorities and requiring the community to renegotiate its position.

---

# Part XI: Munich's LiMux and Why the German City Chose Debian

The **LiMux** project — Munich's famous migration of 14,000 desktop computers from Windows to Linux — is often mentioned in the SUSE story, but a crucial detail is usually glossed over: Munich chose **Debian**, not SUSE, as the base for its Linux migration. This was a German city, migrating to Linux, choosing a non-German distribution over the most prominent German Linux company. Why?

Steve Ballmer himself reportedly flew to Munich to try to dissuade the city council, offering deep discounts on Microsoft licenses. The council voted to proceed anyway. But the choice of Debian reveals important truths about public-sector procurement.

**Vendor independence.** The entire point of LiMux was to reduce Munich's dependence on a single vendor. It would have been counterproductive to replace dependence on Microsoft with dependence on SUSE (or Novell, which owned SUSE at the time). Debian, as a community project with no corporate owner, posed no such risk. If the Debian project changed direction, Munich could fork the code. If SUSE changed owners — which it did, repeatedly — Munich's platform could be destabilized by decisions in a Utah boardroom or London investment bank.

**Licensing purity.** Debian's commitment to free software was more absolute than SUSE's. Debian's main repository contained only software meeting the Debian Free Software Guidelines. SUSE, by contrast, included proprietary components — including YaST's proprietary license at the time — and shipped proprietary drivers and codecs.

**Cost.** Debian was entirely free. SUSE was primarily positioned as a commercial product with subscription fees.

**Political symbolism.** Choosing Debian let Munich frame the project as a move toward public autonomy — not a transfer of reliance from one company to another, even a national one. Public IT choices are political performances. This is one of those moments where SUSE's greatest strength — being a serious commercial Linux company — may also have weakened its appeal for a sovereignty-themed public project.

The LiMux project was implemented but had a painful epilogue. The migration took far longer than planned, cost more than budgeted, and encountered significant resistance. In 2017, under a new mayor, Munich announced it would reverse the migration and return to Windows. Open-source advocates accused the new administration of caving to Microsoft pressure — noting that Microsoft had relocated its German headquarters to Munich shortly before the vote. The full story is complex, involving not just technology but real estate, office politics, and the difficulty of maintaining a custom Linux distribution with limited municipal IT staff.

In a further twist, Munich in 2020 under yet another government coalition announced renewed interest in open-source solutions and began reassessing the return to Microsoft — showing that the story continues to oscillate, driven by political winds as much as technical merit.

The LiMux saga illustrates a truth SUSE knew well: technology decisions in the enterprise and public sector are never purely technical. They are political, cultural, and institutional. The best technology does not always win; the technology with the best institutional support does.

---

# Part XII: SUSE's Distinctive Strengths

## Where SUSE Led

Despite Red Hat's dominance in the overall enterprise market, there were areas where SUSE was the clear leader.

### SAP Environments

The most significant was **SAP**. SAP, the German enterprise software giant, and SUSE had a deep, long-standing partnership rooted in shared geography and culture, but sustained by technical excellence. SUSE's kernel engineers worked closely with SAP's developers to optimize Linux for SAP's specific workload patterns — large memory footprints, heavy I/O, complex multi-threaded applications — achieving SAP-specific optimization that no other Linux distribution could match.

The SAP partnership was also commercially critical. For fiscal year 2022, SUSE reported total revenue of approximately $580 million and Annual Recurring Revenue of approximately $590 million. Industry estimates suggested SAP environments accounted for 30-40% of SUSE's total revenue — by far the largest single use case. SAP customers tend to be large enterprises with high IT spending running SAP for decades, making SAP-anchored subscriptions SUSE's most profitable and most loyal customer segment.

### High-Performance Computing

SUSE carved out a strong position in **high-performance computing (HPC)**. Many of the world's fastest supercomputers — used for climate modeling, drug discovery, nuclear weapons simulation — ran SUSE Linux Enterprise. SUSE's HPC capabilities included optimized kernel configurations, support for specialized interconnects like InfiniBand, and tools for managing massive clusters.

In November 2017, the TOP500 list showed Linux running on 100% of the world's 500 fastest supercomputers — the first time any single operating system family had achieved total dominance. SUSE powered a significant fraction, including systems at the **Swiss National Supercomputing Centre (CSCS)** and the **Leibniz Supercomputing Centre** in Germany.

The HPC work drove innovation that benefited all SUSE users. Kernel improvements developed for supercomputers — better memory management under heavy load, more efficient process scheduling — found their way into the standard SUSE Linux Enterprise Server.

### Mainframes

SUSE was one of the first Linux distributions to support IBM's **System z** mainframe architecture (now IBM Z), and maintained this support continuously for over two decades. The z/Architecture has unique features (channel I/O, hardware cryptographic accelerators, dynamic partition management) that required extensive kernel and driver work. SUSE maintained a team of engineers specializing in mainframe Linux, and their work was critical in the financial services and government sectors where mainframes were prevalent. SUSE's depth in mainframes was widely regarded as superior to Red Hat's.

### European Government and Public Sector

In European government and public sector markets, SUSE's combination of European ownership, strong data sovereignty credentials, and technical capabilities made it the preferred choice for many European government agencies, military organizations, and critical infrastructure operators. The German government was a significant SUSE customer. Government and public sector customers — primarily in Europe — accounted for an estimated 15-20% of SUSE's revenue.

### Geographic Distribution

SUSE's geographic revenue profile reflected its history: EMEA (Europe, Middle East, and Africa) accounted for approximately 55-60% of revenue, with the Americas accounting for roughly 30% and Asia-Pacific for the remainder. The contrast with Red Hat is instructive — before its IBM acquisition, Red Hat's Americas revenue alone exceeded SUSE's total global revenue. The American market, which SUSE had never cracked at scale, accounted for the bulk of the difference.

---

# Part XIII: The Rancher Acquisition and the Kubernetes Era

In **December 2020**, SUSE acquired **Rancher Labs** for $600 million — its largest acquisition and one of the most significant strategic moves in the company's history.

Rancher Labs, founded by **Sheng Liang** and **Shannon Williams** in 2014, had built a popular open-source platform for managing **Kubernetes** clusters. Kubernetes, originally developed by Google, had become the dominant platform for container orchestration. SUSE's organic Kubernetes capabilities were limited, and the Rancher acquisition gave SUSE an immediate and credible presence in the market.

Rancher's products — **Rancher** for multi-cluster Kubernetes management, **K3s** for lightweight Kubernetes designed for edge computing and IoT, and **RKE** (Rancher Kubernetes Engine) for deploying and managing clusters — complemented SUSE's existing infrastructure products.

The acquisition also brought a different perspective. Rancher Labs was a Cupertino, California startup with a culture more aggressive and marketing-savvy than SUSE's traditional European engineering culture. The integration required care. Sheng Liang was given a senior leadership role and significant autonomy to continue developing the Rancher product line; SUSE maintained Rancher as a semi-autonomous unit, connected to its enterprise sales and support infrastructure but retaining its own development practices.

The NeuVector acquisition, completed in October 2021, added container security to the portfolio. SUSE's decision to open-source NeuVector — releasing the entire platform under the Apache 2.0 license — demonstrated SUSE's commitment to open-source principles even with acquired products.

---

# Part XIV: The Founders — Where They Went

The four founders of S.u.S.E. are notably absent from the later chapters of the SUSE story. This absence is itself significant.

**Roland Dyroff** served as managing director through the company's early growth phase and was involved in the negotiations leading to the Novell acquisition in 2003. After the acquisition, his role was subsumed into Novell's management structure, and he eventually departed. Dyroff was, by temperament, a business leader rather than a public figure, and largely withdrew from the public technology scene. Unlike many American technology founders — who become venture capitalists, board members, or serial entrepreneurs — Dyroff's post-SUSE career was relatively quiet, consistent with a German business culture that values privacy and does not celebrate individual founders in the way Silicon Valley does.

**Hubert Mantel** was SUSE's chief technology officer and one of the most technically influential founders. He remained with SUSE through the Novell acquisition and continued contributing to the distribution's technical direction. He eventually stepped back from active leadership, though the exact timing is not well documented in public sources.

**Thomas Fehr** remained connected to SUSE for an extended period, contributing to development and community engagement. He was known within the community as an accessible and knowledgeable figure.

**Burchard Steinbild** was the least publicly visible of the four founders, and his post-SUSE trajectory is the most difficult to trace from public records.

What is striking about the founders' stories is how different they are from the typical Silicon Valley narrative. In the American technology industry, founders are celebrities. In SUSE's case, the founders built something remarkable, ran it for a decade, sold it, and largely disappeared from public view. The decisions that shaped SUSE's subsequent trajectory — the Microsoft deal, the Attachmate sale, the Micro Focus merger — were made by people who had not built SUSE and who, in some cases, did not fully understand what it was.

The founders' absence from the later story is a symptom of the serial-acquisition problem. Had SUSE remained independent — had the founders retained control, as Linus Torvalds retained control of the Linux kernel — the story would have been different. Whether better is an open question. The founders might have lacked the resources to compete with Red Hat at scale. But they would have been spared the experience of watching their creation passed from owner to owner, their community relationships damaged by the Microsoft deal, and their colleagues laid off by distant corporate parents.

The founders built a company strong enough to outgrow their public identities. That is admirable, but it also means that the "what became of them?" question remains less documented than it should be in mainstream accounts.

---

# Part XV: SUSE and European Digital Sovereignty

SUSE's story cannot be fully understood without reference to the broader European policy push for **digital sovereignty** — the idea that Europe should control its own digital infrastructure rather than depending on American or Chinese technology companies.

This concept has deep roots. European concerns about technological dependence predate the internet era — the French government's support for the national technology champion Bull, the European Commission's antitrust cases against Microsoft and Google, various national programs to promote domestic technology industries. But it crystallized in the wake of the **Snowden revelations in 2013**, which demonstrated that American technology companies — voluntarily or under legal compulsion — were providing the NSA with access to vast quantities of European citizens' data.

**GDPR (2018)** was the most significant data protection law in history. While not specifically an open-source measure, it reflected and reinforced European concerns about data concentration in American technology companies.

**GAIA-X (2019)** was the Franco-German initiative to create a federated European cloud infrastructure based on open standards and European data sovereignty principles. SUSE was a participant, contributing its cloud and infrastructure expertise. GAIA-X has had a complicated trajectory — criticized by some as too ambitious, by others as compromised by the participation of American hyperscalers — but it represents the most significant European attempt to create an alternative to American-dominated cloud infrastructure.

**The EU Open Source Strategy** (most recent version 2020) explicitly commits the European Commission to preferring open-source solutions and describes open source as "key to Europe's digital sovereignty."

**The Schrems decisions** — **Schrems I** (2015) and **Schrems II** (2020), brought by Austrian privacy activist Max Schrems — invalidated the legal frameworks allowing American companies to transfer European personal data to the United States, finding that American surveillance laws did not provide adequate protection for European citizens. This created an opportunity for European cloud and infrastructure providers to offer "sovereign" alternatives keeping data within European jurisdictions. SUSE positioned its products explicitly for this market: open-source code that could be inspected and verified, European operations subject to European law, infrastructure deployable on European hardware in European data centers.

**Did SUSE lobby for these policies?** SUSE was a member of multiple industry associations advocating for open-source-friendly policies, including the **Linux Foundation**, the **Open Source Business Alliance** (a German industry group), and the **Open Forum Europe** (a European policy advocacy organization). SUSE engaged directly with European policymakers, though cautiously — in the European context, direct corporate lobbying is less common and less accepted than in the United States. SUSE's approach was typically to position itself as a contributor to the broader open-source ecosystem rather than a direct beneficiary of open-source policies — both genuinely public-spirited and commercially prudent.

However, symbolism and policy power are not the same. SUSE never became the singular flagship of EU digital sovereignty. Europe's sovereignty agenda is fragmented. Open source complicates nationality — Linux-based companies are partly national and partly transnational. And by the time digital sovereignty became a major policy slogan, the cloud era had shifted control upward toward cloud platforms and hyperscale infrastructure, where SUSE was less dominant. The operating-system vendor, however important, was no longer the sole strategic layer.

---

# Part XVI: Stories from the Trenches

## The Heartbleed Response

When the **Heartbleed** vulnerability (CVE-2014-0160) was disclosed on April 7, 2014, SUSE's Security Team had been notified through the coordinated disclosure process and had begun preparing patches before the public announcement. When Heartbleed was made public, SUSE's patches were ready. Customers who applied the patches within hours of the announcement were protected.

Marcus Meissner, a long-time SUSE security engineer, later described the Heartbleed response at a conference: "We knew about the vulnerability several days before the public disclosure. We had patches ready. But we also knew that the moment the disclosure happened, every system administrator in the world would be asking us, 'Am I affected? What do I do?' We had to be ready not just with patches but with answers."

The Heartbleed incident also prompted SUSE to invest more heavily in the **Core Infrastructure Initiative** (later the **Open Source Security Foundation**), created to provide funding and resources to critical open-source projects being maintained by tiny, underfunded teams. SUSE was a founding member.

A similar dynamic played out with the **Log4Shell** vulnerability in December 2021 — a critical vulnerability in Apache Log4j that allowed remote code execution and was actively exploited within hours of disclosure. SUSE's security team again responded quickly, reinforcing the importance of supply chain security work.

## The Supercomputer Milestone

In November 2017, the TOP500 list showed Linux running on 100% of the world's 500 fastest supercomputers. The Japanese **Fugaku** supercomputer, which held the #1 position from June 2020 to November 2021, ran a customized version of Red Hat Enterprise Linux. But many other top-ranked systems — including systems at the Swiss National Supercomputing Centre and the Leibniz Supercomputing Centre — ran SUSE.

## The CentOS Controversy and SUSE's Response

In **December 2020**, Red Hat announced it would shift CentOS from a downstream rebuild of RHEL to **CentOS Stream**, an upstream development branch. This was, in effect, the end of CentOS as a free, stable, RHEL-compatible production distribution. The announcement infuriated a significant portion of the Linux community. Several projects — **AlmaLinux**, **Rocky Linux** (founded by CentOS co-founder Gregory Kurtzer) — sprang up to fill the gap.

SUSE moved quickly to capitalize, launching the **SUSE Liberty Linux** program offering support for CentOS and other RHEL-derived distributions. This was a savvy move that demonstrated SUSE's ability to compete on Red Hat's turf.

Then, in **June 2023**, Red Hat changed its source code distribution policy, restricting access to RHEL source code for non-customers. Some observers saw this as a betrayal of open-source principles; others saw it as a rational business decision by a company losing revenue to free rebuilds of its product. SUSE responded by publicly committing to keep its own source code freely available. The message was clear: if you were unhappy with Red Hat's direction, SUSE offered a stable, open, European alternative.

---

# Part XVII: The Philosophy of SUSE

## Engineering as Identity

Every technology company has a culture, but SUSE's is more sharply defined than most. It is, at its core, an engineering culture — one that values technical excellence, careful design, and thorough testing above all else. It is less about "move fast and break things" (the Silicon Valley ethos) and more about "move deliberately and build things that last."

A SUSE engineer who releases a feature that is not fully tested and documented would feel shame; a Silicon Valley engineer who delays a release for additional testing might be criticized for lack of urgency. This cultural difference has concrete consequences: SUSE Linux Enterprise releases tend to be more stable and polished than competitors at launch, but they also tend to arrive later. In environments where reliability is paramount — running SAP, managing supercomputers, operating critical infrastructure — SUSE's approach has been a significant advantage.

## The Upstream Commitment

One of SUSE's most important philosophical commitments is to **upstream contribution** — contributing improvements back to original open-source projects rather than maintaining private patches. By contributing upstream, SUSE ensures that its changes are maintained by the broader community, reducing long-term maintenance costs, building goodwill, and ensuring that the projects on which SUSE depends remain healthy.

## Linux Should Be Operable

If SUSE's philosophy could be compressed into a few themes: Linux should be operable — power is not enough, systems must be administrable and recoverable. Serious computing deserves serious documentation and tooling. Enterprise trust is earned through engineering discipline, not just marketing claims. Open source can serve institutions and public sector. Community matters, but so does productization.

SUSE's deepest identity is **system stewardship** — free software can be professionally governed, Linux can be a product without ceasing to be open source, and reliability is not the enemy of freedom.

## Open Source as a European Value

There is an argument that open-source software is intrinsically aligned with European values. European political philosophy emphasizes collective welfare, transparency, and limitation of concentrated power. Open-source software embodies these values — collectively developed, transparent in its workings, not controlled by any single entity. When the European Commission pushes for open standards, when the German BSI recommends open-source security tools, when the French Gendarmerie migrates to Linux — SUSE benefits, not just commercially but reputationally. It is seen as a European champion, a company that embodies values Europeans hold dear.

---

# Part XVIII: SUSE Today — Product Portfolio and Challenges

## The Product Portfolio

SUSE's product portfolio spans several key areas:

**SUSE Linux Enterprise Server (SLES)** remains the company's flagship — a rock-solid enterprise Linux distribution with long-term support (up to 13 years with extended support), extensive hardware and software certification, and a reputation for reliability. SLES is particularly strong in SAP environments, HPC, mainframe computing, and mission-critical applications.

**SUSE Rancher** is the Kubernetes management platform providing a unified interface for deploying and managing Kubernetes clusters across multiple cloud providers, on-premises data centers, and edge locations.

**SUSE NeuVector** is a container security platform, open-sourced in 2021 — demonstrating SUSE's commitment to open-source principles even with acquired products.

**SUSE Manager** provides infrastructure management for large fleets of Linux systems from a central console.

**SUSE Linux Enterprise Micro** is a lightweight, immutable operating system designed for containers and edge computing — representing SUSE's response to the trend toward minimal, purpose-built operating systems.

**openSUSE** continues as the community distribution in two forms: **Leap** (regular-release, aligned with SUSE Linux Enterprise) and **Tumbleweed** (rolling-release). Emerging projects include **openSUSE MicroOS**, **openSUSE Aeon**, and **openSUSE Kalpa** (immutable desktop distributions using GNOME and KDE respectively).

**The Adaptive Linux Platform (ALP)**, under development, represents a fundamental architectural shift — from a traditional monolithic Linux distribution to a modular, container-native, cloud-ready platform that can adapt to different workloads and deployment models.

## The Competitive Landscape

The enterprise Linux market has evolved significantly. An increasing proportion of enterprise computing is moving to public cloud platforms. In the cloud, the choice of Linux distribution is less visible and less consequential than on-premises. The competition has shifted from "whose Linux is better?" to "whose Kubernetes platform is better?" — a question still being resolved.

**Edge computing** — in retail stores, factories, vehicles, remote locations — creates demand for lightweight, purpose-built Linux distributions. SUSE's SUSE Linux Enterprise Micro and K3s lightweight Kubernetes distribution are well-positioned here. Edge computing plays to SUSE's strengths: reliability, long lifecycle support, and the ability to operate where continuous connectivity cannot be guaranteed.

After the IBM acquisition of Red Hat in 2019, some Red Hat customers became uncomfortable with IBM ownership, and SUSE was well-positioned to benefit from this unease as the only remaining major independent enterprise Linux company.

---

# Part XIX: Why Red Hat Won — A Complete Answer

It is the question that every SUSE employee, community member, and customer has asked at some point: Why did Red Hat dominate the enterprise Linux market while SUSE remained a strong but perpetual second?

The answer is not simple, and it is not primarily about technology. SUSE's technology was, by most objective measures, at least as good as Red Hat's — and in many areas, superior. But technology alone does not determine market outcomes.

Red Hat dominated because of a **system of advantages**, not any single factor:

It was closer to U.S. enterprise and federal power. It mastered the subscription model and made itself the definitive symbol of enterprise open source. It accumulated ecosystem default status through hardware certifications, ISV partnerships, and the CentOS installed base. It benefited from U.S. procurement and certification gravity in ways SUSE structurally could not match. It turned SELinux and high-assurance security credibility into strategic advantage in the government market. It maintained a clearer corporate narrative for longer through independent ownership. It built a stronger enterprise sales machine and a self-reinforcing certification ecosystem. And it had the capital — from its 1999 IPO and subsequent equity offerings — to execute aggressively in all of these areas simultaneously.

SUSE, by contrast, faced structural disadvantages: a European home market smaller than Red Hat's global footprint, no access to comparable capital, repeated corporate ownership changes that disrupted long-term strategy, and a culture that valued thoroughness over speed in a market that often rewards speed.

Red Hat's dominance was not a verdict that SUSE lacked technical merit. It was the result of market geography, business execution, ecosystem scale, strategic continuity, and the structural advantages that came from being an American company in an American-centered global technology market.

SUSE remained the rival that proved enterprise Linux could have more than one serious tradition. It did not win Linux mythology most completely — Red Hat won more of that, Ubuntu won a different part, Debian won a moral part. But SUSE won the respect of people who know what it means to run systems that must keep working.

---

# Part XX: The Deeper Meaning

## What SUSE Represents

SUSE's story is, on one level, simply the history of a company. But at another level, it is a story about technology, markets, and the relationship between technology and culture.

SUSE represents the proposition that there is more than one way to build a technology company. The Silicon Valley model — aggressive growth funded by venture capital, winner-take-all competition, a culture of disruption and dominance — is not the only model. SUSE embodies an alternative: steady growth, technical excellence, deep customer relationships, community collaboration, and a European sensibility that values thoroughness over speed and sustainability over domination.

SUSE helped invent a style of Linux — documented, administrable, institutionally legible, security-conscious but operationally humane, suitable for critical workloads, shaped by a European suspicion of chaos. Its philosophy was not glamorous revolution. It was disciplined freedom.

SUSE also represents the proposition that open-source software is not exclusively an American phenomenon. While many of the most prominent open-source projects originated in the United States, open source has always been a global movement, and European contributions — from Linus Torvalds' kernel (Finland), to KDE (Germany), to SUSE itself — have been fundamental to its success. SUSE's endurance as a European open-source company, through three decades of American-dominated technology markets, is a testament to the viability of a European approach to technology.

SUSE is, in the end, a story about Linux becoming adult — about free software being professionally governed, about an operating system that needed dreamers and ideologues but also needed adults who would take this wild, open, unfinished system and make it fit for companies, governments, labs, hospitals, and factories. SUSE was one of those adults. That is why it endures.

---

# Epilogue: The Four Men and the Chameleon

There is no monument to Thomas Fehr, Burchard Steinbild, Hubert Mantel, and Roland Dyroff in Nuremberg. No plaque on the wall of their first office. No statue in the town square. This is as it should be, perhaps — they were engineers, not politicians, and Germany does not typically memorialize its entrepreneurs the way Silicon Valley does.

But what they built endures.

Somewhere, right now, a system administrator in a German government agency is using YaST to configure a server. A researcher at a Swiss supercomputing center is running a simulation on a SUSE-powered cluster. A factory in Bavaria is controlling its production line with a SUSE-powered embedded system. A bank in Frankfurt is processing transactions on a SUSE-powered mainframe. A startup in Berlin is deploying containers on Rancher-managed Kubernetes clusters.

And somewhere in Nuremberg, in an office that has changed addresses several times but never left the city, a SUSE engineer is working on the next release. The corporate parent may change again. The market may shift again. The competitors may gain ground again. But the code will be good, the documentation will be thorough, and the chameleon will adapt.

It always does.

---

_"We were never the loudest. We were never the richest. We were never the fastest. But we were always here, and we always will be."_ — A SUSE engineer, speaking at the 30th anniversary celebration, Nuremberg, 2022

_"In the open-source world, the code is the culture. SUSE's code tells you everything you need to know about SUSE: it is careful, thorough, well-documented, and built to last. It is, in a word, German."_ — A SUSE engineer, speaking at a community conference, circa 2018

---

**End.**