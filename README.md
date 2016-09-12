This repo is the
[rmacklin/why_i_dont_recommend_squash_and_merge](https://github.com/rmacklin/why_i_dont_recommend_squash_and_merge)
repo but with the `squash-and-merge` branch set to `master` and the feature
branches deleted. So it resembles a real repo that only uses squash and merge,
and it demonstrates another downside of using squash and merge:

## Pre-squash commits won't be included in clones
If you clone this repo and try to check out an individual commit, such as
[88e4ed3](https://github.com/rmacklin/squash_and_merge_example/commit/88e4ed33f4792b68bca2a80ff8c2b180370dee57)
from [PR #1](https://github.com/rmacklin/squash_and_merge_example/pull/1),
it'll fail:
```sh
$ git checkout 88e4ed33f4792b68bca2a80ff8c2b180370dee57
fatal: reference is not a tree: 88e4ed33f4792b68bca2a80ff8c2b180370dee57
```

This also means you can't revert an individual commit:
```sh
$ git revert 88e4ed33f4792b68bca2a80ff8c2b180370dee57
fatal: bad object 88e4ed33f4792b68bca2a80ff8c2b180370dee57
```
