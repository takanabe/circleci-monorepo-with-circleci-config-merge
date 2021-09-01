# circleci-monorepo-with-circleci-config-merge

A test repository to try monorepo support using CircleCI with https://github.com/suzuki-shunsuke/circleci-config-merge

This project is highly inspired by [Quipper's approach](https://quipper.hatenablog.com/entry/2020/12/01/080000).

## Usage

```
make
```

The above command generates `.circleci/config.yml` from `.circleci/base-config.yml` and `circleci/config.yml` stored in each application directory.

## Project structure


```
.
├── .circleci
│   ├── base-config.yml # base config for CircleCI
│   └── config.yml      # generated config
├── app1
│   └── circleci
│       └── config.yml  # CircleCI config for app1
├── app2
│   └── circleci
│       └── config.yml  # CircleCI config for app2
├── app3
│   └── circleci
│       └── config.yml  # CircleCI config for app3
```


## Pros

* Maintainability is good. We can put `circleci/config.yml` per project in monorepo.

## Cons

* Conflicts occurs potentially (this [commit](https://github.com/takanabe/circleci-monorepo-with-circleci-config-merge/commit/73715ac1f66991a93ecb2e3eb7feee17f9c02d6f) overwrites definitions defined by `app1/circleci/config.yml`)

## References

* [GitHub - suzuki-shunsuke/example-circleci-config-merge: Example usage of circleci-config-merge](https://github.com/suzuki-shunsuke/example-circleci-config-merge)
