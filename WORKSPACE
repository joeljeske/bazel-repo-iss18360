workspace(name = "repro")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "remote_java_tools_v11_12",
    sha256 = "af20366f926b1dadf8c084a51936116ef2f0db90e73e94b406c4ad8180f0788d",
    urls = [
        "https://mirror.bazel.build/bazel_java_tools/releases/java/v11.12/java_tools-v11.12.zip",
        "https://github.com/bazelbuild/java_tools/releases/download/java_v11.12/java_tools-v11.12.zip",
    ],
)

http_archive(
    name = "rules_java",
    sha256 = "060f163a2cf3b7ed7f17d1fc68e40e34ffdb0b7ed554ccfc04c2ab5b7cde2842",
    strip_prefix = "rules_java-8df92300a0df1a5a9048c44a6dde44dfe40001ed",
    urls = [
        "https://github.com/bazelbuild/rules_java/archive/8df92300a0df1a5a9048c44a6dde44dfe40001ed.tar.gz",
    ],
)

load("@rules_java//java:repositories.bzl", "rules_java_dependencies", "rules_java_toolchains")

register_toolchains("//:toolchain_jdk_11_definition")

rules_java_dependencies()

rules_java_toolchains()
