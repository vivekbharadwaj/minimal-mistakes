---
title: "Just how intelligent is AI?"
excerpt: "No need to fear SkyNet just yet"
layout: single
header:
    overlay_image: /assets/images/intelligent-ai-kurzweil-exponential.jpg
    overlay_filter: 0.2
categories:
  - artificial intelligence
  - bayesian program learning
  - one-shot learning
  - transfer learning
  - nips
tags:
  - artificial intelligence
  - general thoughts
author: "Vivek"
date: "23 December 2016"
hidden: false
---

I published this article first on Linkedin Pulse. You can read this  article on Linkedin [here](https://www.linkedin.com/pulse/just-how-intelligent-ai-vivek-bharadwaj/)

Hello everybody. It's been a while since my last note. What a year 2016 has been! Some [strange things](http://www.thelocal.de/20161114/how-german-media-depicts-trumps-victory?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D) happened on the global scene. 2016 was however a very big year in humanity's quest for AI. As a community we challenged many benchmarks and techniques that were previously [state-of-the-art](http://www.theverge.com/2016/3/9/11185030/google-deepmind-alphago-go-artificial-intelligence-impact?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D), AI has caught public attention like never before and we've come together to collaborate through partnerships and through investments.

We live in interesting times. Many problems that were previously thought as intractable, such as "how do we think?" and "where does intelligence come from?" are now being tackled by the smartest people on the planet.

![mission statements]({{ site.url }}{{ site.baseurl }}/assets/images/intelligent-ai-mission.png)

High Technology companies like Google & Facebook are funding business models to support researchers as they boldly claim to "solve intelligence".

DeepMind, a leading AI research team now acquired by Google, claims that it can [create problem solving AI with the general intelligence of a mouse](http://lesswrong.com/lw/nus/deepmind_plans_for_ratlevel_ai/?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D) by 2017. To quote [Tim Urban](http://waitbutwhy.com/2015/01/artificial-intelligence-revolution-1.html?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D), "This doesn’t sound like much until you remember that we were at about a trillionth of human level intellect in 1985, a billionth in 1995, and a millionth in 2005. Being at a thousandth in 2015 puts us right on pace to get to an affordable computer by 2025 that rivals the power of the brain." What's the story behind our confidence?

Much to the embarrassment of futurologists and AI researchers, making any sort of predictions with AI has proven to be extremely difficult.

![wrong before]({{ site.url }}{{ site.baseurl }}/assets/images/intelligent-ai-dartmouth.png)

In 1956, the top computer scientists and researchers in the field proposed to use 10 undergrads for 2 months "to make machines use language, form abstractions and concepts, solve kinds of problems reserved for humans, and improve themselves". This was when many experts consider the field of AI to have been conceived.

6 decades later, we've only scratched at the problem. On the other hand, hard problems that were previously thought of as unsolvable such as winning at Chess and the ancient Chinese game of Go have been solved 20-30 years ahead of expectation. It's no reflection on the predictive capabilities of these top minds. Intelligence is fundamentally hard to solve. As always, the conundrum is succinctly summed up by [xkcd](http://xkcd.com/1425/?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D).

As a budding researcher trying to uncover the current state of progress in AI, I kept getting lost in the phenomenal hype of deep learning, big data and distributed computing. So I decided to use the number of research contributions to the NIPS conference as a directional proxy to indicate the progress of AI. For those among us new to the field, NIPS (Neural Information Processing Systems) is the definitive scientific conference for artificial intelligence where the who's who of the field come and talk about what scientific development excites them and what they've been working on over the past year. The 2016 NIPS conference was held in Spain during the first week of December, just a few weeks ago.

I collated the data (thanks Kaggle!) and [analysing the papers](http://github.com/vivekbharadwaj/nips_papers_analysis?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D) submitted to NIPS. If you'd like more information about the data collected, NIPS paper authors and would like to collaborate with me, feel free to fork my repo or contact me. The results speak loudly about the explosive growth of advancements in neural networks, although growth has been relatively modest in Australia.

![viv-analysis-num-submissions]({{ site.url }}{{ site.baseurl }}/assets/images/intelligent-ai-num-submissions.png)

As a side note, congratulations to the 122+ Australian papers that got accepted to this prestigious conference.

![viv-analysis-aussie-sampling]({{ site.url }}{{ site.baseurl }}/assets/images/intelligent-ai-aussie-sampling.png)

The sheer amount of [information disseminated in the conference](http://nips.cc/Conferences/2016/SpotlightVideos?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D) boggles my mind. What began over the weekend as a hacky analysis to understand the scope of AI research within Australia morphed into something bigger as I began reading and sorting through topics. One paper in particular, titled "[Building Machine that learn and think like people](http://arxiv.org/abs/1604.00289?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D)" and running over 50 pages long, had me wrapped up in interesting thoughts. In this paper, the authors Lake, Tenenbaum et al argue that while current learning systems based on statistical pattern recognition such a deep learning and reinforcement learning have achieved better-than-human level of success in object recognition and control systems, human learning is richer and more efficient. Human beings require extraordinarily few learning examples to learn a concept - think of the number of times you've electrocuted yourself to know that electricity is bad for you. The paper then goes on to list intuitive physics, intuitive psychology, compositionality and causality as the "core ingredients" upon which human intelligence is built. As an illustration to drive the point home, they contrast image captions generated by state-of-the-art deep neural networks with how a human being (you the reader) understands the same scene. Learning a scene without actually perceiving it results in objectively true enough yet funnily incorrect interpretations (image below picked from the paper).

![tenenbaum-misclassified-images]({{ site.url }}{{ site.baseurl }}/assets/images/intelligent-ai-misclassified-imagenet.png)

Overall, this paper was a great read and a good start before delving into the other math-heavy papers! I want to mention that it's truly exceptional that we're now able to have machines even perform image captioning with [94% accuracy rate](http://www.techtimes.com/articles/179240/20160924/google-image-captioning-artificial-intelligence-system-has-94-percent-accuracy.htm?lipi=urn%3Ali%3Apage%3Ad_flagship3_pulse_read%3BBY7aDbmqRcKhTK3UhjhNxQ%3D%3D) and other such incredible feats without explicitly programming them to do so. It's an impressive feat to have achieved so much in a short time-span of a few decades. However, I'd like to leave you with an appreciation of just how far we need to go to achieve general intelligence, let alone awaken sentient machine overlords.

I believe that if we want to get anywhere with intelligence, then we need to develop deep learning systems that are able to learn from less data (one-shot learning), possess "common-sense"/intuition and finally, build causal models of the world. Each facet contributes to the other but there are subtle differences between them. Researchers have been coming up with new strategies and approaches recently to tackle one-shot learning such as inductive transfer(transfer learning), metric learning (representations), memory networks (DeepMind), Hierarchical Bayesian models and Generative networks. With 2016 coming to an end, I intend to spend considerable time next year trying to learn more about generating causal models, developing intuition and helping machines “learn to learn”.

If you'd like to collaborate with me on an interesting project or learn together, don't hesitate to reach out via comments or a private message.

Happy Holidays!

Notes: <br>
- Cover Image: Kurzweil's demonstration of the exponential growth of computing <br>
- Cover Image courtesy: [business insider](https://amp.businessinsider.com/images/5564fd84eab8ea433ec13811-960-720.jpg) <br>