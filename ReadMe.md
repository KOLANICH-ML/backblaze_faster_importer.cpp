Backblaze dataset native importer [![Unlicensed work](https://raw.githubusercontent.com/unlicense/unlicense.org/master/static/favicon.png)](https://unlicense.org/)
=================================
~~![GitLab Build Status](https://gitlab.com/KOLANICH/backblaze_analytics_native_importer/badges/master/pipeline.svg)
~~![GitLab Coverage](https://gitlab.com/KOLANICH/backblaze_analytics_native_importer/badges/master/coverage.svg)~~
[![Libraries.io Status](https://img.shields.io/librariesio/github/KOLANICH/backblaze_analytics_native_importer.svg)](https://libraries.io/github/KOLANICH/backblaze_analytics_native_importer)

**We have moved to https://codeberg.org/KOLANICH-ML/backblaze_analytics_native_importer.cpp , grab new versions there.**

Under the disguise of "better security" Micro$oft-owned GitHub has [discriminated users of 1FA passwords](https://github.blog/2023-03-09-raising-the-bar-for-software-security-github-2fa-begins-march-13/) while having commercial interest in success and wide adoption of [FIDO 1FA specifications](https://fidoalliance.org/specifications/download/) and [Windows Hello implementation](https://support.microsoft.com/en-us/windows/passkeys-in-windows-301c8944-5ea2-452b-9886-97e4d2ef4422) which [it promotes as a replacement for passwords](https://github.blog/2023-07-12-introducing-passwordless-authentication-on-github-com/). It will result in dire consequencies and is competely inacceptable, [read why](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

If you don't want to participate in harming yourself, it is recommended to follow the lead and migrate somewhere away of GitHub and Micro$oft. Here is [the list of alternatives and rationales to do it](https://github.com/orgs/community/discussions/49869). If they delete the discussion, there are certain well-known places where you can get a copy of it. [Read why you should also leave GitHub](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

---

It is an application written in C++ which should import and normalize BackBlaze dataset into an SQLite DB faster than `backblaze_analytics`. `backblaze_analytics` importer written in python + SQLite is damn slow because SQLite is not very smart and uses journal extensively.

How to build
============

In order to build it you need CMake and the `backblaze_analytics`.

1. `python -m backblaze_analytics import generateC++Schema`
2. Then run CMake
3. Then build.
