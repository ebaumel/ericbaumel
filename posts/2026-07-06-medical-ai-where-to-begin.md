---
title: "Medical AI Is Everywhere. Where Should a Clinician Begin?"
description: A radiologist's map for clinicians who want to understand medical AI. Start with the concepts that matter, skip the hype, and build real intuition.
categories:
- digital health
- data science
date: '2026-07-06'
draft: true
toc: false
---

How did you learn your first imaging modality?

Nobody handed you a physics textbook and wished you luck. You learned what the machine was for, what it could see, what it could miss, and only then how it worked under the hood. Learning medical AI works the same way. You don't need a PhD in mathematics. You need a working intuition for what these tools can see and what they can miss.

That's the goal of this video, and this companion post is the written version you can come back to.

{{< video https://www.youtube.com/watch?v=54I_ZMan7Hw >}}

## The landscape, without the hype

Medical AI is already reading alongside us. It flags intracranial hemorrhages in the worklist, measures ejection fractions, drafts patient messages, and summarizes charts. The question stopped being "will AI come to medicine?" years ago. The question now is whether the clinicians using it understand it well enough to supervise it.

Because that's the real job. AI in medicine is not a replacement. It's a very fast resident with no license, no judgment, and no memory of yesterday's mistake. You are still the attending. And no attending signs a report they don't understand.

## Three terms that do most of the work

**Machine learning** is pattern recognition at scale. Show a system enough labeled chest X-rays and it learns the statistical fingerprint of pneumonia the way you learned it: from examples, not from rules.

**Deep learning** is machine learning with many stacked layers, which is what lets a model go from pixels to "probable pneumothorax" without a human writing the intermediate steps.

**Large language models** (the engines behind ChatGPT and Claude) are pattern learners trained on text instead of pixels. They predict the next word, astonishingly well. That's why they draft a discharge summary beautifully and why they can also state a wrong drug dose with perfect confidence. Fluency is not accuracy.

## Where to actually begin

Start with use, not theory. Pick one AI tool that touches your daily work and pay attention to it like you'd pay attention to a new contrast protocol: when does it help, when does it fail, and what are its failure modes?

Then add just enough theory to ask sharp questions. What data was this trained on? Does that population look like my patients? What's the sensitivity and specificity, and against what gold standard? These are questions you already know how to ask. You've been appraising studies your whole career; a model card is just a new kind of methods section.

If you want to go deeper, I wrote a starting roadmap for the technical side in [Machine Learning for Radiology — Where to Begin](https://medium.com/data-science/machine-learning-for-radiology-where-to-begin-3a205db8718f), and the tools in this blog's Python posts are the same ones the field is built on.

## Recap

You don't need to become an engineer. You need modality-level intuition: what the tool is for, what it can see, what it misses, and how to supervise it. Watch the video, pick one tool you already encounter, and start asking it the questions you'd ask any new technology in your department.

The machines are already in the reading room. Be the attending.

---

*__About the author:__ Eric M. Baumel, MD is a board-certified diagnostic radiologist, app developer, and digital health entrepreneur. He teaches technology to healthcare professionals at [Coding4Docs](https://www.youtube.com/@Coding4Docs). Read more on the [About page](/about.html).*
