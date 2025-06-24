# cc-signals


## Welcome!

This Creative Commons (CC) repository contains a draft proposal for CC signals. CC signals is a framework for a simple pact between those stewarding data, and those reusing it for AI development. CC signals provide a set of shared ground rules for an AI ecosystem that is mutually beneficial. They are currently designed to be applied at the dataset level, intended for use by those stewarding collections of content and other assets used as data for AI development.


### 🚀 Start here

1. Read through the CC signals documentation on the CC website. For a comprehensive overview of the current legal, technical, and social context in which CC signals must operate, and rationale behind design decisions, read our report **`LINK NEEDED`**.  
2. Review the elements of the CC signals draft proposal below. 


### How to provide feedback

1. Head over to  [Discussions][discussions] to provide direct feedback on our prepopulated questions and to start new discussion threads with the CC team and broader community. 
2. Use Issues **`LINK NEEDED`** to submit concrete suggestions or edits to  CC signals structure, language, or implementation details. Please check closed issues before opening a new one.

[discussions]: https://github.com/creativecommons/cc-signals-test/discussions


### Note for those new to GitHub

The GitHub web interface offers many capabilities and can, accordingly, feel overwhelming. Thankfully, GitHub offers good documentation:
- [GitHub Docs](https://docs.github.com/en)
  - [Participating in a discussion - GitHub Docs](https://docs.github.com/en/discussions/collaborating-with-your-community-using-discussions/participating-in-a-discussion)


## CC signals framework

Using CC signals, a steward of a large collection of content can express a set of criteria that AI developers must meet. CC signals are designed as global tools, which means they operate across legal systems that work differently. As a result, applying a CC signal is likely to have a different legal effect depending on who applies it and in what context. The CC signals are intended to sit neatly within copyright in a way that leverages the power of copyright where it exists and is applicable, without increasing the power of copyright. 


## CC signals

In this initial proposal, we have drafted four “signal elements” for public feedback. For this phase of prototyping, we have proposed four particular combinations of signal elements that would serve as the suite of CC signals. The four proposed signals are:
  - Credit
  - Credit + Direct Contribution
  - Credit + Ecosystem Contribution
  - Credit + Open 

The files with the initial proposed text for each signal are:

| Name | Directory |
| ---- | --------- |
| [CC Credit 0.1][cr] | [`signals/cr/0.1/`][cr] |
| [CC Credit Direct Contribution 0.1][cr-dc] | [`signals/cr-dc/0.1/`][cr-dc] |
| [CC Credit Ecosystem 0.1][cr-ec] | [`signals/cr-ec/0.1/`][cr-ec] |
| [CC Credit Open 0.1][cr-op] | [`signals/cr-op/0.1/`][cr-op] |


[cr]: signals/cr/0.1/
[cr-dc]: signals/cr-dc/0.1/
[cr-ec]: signals/cr-ec/0.1/
[cr-op]: signals/cr-op/0.1/



## How CC signals work


### Who is applying the signal

A **Declaring Party** is someone who has both the ethical and legal authority to specify how a content collection should be used by machines. Sometimes, the Declaring Party will hold copyright or have authority to represent rightsholders in the content. In these cases, a CC signal may have legal effect depending on the particular jurisdiction. In cases where a collection of content includes works from multiple authors, it is be the responsibility of the Declaring Party to coordinate among its community to determine the appropriate signal(s).


### The scope of machine uses addressed by the signal

The Declaring Party applies CC signals to a set of standard categories that encompass machine use, from general categories to more specific categories, such as Text and Data Mining, AI Training, Generative AI Training, and AI Inference. In order to maximize global interoperability, these categories will not be defined by Creative Commons. Instead, they will be based upon global standards being developed by the Internet Engineering Task Force (IETF). The CC signals framework is designed to evolve as the standard categories are finalized. The selected category makes up the scope of what activity the tool is intended to permit.


### What signal is applied

The Declaring Party selects among the available CC signals. Once selected, that signal reflects the Declaring Party’s preferences regarding machine reuse. This means that the Declaring Party says that the selected category of machine reuse is allowed under the terms of the particular signal elements. 

Similar to the CC licenses, CC signals will be both machine- and human-readable. The human-readable explanation of what happens when a signal is applied will be called a **declaration**. The string of code used to apply a CC signal to a dataset will be called a **content usage expression**. 

A declaration will lay out the full picture of the CC signal application happening in human-readable form, including variation based on whether the Declaring Party has copyright authority. 


### Legal Considerations

CC signals are designed as global tools, which means they operate across legal systems that work differently. As a result, applying a CC signal is likely to have a different legal effect depending on who applies it and in what context.

_When the Declaring Party has copyright authority_, a CC signal may be legally enforceable depending on the jurisdiction. 

In the context of machine reuse, copyright law is limited, uncertain, and inconsistent across jurisdictions. The CC signals are intended to sit neatly within copyright in a way that leverages the power of copyright where it exists and is applicable, without _increasing_ the power of copyright.  

### Adhering to a CC signal 

**Credit:** 
Attribution and provenance in the AI context is both complex and rapidly changing as technologies develop. To account for this, like the attribution requirement in the CC licenses, we imagine this signal requiring credit in any reasonable manner. As a subsequent phase of CC’s preference signals framework, we will develop a set of best practices for credit. For now, at a minimum, we expect this signal requires citation of the training dataset by the reuser. For retrieval augmented generation (RAG) and other use cases where it is technically feasible to connect the data with particular outputs, outputs must cite the collection as a source with a link.

**Direct & Ecosystem Contribution:** 
The contribution signals are not intended to spur a commercial transaction. They are designed to create a structure for financial or non-monetary contributions to support the sustainability of the declaring party or the ecosystem in which the declaring party is situated.  The application of CC signals should not be seen as a business model, or even a way to reliably recoup costs. The contributions are intended to be proportionate, both to the particular type and scale of machine reuse, and to the financial means of the party undertaking it.

At a later stage, CC will develop best practices for valuation and ecosystem contribution available on CC’s site. 

**Open:** 
This signal element reflects the fact that making AI models openly available for others to use and build on is a form of reciprocity. Given the work done by others in the field, our proposal for this signal is more specific about what is required to adhere to it. Prospective users of content made available with this signal must satisfy the Model Openness Framework (MOF) Class II, MOF Class I, or the Open Source AI Definition (OSAID).

At a later stage of development, we can be more specific about what it means to adhere to the open signal. 

## Overview of Technical Implementation

Our implementation proposal is focused on integration with existing but evolving web standards and protocols. The [Internet Engineering Task Force (IETF) AI Preferences Working Group](https://datatracker.ietf.org/wg/aipref/about/) is currently leading on work to ensure that any approaches used to declare preference signals are machine-readable and therefore effective at scale. We propose an extension of that work to incorporate CC signals. This means that a CC signal would be applied as part of the robots.txt and HTTP headers, building on standards work already underway. The string of code used to apply a CC signal is called the "content usage expression." The technical specification is below in Extending the Vocabulary for Expressing AI Usage Preferences.

The design choice to build upon existing work by the IETF affects more than just the mechanics of applying a CC signal. It also means that the scope of attachment of the CC signal is dictated by choices made as part of the content usage expression. For example, someone applying a CC signal (a "Declaring Party") selects the category of machine reuse -- such as Generative AI Training -- using the categories defined by the IETF standards. Once selected, that category of machine reuse is the scope of the CC signal attached by the Declaring Party. 

From a legal perspective, the copyright status of the Declaring Party will change the effect of a CC signal. When the Declaring Party holds copyright authority over the assets to which they are applying a CC signal, the CC signal may have legal implications that vary depending on the jurisdiction. 

We plan to create and release a set of "declarations" that explain the full picture of what is happening when a CC signal is applied, including how they interact with categories and copyright status. See more on that in the Declaration section below.


## Declaration example

Since the scope and effect of a CC signal is dictated by factors outside of the CC signal itself, we plan to create a set of declarations that describe in human-readable terms what is happening when a CC signal is applied, with variation based on the category selected and the copyright status of the Declaring Party. Declarations could be purely an explanatory device for users, or they could create legal documents in some circumstances. This aspect of the implementation is not yet determined.


## Specification for Extending the Vocabulary For Expressing AI Usage Preferences

The CC signals extend the IETF draft [Vocabulary For Expressing AI Usage Preferences][draft-vocab]. It uses parameters (as defined by [RFC 9651: Structured Field Values for HTTP][rfc9651]). The IETF AI Preferences workgroup is initially defining two methods for attaching AI preferences to assets ([Indicating Preferences Regarding Content Usage][draft-attach]):
1. robots.txt ([RFC 9309: Robots Exclusion Protocol][rfc9309]) for location based preferences
2. HTTP Content-Usage header for unit based preferences

[draft-vocab]: https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/
[draft-attach]: https://datatracker.ietf.org/doc/draft-it-aipref-attachment/
[rfc9651]: https://www.rfc-editor.org/rfc/rfc9651.html
[rfc9309]: https://www.rfc-editor.org/rfc/rfc9309.html


### Implementation

AI usage preferences with CC signals is defined in a content usage expression with the value including three components:
```
ai=n;exceptions=cc-cr
▲  ▲            ▲
│  │            └ CC signal
│  └ Preference
└ Category
```
1. Category - the designated scope of machine reuse using defined categories
   - (see [A Vocabulary For Expressing AI Usage Preferences][draft-vocab] for a list of categories)
2. Preference - `y`: allow or `n`: disallow
3. CC signal - the particular CC signal designated


### Robots.txt example

The following `robots.txt` excerpt example allows access to all paths for all user agents with a usage preference of no for AI training unless credit is provided per the CC signal.
```robots.txt
User-Agent: *
Content-Usage: ai=n;exceptions=cc-cr
Allow: /
```

### HTTP header example

The following HTTP Content-Usage header example allows access to the URL with a usage preference of no for generative AI training unless credit and an ecosystem contribution is provided per the CC signal.
```HTTP
200 OK
Date: Mon, 09 Jun 2025 12:42:03 UTC
Content-Type: text/plain
Content-Usage: genai=n;exceptions=cc-cr-ec
```



## Copyright and trademarks used in this repository


### CC Badge, Icons, Images, and Logos

- The badges, icons, images, and logos contained within this repository are for use under the Creative Commons Trademark Policy (see [Policies - Creative Commons][ccpolicies]).
- **The icons, images, and logos are not licensed under a Creative Commons license** (also see [Could I use a CC license to share my logo or trademark? - Frequently Asked Questions - Creative Commons][tmfaq]).

[ccpolicies]: https://creativecommons.org/policies
[tmfaq]: https://creativecommons.org/faq/#could-i-use-a-cc-license-to-share-my-logo-or-trademark


### Dedicated to the public domain

![CC0 1.0 Universal license button][cc0-png]

[`LICENSE`](LICENSE): Excluding CC trademarks and to the extent possible under law, Creative Commons has waived all copyright and related or neighboring rights to this work ([CC0 1.0 Universal][cc0]).

[cc0-png]: https://licensebuttons.net/l/zero/1.0/88x31.png "CC0 1.0 Universal license button"
[cc0]: https://creativecommons.org/publicdomain/zero/1.0/ "Creative Commons — CC0 1.0 Universal"
