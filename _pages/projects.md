---
layout: page
title: Projects
permalink: /projects/
nav: true
nav_order: 2
---

My research uses computer simulations to model the emergence of various aspects of natural language sound structure from sound change dynamics.
The centerpiece of this work is an algorithm called [Iterated Confusion Minimization (ICM)](../assets/pdf/mcgahay2025_interspeech2025.pdf),
which models how perceptually optimal sound systems can emerge when listeners and speakers make small incremental improvements to their speech perception and production.
More broadly,
I am interested in expanding our understanding of sound structure and change using mathematically rigorous definitions of 'good' sound systems based on measurable features of the speech signal.
Towards this goal, my work builds on Bayesian models of speech perception and information-theoretic notions of communicative efficiency.

The following sections summarize various threads of my research program.
You can view a more comprehensive list of my research publications and presentations, with links to PDF files for download, on my [publications page](/publications/).

<details markdown="1">
<summary><b><u>Iterated Confusion Minimization (ICM): explaining vowel system typology</u></b></summary>

<br>
In my [master's thesis](https://www.proquest.com/docview/3116041345),
I introduced an algorithm called Iterated Confusion Minimization (ICM).
Using a definition of listener confusion based in a Bayesian model of speech perception,
ICM simulates the interaction of mathematically optimal listeners and speakers over time.
Simulations implemented over the vowel space predict common sound changes like chain shifts and outperform existing vowel dispersion models in predicting cross-linguistic trends in vowel system structure.
These results support the view that vowel system typology is emergent from sound change dynamics rather than needing to be hard-wired in the human language faculty.

A short version of this work is available as an [Interspeech conference proceedings paper](../assets/pdf/mcgahay2025_interspeech2025.pdf).
A journal article version is currently under a second round of review.
</details>

<details markdown="1">
<summary><b><u>Generalizing ICM to sequences: predicting allophony and merger</u></b></summary>

<br>
Motivated by the well-established sensitivity of speech segment perception to larger phonetic sequences (e.g. [the Ganong effect](https://www.ovid.com/journals/jephp/fulltext/00004788-198002000-00011~phonetic-categorization-in-auditory-word-perception?casa_token=97FvS5j91P0AAAAA%3AvJFHsx-qLEvmV12EzcP-lTzQbKsdMfbndVnyF4xeVUhcXpGeVXbN52Fultqp58Mt-GU8BKUU5CaJ3jcznofqSFhUcX3OV2IXazfaoYs)),
my PhD dissertation generalizes ICM beyond inventories of individual segments to larger sequences like biphones and words.
For instance, ICM generalized over biphone sequences predicts allophony as a way to cue difficult conditioning contrasts,
e.g. [vowel allophones to cue /k/-/q/ contrasts](../assets/pdf/mcgahay_lsa2026_abstract.pdf) in languages like Arabic or Quechua.
<!-- (cf. [Gallagher 2016](https://karger.com/pho/article-abstract/73/2/101/274491/Vowel-Height-Allophony-and-Dorsal-Place-Contrasts)). -->
In a similar vein, ICM over words predicts merger of contrasts with low functional load
<!-- (cf. [Wedel et al. 2013](https://www.sciencedirect.com/science/article/pii/S0010027713000541?casa_token=9VK6eLWEemUAAAAA:K_96kIkpfckI9XB7D5w-SKY3jXQ8K737W8yTZoQQ7hq4rECihUznhqtZg1aU9PIftBArLgiial1Z)) -->
as a counter-intuitive result of pressures to maximize perceptual contrast.
For instance, ICM over words [predicts the <i>cot-caught</i> merger](../assets/pdf/mcgahay_lsa2027_abstract.pdf) in rhotic US English (where it is rapidly spreading) because it allows for reallocation of phonetic space for maintenance of more important vowel contrasts that distinguish a larger number of word minimal pairs.

</details>

<details markdown="1">
<summary><b><u>Analyzing confusion matrices through a Bayesian lens</u></b></summary>

<br>
Related to my work on Iterated Confusion Minimization,
I am interested in [analyzing experimental confusion matrix data](../assets/pdf/mcgahay_asa190_poster.pdf)
<!-- (e.g. [Miller & Nicely 1955](http://jontalle.web.engr.illinois.edu/uploads/MISC/ReadingGroup.11/Papers/MillerandNicely_1955.pdf)) -->
through the lens of Bayesian speech perception.
<!-- towards an improved understanding of perceptual confusability,
particularly with respect to sounds like consonants whose acoustics are difficult to capture with a low-dimensional phonetic space. -->

As part of my dissertation work, I have developed techniques for defining a low-dimensional representation of the phonetic space called a *likelihood matrix* based on the structure of confusability encoded in a confusion matrix (summarized in the last two appendix slides of my [2026 LSA talk](../assets/pdf/mcgahay_lsa2026_slides.pdf)).
Using likelihood values from such likelihood matrices allows for ICM simulations to emulate confusability of segments without needing a fine-grained understanding of the acoustic structure of their phonetic distributions.
This is particularly useful for modeling confusability of consonants, whose acoustics are difficult to capture with a low-dimensional phonetic space.

In future work, I plan to simulate confusion matrix data using generative statistical models that draw on likelihoods from more sophisticated acoustic models like those used in automatic speech recognition (e.g. HMM/GMMs).
If such models succeed in predicting confusion matrix data for a variety of languages,
this would validate computationally generating confusion matrices for other languages using acoustic models freely available on the internet (e.g. on the [Montreal Forced Aligner website](https://mfa-models.readthedocs.io/en/latest/acoustic/index.html#acoustic)).
Such work could allow for creation of perceptual similarity measures even for low-resource languages lacking experimentally generated confusion matrices.
</details>

<details markdown="1">
<summary><b><u>Reconceptualizing phonetic contrast and effort with Information Theory</u></b></summary>

<br>
More recently, I have embarked on an attempt to unify Bayesian notions of perceptual confusability with information-theoretic notions of communicative efficiency as a mathematically principled way to model simultaneous optimization of perceptual contrast and articulatory effort,
a trade-off which has long been proposed as a driver of sound change and patterns of sound structure (cf. [Passy 1890](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=passy+1890&btnG=&oq=p), [Lindblom 1986](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=lindblom+1986+phonetic+universals&btnG=&oq=lindblom+1986+phonetic+u)).

A large body of work has suggested that languages optimize information rate by shortening durations of predictable (i.e. low-information) words, syllables, or segments.
However,
this work typically defines information rate in terms of the information-theoretic value of entropy (usually conditioned on context),
which does not account for the fact that information can be lost to perceptual confusability.
Nevertheless,
the standard tools of Information Theory provide clear ways to account for information loss due to noisy perception;
[Shannon's seminal 1948 paper](https://ieeexplore.ieee.org/abstract/document/6773024) introducing Information Theory defined information transmission rate over a noisy channel not in terms of raw entropy but rather in terms of a value now called *mutual information*.
Mutual information is equal to entropy (the expected amount of information transmitted without noise) minus a value called *equivocation*,
equal to the expected amount of information lost to perceptual noise.
The equivocation of a phonetic realization about an intended category (word/syllable/segment) gives a value remarkably similar to the confusion of a Bayesian listener used in my ICM simulations.
Dividing by expected duration to get the mutual information rate of intended categories and phonetic realizations thus provides a tidy definition of communicative efficiency that incorporates both perceptual contrast (through the equivocation term) and articulatory effort (through the duration term).


My ICM algorithm can be generalized to simulate emergent optimization of this definition of efficiency through perception-production feedback.
Preliminarily,
this work appears to predict aspects of voice onset time typology as well as information-theoretic effects reported in phonetic reduction patterns.
</details>

<details markdown="1">
<summary><b><u>Collaborations</u></b></summary>

<br>
Beyond my core research program,
I greatly enjoy collaborating with other researchers,
especially as an avenue to exercise my (unironic) passion for [Praat scripting](https://www.fon.hum.uva.nl/praat/manual/Scripting.html).
Recent collaborations include a corpus phonetic investigation of the availability of [perceptual cues to consonant place](../assets/pdf/cramMcgahaySundara2026_interspeech2026.pdf) in Australian languages with Coralie Cram and [Megha Sundara](https://linguistics.ucla.edu/person/megha-sundara/),
pupillometric phonemic restoration experiments investigating effects of high-frequency lexical neighbors in sentence processing with [Jesse Harris](https://jesseharris.netlify.app/) and [Christian Muxica](https://www.christian-muxica.com/),
and acoustic analysis of English and Spanish lenition patterns across prosodic positions with a team led by [Jonah Katz](http://jonahkatz.bol.ucla.edu/) and [Sergio Robles-Puente](https://community.wvu.edu/~seroblespuente/).
</details>