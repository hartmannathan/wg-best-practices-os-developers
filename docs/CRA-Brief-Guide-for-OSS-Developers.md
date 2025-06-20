# Cyber Resilience Act (CRA) Brief Guide for Open Source Software (OSS) Developers

The European Union (EU) Cyber Resilience Act (CRA) is a law that applies to software, hardware, products containing them, and their backend services, *if* they are [made available](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#art_1) on the European market. The law applies *regardless* of where its developer(s) are located. This is a brief guide about basics of the CRA's applicability for those who develop open source software (OSS).

Note that *this guide is not legal advice*, it’s just an overview to help you understand a few key CRA concepts. If you are looking for advice on your specific situation, please consult your own legal counsel or other detailed CRA guidance.

## The short version: CRA often does not apply to individual open source contributors

In short, if you are contributing to others’ Open Source Software (OSS) projects, or just publish your OSS code in your own repository and you are not trying to monetize it, you do not have to *worry* about the CRA at all. As soon as you try to monetize the software as a product (such as by trying to commercially profit from the sale or support of the software product), things change.

## The slightly longer version: Don’t panic

The [European Union (EU) Cyber Resilience Act (CRA)](https://eur-lex.europa.eu/eli/reg/2024/2847/oj) is a law that applies to “products with digital elements” (PDEs) made available to the [European single market](https://european-union.europa.eu/priorities-and-actions/actions-topic/single-market_en). A PDE is [defined](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#art_3) as a “software or hardware product and its remote data processing solutions, including software or hardware components being placed on the market separately.” In many cases software is a PDE. The CRA also covers the backend services to the products (these are called [“remote data processing” solutions](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#rct_11)).

You may have heard things about the CRA (especially its early drafts) that made you worried. The published law is what matters, and for typical individual OSS contributors, there’s no need to panic:

1. *The CRA [does not apply to any contributors to someone else’s OSS project](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#rct_18)*.
2. *The CRA does not apply to web sites or web services unless they are [part of the remote data processing of a product put on the market](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#art_3)*.
3. *The CRA only applies to software if it’s “[supplied for distribution or use in the course of a commercial activity](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#rct_15)”*. If the OSS isn’t part of a commercial activity as defined by the CRA, then the CRA does not apply.

Many typical activities of OSS projects [aren’t considered a commercial activity under the CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#rct_18). Examples of such typical activities are: receiving financial support from manufacturers (without a profit), manufacturers contributing to its development, performing regular releases, being hosted on an open repository, accepting donations without the intention of making a profit, and being supported by a not-for-profit organization. We strongly encourage all OSS projects to [develop secure software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software), and the CRA can be a useful guide even when CRA compliance is not required. Yet complying with the CRA isn’t required by activities like these.

### CRA applies when open source is distributed as part of commercial activity

If software or any other product with digital elements (PDE) is [put on the market in the course of a commercial activity, the CRA *does* apply](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#rct_15). Generally “commercial activity” means some attempt to monetize it. [Commercial activities under the CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#rct_15) include:

1. Charging a fee for a PDE,
2. Charging for technical support services beyond their actual costs,
3. An intent to monetize it, for example, by providing a software platform through which the manufacturer monetizes other services,
4. Requiring personal data for reasons other than for very narrow reasons (improving the security, compatibility, or interoperability of the software)
5. Accepting donations exceeding costs.

If you’re putting a PDE on the market in the course of a commercial activity, then you’re considered a [manufacturer](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#art_3) and the CRA applies. This is true even if the PDE is open source software. That’s not a disaster. The CRA has a set of requirements that take work to achieve, but the requirements are intended to be *achievable*.

### If your Open Source Software (OSS) is used by a manufacturer

Manufacturers may integrate OSS components into their product that is put on the market. The CRA ***does*** apply to manufacturers, because they are putting PDEs on the market with commercial intent. The manufacturer is responsible for all parts of the product, including components from third parties. The manufacturer must [perform “due diligence”](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#art_13) to determine what components to use, and must also [report component vulnerabilities](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#art_13) to the component maintainer and upstream fixes if they have any. Using an OSS component in a product makes the manufacturer responsible for its use. As a result, it’s expected that some OSS will be more thoroughly assessed, and it’s likely that there will be a preference for more secure OSS. Manufacturers may sometimes [change how they interact with non-commercial OSS](https://eviltux.com/2025/04/25/what-open-source-developers-need-to-know-about-the-eu-cyber-resilience-act-cra/) due to the CRA. So even developers not directly subject to the CRA should learn more about the CRA and work to create more secure software.  These manufacturer requirements may generate more interest in your software and your practices, which may spawn requests to the project for documentation, patches, or other artifacts such as a Software Bill of Materials (SBOM).

### Some organizations are OSS Stewards

Organizations that [systematically provide sustained support for developing OSS intended for commercial activities](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#art_3), but don’t fill another role like “manufacturer”, may be considered “Open Source Software Stewards” under the CRA. It's known that an organization can be a steward for one program and also a manufacturer for a different program ([Benjamin Bögel, FOSDEM 2024, time 18:10](https://fosdem.org/2024/schedule/event/fosdem-2024-3683-the-regulators-are-coming-one-year-on/)). Stewards have fewer obligations than manufacturers, but they have a few [obligations](https://eur-lex.europa.eu/eli/reg/2024/2847/oj#art_24) such as providing a coordinated vulnerability disclosure (CVD) policy, cooperating with market surveillance at their request, providing certain kinds of documentation, reporting known actively exploited vulnerabilities, notifying about severe incidents, informing impacted users, and providing mitigation. There is no requirement for an OSS project to have a steward. However, an OSS project may *choose* to be supported by a steward (who must then meet its obligations).

### CE marking compliance with the EU product legislation

The CRA is part of a broader set of product legislation that applies to many kinds of products traded in the European Economic Area (EEA). These products must meet certain criteria, and a manufacturer has to apply CE marking confirming this, before they are allowed to be put on the market. CE stands for the French expression "Conformité Européenne," and translates to “European Conformity”. The CRA is basically “CE marking for software” because it adds CE marking requirements for products with digital elements (including many cases of standalone software). The [*Blue Guide*](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A52022XC0629%2804%29&qid=1736866478765) explains how EU product legislation works more generally. At the time of this writing, the *Blue Guide* has not been updated to reflect the CRA. Nevertheless, reading the *Blue Guide* can help you better understand the CRA and how it fits into European legislation. CE Marking is for commercial products.

### Learn more with free classes and in our work groups

To learn more, we encourage you to take the free express course [“Understanding the EU Cyber Resilience Act (CRA) (LFEL1001)”](https://training.linuxfoundation.org/express-learning/understanding-the-eu-cyber-resilience-act-cra-lfel1001/); you can earn a digital badge by completing it. You can also see the [OpenSSF EU Cyber Resilience Act (CRA) related resources](https://openssf.org/public-policy/eu-cyber-resilience-act/). Most developers want the software they create to be secure; to learn how, we encourage you to take our free course “[Developing Secure Software (LFD121)](https://training.linuxfoundation.org/training/developing-secure-software-lfd121/)”. The [Open Source Security Foundation (OpenSSF)](http://OpenSSF.org) has multiple working groups where you can discuss issues with peers. You can also gain knowledge, tools, documentation, and training to assist in making OSS more secure.

*This guide was developed by the [OpenSSF](https://openssf.org/) [Global Cyber Policy Working Group (WG)](https://github.com/ossf/wg-globalcyberpolicy) CRA Readiness+Awareness Special Interest Group (SIG) and the OpenSSF [Best Practices WG](https://github.com/ossf/wg-best-practices-os-developers). David A. Wheeler led its development. Contributors include (sorted by last name): Harald Fischer, Christian “fukami” Horchert, Olle E. Johansson, Goetz Martinek, Christopher “CRob” Robinson, David A. Wheeler, Steve Winslow, and Roman Zhukov. We thank the many contributors\!*
