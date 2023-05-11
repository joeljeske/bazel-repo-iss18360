# bazel-repo-iss18360

Repro:

```sh
export USE_BAZEL_VERSION=6.2.0
bazel clean  --async
bazel build //src/...

# INFO: From Extracting interface //src:lib_b:
# Unknown constant: 11. Passing class through.
# ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^  Unexpected error
```

```sh
export USE_BAZEL_VERSION=6.1.0
bazel clean  --async
bazel build //src/...
```
