# *******************************************************************************
# Copyright (c) 2025 Contributors to the Eclipse Foundation
#
# See the NOTICE file(s) distributed with this work for additional
# information regarding copyright ownership.
#
# This program and the accompanying materials are made available under the
# terms of the Apache License Version 2.0 which is available at
# https://www.apache.org/licenses/LICENSE-2.0
#
# SPDX-License-Identifier: Apache-2.0
# *******************************************************************************
load("@rules_rust//rust:defs.bzl", "rust_library", "rust_test")

rust_library(
    name = "libkyron_foundation",
    srcs = glob(["src/**/*.rs"]),
    crate_features = [
        "tracing"
    ],
    crate_name = "kyron_foundation",
    proc_macro_deps = [
        "@iceoryx2_crates//:iceoryx2-bb-derive-macros",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "@iceoryx2_crates//:iceoryx2-bb-container",
        "@iceoryx2_crates//:iceoryx2-bb-elementary",
        "@iceoryx2_crates//:iceoryx2-bb-elementary_traits",
        "@iceoryx2_crates//:iceoryx2-bb-lock_free",
        "@iceoryx2_crates//:iceoryx2-bb-memory",
        "@iceoryx2_crates//:iceoryx2-bb-posix",
        "@iceoryx2_crates//:iceoryx2-bb-system_types",
        "@iceoryx2_crates//:iceoryx2-bb-testing",
        "@iceoryx2_crates//:iceoryx2-bb-threadsafe",
        "@iceoryx2_crates//:iceoryx2-pal-concurrency_sync",
        "@score_crates//:tracing",
        "@score_crates//:tracing_subscriber",
    ],
)

rust_test(
    name = "tests",
    crate = ":libkyron_foundation",
    crate_features = [
        "tracing"
    ],
)
