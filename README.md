# Hi, I'm Eric Kwoka

[<img src="https://img.shields.io/badge/Portfolio-blue?style=for-the-badge&logo=deno">](https://thekwoka.net)

I'm a United States Marine turned Full Stack Engineer!

I'm passionate about solving big problems with little pieces, and contibuting to the ever evolving tech ecosystem.

## Some of my packages

### [@types/alpinejs](https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/alpinejs)

[<img src="https://img.shields.io/npm/v/@types/alpinejs?label=%20&style=for-the-badge&logo=pnpm&logoColor=white">](https://www.npmjs.com/package/@types/alpinejs)
<img src="https://img.shields.io/npm/types/@types/alpinejs?label=&logo=typescript&logoColor=white&style=for-the-badge">
<img src="https://img.shields.io/npm/dt/@types/alpinejs?style=for-the-badge&logo=npm&logoColor=white">

The types for the AlpineJS UI reactivity system. I maintain the primary types package as well as the types packages for each of the core plugins.

### [ESlint Plugin Filename Export](https://github.com/ekwoka/eslint-plugin-filename-export)

[<img src="https://img.shields.io/npm/v/eslint-plugin-filename-export?label=%20&style=for-the-badge&logo=pnpm&logoColor=white">](https://www.npmjs.com/package/eslint-plugin-filename-export)
<img src="https://img.shields.io/npm/dt/eslint-plugin-filename-export?style=for-the-badge&logo=npm&logoColor=white">

ESLint plugin that enforces that filenames match to the name of an exported value.

### [Preact Heroicons](https://github.com/ekwoka/preact-heroicons)

[<img src="https://img.shields.io/npm/v/preact-heroicons?label=&style=for-the-badge&logo=pnpm&logoColor=white">](https://www.npmjs.com/package/preact-heroicons)
<img src="https://img.shields.io/npm/dt/preact-heroicons?style=for-the-badge&logo=npm&logoColor=white">
<img src="https://img.shields.io/npm/types/preact-heroicons?label=&logo=typescript&logoColor=white&style=for-the-badge">
[<img src="https://img.shields.io/bundlephobia/minzip/preact-heroicons?style=for-the-badge&logo=esbuild&logoColor=white">](https://bundlephobia.com/package/preact-heroicons)

Simple companion package to @tailwindlabs/heroicons with all of the icons as properly typed Preact components!

## Some Fun Utilities

### [Weak LRU Cache](https://github.com/ekwoka/weak-lru-cache)

[<img src="https://img.shields.io/npm/v/@ekwoka/weak-lru-cache?label=%20&style=for-the-badge&logo=pnpm&logoColor=white">](https://www.npmjs.com/package/@ekwoka/weak-lru-cache)
<img src="https://img.shields.io/npm/dt/@ekwoka/weak-lru-cache?style=for-the-badge&logo=npm&logoColor=white">
<img src="https://img.shields.io/npm/types/@ekwoka/weak-lru-cache?label=&logo=typescript&logoColor=white&style=for-the-badge">
[<img src="https://img.shields.io/bundlephobia/minzip/@ekwoka/weak-lru-cache?style=for-the-badge&logo=esbuild&logoColor=white">](https://bundlephobia.com/package/@ekwoka/weak-lru-cache)

A quick and simple implementation of a Weak referenced Least Recently Used Cache, for when you want smart caching in an application that may have a lot of the cached data in use.

### [Rust-TS](https://github.com/ekwoka/rust-ts)

[<img src="https://img.shields.io/npm/v/@ekwoka/rust-ts?label=%20&style=for-the-badge&logo=pnpm&logoColor=white">](https://www.npmjs.com/package/@ekwoka/rust-ts)
<img src="https://img.shields.io/npm/dt/@ekwoka/rust-ts?style=for-the-badge&logo=npm&logoColor=white">
<img src="https://img.shields.io/npm/types/@ekwoka/rust-ts?label=&logo=typescript&logoColor=white&style=for-the-badge">
[<img src="https://img.shields.io/bundlephobia/minzip/@ekwoka/rust-ts?style=for-the-badge&logo=esbuild&logoColor=white">](https://bundlephobia.com/package/@ekwoka/rust-ts)

A fun exploration of implementing some useful Rust Structs in TypeScript. The main practical use of this library is for Rust-style Iterators (exported as `RustIterator`) to provide improved streaming computation of values. These were used quite extensively in my 2023 Advent of Code solutions, for the fun of trying to [stream solutions from the input, with minimal storage of intermediary values](https://github.com/ekwoka/advent-of-code/blob/main/2023/09/index.ts).

This also includes the Monad Structs for `Option` and `Result` to improve handling of errors and null values for safety. Getting Monads to work in typescript to work well with some more advanced methods is tricky.

## Some Notable Contributions

I am a primary contributor to AlpineJS (not officially associated with the project, but I help out and make a lot of PRs). Some have been pretty nice!

### [Refactors Proxy Merging for ~15% performance improvements and ~75% less memory](https://github.com/alpinejs/alpine/pull/3722)

The old way that the Alpine context proxies were merged recreated a lot of the same shaped data for every merge, which happened quite often (every time an expression was evaluated, which is all the time). Not only did this use a lot more memory creating and destroying the same object again and again, doing that takes more processes. This refactors the merge to reuse the same proxy handlers for all merges, as well as simplified the handling of reflections to use more native behaviors that could be offloaded to the runtime.

On top of that, this fixed issues where the merged proxy was difficult to analyze when debugging by properly implementing a `toJSON` method. Oh, and it short circuited some lookups that would happen often to improve performance (this was for the fairly unknown and uncommon `unscopables` symbol that was an issue for Alpine's implementation decisions that could really burn a lot of time doing nothing). Pretty significant tackling of performance issues.

## Obligatory Stats

![Eric's Streak Stats](https://streak-stats.demolab.com/?user=ekwoka&theme=onedark)
![Eric's GitHub Stats](https://github-readme-stats.vercel.app/api?username=ekwoka&show_icons=true&theme=onedark)
![Eric's Top Languages](https://github-readme-stats.vercel.app/api/top-langs?username=ekwoka&show_icons=true&theme=onedark&langs_count=4&layout=compact)
