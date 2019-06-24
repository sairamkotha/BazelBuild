load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")
load("@rules_pods//BazelExtensions:workspace.bzl", "new_pod_repository")
package(default_visibility = ["//visibility:public"])

swift_library(
   name = "BazelBuild",
   srcs = [
      "BazelBuild/AppDelegate.swift",
      "BazelBuild/ViewController.swift"
   ],
   deps = [
      "//Vendor/RxSwift:RxSwift"
   ]
)	

ios_application(
   name = "BazelBuild",
   bundle_id = "com.sairam.build.BazelBuild",
   families = ["iphone"],
   infoplists = ["BazelBuild/Info.plist"],
   visibility = ["//visibility:public"],
   deps = ["BazelBuild"],
   minimum_os_version = "10.0"
)