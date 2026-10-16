# 3d-vectors — what changed, in plain words

The whole history of this project, newest first, written for someone who has never seen the code. It began on 20.0209 as a small piece of math code for arrows in space (vectors), split off from the 2d-vectors project and shared by other projects. Every entry is one step on the main version: a pull request, or a day's changes on one topic.

## October 2026

**3d-vectors #18: Dependabot's updates merge themselves** · [PR #18](https://github.com/travis-horton/3d-vectors/pull/18) · merged 26.1016.1117 · v1.0.7
- Behind the scenes: a new automatic job merges each library update from Dependabot as soon as it opens, then asks the change-log job to record it, so the updates keep landing without anyone clicking merge.

**3d-vectors #17: Bump minimatch from 3.0.4 to 3.1.5** · [PR #17](https://github.com/travis-horton/3d-vectors/pull/17) · merged 26.1016.1031 · v1.0.6
- Behind the scenes: an automatic dependency update — "Bump minimatch from 3.0.4 to 3.1.5".

**3d-vectors #12: Bump brace-expansion from 1.1.11 to 1.1.21** · [PR #12](https://github.com/travis-horton/3d-vectors/pull/12) · merged 26.1016.1001 · v1.0.5
- Behind the scenes: an automatic dependency update — "Bump brace-expansion from 1.1.11 to 1.1.21".

**3d-vectors #13: Bump tmp and eslint** · [PR #13](https://github.com/travis-horton/3d-vectors/pull/13) · merged 26.1016.0956 · v1.0.4
- Behind the scenes: an automatic dependency update — "Bump tmp and eslint".

**3d-vectors #11: Bump flatted and eslint** · [PR #11](https://github.com/travis-horton/3d-vectors/pull/11) · merged 26.1016.0956 · v1.0.3
- Behind the scenes: an automatic dependency update — "Bump flatted and eslint".

**3d-vectors #16: the change log catches up on entries it missed** · [PR #16](https://github.com/travis-horton/3d-vectors/pull/16) · merged 26.1015.0728 · v1.0.2
- Behind the scenes: the robot that writes this file after each change now also writes in any earlier finished change it missed, oldest first, with a "recorded late" note when it is more than an hour late. If GitHub won't answer one of its lookups, it skips only that one, records the newest change anyway, and fills the gap on a later run.

**3d-vectors #10: the project's past, written down** · [PR #10](https://github.com/travis-horton/3d-vectors/pull/10) · merged 26.1010.1209 · v1.0.1
- Behind the scenes: the history file now tells the whole story of the project in plain words, from its first day on 20.0209 up to the history tool, one entry per step, numbered from version 0.1.0.

**3d-vectors #9: security updates and a self-writing history** · [PR #9](https://github.com/travis-horton/3d-vectors/pull/9) · merged 26.1010.1150 · v1.0.0
- **Security updates** · merged 26.1010.1150
  Behind the scenes: six borrowed helper packages were moved to the versions that fix their known security problems, gathered from six waiting automatic update requests into one. Nothing about how the project works changes.
- **History tool** · merged 26.1010.1150
  Behind the scenes: added the tool that writes a plain-language entry into this project's history file every time a change is accepted.

## April 2020

**Helper tools brought up to date** · [commit](https://github.com/travis-horton/3d-vectors/commit/d07f6aa) · merged 20.0427.0842 · v0.1.1
- Behind the scenes: the code-checking tool's style rules and its add-on for checking how files connect were moved to newer versions, along with about a dozen small packages they rely on, including the fixed versions of two with known security problems. The vector math itself did not change.

## February 2020

**The project begins: math for arrows in space** · [commits](https://github.com/travis-horton/3d-vectors/commits/master?since=2020-02-09&until=2020-02-09) · merged 20.0209.2046 · v0.1.0
- **[Code-checking tool](https://github.com/travis-horton/3d-vectors/commit/19518de)** · merged 20.0209.2046
  Behind the scenes: the project got its settings file, under the name 3d-vectors, and a code-checking tool that flags mistakes and keeps the code to one consistent style.
- **[The vector math](https://github.com/travis-horton/3d-vectors/commit/695056f)** · merged 20.0209.1412
  New: a reusable piece of code for arrows in space, each with a left-right, an up-down and a near-far amount. It can measure an arrow's length, shrink it to length one, subtract one arrow from another, stretch it by a number, and multiply two arrows into a single number. It was written in the 2d-vectors project minutes earlier and moved here as its own project.
  Try it: open Terminal and paste
      cd ~/code/3d-vectors && node --no-warnings -e "import('./3d-vectors.js').then(({default: V}) => console.log(new V(3, 4, 12).magnitude()))"
