load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "4.1"
RULES_JVM_EXTERNAL_SHA = "f36441aa876c4f6427bfb2d1f2d723b48e9d930b62662bf723ddfb8fc80f0140"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "com.indico:indico-client-java:4.12.1",
        "com.google.code.gson:gson:2.8.9",
    ],
    fetch_sources = True,
    repositories = [
        # Private repositories are supported through HTTP Basic auth
        # "http://username:password@localhost:8081/artifactory/my-repository",
        # "https://maven.google.com",
        "http://uk.maven.org/maven2",
        "https://jcenter.bintray.com/",
    ],
)