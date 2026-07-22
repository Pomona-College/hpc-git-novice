---
title: Licensing
teaching: 5
exercises: 0
---

::::::::::::::::::::::::::::::::::::::: objectives

- Explain why adding licensing information to a repository is important.
- Choose a proper license.
- Explain differences in licensing and social expectations.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What licensing information should I include with my work?

::::::::::::::::::::::::::::::::::::::::::::::::::

When a repository with source code, a manuscript or other creative
works becomes public, it should include a file `LICENSE` or
`LICENSE.txt` in the base directory of the repository that clearly
states under which license the content is being made available. This
is because creative works are automatically eligible for intellectual
property (and thus copyright) protection. Reusing creative works
without a license is dangerous, because the copyright holders could
sue you for copyright infringement.

:::::::::::::::::::::::::::::::::::::::  callout

## Choose Your License Early

Deciding on a license at the beginning of your project is crucial. If you wait until the project is done and then try to add a license, you'll need to get approval from every contributor. Many academic institutions have policies about open source licenses; check with your department before pushing code to GitHub.

:::::::::::::::::::::::::::::::::::::::::

A license solves this problem by granting rights to others (the
licensees) that they would otherwise not have. What rights are being
granted under which conditions differs, often only slightly, from one
license to another. In practice, a few licenses are by far the most
popular, and [choosealicense.com](https://choosealicense.com/) will
help you find a common license that suits your needs.  Important
considerations include:

- Whether you want to address patent rights.
- Whether you require people distributing derivative works to also
  distribute their source code.
- Whether the content you are licensing is source code.
- Whether you want to license the code at all.

Choosing a license that is in common use makes life easier for
contributors and users, because they are more likely to already be
familiar with the license and don't have to wade through a bunch of
jargon to decide if they're ok with it.  The [Open Source
Initiative](https://opensource.org/licenses) and [Free Software
Foundation](https://www.gnu.org/licenses/license-list.html) both
maintain lists of licenses which are good choices.

[This article][software-licensing] provides an excellent overview of
licensing and licensing options from the perspective of scientists who
also write code.

At the end of the day what matters is that there is a clear statement
as to what the license is. Also, the license is best chosen from the
get-go, even if for a repository that is not public. Pushing off the
decision only makes it more complicated later, because each time a new
collaborator starts contributing, they, too, hold copyright and will
thus need to be asked for approval once a license is chosen.

:::::::::::::::::::::::::::::::::::::::  challenge

## Can I Use Open License?

Find out whether you are allowed to apply an open license to your software.
Can you do this unilaterally,
or do you need permission from someone in your institution?
If so, who?

:::::::::::::::  solution

## Solution

The honest answer is: **it depends, and you should check before you push.** A few patterns to keep in mind:

- **Pomona College students and post-docs.** Code you write outside of grant-funded research is typically yours, but anything written using College resources or under a faculty member's grant may be jointly owned. Pomona ITS and the relevant department chair can advise; for grant-funded code, the faculty PI is usually the right first contact.
- **Faculty.** Most institutions distinguish between "scholarly works" (copyright stays with the author) and "sponsored works" (rights may be assigned to the institution or funder). Check Pomona's IP policy and any specific terms in the grant agreement.
- **Industry collaborations.** If a company has contributed funding or unpublished IP, an open license usually requires their written sign-off.

When in doubt, **email its-hpc@pomona.edu** to ask, and CC your PI or department chair. The cost of a one-paragraph email is much smaller than the cost of releasing code you weren't allowed to release.

For most pedagogical and small research-utility code, an MIT or BSD-2-Clause license cleared with your PI is a safe, low-friction default.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## What licenses have I already accepted?

Many of the software tools we use on a daily basis (including in this workshop) are
released as open-source software. Pick a project on GitHub from the list below, or
one of your own choosing. Find its license (usually in a file called `LICENSE` or
`COPYING`) and talk about how it restricts your use of the software. Is it one of
the licenses discussed in this session? How is it different?
- [Git](https://github.com/git/git), the source-code management tool
- [CPython](https://github.com/python/cpython), the standard implementation of the Python language
- [Jupyter](https://github.com/jupyter), the project behind the web-based Python notebooks we'll be using
- [EtherPad](https://github.com/ether/etherpad-lite), a real-time collaborative editor
  

:::::::::::::::  solution

## Solution

You will likely encounter a small set of licenses repeatedly:

- **Git** is licensed under **GPLv2**. GPL licenses are *copyleft*: if you redistribute software that links Git's source, your derivative must also be released under a compatible GPL license. For a researcher who simply *uses* Git as a tool, this has no practical effect on their own code.
- **CPython** uses the **PSF License** (a permissive, BSD-style license written specifically for Python). You can freely embed and redistribute the interpreter, including in commercial products.
- **Jupyter** is published under the **BSD-3-Clause** license, a short permissive license that requires attribution but otherwise places very few restrictions on reuse.
- **EtherPad-Lite** uses the **Apache-2.0** license, a permissive license that adds an explicit patent grant on top of an MIT/BSD-style core.

The biggest practical distinction is **permissive (MIT, BSD, Apache-2.0)** vs **copyleft (GPL, AGPL, LGPL)**. Permissive licenses let downstream users keep their derivative works closed; copyleft licenses require derivatives to also be open. For research code shared so others can read and reproduce it, a permissive license is usually appropriate. For tools whose social value depends on staying open (like Git), copyleft is intentional.

Compatibility matters too: code under GPL cannot generally be combined into a project distributed under a more permissive license, but the reverse is fine. If you intend to mix dependencies, sketch the license tree before you write the import statement.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

[software-licensing]: https://doi.org/10.1371/journal.pcbi.1002598


:::::::::::::::::::::::::::::::::::::::: keypoints

- The `LICENSE`, `LICENSE.md`, or `LICENSE.txt` file is often used in a repository to indicate how the contents of the repo may be used by others.
- People who incorporate General Public License (GPL'd) software into their own software must make their software also open under the GPL license; most other open licenses do not require this.
- The Creative Commons family of licenses allow people to mix and match requirements and restrictions on attribution, creation of derivative works, further sharing, and commercialization.
- People who are not lawyers should not try to write licenses from scratch.

::::::::::::::::::::::::::::::::::::::::::::::::::


