---
title: Open Science
teaching: 5
exercises: 5
---

::::::::::::::::::::::::::::::::::::::: objectives

- Explain how a version control system can be leveraged as an electronic lab notebook for computational work.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- How can version control help me make my work more open?

::::::::::::::::::::::::::::::::::::::::::::::::::

> The opposite of "open" isn't "closed".
> The opposite of "open" is "broken".
>
> - John Wilbanks

Free sharing of information might be the ideal in science,
but the reality is often more complicated.
Normal practice today looks something like this:

- A scientist collects some data and stores it on a machine
  that is occasionally backed up by their department.
- They then write or modify a few small programs
  (which also reside on the machine)
  to analyze that data.
- Once they have some results,
  they write them up and submit a paper.
  The scientist might include their data (a growing number of journals require this), but
  they probably don't include the code.
- Time passes.
- The journal sends the scientist reviews written anonymously by a handful of other people in their field.
  The scientist revises the paper to satisfy the reviewers,
  during which time they might also modify the scripts they wrote earlier,
  and resubmits.
- More time passes.
- The paper is eventually published.
  It might include a link to an online copy of the data,
  but the paper itself will be behind a paywall:
  only people who have personal or institutional access
  will be able to read it.

For a growing number of scientists,
though,
the process looks like this:

- The data that the scientist collects is stored in an open access repository
  like [figshare](https://figshare.com/) or
  [Zenodo](https://zenodo.org), possibly as soon as it's collected,
  and given its own
  [Digital Object Identifier](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI).
  Or the data was already published and is stored in
  [Dryad](https://datadryad.org/).
- The scientist creates a new repository on GitHub to hold their work.
- During analysis,
  they push changes to their scripts
  (and possibly some output files)
  to that repository.
  The scientist also uses the repository for their paper;
  that repository is then the hub for collaboration with colleagues.
- When they are happy with the state of the paper,
  the scientist posts a version to [arXiv](https://arxiv.org/)
  or some other preprint server
  to invite feedback from peers.
- Based on that feedback,
  they may post several revisions
  before finally submitting the paper to a journal.
- The published paper includes links to the preprint
  and to the code and data repositories,
  which makes it much easier for other scientists
  to use their work as starting point for their own research.

This open model accelerates discovery:
the more open work is,
[the more widely it is cited and re-used](https://doi.org/10.1371/journal.pone.0000308).
However,
people who want to work this way need to make some decisions
about what exactly "open" means and how to do it. You can find more on the different aspects of Open Science in [this book](https://link.springer.com/book/10.1007/978-3-319-00026-8).

This is one of the (many) reasons we teach version control.
When used diligently,
it answers the "how" question
by acting as a shareable electronic lab notebook for computational work:

- The conceptual stages of your work are documented, including who did
  what and when. Every step is stamped with an identifier (the commit ID)
  that is for most intents and purposes unique.
- You can tie documentation of rationale, ideas, and other
  intellectual work directly to the changes that spring from them.
- You can refer to what you used in your research to obtain your
  computational results in a way that is unique and recoverable.
- With a version control system such as Git,
  the entire history of the repository is easy to archive for perpetuity.

:::::::::::::::::::::::::::::::::::::::::  callout

## Making Code Citable

Anything that is hosted in a version control repository (data, code, papers,
etc.) can be turned into a citable object. You'll learn how to do this in
[the later episode on Citation](12-citation.md).


::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## How Reproducible Is My Work?

Ask one of your labmates to reproduce a result you recently obtained
using only what they can find in your papers or on the web.
Try to do the same for one of their results,
then try to do it for a result from a lab you work with.

:::::::::::::::  solution

## Solution

Most teams discover that "fully reproducible" is harder than they expected. Common gaps include: data files stored only on a personal laptop or in lab Slack/Email; analysis scripts that are not under version control; software dependencies that have not been pinned to specific versions; and figures generated by clicking through a GUI rather than by a script.

A pragmatic remediation plan, building on what you have just learned about Git, is:

1. Move data and code into a Git repository (with a `data/` folder for raw inputs and a `scripts/` folder for analysis code).
2. Tag the commit that produced the published figure (`git tag v1.0-paper`) so reviewers can check out exactly that state.
3. Record the software environment alongside the code (an `environment.yml`, `requirements.txt`, `renv.lock`, or container recipe).
4. Push to a public host (GitHub, GitLab, or Pomona's institutional GitHub) and archive a release on Zenodo so the work has a citable DOI.

The exercise's real value is the conversation: it usually surfaces several "I forgot I did that step manually" moments that are best fixed *before* the next paper goes out the door.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## How to Find an Appropriate Data Repository?

Surf the internet for a couple of minutes and check out the data repositories
mentioned above: [Figshare](https://figshare.com/), [Zenodo](https://zenodo.org),
[Dryad](https://datadryad.org/). Depending on your field of research, you might
find community-recognized repositories that are well-known in your field.
You might also find useful [these data repositories recommended by Nature](https://www.nature.com/sdata/data-policies/repositories).
Discuss with your neighbor which data repository you might want to
approach for your current project and explain why.

:::::::::::::::  solution

## Solution

There is rarely a single right answer; the best repository depends on the *type* of data, the *audience*, and any *funder or journal mandates* you are subject to. A useful decision-checklist:

- **Is there a community-standard repository for my data type?** Genomics work usually goes to NCBI/SRA or EBI/ENA; protein structures to the PDB; ecology and earth observations to DataONE/EDI; astronomy to the relevant survey archive. Field-specific repositories typically come with metadata schemas reviewers expect to see.
- **Do I need a citable DOI?** Both Zenodo and Figshare mint DOIs immediately and accept any data type. Zenodo is usually the easiest pairing with a GitHub release.
- **Is the dataset large or restricted?** Dryad accepts up to 300 GB and is often paired with journals. For sensitive Pomona data (FERPA, PHI, export-controlled), a public repository is *not* appropriate; talk to its-hpc@pomona.edu about controlled-access options.
- **Does my funder require a specific repository?** NIH-funded work increasingly requires a designated data repository; NSF awards expect a Data Management Plan.

For a typical Pomona research project that just needs a citable record of code plus a small dataset, "GitHub repo + Zenodo release for archival DOI" is a low-effort, fully-citable default.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## How to Track Large Data or Image Files using Git?

Large data or image files such as `.md5` or `.psd` file types can be tracked within
a github repository using the [Git Large File Storage](https://git-lfs.github.com)
open source extension tool.  This tool automatically uploads large file contents to
a remote server and replaces the file with a text pointer within the github repository.

Try downloading and installing the Git Large File Storage extension tool, then add
tracking of a large file to your github repository.  Ask a colleague to clone your
repository and describe what they see when they access that large file.  

:::::::::::::::  solution

## Solution

After installing Git LFS (`git lfs install`) and telling Git which paths to track (e.g., `git lfs track "*.psd"`), Git LFS rewrites those large files in the working tree as small text *pointer files* (a few hundred bytes containing a SHA-256 hash and the file size). The actual binary content is uploaded to the LFS server.

When a colleague runs `git clone`, they pull the lightweight repository as usual; the pointer files are populated on demand by `git lfs pull`. They will see normal-looking filenames in the working tree, but if LFS is not installed locally they will see the pointer-file *contents* (the SHA-256 stub) instead of the binary asset.

Two things to watch for at Pomona:

1. **Storage quota** — GitHub's free LFS quota is 1 GB storage and 1 GB/month bandwidth per account. For larger genomics or imaging datasets, prefer Sagehen HPC storage (`/bigdata/lab/<labname>`) plus a small GitHub repo with code and metadata.
2. **Sensitive data** — never push restricted data to a public LFS-backed repository. The encryption pattern from the Sagehen Security Awareness modules (gocryptfs on `/bigdata`) is the right tool for those files.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: keypoints

- Open scientific work is more useful and more highly cited than closed.

::::::::::::::::::::::::::::::::::::::::::::::::::

<!-- highlight <labname>/<myusername> placeholders in code blocks; remove if the varnish theme handles this natively -->
<script>(function(){var CSS='.sh-placeholder{color:#c2410c;font-weight:700}[data-bs-theme="dark"] .sh-placeholder,html.dark .sh-placeholder{color:#fdba74}@media (prefers-color-scheme: dark){[data-bs-theme="auto"] .sh-placeholder{color:#fdba74}}';var RX=/<labname>|<myusername>/g;function firstMatch(el){var w=document.createTreeWalker(el,NodeFilter.SHOW_TEXT,null),nodes=[],full='';while(w.nextNode()){nodes.push({n:w.currentNode,s:full.length});full+=w.currentNode.nodeValue;}RX.lastIndex=0;var m;while((m=RX.exec(full))){var s=m.index,e=s+m[0].length,inSpan=false,parts=[];for(var j=0;j<nodes.length;j++){var ns=nodes[j].s,ne=ns+nodes[j].n.nodeValue.length;if(ne<=s||ns>=e)continue;parts.push({node:nodes[j].n,a:Math.max(s-ns,0),b:Math.min(e-ns,nodes[j].n.nodeValue.length)});var p=nodes[j].n.parentNode;while(p&&p!==el){if(p.classList&&p.classList.contains('sh-placeholder')){inSpan=true;break;}p=p.parentNode;}}if(!inSpan&&parts.length)return parts;}return null;}function wrapParts(parts){for(var i=parts.length-1;i>=0;i--){var t=parts[i].node,txt=t.nodeValue,a=parts[i].a,b=parts[i].b;var span=document.createElement('span');span.className='sh-placeholder';span.textContent=txt.slice(a,b);var f=document.createDocumentFragment();if(a>0)f.appendChild(document.createTextNode(txt.slice(0,a)));f.appendChild(span);if(b<txt.length)f.appendChild(document.createTextNode(txt.slice(b)));t.parentNode.replaceChild(f,t);}}function run(){var st=document.createElement('style');st.textContent=CSS;document.head.appendChild(st);document.querySelectorAll('pre,code').forEach(function(el){var guard=0,parts;while((parts=firstMatch(el))&&guard++<500){wrapParts(parts);}});}if(document.readyState==='loading'){document.addEventListener('DOMContentLoaded',run);}else{run();}})();</script>
