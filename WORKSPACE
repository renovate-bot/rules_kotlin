# Copyright 2018 The Bazel Authors. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
workspace(name = "io_bazel_rules_kotlin")

load("//kotlin/internal/repositories:repositories.bzl", "github_archive")

github_archive(
    name = "com_google_protobuf",
    commit = "106ffc04be1abf3ff3399f54ccf149815b287dd9",
    repo = "google/protobuf",
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive", "http_jar")

http_jar(
    name = "bazel_deps",
    sha256 = "05498224710808be9687f5b9a906d11dd29ad592020246d4cd1a26eeaed0735e",
    url = "https://github.com/hsyed/bazel-deps/releases/download/v0.1.0/parseproject_deploy.jar",
)

http_archive(
    name = "bazel_toolchains",
    sha256 = "109a99384f9d08f9e75136d218ebaebc68cc810c56897aea2224c57932052d30",
    strip_prefix = "bazel-toolchains-94d31935a2c94fe7e7c7379a0f3393e181928ff7",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/bazel-toolchains/archive/94d31935a2c94fe7e7c7379a0f3393e181928ff7.tar.gz",
        "https://github.com/bazelbuild/bazel-toolchains/archive/94d31935a2c94fe7e7c7379a0f3393e181928ff7.tar.gz",
    ],
)

load("//kotlin:kotlin.bzl", "kotlin_repositories", "kt_register_toolchains")

kotlin_repositories()

kt_register_toolchains()
