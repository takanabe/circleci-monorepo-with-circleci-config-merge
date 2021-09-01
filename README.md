# circleci-monorepo-with-circleci-config-merge

A test repository to try monorepo support using CircleCI with https://github.com/suzuki-shunsuke/circleci-config-merge

This project is highly inspired by [Quipper's approach](https://quipper.hatenablog.com/entry/2020/12/01/080000).


## Pros

* Maintainability is good. We can put `circleci/config.yml` per project in monorepo.

## Cons

* Conflicts occurs potentially (this [commit](https://github.com/takanabe/circleci-monorepo-with-circleci-config-merge/commit/73715ac1f66991a93ecb2e3eb7feee17f9c02d6f) overwrites definitions defined by `app1/circleci/config.yml`)

## References

* [GitHub - suzuki-shunsuke/example-circleci-config-merge: Example usage of circleci-config-merge](https://github.com/suzuki-shunsuke/example-circleci-config-merge)
