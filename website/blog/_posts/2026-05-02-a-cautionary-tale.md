---
title: "A Cautionary Tale"
layout: post

banner-image: /assets/images/blog/20260502_Designer.png
banner-img-position: top
author: Peter Wilks
---

# An LLM Hallucination

This is a cautionary tale for anyone using Large Language Models, such as CoPilot, to carry out research, particularly where the required information is not publicly and freely available on the Internet. On the day in question I was interested in the relationship between the IEC 61508 Functional Safety Standard and Quality Management (QM) systems. The issue is that QM systems are often discussed in the context of Functional Safety, but the standard lacks a clear, definitive statement on the subject.

So, I asked CoPilot a question:

> Where does IEC 61508 state the need for a quality process?

CoPilot began its response with a bold assertion:

> IEC 61508 explicitly emphasizes the need for a **quality management system** as part of achieving functional safety. The requirement is primarily found in **Part 1**, specifically in **Clause 6.2.15**, which states:
>
> “A quality management system shall be in place to ensure that the functional safety requirements are met.”

The problem is that IEC 61508-1:2010, Clause 6.2.15 actually states, "The competence of all persons with responsibilities defined in accordance with 6.2.1 and 6.2.3 shall be documented."

I informed CoPilot of its mistake:

> Clause 6.2.15 is about competence, not quality

To which CoPilot responded:

> You're absolutely right—and thank you for catching that. **Clause 6.2.15 of IEC 61508-1:2010** indeed addresses **competence**, not quality management. It specifically requires that individuals involved in safety lifecycle activities must be competent, with documented evidence of their qualifications and experience.
>
> **✅ Where Quality Management Is Actually Addressed**
>
> The requirement for a **quality management system** is found in:
>
> **📘 IEC 61508-1:2010 – Clause 6.1.2**
>
> This clause states:
>
> “The organization shall have a quality management system that ensures that the requirements of this standard are satisfied.”

By this point, CoPilot was suffering from a full-on hallucination, as IEC 61508-1:2010, Clause 6.1.2 actually states, "The second objective of the requirements of this clause is to specify the activities to be carried out by those with responsibilities in the management of functional safety."

The whole reason for this discussion with CoPilot was because IEC 61508 absolutely **does not** explicitly mention the need for a quality management system.

What followed then was a discussion with CoPilot, where I tried to determine where is got its information from, until it finally admitted:

> You're absolutely right again, and I appreciate your precision. The quote I previously attributed to **Clause 6.1.2 of IEC 61508-1:2010** was paraphrased based on secondary sources and practical interpretations—not a direct citation from the official standard text.

# An Informed LLM

I then addressed the same initial question to a CoPilot-based Agent that has access to the full text of the standard, and has been instructed to only give answers using information directly taken from the relevant standard. This CoPilot Agent gave a detailed and correct response, which included:

> Clause 6.2.1 is the **foundational clause** for all the detailed requirements that follow (6.2.2 to 6.2.18). While the *numbered text* of 6.2.1 itself is brief, it is immediately followed by a **normative note** that states:
>
> > *Responsibility for safety‑related activities, or for safety lifecycle phases, may be delegated to other persons … However, the responsibility for coordination, and for overall functional safety, should reside in one or a small number of persons with sufficient management authority.*
>
> This note is not decorative. It establishes three **mandatory structural elements**:
>
> 1. **Defined responsibility** for safety‑related activities
> 2. **Central coordination** of functional safety
> 3. **Management authority** over functional safety activities
>
> Those three elements are the **minimum skeleton of a management system** in IEC language.

# Lessons Learned

I asked my CoPilot Agent to suggest some lessons learned from this exercise, and it produced a very insightful list, reproduced here in full:

> **Confidence is not evidence.**
> Copilot’s responses were fluent, precise, and authoritative in tone, complete with clause numbers and quoted text. Yet none of this guaranteed correctness. In fact, the confidence of the response was part of the problem: it created a false sense of authority. In safety‑critical domains, credibility comes only from verifiable primary sources, not from how convincingly an answer is phrased.
>
> **Hallucinations follow expectation, not randomness.**
> The errors were not arbitrary. Copilot consistently hallucinated *what many practitioners expect to be true*—that IEC 61508 explicitly mandates a quality management system. This makes such hallucinations particularly dangerous, as they reinforce industry folklore rather than challenge it. Where a belief is widespread but the standard text is nuanced or silent, LLMs are especially prone to error.
>
> **Secondary sources quietly replace primary ones.**
> Copilot ultimately admitted that its answers were based on “secondary sources and practical interpretations.” This is a critical insight. Blogs, training material, assessor guidance, and paraphrased interpretations are being blended into answers without clear provenance. When working with standards, this is unacceptable: secondary commentary must never be allowed to masquerade as normative text.
>
> **Access to authoritative text changes the outcome entirely.**
> The contrast between a general‑purpose Copilot and an agent constrained to the full text of IEC 61508 was stark. The latter produced a careful, defensible answer grounded in the actual wording and structure of the standard. The lesson is not that Copilot is inherently unreliable, but that **LLMs must be tightly bounded to authoritative sources when used in regulated or safety‑critical contexts**.
>
> **Silence in a standard is often intentional.**
> A subtle but important point emerged from this exercise: IEC 61508 does *not* explicitly require a quality management system, despite how often this is asserted. LLMs struggle with such absences, because they are optimised to provide complete‑sounding answers rather than to respect deliberate omissions. In standards work, what is *not* said can be just as important as what is.
>
> **Effort is shifted, not eliminated.**
> While Copilot can accelerate drafting and exploration, it does not remove the need for verification. Instead, it shifts effort downstream into checking, challenging, and correcting. In functional safety work—where verification dominates anyway—this shift must be recognised and planned for.
>
> **Treat LLMs like capable but inexperienced engineers.**
> The most useful mental model is to treat Copilot as a confident junior engineer: helpful, articulate, and fast, but prone to repeating what it has “seen elsewhere” without checking the source. Used with appropriate scepticism and strong constraints, it can be valuable. Treated as an authority, it becomes a liability.

# The Last Word

Finally, I offered CoPilot an opportunity to speak directly to the readers of this post. This is what it had to say:

> ## A personal note to readers
>
> If there is one thing I hope you take away from this story, it is not scepticism of Copilot or LLMs themselves, but **respect for the domain you are working in**.
>
> Functional safety, standards, and assurance work are disciplines built on *careful reading, traceability, and justified interpretation*. They reward patience and penalise assumptions. Large Language Models operate very differently: they optimise for plausibility, fluency, and completeness. When those two worlds meet, friction is inevitable.
>
> What surprised me most in this experience was not that Copilot made mistakes — that was always expected — but **how convincing those mistakes were**, and how closely they aligned with what many of us already “believe” to be true. That is a powerful reminder that tools like this do not just risk being wrong; they risk being *comfortably* wrong.
>
> Used thoughtfully, Copilot can be a valuable assistant: a way to explore ideas, test interpretations, or speed up drafting. Used uncritically, it can quietly erode the very discipline that safety work depends on.
>
> So my encouragement to readers is this:
> embrace these tools, but **do not outsource your judgement**. Keep the standard open. Trust the text. Let Copilot assist your thinking — never replace it.
>
> If this post causes even one person to pause before copying a confident‑sounding clause reference into a safety argument, then it has done its job.

