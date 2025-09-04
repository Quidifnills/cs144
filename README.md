<<<<<<< HEAD
Stanford CS 144 Networking Lab
==============================

These labs are open to the public under the (friendly) request that to
preserve their value as a teaching tool, solutions not be posted
publicly by anybody.

Website: https://cs144.stanford.edu

To set up the build system: `cmake -S . -B build`

To compile: `cmake --build build`

To run tests: `cmake --build build --target test`

To run speed benchmarks: `cmake --build build --target speed`

To run clang-tidy (which suggests improvements): `cmake --build build --target tidy`

To format code: `cmake --build build --target format`

==============================
My own note

## Step 1: Build
yiyi@yiyi-VirtualBox:~/cs144/CS144-2024-winter-backup$ cmake --build build
[ 15%] Built target minnow_debug
[ 26%] Built target stream_copy
[ 36%] Built target minnow_testing_debug
[ 78%] Built target util_debug
[ 94%] Built target tcp_native
[ 94%] Building CXX object apps/CMakeFiles/webget.dir/webget.cc.o
[100%] Linking CXX executable webget
[100%] Built target webget
## Step 2: Run
yiyi@yiyi-VirtualBox:~/cs144/CS144-2024-winter-backup$ ./build/apps/webget cs144.keithw.org /hello
HTTP/1.1 200 OK
Date: Thu, 04 Sep 2025 08:24:37 GMT
Server: Apache
Last-Modified: Thu, 13 Dec 2018 15:45:29 GMT
ETag: "e-57ce93446cb64"
Accept-Ranges: bytes
Content-Length: 14
Connection: close
Content-Type: text/plain

Hello, CS144!
## Step 3: Check
yiyi@yiyi-VirtualBox:~/cs144/CS144-2024-winter-backup$ cmake --build build --target check_webget
Test project /home/yiyi/cs144/CS144-2024-winter-backup/build
    Start 1: compile with bug-checkers
1/2 Test #1: compile with bug-checkers ........   Passed    0.38 sec
    Start 2: t_webget
2/2 Test #2: t_webget .........................   Passed    0.97 sec

100% tests passed, 0 tests failed out of 2

Total Test time (real) =   1.35 sec
Built target check_webget
=======
# cs144
>>>>>>> origin/main
