---
layout: default
permalink: /projects/
title: projects
nav: true
nav_order: 2
---


# Iterated Confusion Minimization

Iterated Confusion Minimization (ICM) is an algorithm and model of sound change that I have have put forward based on the interaction of mathematically optimal listeners and speakers over time.

In my [master's thesis](https://www.proquest.com/docview/3116041345), advised by [Bruce Hayes](https://brucehayes.org/) (co-chair), [Megha Sundara](https://linguistics.ucla.edu/person/megha-sundara/) (co-chair), and [Meg Cychosz](https://megseekosh.github.io/), I demonstrated that ICM simulations over the vowel space improve upon past models in Dispersion Theory in explaining vowel system typology, yielding improved predictions about typological variation and the acoustic structure of larger vowel systems, while also connecting these typological patterns to a plausible model of sound change. A journal article version of the this thesis is currently under review.

Ongoing work involves simulating ICM over phoneme sequences to model patterns of allophony and augmenting ICM with a model of phonetic category acquisition to model patterns of phonemic merger.


# Phoneme confusability measures from HMM/GMM acoustic models

ICM requires statistically modeling phonetic distributions to estimate the confusion rate associated with different sound systems. Although this is relatively straightforward for vowels, which can be idealized as occupying a two-dimensional phonetic space corresponding to the first and second formants, there is no analogous low-dimensionality acoustic space that can be used for modeling phonetic distributions of consonants.

Meanwhile, experimentally informed measures of phonetic similarity based on perceptual confusion matrices (cf. [Miller & Nicely, 1955](http://jontalle.web.engr.illinois.edu/uploads/MISC/ReadingGroup.11/Papers/MillerandNicely_1955.pdf)) are resource-intensive to produce and generally only exist for well-studied languages. 

To fill this gap, I am engaged in ogoing research to extract confusability measures from HMM/GMM acoustic models, widely used in a variety of automatic speech recognition applicaitons, and validate these measures against empirical data from speech perception studies. Given the wide online availability of pre-trained GMM/HMM acoustic models, developing techniques to extract confusability measures from acoustic models may provide a less resource-intensive alternative method of phoneme confusability estimation with a variety of applications in phonetic research.


# Frequency effects in phonetic categorization

In the future, I intend to use ICM to simulate frequency effects in sound change. Empirically grounding these simulations requires thorough experimental investigation of how frequency effects influence speech perception.

To this end, I am currently running experiments investigating the effect of monophone frequency in phonetic categorization with collaborators [Megha Sundara](https://linguistics.ucla.edu/person/megha-sundara/) and [Jeremy Steffman](https://jsteffman.github.io/), who have previously demonstrated biphone frequency effects in phonetic categorization ([Steffman & Sundara, ](https://pubs.aip.org/asa/jel/article/3/12/125202/2929413)).

# Phonemic restoration and phonological neighborhood effects

I am involved in a collaboration with [Jesse Harris](https://jesseharris.netlify.app/) and [Christian Muxica](https://www.christian-muxica.com/) using pupillometry to investigate early inhibition and extended competition during sentence processing between minimal pairs including low- and high-frequency phonological neighbors. These experiments involve a phonemic restoration component, with each minimal pair rendered ambiguous by masking the disambiguating segment. I have primarily been involved in writing Praat scripts to mask and splice together the audio for stimuli across experimental conditions.
