---
permalink: index.html
site: sandpaper::sandpaper_site
---

::::::::::::::::::::::::::::::::::::: callout

## Pomona College HPC Workshop Series

This workshop is part of the **Pomona College Research Computing Workshop
Series**, adapted from [Version Control with Git](https://swcarpentry.github.io/git-novice/)
by [Software Carpentry](https://software-carpentry.org/).
- **Cluster:** sagehen.hpc.pomona.edu
- **Web Portal:** [OnDemand](https://ondemand.hpc.pomona.edu/)
- **Support:** its-hpc@pomona.edu

Version control is essential for reproducible research on HPC systems.
All examples can be practiced on the Sagehen cluster.

*Adapted for Pomona College by Andrew Wilson, ITS Research Computing.
Licensed under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).*

::::::::::::::::::::::::::::::::::::::::::::::::

Cecil and Frary have been hired by Sagehen Space Lab (a research
group at Pomona College) to investigate if it
is possible to send their next planetary lander to Mars.  They want to
be able to work on the plans at the same time, but they have run into
problems doing this in the past.  If they take turns, each one will
spend a lot of time waiting for the other to finish, but if they work
on their own copies and email changes back and forth things will be
lost, overwritten, or duplicated.

A colleague suggests using [version control](learners/reference.md#version-control) to
manage their work. Version control is better than mailing files back and forth:

- Nothing that is committed to version control is ever lost, unless
  you work really, really hard at it. Since all old versions of
  files are saved, it's always possible to go back in time to see
  exactly who wrote what on a particular day, or what version of a
  program was used to generate a particular set of results.

- As we have this record of who made what changes when, we know who to ask
  if we have questions later on, and, if needed, revert to a previous
  version, much like the "undo" feature in an editor.

- When several people collaborate in the same project, it's possible to
  accidentally overlook or overwrite someone's changes. The version control
  system automatically notifies users whenever there's a conflict between one
  person's work and another's.

Teams are not the only ones to benefit from version control: lone
researchers can benefit immensely.  Keeping a record of what was
changed, when, and why is extremely useful for all researchers if they
ever need to come back to the project later on (e.g., a year later,
when memory has faded).

Version control is the lab notebook of the digital world: it's what
professionals use to keep track of what they've done and to
collaborate with other people.  Every large software development
project relies on it, and most programmers use it for their small jobs
as well.  And it isn't just for software: books,
papers, small data sets, and anything that changes over time or needs
to be shared can and should be stored in a version control system.

::::::::::::::::::::::::::::::::::::::::::  prereq

## Prerequisites

In this lesson we use Git from the Unix Shell.
Some previous experience with the shell is expected,
*but isn't mandatory*.


::::::::::::::::::::::::::::::::::::::::::::::::::


