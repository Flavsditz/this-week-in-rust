Title: This Week in Rust 252
Number: 252
Date: 2018-09-18
Category: This Week in Rust

Hello and welcome to another issue of *This Week in Rust*!
[Rust](http://rust-lang.org) is a systems language pursuing the trifecta: safety, concurrency, and speed.
This is a weekly summary of its progress and community.
Want something mentioned? Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) or [send us a pull request](https://github.com/cmr/this-week-in-rust).
Want to get involved? [We love contributions](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

*This Week in Rust* is openly developed [on GitHub](https://github.com/cmr/this-week-in-rust).
If you find any errors in this week's issue, [please submit a PR](https://github.com/cmr/this-week-in-rust/pulls).

# Updates from Rust Community

## News & Blog Posts

# Crate of the Week

This week's crate is [mtpng](https://github.com/brion/mtpng), a parallelized PNG encoder. Thanks to [Willi Kappler](https://users.rust-lang.org/t/crate-of-the-week/2704/454) for the suggestion!

[Submit your suggestions and votes for next week][submit_crate]!

[submit_crate]: https://users.rust-lang.org/t/crate-of-the-week/2704

# Call for Participation

Always wanted to contribute to open-source projects but didn't know where to start?
Every week we highlight some tasks from the Rust community for you to pick and get started!

Some of these tasks may also have mentors available, visit the task page for more information.

* [auto_impl has a few issues for beginners interested in working with the new proc macro API](https://users.rust-lang.org/t/twir-call-for-participation/4821/204).

If you are a Rust project owner and are looking for contributors, please submit tasks [here][guidelines].

[guidelines]: https://users.rust-lang.org/t/twir-call-for-participation/4821

# Updates from Rust Core

131 pull requests were [merged in the last week][merged]

[merged]: https://github.com/search?q=is%3Apr+org%3Arust-lang+is%3Amerged+merged%3A2018-09-10..2018-09-17

* [temporarily prohibit proc macro attributes placed after derives](https://github.com/rust-lang/rust/pull/54277)
* [add target thumbv7a-pc-windows-msvc](https://github.com/rust-lang/rust/pull/53621)
* [PowerPC: fix the calling convention for i1 arguments on PPC32](https://github.com/rust-lang/llvm/pull/127)
* [allow for opting out of ThinLTO and clean up LTO related cli flag handling](https://github.com/rust-lang/rust/pull/53950)
* [resolve: allow only core, std, meta and --extern in Rust 2018 paths](https://github.com/rust-lang/rust/pull/54116)
* [resolve: do not error on access to proc macros imported with `#[macro_use]`](https://github.com/rust-lang/rust/pull/53461)
* [add inspection and setter methods to proc_macro::Diagnostic](https://github.com/rust-lang/rust/pull/52896)
* [support ascription for patterns in NLL](https://github.com/rust-lang/rust/pull/53873)
* [allow named lifetimes in async functions](https://github.com/rust-lang/rust/pull/54000)
* [suggest && and || instead of 'and' and 'or'](https://github.com/rust-lang/rust/pull/54181)
* [use structured suggestion for "missing mut" label](https://github.com/rust-lang/rust/pull/54157)
* [de-overlap the lifetimes of `flow_inits` and `flow_{un,ever_}inits`](https://github.com/rust-lang/rust/pull/54213)
* [don't compute padding of braces unless they are unmatched](https://github.com/rust-lang/rust/pull/54092)
* [don't suggest extra clone when converting cloned slice to Vec](https://github.com/rust-lang/rust/pull/54080)
* [reexport `CheckLintNameResult`](https://github.com/rust-lang/rust/pull/54106)
* [miri: keep around some information for dead allocations](https://github.com/rust-lang/rust/pull/54254)
* [miri loop detector hashing](https://github.com/rust-lang/rust/pull/54076)
* [fix some uses of pointer intrinsics with invalid pointers](https://github.com/rust-lang/rust/pull/53804)
* [first step towards `u128` instead of `Const` in `PatternKind::Range`](https://github.com/rust-lang/rust/pull/51159)
* [stabilize outlives requirements](https://github.com/rust-lang/rust/pull/53793)
* [stabilize `#[used]`](https://github.com/rust-lang/rust/pull/51363)
* [stabilize slice_align_to](https://github.com/rust-lang/rust/pull/53754)
* [implement `tuple_struct_self_ctor`](https://github.com/rust-lang/rust/pull/53751) (RFC [#2302](https://rust-lang.github.io/rfcs/2302-tuple-struct-self-ctor.html))
* [implement `map_or_else` for `Result<T, E>`](https://github.com/rust-lang/rust/pull/53777)
* [add a implementation of `From` for converting `&'a Option<T>` into `Option<&'a T>`](https://github.com/rust-lang/rust/pull/53218)
* [cargo: add empty ctrlc handler on Windows](https://github.com/rust-lang/cargo/pull/6004)

## Approved RFCs

Changes to Rust follow the Rust [RFC (request for comments)
process](https://github.com/rust-lang/rfcs#rust-rfcs). These
are the RFCs that were approved for implementation this week:

* [Amend RFC 2175 to support for loops and leading vert](https://github.com/rust-lang/rfcs/pull/2530).

## Final Comment Period

Every week [the team](https://www.rust-lang.org/team.html) announces the
'final comment period' for RFCs and key PRs which are reaching a
decision. Express your opinions now.

### [RFCs](https://github.com/rust-lang/rfcs/labels/final-comment-period)

* [disposition: merge] [Deny the `overflowing_literals` lint for the 2018 edition](https://github.com/rust-lang/rfcs/pull/2438).

### [Tracking Issues & PRs](https://github.com/rust-lang/rust/labels/final-comment-period)

* [disposition: merge] [Fix camel case type warning for types with trailing underscores](https://github.com/rust-lang/rust/pull/54101).
* [disposition: merge] [Limit the promotion of const fns to the libstd and the `rustc_promotable` attribute](https://github.com/rust-lang/rust/pull/53851).
* [disposition: merge] [Support an explicit annotation for marker traits](https://github.com/rust-lang/rust/pull/53693).

## New RFCs

* [RFC: Elide array size](https://github.com/rust-lang/rfcs/pull/2545).
* [Make the turbofish syntax redundant](https://github.com/rust-lang/rfcs/pull/2544).
* [syntactic sugar for `EnumVariant(())`](https://github.com/rust-lang/rfcs/issues/2543).
* [Provide the llvm.is.constant/__builtin_constant_p intrinsic](https://github.com/rust-lang/rfcs/issues/2542).
* [Use `T: ToString` for `thread::Builder::name`](https://github.com/rust-lang/rfcs/pull/2541).
* [Add Duration::ZERO constant](https://github.com/rust-lang/rfcs/issues/2540).
* [#[cfg_attr] expanding to multiple attributes](https://github.com/rust-lang/rfcs/pull/2539).
* [Lint for function call in `unwrap_or(..)` parameter](https://github.com/rust-lang/rfcs/issues/2536).
* [RFC: Or patterns, i.e `Foo(Bar(x) | Baz(x))`](https://github.com/rust-lang/rfcs/pull/2535).
* [RFC: Write References for Direct and Partial Initialization using &out T and &uninit T](https://github.com/rust-lang/rfcs/pull/2534).
* [Keeping Secrets in Rust](https://github.com/rust-lang/rfcs/issues/2533).
* [RFC: Associated type defaults and Default groups](https://github.com/rust-lang/rfcs/pull/2532).
* [RFC: Hidden trait implementations](https://github.com/rust-lang/rfcs/pull/2529).
* [Type-changing struct update syntax](https://github.com/rust-lang/rfcs/pull/2528).
* [Support underscores as constant names](https://github.com/rust-lang/rfcs/pull/2526).
* [RFC: Permit _ in type aliases](https://github.com/rust-lang/rfcs/pull/2524).

# Upcoming Events

### Online

* [Sep 19. Rust Community Team Meeting in Discord](https://discordapp.com/channels/442252698964721669/443773747350994945).
* [Sep 25. Rust Community Content Subteam Meeting at channel #rust-community](irc://irc.mozilla.org/rust-community).
* [Sep 26. Rust Events Team Meeting in Telegram](https://t.me/joinchat/EkKINhHCgZ9llzvPidOssA).
* [Sep 26. Rust Community Team Meeting in Discord](https://discordapp.com/channels/442252698964721669/443773747350994945).
* [Oct 3. Rust Community Team Meeting at #rust-community on irc.mozilla.org](irc://irc.mozilla.org/rust-community).

### Africa

* [Oct 2. Johannesburg, SA - Johannesburg meetup](https://www.meetup.com/Johannesburg-Rust-Meetup).

### Europe

* [Sep 19. Berlin, DE - Berlin Rust Hack and Learn](https://www.meetup.com/opentechschool-berlin/events/253541005/).
* [Sep 20. Cambridge, GB - Cambridge Rust Meetup](https://www.meetup.com/Cambridge-Rust-Meetup/events/pzwshpyxmbbc/).
* [Oct 3. Vilnius, LT - Vilnius Rust Meetup #3 - Network Simulation and Web Assembly](https://www.meetup.com/Rust-in-Vilnius/events/254403141/).
* [Oct 3. Berlin, DE - Berlin Rust Hack and Learn](https://www.meetup.com/opentechschool-berlin/events/).

### North America

* [Sep 19. Vancouver, CA - Vancouver Rust meetup - Study/Hack/Hang-out](https://www.meetup.com/Vancouver-Rust/events/dqldspyxmbzb/).
* [Sep 20. Arlington, US - Rust DC - Mid-month Rustful](https://www.meetup.com/RustDC/events/253787454).
* [Sep 23. Mountain View, US - Rust Dev in Mountain View!](https://www.meetup.com/Rust-Dev-in-Mountain-View/events/glnfcpyxmbfc/).
* [Sep 24. Durham, US - Triangle Rustaceans](https://www.meetup.com/triangle-rustaceans/events/mfglwpyxmbgc/).
* [Sep 25. Dallas, US - Dallas Rust - Last Tuesday](https://www.meetup.com/Dallas-Rust/events/zfgwzmyxmbhc/).
* [Sep 30. Mountain View, US - Rust Dev in Mountain View!](https://www.meetup.com/Rust-Dev-in-Mountain-View).
* [Oct 3. Indianopolis, US - Indy.rs](https://www.meetup.com/indyrs/events/246726699/).
* [Oct 3. Atlanta, US - Rust Atlanta Meetup](https://www.meetup.com/Rust-ATL/).
* [Oct 3. Vancouver, CA - Vancouver Rust meetup](https://www.meetup.com/Vancouver-Rust/events/).
* **[Oct 19 & 20. Ann Arbor, US - Rust Belt Rust 2018](https://rust-belt-rust.com/).**


If you are running a Rust event please add it to the [calendar] to get
it mentioned here. Please remember to add a link to the event too.
Email the [Rust Community Team][community] for access.

[calendar]: https://www.google.com/calendar/embed?src=apd9vmbc22egenmtu5l6c5jbfc%40group.calendar.google.com
[community]: mailto:community-team@rust-lang.org

# Rust Jobs

* [Rust Developer at Parity, Berlin, DE](https://paritytech.io/jobs/).
* [Software Engineer at VMRay, Bochum, DE](https://careers.vmray.com/apply-software-engineer-rust-en/).

*Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) to get your job offers listed here!*

# Quote of the Week

> Sometimes bad designs will fail faster in Rust

– [Catherine West @ Rustconf](https://youtu.be/aKLntZcp27M?t=1444).

Thanks to [kornel](https://users.rust-lang.org/t/twir-quote-of-the-week/328/561) for the suggestion!

[Please submit your quotes for next week](http://users.rust-lang.org/t/twir-quote-of-the-week/328)!

*This Week in Rust is edited by: [nasa42](https://github.com/nasa42), [llogiq](https://github.com/llogiq), and [Flavsditz](https://github.com/Flavsditz).*

<small>[Discuss on r/rust]().</small>