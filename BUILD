# Hey Emacs, this is -*- coding: utf-8; mode: bazel -*-

package(default_visibility = ["//visibility:public"])

# The following commented load() should fail!
# So it is impossible to accidentally load "ts_library"
# from "@npm_bazel_typescript//:index.bzl":
#
# load("@npm_bazel_typescript//:index.bzl", "ts_library") # <-- WILL FAIL!

load(":ts_library.bzl", "ts_library")

ts_library(
  name = "castle",
  srcs = glob(["server/**/*.ts"]),
  deps = [
    "@npm//koa",
    "@npm//@types/koa",
    "@npm//apollo-server-koa",
    "@npm//type-graphql",
    "@npm//arangojs",
  ],
)
