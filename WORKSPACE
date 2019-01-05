workspace(name = "remote_client")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Needed for "well-known protos" and @com_google_protobuf//:protoc.
http_archive(
    name = "com_google_protobuf",
    sha256 = "091d4263d9a55eccb6d3c8abde55c26eaaa933dea9ecabb185cdf3795f9b5ca2",
    strip_prefix = "protobuf-3.5.1.1",
    urls = ["https://github.com/google/protobuf/archive/v3.5.1.1.zip"],
)

# Needed for @grpc_java//compiler:grpc_java_plugin.
http_archive(
    name = "grpc_java",
    sha256 = "000a6f8579f1b93e5d1b085c29d89dbc1ea8b5a0c16d7427f42715f0d7f0b247",
    strip_prefix = "grpc-java-d792a72ea15156254e3b3735668e9c4539837fd3",
    urls = ["https://github.com/grpc/grpc-java/archive/d792a72ea15156254e3b3735668e9c4539837fd3.zip"],
)

http_archive(
    name = "googleapis",
    sha256 = "7b6ea252f0b8fb5cd722f45feb83e115b689909bbb6a393a873b6cbad4ceae1d",
    url = "https://github.com/googleapis/googleapis/archive/143084a2624b6591ee1f9d23e7f5241856642f4d.zip",
    strip_prefix = "googleapis-143084a2624b6591ee1f9d23e7f5241856642f4d",
    build_file = "@//:BUILD.googleapis",
)

http_archive(
    name = "remoteapis",
    sha256 = "8ddb673b1346cc7c664bc3ff8b01060b2d2b5eede36d26439e2f1c658d8143f4",
    url = "https://github.com/bazelbuild/remote-apis/archive/998b8625d5947f272142037a1e52a61be33fcefb.zip",
    strip_prefix = "remote-apis-998b8625d5947f272142037a1e52a61be33fcefb",
    build_file = "@//:BUILD.remoteapis",
)

# Bazel toolchains
http_archive(
  name = "bazel_toolchains",
  urls = [
    "https://mirror.bazel.build/github.com/bazelbuild/bazel-toolchains/archive/bc0091adceaf4642192a8dcfc46e3ae3e4560ea7.tar.gz",
    "https://github.com/bazelbuild/bazel-toolchains/archive/bc0091adceaf4642192a8dcfc46e3ae3e4560ea7.tar.gz",
  ],
  strip_prefix = "bazel-toolchains-bc0091adceaf4642192a8dcfc46e3ae3e4560ea7",
  sha256 = "7e85a14821536bc24e04610d309002056f278113c6cc82f1059a609361812431",
)
load("//3rdparty:workspace.bzl", "maven_dependencies", "declare_maven")

maven_dependencies(declare_maven)
