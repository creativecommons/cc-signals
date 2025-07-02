# cc-signals


## Welcome!

This Creative Commons (CC) repository contains a draft proposal for CC signals. CC signals is a framework for a simple pact between those stewarding data, and those reusing it for AI development. CC signals provide a set of shared ground rules for an AI ecosystem that is mutually beneficial. They are currently intended for use by those stewarding collections of content and other assets used as data for AI development.


### 🚀 Start here

1. Read through the [CC signals documentation](https://creativecommons.org/ai-and-the-commons/cc-signals/) on the CC website. For a comprehensive overview of the current legal, technical, and social context in which CC signals must operate, and rationale behind design decisions, read our [report](http://bit.ly/3G40J1j).
2. Review the elements of the CC signals draft proposal below.


### How to provide feedback

1. Head over to [Discussions][discussions] to provide direct feedback on our prepopulated questions and to start new discussion threads with the CC team and broader community.
2. Use [Issues][issues] to submit concrete suggestions or edits to CC signals structure, language, or implementation details. Please check closed issues before opening a new one.

[discussions]: https://github.com/creativecommons/cc-signals/discussions
[issues]: https://github.com/creativecommons/cc-signals/issues


### Note for those new to GitHub

The GitHub web interface offers many capabilities and can, accordingly, feel overwhelming. Thankfully, GitHub offers good documentation:
- [GitHub Docs](https://docs.github.com/en)
  - [Creating an account on GitHub - GitHub Docs](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github)
  - [Participating in a discussion - GitHub Docs](https://docs.github.com/en/discussions/collaborating-with-your-community-using-discussions/participating-in-a-discussion)


## CC signals framework

Using CC signals, a steward of a large collection of content can express a set of criteria that AI developers must meet. The criteria are organized around different dimensions of reciprocity, and are intended to drive meaningful, practical action. CC signals are designed to be interpretable by machines, as well as humans. To accomplish this, they build on [developing standards for expressing AI usage preferences][draft-vocab]. Those standards will include options for fully opting out, so no CC signal is needed to do so. CC signals are intended for use cases where someone wants to allow reuse, but with terms attached.

[draft-vocab]: https://ietf-wg-aipref.github.io/drafts/draft-ietf-aipref-vocab.html


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

A **Declaring Party** is someone who specifies how a content collection should be used by machines. Sometimes, the Declaring Party will hold copyright or have authority to represent rightsholders in the content. In these cases, a CC signal may have legal effect depending on the particular jurisdictions. In cases where a collection of content includes content from multiple authors, it will be the responsibility of the Declaring Party to coordinate among its community to determine the appropriate signal(s).


### The scope of machine uses addressed by the signal

The Declaring Party applies CC signals to a set of standard categories that encompass machine use, from general categories to more specific categories, such as Text and Data Mining, AI Training, Generative AI Training, and AI Inference. In order to maximize global interoperability, these categories will not be defined by Creative Commons. Instead, they will be based upon global standards being developed by the Internet Engineering Task Force (IETF). The CC signals framework is designed to evolve as the standard categories are finalized. The selected category makes up the scope of what activity the tool is intended to address.


### What signal is applied

The Declaring Party selects among the available CC signals. Once selected, that signal reflects the Declaring Party’s preferences regarding machine reuse. This means that the Declaring Party says that the selected category of machine reuse is granted under the terms of the particular signal elements.

Similar to the CC licenses, CC signals will be both machine- and human-readable. The human-readable explanation of what happens when a signal is applied will be called a **declaration**. The string of code used to apply a CC signal to a dataset will be called a **content usage expression**.

A declaration will lay out the full picture of the CC signal application happening in human-readable form, including variation based on whether the Declaring Party has copyright authority.


### Legal Considerations

CC signals are designed as global tools, which means they operate across legal systems that work differently. In the context of machine reuse, copyright law is limited, uncertain, and inconsistent across jurisdictions. As a result, applying a CC signal is likely to have a different legal effect depending on who applies it and in what context.

Where copyright exists and is applicable, CC signals are intended to leverage the power of copyright without increasing its power.

This is not about creating new property rights; it is more like defining manners for machines.

For more detail, please see the [report](http://bit.ly/3G40J1j). Further research and analysis about the legal implications of CC signals will be a major focus of our efforts in the coming months.


### Declaration example

Since the scope and effect of a CC signal is dictated by factors outside of the CC signal itself, we plan to create a set of declarations that describe in human-readable terms what is happening when a CC signal is applied, with variation based on the category selected and the copyright status of the Declaring Party. Declarations could be purely an explanatory device for users, or they could create legal documents in some circumstances. This aspect of the implementation is not yet determined.


### Opting out

CC signals modify the IETF AI Preferences opt-out with an exception that encourages reciprocity. To simply opt out, you do not need CC signals. For more information see the IETF [AI Preferences (aipref)](https://datatracker.ietf.org/wg/aipref/about/) working group.


### Adhering to a CC signal


#### Credit

Attribution and provenance in the context of large AI models is complex, difficult, and rapidly evolving as technologies develop. However, this does not mean that the concept of credit should be seen as irrelevant or impossible in the context of AI. We seek to establish norms around what is possible, not letting the perfect be the enemy of the good. Like the attribution condition in the CC licenses, we imagine the credit signal element being enacted in any reasonable manner. We plan to develop guidance and best practices around credit in future stages of this work, drawing on the progress being made in this area by others in the field. For now, at a minimum, we expect this signal to require citation of the training dataset by the reuser. For techniques that enable models to retrieve information in response to queries, such as retrieval augmented generation (RAG), and other use cases where it is technically feasible to connect content with particular outputs, outputs must cite the collection as a source with a link.


#### Direct Contribution

This is not intended as a commercial transaction. It is designed to create a structure for financial or in-kind contribution to support the sustainability of the Declaring Party. The application of CC signals should not be seen as a business model, or even a way to reliably recoup costs. The contributions are intended to be proportionate, both to the particular type and scale of machine reuse, and to the financial means of the party undertaking it. As with credit, we plan to produce guidance and best practices for direct contribution as CC signals develop.


#### Ecosystem Contribution

This is designed to spur contributions that support the commons as a whole. While the initial phrasing is very open-ended, we hope and expect that norms, best practices, and even new, collective-minded structures could grow around this notion in different sectors and for different types of reuses. The aim is to encourage a practice of giving back, infusing a norm of reciprocity in ways that will help sustain the ecosystem for all.


#### Open

This signal element reflects the fact that making AI models open—by releasing model weights, code, or datasets for others to use and build on—is a form of reciprocity.  Given the progress made by others in the field to provide meaningful definitions of openness, our proposal for this signal is more specific about what is required to adhere to it.


#### Incentivizing Adherence by AI Developers

We recognize that CC signals will rely on willing participation by AI developers to adhere to it. There are many reasons to be cynical about adherence, particularly when it is not legally required, and there are and will always be bad actors. However, we see many reasons to believe that uptake is likely.
  For one thing, there is precedent. Although adherence hasn’t always been perfect, robots.txt functioned for many years as a way to encode normative expectations about—and help maintain the social contract for—machine reuse of content on the web. We also see the success of CC licensing as evidence that voluntary buy-in is possible. While CC licenses are built atop copyright law and therefore carry the weight of copyright infringement risk, in reality they work because people have chosen to adhere to them. Litigation involving enforcement of CC licenses is rare, and much of it involves litigants who are not operating in good faith. Instead, there are now tens of billions of CC-licensed works available in the commons because they are grounded in intuitive notions about what is fair and prosocial when it comes to sharing and reuse of knowledge.
  There are also clear reasons why rational actors should respect and adhere to preference signals. As we’ve written earlier in this report, data from across the public web is a key component in developing large AI models. If those developing AI do not respect the wishes of creators, they risk eliminating incentives for people to share and widely distribute their works. Over time, this will compromise the accuracy, safety and currency of the models and services they build. This will be particularly acute for small firms, startups, nonprofits, and academic researchers, who would not have the resources to instead rely on costly licensing deals.


## Overview of Technical Implementation

Our implementation proposal is focused on integration with existing but evolving web standards and protocols. The [Internet Engineering Task Force (IETF) AI Preferences Working Group](https://datatracker.ietf.org/wg/aipref/about/) is currently leading on work to ensure that any approaches used to declare preference signals are machine-readable and therefore effective at scale. We propose an extension of that work to incorporate CC signals. This means that a CC signal would be applied as part of the robots.txt and HTTP headers, building on standards work already underway. The string of code used to apply a CC signal is called the "content usage expression." The technical specification is below in Extending the Vocabulary for Expressing AI Usage Preferences.

The design choice to build upon existing work by the IETF affects more than just the mechanics of applying a CC signal. It also means that the scope of attachment of the CC signal is dictated by choices made as part of the content usage expression. For example, someone applying a CC signal (a "Declaring Party") selects the category of machine reuse -- such as Generative AI Training -- using the categories defined by the IETF standards. Once selected, that category of machine reuse is the scope of the CC signal attached by the Declaring Party.

From a legal perspective, the copyright status of the Declaring Party will change the effect of a CC signal. When the Declaring Party holds copyright authority over the assets to which they are applying a CC signal, the CC signal may have legal implications that vary depending on the jurisdiction.

We plan to create and release a set of "declarations" that explain the full picture of what is happening when a CC signal is applied, including how they interact with categories and copyright status. See more on that in the Declaration section below.


### Specification for extending the Vocabulary For Expressing AI Usage Preferences

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
2. Preference - `y`: grant or `n`: deny
3. CC signal - the particular CC signal designated


### Robots.txt example

The following `robots.txt` excerpt example grants permission to all paths for all user agents with a usage preference of no for AI training unless credit is provided per the CC signal.
```robots.txt
User-Agent: *
Content-Usage: ai=n;exceptions=cc-cr
Allow: /
```


### HTTP header example

The following HTTP Content-Usage header example grants permission to the URL with a usage preference of no for generative AI training unless credit and an ecosystem contribution is provided per the CC signal.
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


### License

[![CC BY 4.0 license button][cc-by-png]][cc-by]

[`LICENSE`](LICENSE): Licensed under a [Creative Commons Attribution 4.0
International License][cc-by].

[cc-by-png]: https://licensebuttons.net/l/by/4.0/88x31.png#floatleft "CC BY 4.0 license button"
[cc-by]: https://creativecommons.org/licenses/by/4.0/ "Creative Commons Attribution 4.0 International License"
