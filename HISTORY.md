# 3d-vectors — what changed, in plain words

The whole history of this project, newest first, written for someone who has never seen the code. It began on 20.0209 as a small piece of math code for arrows in space (vectors), split off from the 2d-vectors project and shared by other projects. Every entry is one step on the main version: a pull request, or a day's changes on one topic.

## October 2026

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
