workspace(name = "xnnpack")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Bazel rule definitions
http_archive(
    name = "rules_cc",
    strip_prefix = "rules_cc-master",
    urls = ["https://github.com/bazelbuild/rules_cc/archive/master.zip"],
)

# Google Test framework, used by most unit-tests.
http_archive(
    name = "com_google_googletest",
    strip_prefix = "googletest-master",
    urls = ["https://github.com/google/googletest/archive/master.zip"],
)

# Google Benchmark library, used in micro-benchmarks.
http_archive(
    name = "com_google_benchmark",
    strip_prefix = "benchmark-master",
    urls = ["https://github.com/google/benchmark/archive/master.zip"],
)

# FP16 library, used for half-precision conversions
http_archive(
    name = "FP16",
    strip_prefix = "FP16-3c54eacb74f6f5e39077300c5564156c424d77ba",
    sha256 = "0d56bb92f649ec294dbccb13e04865e3c82933b6f6735d1d7145de45da700156",
    urls = [
        "https://github.com/Maratyszcza/FP16/archive/3c54eacb74f6f5e39077300c5564156c424d77ba.zip",
    ],
    build_file = "@//third_party:FP16.BUILD",
)

# FXdiv library, used for repeated integer division by the same factor
http_archive(
    name = "FXdiv",
    strip_prefix = "FXdiv-b408327ac2a15ec3e43352421954f5b1967701d1",
    sha256 = "ab7dfb08829bee33dca38405d647868fb214ac685e379ec7ef2bebcd234cd44d",
    urls = ["https://github.com/Maratyszcza/FXdiv/archive/b408327ac2a15ec3e43352421954f5b1967701d1.zip"],
)

# pthreadpool library, used for parallelization
http_archive(
    name = "pthreadpool",
    strip_prefix = "pthreadpool-b4589998be9a0f794236cf46f1b5b232b2b15ca3",
    sha256 = "b09f79d1b609239861bce5ed4ba4fbcf04f36e2c31471276158c44e5e15fde95",
    urls = ["https://github.com/Maratyszcza/pthreadpool/archive/b4589998be9a0f794236cf46f1b5b232b2b15ca3.zip"],
)

# clog library, used for logging
http_archive(
    name = "clog",
    strip_prefix = "cpuinfo-d5e37adf1406cf899d7d9ec1d317c47506ccb970",
    sha256 = "3f2dc1970f397a0e59db72f9fca6ff144b216895c1d606f6c94a507c1e53a025",
    urls = [
        "https://github.com/pytorch/cpuinfo/archive/d5e37adf1406cf899d7d9ec1d317c47506ccb970.tar.gz",
    ],
    build_file = "@//third_party:clog.BUILD",
)


# cpuinfo library, used for detecting processor characteristics
http_archive(
    name = "cpuinfo",
    strip_prefix = "cpuinfo-5916273f79a21551890fd3d56fc5375a78d1598d",
    sha256 = "2a160c527d3c58085ce260f34f9e2b161adc009b34186a2baf24e74376e89e6d",
    urls = [
        "https://github.com/pytorch/cpuinfo/archive/5916273f79a21551890fd3d56fc5375a78d1598d.zip",
    ],
    build_file = "@//third_party:cpuinfo.BUILD",
    patches = ["@//third_party:cpuinfo.patch"],
)

# Ruy library, used to benchmark against
http_archive(
   name = "ruy",
   strip_prefix = "ruy-9f53ba413e6fc879236dcaa3e008915973d67a4f",
   sha256 = "fe8345f521bb378745ebdd0f8c5937414849936851d2ec2609774eb2d7098e54",
   urls = [
       "https://github.com/google/ruy/archive/9f53ba413e6fc879236dcaa3e008915973d67a4f.zip",
   ],
)

# Android NDK location and version is auto-detected from $ANDROID_NDK_HOME environment variable
android_ndk_repository(name = "androidndk")

# Android SDK location and API is auto-detected from $ANDROID_HOME environment variable
android_sdk_repository(name = "androidsdk")
