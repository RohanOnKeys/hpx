..
    Copyright (C) 2007-2025 Hartmut Kaiser

    SPDX-License-Identifier: BSL-1.0
    Distributed under the Boost Software License, Version 1.0. (See accompanying
    file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)

.. _hpx_2_0_0:

============================
|hpx| V2.0.0 (TBD)
============================

General changes
===============

Breaking changes
================

Closed issues
=============

* :hpx-issue:`7569` - godbolt-minimal does not install hpx/experimental/sandbox.hpp
* :hpx-issue:`7557` - examples/quickstart/sort_by_key_demo fails to compile with Apple clang 21 (libc++ __sift_down vs compare_projected)
* :hpx-issue:`7539` - libhpx_wrap has an unpropagated oneTBB dependency
* :hpx-issue:`7520` - Data race in hostname_print_helper::get_hostname() on worker thread startup
* :hpx-issue:`7517` - HPX_FORWARD does not forward under nvcc: cudafe strips && from static_cast<decltype(x)&&>
* :hpx-issue:`7513` - dijkstra_termination_disconnected_*_7474 abort on any HPX_WITH_SUPERVISION=OFF build
* :hpx-issue:`7483` - force_disconnect: race between disconnect completion and AGAS resolve visibility
* :hpx-issue:`7470` - late_component_launcher: demonstrate crash detection -> force_disconnect purge -> relaunch
* :hpx-issue:`7461` - check-circular-deps CI failing on master (pre-existing, unrelated to PR #base 4f5b0d6b)
* :hpx-issue:`7428` - v1.11.0 fails to build with asio-1.38.2
* :hpx-issue:`7411` - Regression: flat all_to_all ~66x slower since 6df14adf09 (PU offset suppressed for all localities)
* :hpx-issue:`7389` - `waittime` vs `wait_time` name mismatch when `HPX_HAVE_THREAD_QUEUE_WAITTIME` is ON
* :hpx-issue:`7383` - HPX affinity binds introduce randomised offsets for multiple localities in single node
* :hpx-issue:`7333` - Insecure Deserialization - Type Confusion in Shared Pointers - HPX v1.11.0
* :hpx-issue:`7287` - vector_pack_load::unaligned broadcasts scalar instead of loading pack
* :hpx-issue:`7251` - stdexec warning about transform_completion_signatures
* :hpx-issue:`7245` - CMake developer warning regarding fetching Stdexec
* :hpx-issue:`7225` - Proposal / Feedback Request: HPX-Vision (Distributed Observability Prototype for HPX)
* :hpx-issue:`7214` - Implement `hpx::experimental::for_each_index` as described in P4150
* :hpx-issue:`7212` - Make inspect report links use the scanned tree’s actual Git commit
* :hpx-issue:`7203` - Reimplement the distributed barrier on top of collectives infrastructure
* :hpx-issue:`7199` - Deduplicate tests.examples exclusion regex generation in Windows workflows
* :hpx-issue:`7197` - Fix external builds with C++ modules enabled
* :hpx-issue:`7185` - Memory usage accumulates while iterating, using a sliding semaphore
* :hpx-issue:`7184` - Memory leak in overlapping relocation test functions
* :hpx-issue:`7167` - Compare performance of HPX's MPMC queue with other implementations
* :hpx-issue:`7158` - Potential Inconsistent State and Race Condition in hpx::lockfree::deque::empty()
* :hpx-issue:`7151` - Dynamic build-and-test workflow lost several previously excluded tests
* :hpx-issue:`7150` - Memory usage accumulates while creating tasks
* :hpx-issue:`7131` - Fix Sender Algorithm Customization
* :hpx-issue:`7124` - 1d_stencil_5 uses non-owning serialization for partition_data buffer
* :hpx-issue:`7117` - CircleCI container_algorithms shard uses partial ctest regex and runs unbuilt test target
* :hpx-issue:`7112` - Improve performance of SPSC queue used in work-requesting scheduler
* :hpx-issue:`7099` - [wrap] Enable hpx_main wrapping for local-only (non-distributed) builds
* :hpx-issue:`7091` - [Feature] NUMA-Distance-Aware Work Stealing in Schedulers
* :hpx-issue:`7087` - Unify and Restructure GitHub Actions Workflows via Composite Actions
* :hpx-issue:`7085` - thread_queue: batch the atomic decrement in cleanup_terminated_locked()
* :hpx-issue:`7077` - par policy silently falls back to sequential for non-contiguous iterators in all three uninitialized_relocate CPOs
* :hpx-issue:`7075` - [FEA] Implement CI Workflow using Slash Commands
* :hpx-issue:`7062` - Remove usage of deprecated asio::ip::tcp::resolver::query
* :hpx-issue:`7059` - HPX Build Configuration Error: Missing Asio Dependency
* :hpx-issue:`7052` - Segmented algorithms: Incorrect single-segment subrange handling + Few other bugs in scan.hpp
* :hpx-issue:`7050` - thread_queue: per-task heap allocation in staged queue could be further optimised
* :hpx-issue:`7049` - Introduce minimal tracing abstraction layer (hpx::tracing) for Tracy
* :hpx-issue:`7046` - Replace unsafe `std::strcat` with safer string operations in `print.cpp`
* :hpx-issue:`7040` - exception Safety Risk in `options_description_easy_init` Could Lead to Memory Leaks
* :hpx-issue:`7037` - `is_sorted` / `is_sorted_until` force class level template parameters in methods
* :hpx-issue:`7035` - hpx::compute::vector is missing standard std::vector methods (assign, at, const iterators)
* :hpx-issue:`7034` - Semantic Mismatch in Serialization Archive Flags
* :hpx-issue:`7030` - mpi::experimental::detail::async ignores MPI error codes from MPI_Ixxx calls, leading to potential hangs

Closed pull requests
====================

* :hpx-pr:`7581` - Raise documentation build step timeouts to restore headroom
* :hpx-pr:`7577` - Make fibhash return std::size_t
* :hpx-pr:`7567` - Keep LSU CI results when builds are interrupted
* :hpx-pr:`7566` - Add a 32 bit Windows CI job
* :hpx-pr:`7561` - performance_counters: discover counters registered after startup
* :hpx-pr:`7559` - make operator_brackets_proxy transparent to hpx::get for tuple-like references
* :hpx-pr:`7558` - build(deps): bump github/codeql-action from 4.37.9 to 4.38.0
* :hpx-pr:`7556` - fix: drop redundant HPX_CORE_EXPORT on version check definitions
* :hpx-pr:`7554` - Exclude docs from Codacy's duplication analysis
* :hpx-pr:`7552` - config: remove TBB example benchmarks and unused FindTBB module
* :hpx-pr:`7549` - Add a first draft of the V2.0.0 release notes
* :hpx-pr:`7548` - Port generate_issue_pr_list.sh from hub to the GitHub CLI
* :hpx-pr:`7546` - debugging: add regression test for hostname_print_helper race
* :hpx-pr:`7544` - tracing: sample per-task lifecycle events 1-in-N
* :hpx-pr:`7542` - Use an HPX-aware mutex in numa_binding_allocator::initialize_pages
* :hpx-pr:`7541` - Factor the duplicated AGAS instance-name formatting into a shared helper
* :hpx-pr:`7540` - Explicitly disable the use of TBB as the parallelization backend for libstdc++
* :hpx-pr:`7537` - Refactor disconnected locality dispatch guard
* :hpx-pr:`7536` - Factor the disconnected-locality dispatch guard into a shared helper
* :hpx-pr:`7535` - Fix data race in hostname_print_helper::get_hostname()"
* :hpx-pr:`7534` - Keep LSU matrix artifacts separate
* :hpx-pr:`7533` - Stop failed LSU builds from publishing installs
* :hpx-pr:`7532` - Fix LSU GitHub status reporting
* :hpx-pr:`7531` - Bound Slurm waits in LSU CI
* :hpx-pr:`7530` - Add feature build check for std::filesystem::display_string
* :hpx-pr:`7529` - Tracing: add per-subsystem gates for event classes
* :hpx-pr:`7528` - Tracy: bump to v0.14.1
* :hpx-pr:`7527` - Keep the caching allocator's thread_local lookup out of line
* :hpx-pr:`7526` - Avoid communicator reuse between collectives test phases
* :hpx-pr:`7525` - Fix data race in debug hostname printing
* :hpx-pr:`7524` - collectives, colocated, parcelset: drop whole-file device-code guards
* :hpx-pr:`7523` - async_distributed: add distributed tests for reflect sync, post, dataflow, and async_continue
* :hpx-pr:`7522` - docs: note HPX-specific names without std counterparts
* :hpx-pr:`7521` - Whiten the Dijkstra locality before the token is transmitted
* :hpx-pr:`7518` - config: skip the decltype form of HPX_FORWARD under nvcc
* :hpx-pr:`7516` - Bound the Dijkstra termination probe retry when the token cannot be delivered
* :hpx-pr:`7515` - async_distributed: add reflection overloads for async_continue, post_cb policy, and dataflow
* :hpx-pr:`7514` - Fill in documentation gaps for the tracing modules
* :hpx-pr:`7511` - parcelset,tracing: Emit Tracy events for parcel send and receive
* :hpx-pr:`7510` - Disable force_disconnect tests if not configured
* :hpx-pr:`7509` - async_distributed: add launch policy overloads for reflect sync and async_cb
* :hpx-pr:`7508` - examples: add factorial_reflection demonstrating C++26 reflection API
* :hpx-pr:`7507` - Make the nvcc CUDA configurations compile and pass again
* :hpx-pr:`7506` - Fix the two shutdown regressions from #7471 that hang the distributed CIs
* :hpx-pr:`7505` - Waiting for threads in pools to start running before continuing
* :hpx-pr:`7504` - build(deps): bump github/codeql-action from 4.37.8 to 4.37.9
* :hpx-pr:`7502` - Fix the -Werror=comment build break in reflect_action_overhead
* :hpx-pr:`7501` - Fixing apparent multi-line comment
* :hpx-pr:`7500` - Stop the colocated tests finalizing from inside the hpx_main loop
* :hpx-pr:`7499` - examples: rename background_work_smoke subsystems to fix HPX_WITH_CUDA build

