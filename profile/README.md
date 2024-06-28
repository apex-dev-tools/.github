# Apex Dev Tools

This organization contains libraries that are used to build Salesforce Apex tools. The libraries are maintained by Certinia (formerly FinancialForce) and produced primarily for use in Certinia's internal developer tooling, but they are also being used in other projects such as [PMD](https://github.com/pmd), [dx@scale](https://github.com/dxatscale) and [Apex Assist](https://github.com/nawforce/apex-assist).

By making Certinia tooling libraries open source and bringing all of these repos together in a single GitHub organisation we hope to encourage wider involvement in their development, foster a coherent approach and ultimately bring useful productivity tools to the Salesforce developer community.

---

Quick Links: [Open PRs](https://github.com/pulls?q=is%3Aopen+is%3Apr+archived%3Afalse+user%3Aapex-dev-tools) • [Open Bugs](https://github.com/issues?q=is%3Aopen+is%3Aissue+archived%3Afalse+user%3Aapex-dev-tools+label%3Abug)

---

## Repos Overview

The diagram below shows the structure in which the repos are used to create Apex tools.

![RepoOverview](https://github.com/apex-dev-tools/.github/blob/main/res/overview.png)

## Project Background

These libraries have come from a number of different sources, some of which were internal to Certinia and others were originated by individuals. Taken together they provide a facility to syntactically and semantically check the Apex code in packaged and unmanaged projects, without the need to deploy those projects to a Salesforce org. The validations are very much centred on Apex, but some errors in other types of metadata are also detected. The libraries also provide wider DX features, such as code completion support for IDEs and reliable parallel test running.

Early work on providing this type of capability from within a VSCode extension was undertaken by Certinia in 2018, based on the [@nawforce](#nawforce) apex-link github project. This resulted in considerable progress towards the goal but loading performance and correctness remained challenging in some areas.

Starting in 2019 apex-link was re-architected to support an exact validation model via simulating the internal parts of an org that impact Apex correctness such as modelling the Schema for SObjects. A caching model was later added to address loading performance concerns. Additional feature have been added over time, such as the ability to download metadata from an org.

This 2nd generation apex-link (now known as apex-ls) has became the core supporting library for Apex related DX tools at Certinia, and is the foundation for tools that have in use by the majority of Certinia developers since 2021.

### @nawforce

[@nawforce](https://github.com/nawforce/) is the personal GitHub account of Kevin Jones. Kevin is currently Director, Technical Architecture at Certinia - providing architectural leadership and with particular interests in developer tooling and product performance and scalability.
