# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.

#
# arrow_util
#

# Headers: top level
arrow_install_all_headers("arrow/util")

#
# arrow_test_main
#

add_arrow_test(utility-test
               SOURCES
               checked-cast-test.cc
               key-value-metadata-test.cc
               hashing-test.cc
               int-util-test.cc
               io-util-test.cc
               lazy-test.cc
               parsing-util-test.cc
               stl-util-test.cc
               trie-test.cc
               utf8-util-test.cc)

add_arrow_test(bit-util-test)
add_arrow_test(compression-test)
add_arrow_test(decimal-test)
add_arrow_test(logging-test)
add_arrow_test(rle-encoding-test)
add_arrow_test(task-group-test)
add_arrow_test(thread-pool-test)
if(ARROW_WITH_URIPARSER)
  add_arrow_test(uri-test)
endif()

add_arrow_benchmark(bit-util-benchmark)
add_arrow_benchmark(compression-benchmark)
add_arrow_benchmark(decimal-benchmark)
add_arrow_benchmark(hashing-benchmark)
add_arrow_benchmark(int-util-benchmark)
add_arrow_benchmark(lazy-benchmark)
add_arrow_benchmark(machine-benchmark)
add_arrow_benchmark(number-parsing-benchmark)
add_arrow_benchmark(thread-pool-benchmark)
add_arrow_benchmark(trie-benchmark)
add_arrow_benchmark(utf8-util-benchmark)
