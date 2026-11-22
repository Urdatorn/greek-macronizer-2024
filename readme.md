# Master thesis: "A Macronizer for Ancient Greek"

NOTE: This repo is for archiving the code accompanying [my master thesis from 2024](Thörn Cleland 2024 - A Macronizer for Ancient_Greek.pdf), and is neither active nor any longer recommended. For a working SOTA deterministic macronizer, see rather my [grc-macronizer](https://github.com/Urdatorn/grc-macronizer)!

Much philological work on Ancient Greek texts hinges on correctly disambiguating the vowel length of the so-called dichrona vowels, α, ι and υ, a process known as macronization. Inspired by the Latin macronizer of \textcite{wingeAutomaticAnnotationLatin2015}, this thesis shows how the vowel lengths of Ancient Greek tokens can be programmatically compiled into a dictionary using digital grammars, lexica and other sources, a first step towards a macronizer for Ancient Greek. Given three hundred thousand morphologically tagged tokens from all the extant Ancient Greek tragedies, around forty-two thousand tokens containing the ambiguities in question are culled out. Vowel length data from sources including two dictionaries and an online repository of scanned verse are crawled and carefully collated, disambiguating roughly four tenths of the tragic corpus. Finally, a number of ways in which the percentage of macronized dichrona can be increased algorithmically are presented, with three of them solely ``shuffling around'' the data already contained in the sourced dictionary, and two requiring formalization of morphological rules, such as those governing prefixes and the endings of nominal forms.

## Dependencies 

    Python:

        pip3 install requests
        pip3 install tqdm
        pip3 install bs4
        pip3 install greek_accentuation
        pip3 install numpy
        pip3 install scipy
        pip3 install pyuca
        pip3 install beautifulsoup

    Ruby:
        gem install parallel
        tinycus and genos need to be cloned from Bitbucket into the ifthimos folder

## Explanation of tags

Taggen i raden
    `VERB	λάβηι	v3sasa---	λάβηι`
läses som 
    v = VERB
    3 = tredje person
    s = singular
    a = aorist
    s = subjunktiv
    a = aktivum

### POS tags (source: https://github.com/cltk/greek_treebank_perseus)

        1: 	part of speech
        
            n	noun
            v	verb
            t	participle
            a	adjective
            d	adverb
            l	article
            g	particle
            c	conjunction
            r	preposition
            p	pronoun
            m	numeral
            i	interjection
            e	exclamation
            u	punctuation
        
        2: 	person
        
            1	first person
            2	second person
            3	third person
        
        3: 	number
        
            s	singular
            p	plural
            d	dual
        
        4: 	tense
        
            p	present
            i	imperfect
            r	perfect
            l	pluperfect
            t	future perfect
            f	future
            a	aorist
        
        5: 	mood
        
            i	indicative
            s	subjunctive
            o	optative
            n	infinitive
            m	imperative
            p	participle
        
        6: 	voice
        
            a	active
            p	passive
            m	middle
            e	medio-passive
        
        7:	gender
        
            m	masculine
            f	feminine
            n	neuter
        
        8: 	case
        
            n	nominative
            g	genitive
            d	dative
            a	accusative
            v	vocative
            l	locative
        
        9: 	degree
        
            c	comparative
            s	superlative
