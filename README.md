# DawnBSD source repository

See the other included guide files for additional information.

### What is DawnBSD?  
DawnBSD is an operating system focused on designed simplicity, using strict
adherence to the POSIX and C standards as its focus. Features, including from
the kernel level to the base system software level, should be regulated on an
as-needed basis. Extraneous software should be downloaded via the ports tree.

### Design Goals

DawnBSD aims to provide a base system which is minimal, standards-oriented, and
highly documented. Components of this system should be written in clean, generic
C code. Documentation, including comments and file documentation, should be used
generously and skillfully. The POSIX standard should be followed even in cases
where its use is vague or obtuse.

### Who is DawnBSD for?

Though not explicit goals of DawnBSD, its design coincides with principles of
minimalism, predictable behavior, and clean, well-documented code. These
coincidental features are mutually exclusive with its design goals and should be
considered features of DawnBSD. These features should enhance accessibility to
tinkerers, those wishing to understand operating system design, and those
wishing to administer a predictable system which offers consistent tooling and
minimal abstractions. This system could coincidentally offer a retro-style
Unix-like OS which should be familiar to experienced Unix-like OS users.

### Source tree layout


### Contributions
Contributions are welcomed. Please read below to familiarize yourself with the
project contribution guidelines.

The source tree has three active branches, in descending order of their
maturity; master, beta, and alpha. This scheme is based on the original which
was implemented by the Computer Science Research Group (CSRG) who developed BSD.

The alpha branch is where experimental development takes place. This is where
features in your local branch should be headed. Prior to shipping your
development, you should verify the following; the base system builds, the code
has been documented well, the DawnBSD project coding standards have been
followed, the code has been licensed correctly and you've made your Copyright
claim, and that every part of this code is your original work; note that
neither the DawnBSD project nor its contributors are liable for your work. The
alpha branch follows a rolling point release model.

The beta branch is where features which are stable and useful are moved to. This
branch forms the core of the next point release. Features included here are
expected to be reasonably mature, with development focus shifting in the beta
branch to stability and bug fixes. Like the alpha branch, this branch does not
follow a point release schedule and instead a rolling point release.

The master branch is based on the beta branch. Once the beta branch has met its
release deadline, the current master branch will be renamed to its point release
versioning name, and the beta branch will be cloned and this clone used as the
new master branch. Only bug fixes found during system usage should be submitted
here. The master branch follows a fixed point release schedule, with a new
release expected every six months.

Community contributions to DawnBSD are welcomed. This repository and the ports
tree repository constitute the majority of DawnBSD development. Contributions
ranging from development, grammar fixes, documentation, bug fixes, refactoring,
are welcomed. Please fork a copy of DawnBSD, clone it, develop it locally, and
build it locally before submitting changes upstream. 

### Mandatory "Why not the other BSDs?"
FreeBSD and NetBSD are large, feature-rich operating systems with innovative
technology. These features also introduce complexity on par with other large
operating system such as GNU/Linux and the illumos project. 386BSD 0.1 and
4.4BSD Lite2 are two small, functional Unix-like operating systems which partly
served as inspiration for this project. A natural choice for an intelligently
small operating system is OpenBSD; it is minimal, has a significant reduction in
base size, including kernel files, from its peers, and unlike the early BSDs,
includes features essential for a modern system. Although it serves as an
excellent base system and one to start DawnBSD from, there are some
irreconcilable differences that DawnBSD supports. DawnBSD aims to be more POSIX
compliant than OpenBSD, especially in areas where the OpenBSD project explicitly
foregoes the POSIX standard in favor of enhanced security. DawnBSD aims to
remove non-POSIX pieces of the system, reducing its functionality to the bare
minimum needed to have a functional operating system. The DawnBSD project also
strives to welcome contributors, ease the cognitive load of contributors, and
offer and constructive environment for its development [and the development of
its developers].

### Insight on why I started this project
A common point to rally around I see is the lack of a modern Unix-like operating
system which is intelligently small and comprehensible while also being
fully-featured. The majority of Unix-like systems which persist
today include features beyond the essential of what's necessary to have a
POSIX-compliant system with little else. This complexity emanates to users,
designers, and researchers. I want to minimize that cognitive load, and see to
it an operating system which can follow the principle of least surprise. 

I want the base operating system to reduce or avoid the use of manual installers, 
package managers, and systemwide software suites. This system should be
predictable and stable, both in terms of architecture and user familiarity. The
C code should be readable and optimizations should be used with discretion,
focusing on bottlenecks and critical areas with generous documentation. The
source tree should be easily navigable and in-tree READMEs and other source tree
explanations should be used.

New contributors should be welcomed. Experienced administrators, researchers,
and tinkerers alike should find value in DawnBSD as being an intelligently small
and coherent system from which to base.

I reflect on my own experiences in learning operating system design, system
administration, and the paths taken by past operating system projects as
inspiration for this system.
