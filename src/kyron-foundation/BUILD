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
        "@iceoryx2_crates//:iceoryx2_bb_derive_macros",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "@iceoryx2_crates//:iceoryx2_bb_container",
        "@iceoryx2_crates//:iceoryx2_bb_elementary",
        "@iceoryx2_crates//:iceoryx2_bb_elementary_traits",
        "@iceoryx2_crates//:iceoryx2_bb_lock_free",
        "@iceoryx2_crates//:iceoryx2_bb_memory",
        "@iceoryx2_crates//:iceoryx2_bb_posix",
        "@iceoryx2_crates//:iceoryx2_bb_system_types",
        "@iceoryx2_crates//:iceoryx2_bb_testing",
        "@iceoryx2_crates//:iceoryx2_bb_threadsafe",
        "@iceoryx2_crates//:iceoryx2_pal_concurrency_sync",
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
