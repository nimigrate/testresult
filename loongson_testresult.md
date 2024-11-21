
reExitcodesDiffer
==============
### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --mm:refc --threads:off`
- category: dll
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  Traceback (most recent call last)
  nimhcr_unit.nim(110)     nimhcr_unit
  SIGILL: Illegal operation.
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --mm:refc --threads:off`
- category: dll
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   -d:nimDebugDlOpen --mm:refc --threads:off --nimCache:nimcache/tests/dll/nimhcr_unit.nim_10e2d4851f82de403faad30946150b31  tests/dll/nimhcr_unit.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/dll/nimhcr_unit.nim.cfg' [Conf]
  Hint:  [Link]
  Hint: mm: refc; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  39757 lines; 0.413s; 38.582MiB peakmem; proj: nimhcr_unit; out: nimhcr_unit [SuccessX]
  ```


### dll/nimhcr_basic.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --mm:refc --threads:off --forceBuild --hotCodeReloading:on`
- category: dll
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  Traceback (most recent call last)
  /home/loongson/build_nim/Nim/lib/nimhcr.nim(535) hcrInit
  /home/loongson/build_nim/Nim/lib/nimhcr.nim(507) initModules
  /home/loongson/build_nim/Nim/lib/nimhcr.nim(472) initGlobalScope
  SIGSEGV: Illegal storage access. (Attempt to read from nil?)
  ```


### dll/nimhcr_basic.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --mm:refc --threads:off --forceBuild --hotCodeReloading:on`
- category: dll
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   -d:nimDebugDlOpen --mm:refc --threads:off --forceBuild --hotCodeReloading:on  --nimCache:nimcache/tests/dll/nimhcr_basic.nim_b1d30cec8c7f8cb45c2f68201a9a3571  tests/dll/nimhcr_basic.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  CC: ../../lib/system/exceptions.nim
  CC: ../../lib/std/private/since.nim
  CC: ../../lib/system/ctypes.nim
  CC: ../../lib/std/sysatomics.nim
  CC: ../../lib/system/ansi_c.nim
  CC: ../../lib/system/memory.nim
  CC: ../../lib/std/private/digitsutils.nim
  CC: ../../lib/std/private/miscdollars.nim
  CC: ../../lib/std/assertions.nim
  CC: ../../lib/system/iterators.nim
  CC: ../../lib/system/coro_detection.nim
  CC: ../../lib/std/private/dragonbox.nim
  CC: ../../lib/std/private/schubfach.nim
  CC: ../../lib/std/formatfloat.nim
  CC: ../../lib/std/objectdollar.nim
  CC: ../../lib/system/dollars.nim
  CC: ../../lib/system/stacktraces.nim
  CC: ../../lib/std/private/bitops_utils.nim
  CC: ../../lib/system/countbits_impl.nim
  CC: ../../lib/std/private/syslocks.nim
  CC: ../../lib/std/widestrs.nim
  CC: ../../lib/std/syncio.nim
  CC: ../../lib/system.nim
  CC: nimhcr_basic.nim
  Link: ../../lib/system/exceptions.nim
  Link: ../../lib/std/private/since.nim
  Link: ../../lib/system/ctypes.nim
  Link: ../../lib/std/sysatomics.nim
  Link: ../../lib/system/ansi_c.nim
  Link: ../../lib/system/memory.nim
  Link: ../../lib/std/private/digitsutils.nim
  Link: ../../lib/std/private/miscdollars.nim
  Link: ../../lib/std/assertions.nim
  Link: ../../lib/system/iterators.nim
  Link: ../../lib/system/coro_detection.nim
  Link: ../../lib/std/private/dragonbox.nim
  Link: ../../lib/std/private/schubfach.nim
  Link: ../../lib/std/formatfloat.nim
  Link: ../../lib/std/objectdollar.nim
  Link: ../../lib/system/dollars.nim
  Link: ../../lib/system/stacktraces.nim
  Link: ../../lib/std/private/bitops_utils.nim
  Link: ../../lib/system/countbits_impl.nim
  Link: ../../lib/std/private/syslocks.nim
  Link: ../../lib/std/widestrs.nim
  Link: ../../lib/std/syncio.nim
  Link: ../../lib/system.nim
  Link: nimhcr_basic.nim
  Hint: mm: refc; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  37749 lines; 57.852s; 38.582MiB peakmem; proj: nimhcr_basic; out: nimhcr_basic [SuccessX]
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --mm:refc --threads:off`
- category: dll
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  SIGSEGV: Illegal storage access. (Attempt to read from nil?)
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --mm:refc --threads:off`
- category: dll
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   -d:nimDebugDlOpen -d:release --mm:refc --threads:off --nimCache:nimcache/tests/dll/nimhcr_unit.nim_53c97bedd7e85354cc92ab9bfbd3e050  tests/dll/nimhcr_unit.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/dll/nimhcr_unit.nim.cfg' [Conf]
  Hint:  [Link]
  Hint: mm: refc; opt: speed; options: -d:release
  39757 lines; 0.394s; 38.598MiB peakmem; proj: nimhcr_unit; out: nimhcr_unit [SuccessX]
  ```


### dll/nimhcr_basic.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --mm:refc --threads:off --forceBuild --hotCodeReloading:on`
- category: dll
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  ```


### dll/nimhcr_basic.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --mm:refc --threads:off --forceBuild --hotCodeReloading:on`
- category: dll
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   -d:nimDebugDlOpen -d:release --mm:refc --threads:off --forceBuild --hotCodeReloading:on  --nimCache:nimcache/tests/dll/nimhcr_basic.nim_ab299b9ce1260ff565c4086725efc31e  tests/dll/nimhcr_basic.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  CC: ../../lib/system/exceptions.nim
  CC: ../../lib/std/private/since.nim
  CC: ../../lib/system/ctypes.nim
  CC: ../../lib/std/sysatomics.nim
  CC: ../../lib/system/ansi_c.nim
  CC: ../../lib/system/memory.nim
  CC: ../../lib/std/private/digitsutils.nim
  CC: ../../lib/std/private/miscdollars.nim
  CC: ../../lib/std/assertions.nim
  CC: ../../lib/system/iterators.nim
  CC: ../../lib/system/coro_detection.nim
  CC: ../../lib/std/private/dragonbox.nim
  CC: ../../lib/std/private/schubfach.nim
  CC: ../../lib/std/formatfloat.nim
  CC: ../../lib/std/objectdollar.nim
  CC: ../../lib/system/dollars.nim
  CC: ../../lib/system/stacktraces.nim
  CC: ../../lib/std/private/bitops_utils.nim
  CC: ../../lib/system/countbits_impl.nim
  CC: ../../lib/std/private/syslocks.nim
  CC: ../../lib/std/widestrs.nim
  CC: ../../lib/std/syncio.nim
  CC: ../../lib/system.nim
  CC: nimhcr_basic.nim
  Link: ../../lib/system/exceptions.nim
  Link: ../../lib/std/private/since.nim
  Link: ../../lib/system/ctypes.nim
  Link: ../../lib/std/sysatomics.nim
  Link: ../../lib/system/ansi_c.nim
  Link: ../../lib/system/memory.nim
  Link: ../../lib/std/private/digitsutils.nim
  Link: ../../lib/std/private/miscdollars.nim
  Link: ../../lib/std/assertions.nim
  Link: ../../lib/system/iterators.nim
  Link: ../../lib/system/coro_detection.nim
  Link: ../../lib/std/private/dragonbox.nim
  Link: ../../lib/std/private/schubfach.nim
  Link: ../../lib/std/formatfloat.nim
  Link: ../../lib/std/objectdollar.nim
  Link: ../../lib/system/dollars.nim
  Link: ../../lib/system/stacktraces.nim
  Link: ../../lib/std/private/bitops_utils.nim
  Link: ../../lib/system/countbits_impl.nim
  Link: ../../lib/std/private/syslocks.nim
  Link: ../../lib/std/widestrs.nim
  Link: ../../lib/std/syncio.nim
  Link: ../../lib/system.nim
  Link: nimhcr_basic.nim
  Hint: mm: refc; opt: speed; options: -d:release
  37749 lines; 1.711s; 38.645MiB peakmem; proj: nimhcr_basic; out: nimhcr_basic [SuccessX]
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --threads:off`
- category: dll
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  Traceback (most recent call last)
  nimhcr_unit.nim(110)     nimhcr_unit
  SIGILL: Illegal operation.
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --threads:off`
- category: dll
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   -d:nimDebugDlOpen --threads:off --nimCache:nimcache/tests/dll/nimhcr_unit.nim_61c3d161fd222555f024b1c2205df233  tests/dll/nimhcr_unit.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/dll/nimhcr_unit.nim.cfg' [Conf]
  Hint:  [Link]
  Hint: mm: orc; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  38909 lines; 0.389s; 48.02MiB peakmem; proj: nimhcr_unit; out: nimhcr_unit [SuccessX]
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --threads:off`
- category: dll
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  SIGILL: Illegal operation.
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --threads:off`
- category: dll
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   -d:nimDebugDlOpen -d:release --threads:off --nimCache:nimcache/tests/dll/nimhcr_unit.nim_dedefe4c2b8e1e6b119a95efa055b922  tests/dll/nimhcr_unit.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/dll/nimhcr_unit.nim.cfg' [Conf]
  Hint:  [Link]
  Hint: mm: orc; opt: speed; options: -d:release
  38909 lines; 0.386s; 48.004MiB peakmem; proj: nimhcr_unit; out: nimhcr_unit [SuccessX]
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --gc:boehm --threads:off`
- category: dll
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  Traceback (most recent call last)
  nimhcr_unit.nim(110)     nimhcr_unit
  SIGILL: Illegal operation.
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --gc:boehm --threads:off`
- category: dll
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   -d:nimDebugDlOpen --gc:boehm --threads:off --nimCache:nimcache/tests/dll/nimhcr_unit.nim_94eb843698fdd6370c7eb241ed4be0ca  tests/dll/nimhcr_unit.nim
  command line(1, 2) Warning: `gc:option` is deprecated; use `mm:option` instead [Deprecated]
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/dll/nimhcr_unit.nim.cfg' [Conf]
  command line(1, 2) Warning: `gc:option` is deprecated; use `mm:option` instead [Deprecated]
  Hint:  [Link]
  Hint: mm: boehm; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  36613 lines; 0.328s; 38.582MiB peakmem; proj: nimhcr_unit; out: nimhcr_unit [SuccessX]
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --gc:boehm --threads:off`
- category: dll
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  SIGSEGV: Illegal storage access. (Attempt to read from nil?)
  ```


### dll/nimhcr_unit.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --gc:boehm --threads:off`
- category: dll
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   -d:nimDebugDlOpen -d:release --gc:boehm --threads:off --nimCache:nimcache/tests/dll/nimhcr_unit.nim_1cfdc4117b70131af20c9af5780556cc  tests/dll/nimhcr_unit.nim
  command line(1, 2) Warning: `gc:option` is deprecated; use `mm:option` instead [Deprecated]
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/dll/nimhcr_unit.nim.cfg' [Conf]
  command line(1, 2) Warning: `gc:option` is deprecated; use `mm:option` instead [Deprecated]
  Hint:  [Link]
  Hint: mm: boehm; opt: speed; options: -d:release
  36613 lines; 0.330s; 38.594MiB peakmem; proj: nimhcr_unit; out: nimhcr_unit [SuccessX]
  ```


### js/tnativeexc.nim
- backend: js
- argv: `js`
- category: js
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  /home/loongson/build_nim/Nim/tests/js/tnativeexc.js:770
      throw new Error(cbuf_33556640);
      ^
  
  Error: Error: unhandled exception: tnativeexc.nim(21, 3) `se.message == "Unexpected token \';\', \";;\" is not valid JSON"`  [AssertionDefect]
  Traceback (most recent call last)
  tnativeexc.nim(21) at module tnativeexc
  assertions.nim(41) at assertions.failedAssertImpl
  assertions.nim(36) at assertions.raiseAssert
  fatal.nim(53) at sysFatal.sysFatal
  
      at unhandledException (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:770:11)
      at raiseException (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:369:5)
      at sysFatal__stdZassertions_u45 (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:785:5)
      at raiseAssert__stdZassertions_u43 (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:796:5)
      at failedAssertImpl__stdZassertions_u85 (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:807:5)
      at Object.<anonymous> (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:873:1)
      at Module._compile (internal/modules/cjs/loader.js:1063:30)
      at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
      at Module.load (internal/modules/cjs/loader.js:928:32)
      at Function.Module._load (internal/modules/cjs/loader.js:769:14)
  ```


### js/tnativeexc.nim
- backend: js
- argv: `js`
- category: js
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim js --hints:on -d:testing --nimblePath:build/deps/pkgs2 -d:nodejs  --nimCache:nimcache/tests/js/tnativeexc.nim_32981a13284db7a021131df49e6cd203  tests/js/tnativeexc.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  tnativeexc.nim(22, 19) Hint: 'e' is declared but not used [XDeclaredButNotUsed]
  tnativeexc.nim(28, 19) Hint: 'e' is declared but not used [XDeclaredButNotUsed]
  tnativeexc.nim(9, 3) Warning: 'asm' for the JS target is deprecated, use the 'emit' pragma [Deprecated]
  tnativeexc.nim(17, 3) Warning: 'asm' for the JS target is deprecated, use the 'emit' pragma [Deprecated]
  tnativeexc.nim(27, 3) Warning: 'asm' for the JS target is deprecated, use the 'emit' pragma [Deprecated]
  Hint: opt: none (DEBUG BUILD, `-d:release` generates faster code)
  42059 lines; 0.319s; 48.043MiB peakmem; proj: tnativeexc; out: tnativeexc.js [SuccessX]
  ```


### js/tnativeexc.nim
- backend: js
- argv: `js '' -d:release`
- category: js
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  /home/loongson/build_nim/Nim/tests/js/tnativeexc.js:357
      throw new Error(cbuf_33556640);
      ^
  
  Error: Error: unhandled exception: tnativeexc.nim(21, 3) `se.message == "Unexpected token \';\', \";;\" is not valid JSON"`  [AssertionDefect]
  
      at unhandledException (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:357:11)
      at raiseException (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:245:5)
      at sysFatal__stdZassertions_u45 (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:368:5)
      at raiseAssert__stdZassertions_u43 (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:374:5)
      at failedAssertImpl__stdZassertions_u85 (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:380:5)
      at Object.<anonymous> (/home/loongson/build_nim/Nim/tests/js/tnativeexc.js:431:1)
      at Module._compile (internal/modules/cjs/loader.js:1063:30)
      at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
      at Module.load (internal/modules/cjs/loader.js:928:32)
      at Function.Module._load (internal/modules/cjs/loader.js:769:14)
  ```


### js/tnativeexc.nim
- backend: js
- argv: `js '' -d:release`
- category: js
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim js --hints:on -d:testing --nimblePath:build/deps/pkgs2 -d:nodejs  -d:release --nimCache:nimcache/tests/js/tnativeexc.nim_386c595610d30a2c775f5f3685f46f1b  tests/js/tnativeexc.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  tnativeexc.nim(22, 19) Hint: 'e' is declared but not used [XDeclaredButNotUsed]
  tnativeexc.nim(28, 19) Hint: 'e' is declared but not used [XDeclaredButNotUsed]
  tnativeexc.nim(9, 3) Warning: 'asm' for the JS target is deprecated, use the 'emit' pragma [Deprecated]
  tnativeexc.nim(17, 3) Warning: 'asm' for the JS target is deprecated, use the 'emit' pragma [Deprecated]
  tnativeexc.nim(27, 3) Warning: 'asm' for the JS target is deprecated, use the 'emit' pragma [Deprecated]
  Hint: opt: speed; options: -d:release
  42059 lines; 0.328s; 48.078MiB peakmem; proj: tnativeexc; out: tnativeexc.js [SuccessX]
  ```


### stdlib/thttpclient_ssl.nim
- backend: c
- argv: `c`
- category: stdlib
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  
  [Suite] SSL self signed certificate check
  threadpool.nim(372)      slave
  thttpclient_ssl.nim      runServerWrapper
  thttpclient_ssl.nim(49)  runServer
  net.nim(1315)            setSockOpt
  nativesockets.nim(749)   setSockOptInt
  oserrors.nim(92)         raiseOSError
  Error: unhandled exception: Protocol not available [OSError]
  ```


### stdlib/thttpclient_ssl.nim
- backend: c
- argv: `c`
- category: stdlib
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --mm:refc -d:ssl   --nimCache:nimcache/tests/stdlib/thttpclient_ssl.nim_4a8a08f09d37b73795649038408b5f33  tests/stdlib/thttpclient_ssl.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/stdlib/config.nims' [Conf]
  thttpclient_ssl.nim(28, 5) Warning: use the nimble packages `malebolgia`, `taskpools` or `weave` instead; threadpool is deprecated [Deprecated]
  thttpclient_ssl.nim(85, 3) template/generic instantiation of `suite` from here
  thttpclient_ssl.nim(87, 5) template/generic instantiation of `test` from here
  thttpclient_ssl.nim(98, 7) Warning: The bare except clause is deprecated; use `except CatchableError:` instead [BareExcept]
  thttpclient_ssl.nim(89, 11) Hint: 't' is declared but not used [XDeclaredButNotUsed]
  thttpclient_ssl.nim(85, 3) template/generic instantiation of `suite` from here
  thttpclient_ssl.nim(102, 5) template/generic instantiation of `test` from here
  thttpclient_ssl.nim(111, 7) Warning: The bare except clause is deprecated; use `except CatchableError:` instead [BareExcept]
  thttpclient_ssl.nim(104, 11) Hint: 't' is declared but not used [XDeclaredButNotUsed]
  thttpclient_ssl.nim(85, 3) template/generic instantiation of `suite` from here
  thttpclient_ssl.nim(116, 5) template/generic instantiation of `test` from here
  thttpclient_ssl.nim(127, 7) Warning: The bare except clause is deprecated; use `except CatchableError:` instead [BareExcept]
  thttpclient_ssl.nim(118, 11) Hint: 't' is declared but not used [XDeclaredButNotUsed]
  thttpclient_ssl.nim(85, 3) template/generic instantiation of `suite` from here
  thttpclient_ssl.nim(136, 5) template/generic instantiation of `test` from here
  thttpclient_ssl.nim(146, 7) Warning: The bare except clause is deprecated; use `except CatchableError:` instead [BareExcept]
  thttpclient_ssl.nim(138, 11) Hint: 't' is declared but not used [XDeclaredButNotUsed]
  Hint:  [Link]
  Hint: mm: refc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  101850 lines; 2.080s; 142.129MiB peakmem; proj: thttpclient_ssl; out: thttpclient_ssl [SuccessX]
  ```


### stdlib/tsocketstreams.nim
- backend: c
- argv: `c --mm:refc`
- category: stdlib
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  OM
  NIM
  3
  NIM
  NIM
  tsocketstreams.nim(38)   tsocketstreams
  net.nim(1315)            setSockOpt
  nativesockets.nim(749)   setSockOptInt
  oserrors.nim(92)         raiseOSError
  Error: unhandled exception: Protocol not available [OSError]
  ```


### stdlib/tsocketstreams.nim
- backend: c
- argv: `c --mm:refc`
- category: stdlib
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/stdlib/tsocketstreams.nim_4a8a08f09d37b73795649038408b5f33 --mm:refc tests/stdlib/tsocketstreams.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/stdlib/config.nims' [Conf]
  CC: ../../lib/system/exceptions.nim
  CC: ../../lib/system/ctypes.nim
  CC: ../../lib/std/private/digitsutils.nim
  CC: ../../lib/std/assertions.nim
  CC: ../../lib/system/dollars.nim
  CC: ../../lib/system.nim
  CC: ../../lib/pure/strutils.nim
  CC: ../../lib/std/oserrors.nim
  CC: ../../lib/pure/options.nim
  CC: ../../lib/pure/times.nim
  CC: ../../lib/std/envvars.nim
  CC: ../../lib/std/cmdline.nim
  CC: ../../lib/pure/nativesockets.nim
  CC: ../../lib/pure/net.nim
  CC: ../../lib/pure/streams.nim
  CC: ../../lib/std/socketstreams.nim
  CC: tsocketstreams.nim
  Hint:  [Link]
  Hint: mm: refc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  79779 lines; 1.675s; 92MiB peakmem; proj: tsocketstreams; out: tsocketstreams [SuccessX]
  ```


### stdlib/tsocketstreams.nim
- backend: c
- argv: `c --mm:orc`
- category: stdlib
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  OM
  NIM
  3
  NIM
  NIM
  tsocketstreams.nim(38)   tsocketstreams
  net.nim(1315)            setSockOpt
  nativesockets.nim(749)   setSockOptInt
  oserrors.nim(92)         raiseOSError
  Error: unhandled exception: Protocol not available [OSError]
  ```


### stdlib/tsocketstreams.nim
- backend: c
- argv: `c --mm:orc`
- category: stdlib
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/stdlib/tsocketstreams.nim_4a8a08f09d37b73795649038408b5f33 --mm:orc tests/stdlib/tsocketstreams.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/stdlib/config.nims' [Conf]
  CC: ../../lib/system/exceptions.nim
  CC: ../../lib/system/ctypes.nim
  CC: ../../lib/std/private/digitsutils.nim
  CC: ../../lib/std/assertions.nim
  CC: ../../lib/system/dollars.nim
  CC: ../../lib/system.nim
  CC: ../../lib/pure/strutils.nim
  CC: ../../lib/std/oserrors.nim
  CC: ../../lib/pure/options.nim
  CC: ../../lib/pure/times.nim
  CC: ../../lib/std/envvars.nim
  CC: ../../lib/std/cmdline.nim
  CC: ../../lib/pure/nativesockets.nim
  CC: ../../lib/pure/net.nim
  CC: ../../lib/pure/streams.nim
  CC: ../../lib/std/socketstreams.nim
  CC: tsocketstreams.nim
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  78734 lines; 33.397s; 114.379MiB peakmem; proj: tsocketstreams; out: tsocketstreams [SuccessX]
  ```


### testament/tshould_not_work.nim
- backend: c
- argv: `c`
- category: testament
- action: run
- expected:   
  ```
  exitcode: 0
  ```
- given:   
  ```
  exitcode: 1
  
  Output:
  tshould_not_work.nim(53) tshould_not_work
  tshould_not_work.nim(52) main
  assertions.nim(41)       failedAssertImpl
  assertions.nim(36)       raiseAssert
  fatal.nim(53)            sysFatal
  Error: unhandled exception: tshould_not_work.nim(52, 3) `ok` 
  expected:
  FAIL: tests/shouldfail/tccodecheck.nim
  Failure: reCodegenFailure
  Expected:
  baz
  FAIL: tests/shouldfail/tcolumn.nim
  Failure: reLinesDiffer
  FAIL: tests/shouldfail/terrormsg.nim
  Failure: reMsgsDiffer
  FAIL: tests/shouldfail/texitcode1.nim
  Failure: reExitcodesDiffer
  FAIL: tests/shouldfail/tfile.nim
  Failure: reFilesDiffer
  FAIL: tests/shouldfail/tline.nim
  Failure: reLinesDiffer
  FAIL: tests/shouldfail/tmaxcodesize.nim
  Failure: reCodegenFailure
  max allowed size: 1
  FAIL: tests/shouldfail/tnimout.nim
  Failure: reMsgsDiffer
  FAIL: tests/shouldfail/tnimoutfull.nim
  Failure: reMsgsDiffer
  FAIL: tests/shouldfail/toutput.nim
  Failure: reOutputsDiffer
  FAIL: tests/shouldfail/toutputsub.nim
  Failure: reOutputsDiffer
  FAIL: tests/shouldfail/treject.nim
  Failure: reFilesDiffer
  FAIL: tests/shouldfail/tsortoutput.nim
  Failure: reOutputsDiffer
  FAIL: tests/shouldfail/ttimeout.nim
  Failure: reTimeout
  FAIL: tests/shouldfail/tvalgrind.nim
  Failure: reExitcodesDiffer
  
  outp:
  FAIL: tests/shouldfail/tccodecheck.nim c                           ( 0.54 sec)
  Test "tests/shouldfail/tccodecheck.nim" in category "shouldfail"
  Failure: reCodegenFailure
  Expected:
  baz
  
  Gotten:
  
  
  diff --git a/tmp/diffStrings_a_xuUIC6I7 b/tmp/diffStrings_b_BEPj6abG
  index 3f9538666..e69de29bb 100644
  --- a/tmp/diffStrings_a_xuUIC6I7
  +++ b/tmp/diffStrings_b_BEPj6abG
  @@ -1 +0,0 @@
  -baz
  \ No newline at end of file
  
  FAIL: tests/shouldfail/tcolumn.nim c                               ( 0.48 sec)
  Test "tests/shouldfail/tcolumn.nim" in category "shouldfail"
  Failure: reLinesDiffer
  Expected:
  9:7
  
  Gotten:
  8:6
  
  diff --git a/tmp/diffStrings_a_pDcvfUmn b/tmp/diffStrings_b_zujMJHOh
  index 61be3f2a6..f581d95f9 100644
  --- a/tmp/diffStrings_a_pDcvfUmn
  +++ b/tmp/diffStrings_b_zujMJHOh
  @@ -1 +1 @@
  -9:7
  \ No newline at end of file
  +8:6
  \ No newline at end of file
  
  FAIL: tests/shouldfail/terrormsg.nim c                             ( 0.49 sec)
  Test "tests/shouldfail/terrormsg.nim" in category "shouldfail"
  Failure: reMsgsDiffer
  Expected:
  wrong error message
  
  Gotten:
  undeclared identifier: 'undeclared'
  
  diff --git a/tmp/diffStrings_a_LDFCM0Zt b/tmp/diffStrings_b_AttGrslS
  index 3f537439b..af5686c0f 100644
  --- a/tmp/diffStrings_a_LDFCM0Zt
  +++ b/tmp/diffStrings_b_AttGrslS
  @@ -1 +1 @@
  -wrong error message
  \ No newline at end of file
  +undeclared identifier: 'undeclared'
  \ No newline at end of file
  
  FAIL: tests/shouldfail/texitcode1.nim c                            ( 0.53 sec)
  Test "tests/shouldfail/texitcode1.nim" in category "shouldfail"
  Failure: reExitcodesDiffer
  Expected:
  exitcode: 1
  
  Gotten:
  exitcode: 0
  
  Output:
  
  
  diff --git a/tmp/diffStrings_a_16dBI0wV b/tmp/diffStrings_b_oD5CdRiM
  index 2b81d49cb..da603a512 100644
  --- a/tmp/diffStrings_a_16dBI0wV
  +++ b/tmp/diffStrings_b_oD5CdRiM
  @@ -1 +1,3 @@
  -exitcode: 1
  \ No newline at end of file
  +exitcode: 0
  +
  +Output:
  
  FAIL: tests/shouldfail/texitcode1.nim c                            ( 0.54 sec)
  Test "tests/shouldfail/texitcode1.nim" in category "shouldfail"
  Failure: reExitcodesDiffer
  Expected:
  
  
  Gotten:
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/shouldfail/texitcode1.nim_4a8a08f09d37b73795649038408b5f33  tests/shouldfail/texitcode1.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  .....................................................................
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  28219 lines; 0.365s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/texitcode1.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/texitcode1 [SuccessX]
  
  
  diff --git a/tmp/diffStrings_a_XeCOI1ee b/tmp/diffStrings_b_rY1zOIMr
  index e69de29bb..5ad2188de 100644
  --- a/tmp/diffStrings_a_XeCOI1ee
  +++ b/tmp/diffStrings_b_rY1zOIMr
  @@ -0,0 +1,7 @@
  +$ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/shouldfail/texitcode1.nim_4a8a08f09d37b73795649038408b5f33  tests/shouldfail/texitcode1.nim
  +Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  +Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  +.....................................................................
  +Hint:  [Link]
  +Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  +28219 lines; 0.365s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/texitcode1.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/texitcode1 [SuccessX]
  
  FAIL: tests/shouldfail/tfile.nim c                                 ( 0.49 sec)
  Test "tests/shouldfail/tfile.nim" in category "shouldfail"
  Failure: reFilesDiffer
  Expected:
  notthisfile.nim
  
  Gotten:
  tfile.nim
  
  diff --git a/tmp/diffStrings_a_P3AiIrWi b/tmp/diffStrings_b_teunpbOc
  index 31496a0f7..c5ca60e2b 100644
  --- a/tmp/diffStrings_a_P3AiIrWi
  +++ b/tmp/diffStrings_b_teunpbOc
  @@ -1 +1 @@
  -notthisfile.nim
  \ No newline at end of file
  +tfile.nim
  \ No newline at end of file
  
  FAIL: tests/shouldfail/tline.nim c                                 ( 0.49 sec)
  Test "tests/shouldfail/tline.nim" in category "shouldfail"
  Failure: reLinesDiffer
  Expected:
  10:6
  
  Gotten:
  8:6
  
  diff --git a/tmp/diffStrings_a_hlZyzZNe b/tmp/diffStrings_b_mY6N34AT
  index 097944196..f581d95f9 100644
  --- a/tmp/diffStrings_a_hlZyzZNe
  +++ b/tmp/diffStrings_b_mY6N34AT
  @@ -1 +1 @@
  -10:6
  \ No newline at end of file
  +8:6
  \ No newline at end of file
  
  FAIL: tests/shouldfail/tmaxcodesize.nim c                          ( 0.52 sec)
  Test "tests/shouldfail/tmaxcodesize.nim" in category "shouldfail"
  Failure: reCodegenFailure
  Expected:
  max allowed size: 1
  
  Gotten:
  generated code size: 3900
  
  diff --git a/tmp/diffStrings_a_vchsvxQl b/tmp/diffStrings_b_nrp4VZOd
  index 939aae198..127796420 100644
  --- a/tmp/diffStrings_a_vchsvxQl
  +++ b/tmp/diffStrings_b_nrp4VZOd
  @@ -1 +1 @@
  -max allowed size: 1
  \ No newline at end of file
  +generated code size: 3900
  \ No newline at end of file
  
  FAIL: tests/shouldfail/tnimout.nim c                               ( 0.53 sec)
  Test "tests/shouldfail/tnimout.nim" in category "shouldfail"
  Failure: reMsgsDiffer
  Expected:
  Hello World!
  
  Gotten:
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  .....................................................................
  something else
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  28223 lines; 0.371s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tnimout.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tnimout [SuccessX]
  
  diff --git a/tmp/diffStrings_a_ct9LTGet b/tmp/diffStrings_b_Rjfpv4Ml
  index c57eff55e..a72a44a59 100644
  --- a/tmp/diffStrings_a_ct9LTGet
  +++ b/tmp/diffStrings_b_Rjfpv4Ml
  @@ -1 +1,7 @@
  -Hello World!
  \ No newline at end of file
  +Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  +Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  +.....................................................................
  +something else
  +Hint:  [Link]
  +Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  +28223 lines; 0.371s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tnimout.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tnimout [SuccessX]
  \ No newline at end of file
  
  FAIL: tests/shouldfail/tnimoutfull.nim c                           ( 0.53 sec)
  Test "tests/shouldfail/tnimoutfull.nim" in category "shouldfail"
  Failure: reMsgsDiffer
  Expected:
  msg1
  msg2
  
  
  Gotten:
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  .....................................................................
  msg1
  msg2
  msg3
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  28230 lines; 0.377s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tnimoutfull.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tnimoutfull [SuccessX]
  
  diff --git a/tmp/diffStrings_a_jJ9zMdll b/tmp/diffStrings_b_BCVk0obo
  index a252626cc..2b0ac4e9e 100644
  --- a/tmp/diffStrings_a_jJ9zMdll
  +++ b/tmp/diffStrings_b_BCVk0obo
  @@ -1,2 +1,9 @@
  +Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  +Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  +.....................................................................
   msg1
   msg2
  +msg3
  +Hint:  [Link]
  +Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  +28230 lines; 0.377s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tnimoutfull.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tnimoutfull [SuccessX]
  \ No newline at end of file
  
  FAIL: tests/shouldfail/toutput.nim c                               ( 0.53 sec)
  Test "tests/shouldfail/toutput.nim" in category "shouldfail"
  Failure: reOutputsDiffer
  Expected:
    done
    
  
  Gotten:
  broken
  
  
  diff --git a/tmp/diffStrings_a_4fQ9mYNK b/tmp/diffStrings_b_PIby9iKM
  index b2eb021b0..57f89ed17 100644
  --- a/tmp/diffStrings_a_4fQ9mYNK
  +++ b/tmp/diffStrings_b_PIby9iKM
  @@ -1,2 +1 @@
  -  done
  -  
  \ No newline at end of file
  +broken
  
  FAIL: tests/shouldfail/toutput.nim c                               ( 0.53 sec)
  Test "tests/shouldfail/toutput.nim" in category "shouldfail"
  Failure: reOutputsDiffer
  Expected:
  
  
  Gotten:
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/shouldfail/toutput.nim_4a8a08f09d37b73795649038408b5f33  tests/shouldfail/toutput.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  .....................................................................
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  28223 lines; 0.373s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/toutput.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/toutput [SuccessX]
  
  
  diff --git a/tmp/diffStrings_a_IKp9D1pd b/tmp/diffStrings_b_JMmeQQhr
  index e69de29bb..fa0ca6587 100644
  --- a/tmp/diffStrings_a_IKp9D1pd
  +++ b/tmp/diffStrings_b_JMmeQQhr
  @@ -0,0 +1,7 @@
  +$ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/shouldfail/toutput.nim_4a8a08f09d37b73795649038408b5f33  tests/shouldfail/toutput.nim
  +Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  +Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  +.....................................................................
  +Hint:  [Link]
  +Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  +28223 lines; 0.373s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/toutput.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/toutput [SuccessX]
  
  FAIL: tests/shouldfail/toutputsub.nim c                            ( 0.52 sec)
  Test "tests/shouldfail/toutputsub.nim" in category "shouldfail"
  Failure: reOutputsDiffer
  Expected:
  something else
  
  Gotten:
  Hello World!
  
  
  diff --git a/tmp/diffStrings_a_NFH6cw84 b/tmp/diffStrings_b_ObCL1EI2
  index 339f0be6c..980a0d5f1 100644
  --- a/tmp/diffStrings_a_NFH6cw84
  +++ b/tmp/diffStrings_b_ObCL1EI2
  @@ -1 +1 @@
  -something else
  \ No newline at end of file
  +Hello World!
  
  FAIL: tests/shouldfail/toutputsub.nim c                            ( 0.52 sec)
  Test "tests/shouldfail/toutputsub.nim" in category "shouldfail"
  Failure: reOutputsDiffer
  Expected:
  
  
  Gotten:
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/shouldfail/toutputsub.nim_4a8a08f09d37b73795649038408b5f33  tests/shouldfail/toutputsub.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  .....................................................................
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  28221 lines; 0.362s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/toutputsub.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/toutputsub [SuccessX]
  
  
  diff --git a/tmp/diffStrings_a_hg8l7o51 b/tmp/diffStrings_b_d9augE8K
  index e69de29bb..8ff4edd4c 100644
  --- a/tmp/diffStrings_a_hg8l7o51
  +++ b/tmp/diffStrings_b_d9augE8K
  @@ -0,0 +1,7 @@
  +$ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/shouldfail/toutputsub.nim_4a8a08f09d37b73795649038408b5f33  tests/shouldfail/toutputsub.nim
  +Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  +Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  +.....................................................................
  +Hint:  [Link]
  +Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  +28221 lines; 0.362s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/toutputsub.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/toutputsub [SuccessX]
  
  FAIL: tests/shouldfail/treject.nim c                               ( 0.52 sec)
  Test "tests/shouldfail/treject.nim" in category "shouldfail"
  Failure: reFilesDiffer
  Expected:
  tests/shouldfail/treject.nim
  
  Gotten:
  
  
  diff --git a/tmp/diffStrings_a_8nacNAK6 b/tmp/diffStrings_b_oaNyp8ye
  index f530febe7..e69de29bb 100644
  --- a/tmp/diffStrings_a_8nacNAK6
  +++ b/tmp/diffStrings_b_oaNyp8ye
  @@ -1 +0,0 @@
  -tests/shouldfail/treject.nim
  \ No newline at end of file
  
  FAIL: tests/shouldfail/treject.nim c                               ( 0.52 sec)
  Test "tests/shouldfail/treject.nim" in category "shouldfail"
  Failure: reExitcodesDiffer
  Expected:
  exitcode: 1
  
  Gotten:
  exitcode: 0
  
  Output:
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  .....................................................................
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  28223 lines; 0.364s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/treject.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/treject [SuccessX]
  
  
  diff --git a/tmp/diffStrings_a_iLhQqfP0 b/tmp/diffStrings_b_h6WaQ7De
  index 2b81d49cb..475270948 100644
  --- a/tmp/diffStrings_a_iLhQqfP0
  +++ b/tmp/diffStrings_b_h6WaQ7De
  @@ -1 +1,9 @@
  -exitcode: 1
  \ No newline at end of file
  +exitcode: 0
  +
  +Output:
  +Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  +Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  +.....................................................................
  +Hint:  [Link]
  +Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  +28223 lines; 0.364s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/treject.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/treject [SuccessX]
  
  FAIL: tests/shouldfail/tsortoutput.nim c                           ( 0.53 sec)
  Test "tests/shouldfail/tsortoutput.nim" in category "shouldfail"
  Failure: reOutputsDiffer
  Expected:
  2
  1
  
  
  Gotten:
  1
  2
  
  
  diff --git a/tmp/diffStrings_a_qdFv18pc b/tmp/diffStrings_b_H28Dedyr
  index 5f1d0ecea..1191247b6 100644
  --- a/tmp/diffStrings_a_qdFv18pc
  +++ b/tmp/diffStrings_b_H28Dedyr
  @@ -1,2 +1,2 @@
  -2
   1
  +2
  
  FAIL: tests/shouldfail/tsortoutput.nim c                           ( 0.53 sec)
  Test "tests/shouldfail/tsortoutput.nim" in category "shouldfail"
  Failure: reOutputsDiffer
  Expected:
  
  
  Gotten:
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/shouldfail/tsortoutput.nim_4a8a08f09d37b73795649038408b5f33  tests/shouldfail/tsortoutput.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  .....................................................................
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  28227 lines; 0.361s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tsortoutput.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tsortoutput [SuccessX]
  
  
  diff --git a/tmp/diffStrings_a_hn9ZK2Hh b/tmp/diffStrings_b_L2KRmFQD
  index e69de29bb..fd349940d 100644
  --- a/tmp/diffStrings_a_hn9ZK2Hh
  +++ b/tmp/diffStrings_b_L2KRmFQD
  @@ -0,0 +1,7 @@
  +$ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/shouldfail/tsortoutput.nim_4a8a08f09d37b73795649038408b5f33  tests/shouldfail/tsortoutput.nim
  +Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  +Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  +.....................................................................
  +Hint:  [Link]
  +Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  +28227 lines; 0.361s; 30.957MiB peakmem; proj: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tsortoutput.nim; out: /home/loongson/build_nim/Nim/testament/tests/shouldfail/tsortoutput [SuccessX]
  
  FAIL: tests/shouldfail/ttimeout.nim c                              ( 2.29 sec)
  Test "tests/shouldfail/ttimeout.nim" in category "shouldfail"
  Failure: reTimeout
  Expected:
  
  
  Gotten:
  
  
  
  oserrors.nim(92)         raiseOSError
  Error: unhandled exception: No such file or directory
  Additional info: Could not find command: 'valgrind'. OS error: No such file or directory [OSError]
   [AssertionDefect]
  ```


### testament/tshould_not_work.nim
- backend: c
- argv: `c`
- category: testament
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/testament/tshould_not_work.nim_4a8a08f09d37b73795649038408b5f33  tests/testament/tshould_not_work.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint:  [Link]
  Hint: mm: orc; threads: on; opt: none (DEBUG BUILD, `-d:release` generates faster code)
  69122 lines; 1.281s; 91.824MiB peakmem; proj: tshould_not_work; out: tshould_not_work [SuccessX]
  ```




reNimcCrash
==============
### compiler/tasm.nim
- backend: c
- argv: `c`
- category: compiler
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/compiler/tasm.nim_4a8a08f09d37b73795649038408b5f33  tests/compiler/tasm.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/compiler/nim.cfg' [Conf]
  CC: tasm.nim
  /tmp/ccIqhoV5.s: Assembler messages:
  /tmp/ccIqhoV5.s:182: 致命错误：no match insn: mov	$r12,$r12
  Error: execution of an external compiler program 'gcc -c  -w -fmax-errors=3 -pthread -std=c99   -I/home/loongson/build_nim/Nim/lib -I/home/loongson/build_nim/Nim/tests/compiler -o /home/loongson/build_nim/Nim/nimcache/tests/compiler/tasm.nim_4a8a08f09d37b73795649038408b5f33/@mtasm.nim.c.o /home/loongson/build_nim/Nim/nimcache/tests/compiler/tasm.nim_4a8a08f09d37b73795649038408b5f33/@mtasm.nim.c' failed with exit code: 1
  
  
  ```


### cpp/tasync_cpp.nim
- backend: cpp
- argv: `cpp`
- category: cpp
- action: run
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim cpp --clearNimblePath --nimblePath:build/deps/pkgs2 tests/cpp/tasync_cpp.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  tasync_cpp.nim(9, 8) Error: cannot open file: jester
  ```


### manyloc/keineschweine/keineschweine.nim
- backend: c
- argv: `c`
- category: manyloc
- action: compile
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/manyloc/keineschweine/keineschweine.nim_4a8a08f09d37b73795649038408b5f33  tests/manyloc/keineschweine/keineschweine.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/manyloc/keineschweine/keineschweine.nim.cfg' [Conf]
  dependencies/sfml/sfml.nim(1116, 6) Hint: 'perpendicular' is declared but not used [XDeclaredButNotUsed]
  dependencies/sfml/sfml.nim(1119, 6) Hint: 'cross' is declared but not used [XDeclaredButNotUsed]
  dependencies/chipmunk/chipmunk.nim(1279, 10) Hint: 'defConstraintProp' is declared but not used [XDeclaredButNotUsed]
  dependencies/genpacket/macro_dsl.nim(44, 25) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/macro_dsl.nim(44, 15) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/macro_dsl.nim(50, 19) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/macro_dsl.nim(50, 13) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/macro_dsl.nim(48, 7) Hint: '?' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(155, 15) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(156, 17) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(167, 25) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(168, 25) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(183, 25) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(184, 25) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(321, 25) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(322, 25) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(378, 35) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(379, 54) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(380, 37) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(412, 40) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(414, 24) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(428, 17) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(543, 41) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(557, 34) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(559, 43) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(604, 42) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/enet/enet.nim(242, 3) Hint: 'ENET_HOST_RECEIVE_BUFFER_SIZE' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(243, 3) Hint: 'ENET_HOST_SEND_BUFFER_SIZE' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(244, 3) Hint: 'ENET_HOST_BANDWIDTH_THROTTLE_INTERVAL' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(245, 3) Hint: 'ENET_HOST_DEFAULT_MTU' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(247, 3) Hint: 'ENET_PEER_DEFAULT_ROUND_TRIP_TIME' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(248, 3) Hint: 'ENET_PEER_DEFAULT_PACKET_THROTTLE' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(249, 3) Hint: 'ENET_PEER_PACKET_THROTTLE_SCALE' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(250, 3) Hint: 'ENET_PEER_PACKET_THROTTLE_COUNTER' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(251, 3) Hint: 'ENET_PEER_PACKET_THROTTLE_ACCELERATION' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(252, 3) Hint: 'ENET_PEER_PACKET_THROTTLE_DECELERATION' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(253, 3) Hint: 'ENET_PEER_PACKET_THROTTLE_INTERVAL' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(254, 3) Hint: 'ENET_PEER_PACKET_LOSS_SCALE' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(255, 3) Hint: 'ENET_PEER_PACKET_LOSS_INTERVAL' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(256, 3) Hint: 'ENET_PEER_WINDOW_SIZE_SCALE' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(257, 3) Hint: 'ENET_PEER_TIMEOUT_LIMIT' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(258, 3) Hint: 'ENET_PEER_TIMEOUT_MINIMUM' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(259, 3) Hint: 'ENET_PEER_TIMEOUT_MAXIMUM' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(260, 3) Hint: 'ENET_PEER_PING_INTERVAL' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(261, 3) Hint: 'ENET_PEER_UNSEQUENCED_WINDOWS' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(263, 3) Hint: 'ENET_PEER_FREE_UNSEQUENCED_WINDOWS' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(265, 3) Hint: 'ENET_PEER_RELIABLE_WINDOW_SIZE' is declared but not used [XDeclaredButNotUsed]
  dependencies/enet/enet.nim(266, 3) Hint: 'ENET_PEER_FREE_RELIABLE_WINDOWS' is declared but not used [XDeclaredButNotUsed]
  lib/estreams.nim(41, 34) Warning: use `char` or `uint8` instead; cuchar is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(21, 35) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(21, 25) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(44, 39) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(44, 29) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(66, 33) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(66, 12) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(73, 53) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(73, 44) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(105, 30) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(105, 12) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(112, 68) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(112, 50) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(115, 68) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(115, 50) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(140, 33) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(140, 23) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(209, 29) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(209, 19) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(224, 29) Warning: Deprecated since version 0.18.1; All functionality is defined on 'NimNode'.; ident is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(224, 10) Warning: Deprecated since version 0.18.1; Use 'strVal' instead.; $ is deprecated [Deprecated]
  dependencies/genpacket/genpacket_enet.nim(206, 5) Hint: 'streamID' is declared but not used [XDeclaredButNotUsed]
  dependencies/genpacket/genpacket_enet.nim(1, 27) Warning: imported and not used: 'estreams' [UnusedImport]
  dependencies/genpacket/genpacket_enet.nim(2, 6) Warning: imported and not used: 'strutils' [UnusedImport]
  
  proc readMD5Digest*(s: PBuffer = nil): MD5Digest =
    read(s, result[0])
    read(s, result[1])
    read(s, result[2])
    read(s, result[3])
    read(s, result[4])
    read(s, result[5])
    read(s, result[6])
    read(s, result[7])
    read(s, result[8])
    read(s, result[9])
    read(s, result[10])
    read(s, result[11])
    read(s, result[12])
    read(s, result[13])
    read(s, result[14])
    read(s, result[15])
  
  proc pack*(s: PBuffer = nil; p: var MD5Digest) =
    writeBE(s, p[0])
    writeBE(s, p[1])
    writeBE(s, p[2])
    writeBE(s, p[3])
    writeBE(s, p[4])
    writeBE(s, p[5])
    writeBE(s, p[6])
    writeBE(s, p[7])
    writeBE(s, p[8])
    writeBE(s, p[9])
    writeBE(s, p[10])
    writeBE(s, p[11])
    writeBE(s, p[12])
    writeBE(s, p[13])
    writeBE(s, p[14])
    writeBE(s, p[15])
  
  dependencies/genpacket/genpacket_enet.nim(9, 18) Warning: imported and not used: 'macro_dsl' [UnusedImport]
  lib/sg_packets.nim(3, 44) Warning: imported and not used: 'enet' [UnusedImport]
  dependencies/genpacket/genpacket_enet.nim(9, 10) Warning: imported and not used: 'macros' [UnusedImport]
  lib/zlib_helpers.nim(3, 11) Error: cannot open file: zip/zlib
  ```


### manyloc/nake/nakefile.nim
- backend: c
- argv: `c`
- category: manyloc
- action: compile
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim c --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/manyloc/nake/nakefile.nim_4a8a08f09d37b73795649038408b5f33  tests/manyloc/nake/nakefile.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/manyloc/nake/nakefile.nim.cfg' [Conf]
  nake.nim(10, 18) Warning: imported and not used: 'parseopt' [UnusedImport]
  nakefile.nim(2, 23) Error: cannot open file: zip/zipfiles
  ```


### niminaction/Chapter8/sfml/sfml_test.nim
- backend: cpp
- argv: `cpp`
- category: niminaction
- action: compile
- expected: *None*
- given:   
  ```
  $ /home/loongson/build_nim/Nim/bin/nim cpp --hints:on -d:testing --nimblePath:build/deps/pkgs2   --nimCache:nimcache/tests/niminaction/Chapter8/sfml/sfml_test.nim_2c5f2cba9af7f92986d3de1e753f3faa  tests/niminaction/Chapter8/sfml/sfml_test.nim
  Hint: used config file '/home/loongson/build_nim/Nim/config/nim.cfg' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/config/config.nims' [Conf]
  Hint: used config file '/home/loongson/build_nim/Nim/tests/config.nims' [Conf]
  CC: sfml_test.nim
  /home/loongson/build_nim/Nim/nimcache/tests/niminaction/Chapter8/sfml/sfml_test.nim_2c5f2cba9af7f92986d3de1e753f3faa/@msfml_test.nim.cpp:8:10: fatal error: SFML/Graphics.hpp: 没有那个文件或目录
   #include <SFML/Graphics.hpp>
            ^~~~~~~~~~~~~~~~~~~
  compilation terminated.
  Error: execution of an external compiler program 'g++ -c -std=gnu++17 -funsigned-char  -w -fmax-errors=3 -fpermissive -pthread   -I/home/loongson/build_nim/Nim/lib -I/home/loongson/build_nim/Nim/tests/niminaction/Chapter8/sfml -o /home/loongson/build_nim/Nim/nimcache/tests/niminaction/Chapter8/sfml/sfml_test.nim_2c5f2cba9af7f92986d3de1e753f3faa/@msfml_test.nim.cpp.o /home/loongson/build_nim/Nim/nimcache/tests/niminaction/Chapter8/sfml/sfml_test.nim_2c5f2cba9af7f92986d3de1e753f3faa/@msfml_test.nim.cpp' failed with exit code: 1
  
  
  ```




reDisabled
==============
### array/t15117.nim
- backend: c
- argv: `c --cc:vcc`
- category: array
- action: run
- expected: *None*
- given: *None*


### alloc/tmembug2.nim
- backend: c
- argv: `c`
- category: alloc
- action: run
- expected: *None*
- given: *None*


### assign/toverload_asgn2.nim
- backend: c
- argv: `c`
- category: assign
- action: run
- expected: *None*
- given: *None*


### closure/texplicit_dummy_closure.nim
- backend: c
- argv: `c`
- category: closure
- action: run
- expected: *None*
- given: *None*


### compiler/tcmdlineoswin.nim
- backend: c
- argv: `c`
- category: compiler
- action: run
- expected: *None*
- given: *None*


### compiler/tdebugutils.nim
- backend: c
- argv: `c`
- category: compiler
- action: run
- expected: *None*
- given: *None*


### concepts/tswizzle.nim
- backend: c
- argv: `c`
- category: concepts
- action: run
- expected: *None*
- given: *None*


### coroutines/texceptions.nim
- backend: c
- argv: `c`
- category: coroutines
- action: run
- expected: *None*
- given: *None*


### coroutines/titerators.nim
- backend: c
- argv: `c`
- category: coroutines
- action: run
- expected: *None*
- given: *None*


### cpp/tdont_init_instantiation.nim
- backend: cpp
- argv: `cpp`
- category: cpp
- action: run
- expected: *None*
- given: *None*


### cpp/tterminate_handler.nim
- backend: cpp
- argv: `cpp`
- category: cpp
- action: run
- expected: *None*
- given: *None*


### cpp/tvectorseq.nim
- backend: cpp
- argv: `cpp`
- category: cpp
- action: run
- expected: *None*
- given: *None*


### dll/nimhcr_integration.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --mm:refc --threads:off --forceBuild --hotCodeReloading:on`
- category: dll
- action: run
- expected: *None*
- given: *None*


### dll/nimhcr_integration.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --mm:refc --threads:off --forceBuild --hotCodeReloading:on`
- category: dll
- action: run
- expected: *None*
- given: *None*


### dll/nimhcr_integration.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen --threads:off --forceBuild --hotCodeReloading:on`
- category: dll
- action: run
- expected: *None*
- given: *None*


### dll/nimhcr_integration.nim
- backend: c
- argv: `c '' -d:nimDebugDlOpen -d:release --threads:off --forceBuild --hotCodeReloading:on`
- category: dll
- action: run
- expected: *None*
- given: *None*


### enum/tpure_enums_conflict.nim
- backend: c
- argv: `c`
- category: enum
- action: reject
- expected: *None*
- given: *None*


### exception/texceptions2.nim
- backend: c
- argv: `c -d:nimStdSetjmp`
- category: exception
- action: run
- expected: *None*
- given: *None*


### exception/texceptions2.nim
- backend: c
- argv: `c -d:nimRawSetjmp`
- category: exception
- action: run
- expected: *None*
- given: *None*


### exception/texceptions2.nim
- backend: c
- argv: `c -d:nimBuiltinSetjmp`
- category: exception
- action: run
- expected: *None*
- given: *None*


### fragmentation/tfragment_alloc.nim
- backend: c
- argv: `c`
- category: fragmentation
- action: run
- expected: *None*
- given: *None*


### fragmentation/tfragment_gc.nim
- backend: c
- argv: `c`
- category: fragmentation
- action: run
- expected: *None*
- given: *None*


### global/tglobal.nim
- backend: c
- argv: `c`
- category: global
- action: run
- expected: *None*
- given: *None*


### int/tunsignedcomp.nim
- backend: c
- argv: `c`
- category: int
- action: run
- expected: *None*
- given: *None*


### iter/tchainediterators.nim
- backend: c
- argv: `c`
- category: iter
- action: run
- expected: *None*
- given: *None*


### iter/titerable.nim
- backend: c
- argv: `c`
- category: iter
- action: run
- expected: *None*
- given: *None*


### iter/tscheduler.nim
- backend: c
- argv: `c`
- category: iter
- action: run
- expected: *None*
- given: *None*


### method/tmultimjs.nim
- backend: js
- argv: `js`
- category: js
- action: run
- expected: *None*
- given: *None*


### method/tmultimjs.nim
- backend: js
- argv: `js '' -d:release`
- category: js
- action: run
- expected: *None*
- given: *None*


### lexer/tlexer.nim
- backend: c
- argv: `c`
- category: lexer
- action: run
- expected: *None*
- given: *None*


### macros/tmacro7.nim
- backend: c
- argv: `c`
- category: macros
- action: run
- expected: *None*
- given: *None*


### method/tmultim.nim
- backend: c
- argv: `c --multimethods:on`
- category: method
- action: run
- expected: *None*
- given: *None*


### method/tmultimjs.nim
- backend: c
- argv: `c`
- category: method
- action: run
- expected: *None*
- given: *None*


### misc/t14667.nim
- backend: c
- argv: `c --cc:vcc`
- category: misc
- action: run
- expected: *None*
- given: *None*


### misc/tdllvar.nim
- backend: c
- argv: `c`
- category: misc
- action: run
- expected: *None*
- given: *None*


### misc/tmissingnilcheck.nim
- backend: c
- argv: `c`
- category: misc
- action: run
- expected: *None*
- given: *None*


### misc/tvcc.nim
- backend: c
- argv: `c --cc:vcc`
- category: misc
- action: run
- expected: *None*
- given: *None*


### modules/tnotuniquename2.nim
- backend: c
- argv: `c`
- category: modules
- action: reject
- expected: *None*
- given: *None*


### modules/trecmod.nim
- backend: c
- argv: `c`
- category: modules
- action: reject
- expected: *None*
- given: *None*


### navigator/tincludefile_temp.nim
- backend: c
- argv: `c '' --ic:on -d:nimIcNavigatorTests --hint:Conf:off --warnings:off`
- category: navigator
- action: compile
- expected: *None*
- given: *None*


### navigator/tnav1_temp.nim
- backend: c
- argv: `c '' --ic:on -d:nimIcNavigatorTests --hint:Conf:off --warnings:off`
- category: navigator
- action: compile
- expected: *None*
- given: *None*


### niminaction/Chapter7/Tweeter/src/tweeter.nim
- backend: c
- argv: `c --threads:off`
- category: niminaction
- action: compile
- expected: *None*
- given: *None*


### niminaction/Chapter7/Tweeter/src/createDatabase.nim
- backend: c
- argv: `c`
- category: niminaction
- action: run
- expected: *None*
- given: *None*


### niminaction/Chapter7/Tweeter/tests/database_test.nim
- backend: c
- argv: `c`
- category: niminaction
- action: run
- expected: *None*
- given: *None*


### objects/tobjpragma.nim
- backend: c
- argv: `c`
- category: objects
- action: run
- expected: *None*
- given: *None*


### objvariant/tfloatrangeobj.nim
- backend: c
- argv: `c`
- category: objvariant
- action: run
- expected: *None*
- given: *None*


### parallel/t5000.nim
- backend: c
- argv: `c`
- category: parallel
- action: run
- expected: *None*
- given: *None*


### parallel/treadafterwrite.nim
- backend: c
- argv: `c`
- category: parallel
- action: reject
- expected: *None*
- given: *None*


### parallel/tuseafterdef.nim
- backend: c
- argv: `c --mm:refc`
- category: parallel
- action: compile
- expected: *None*
- given: *None*


### stdlib/tjsontestsuite.nim
- backend: c
- argv: `c`
- category: stdlib
- action: run
- expected: *None*
- given: *None*


### stdlib/tos_unc.nim
- backend: c
- argv: `c --mm:refc`
- category: stdlib
- action: run
- expected: *None*
- given: *None*


### stdlib/tos_unc.nim
- backend: c
- argv: `c --mm:orc`
- category: stdlib
- action: run
- expected: *None*
- given: *None*


### stdlib/tparsopt.nim
- backend: c
- argv: `c`
- category: stdlib
- action: run
- expected: *None*
- given: *None*


### stdlib/tregistry.nim
- backend: c
- argv: `c --mm:refc`
- category: stdlib
- action: run
- expected: *None*
- given: *None*


### stdlib/tregistry.nim
- backend: c
- argv: `c --mm:orc`
- category: stdlib
- action: run
- expected: *None*
- given: *None*


### system/t7894.nim
- backend: c
- argv: `c`
- category: system
- action: run
- expected: *None*
- given: *None*


### system/techo_unicode.nim
- backend: c
- argv: `c`
- category: system
- action: run
- expected: *None*
- given: *None*


### system/tio.nim
- backend: c
- argv: `c`
- category: system
- action: run
- expected: *None*
- given: *None*


### template/tmodulealias.nim
- backend: c
- argv: `c`
- category: template
- action: run
- expected: *None*
- given: *None*


### typerel/tno_gcmem_in_shared.nim
- backend: c
- argv: `c`
- category: typerel
- action: reject
- expected: *None*
- given: *None*


### typerel/trectuple.nim
- backend: c
- argv: `c`
- category: typerel
- action: reject
- expected: *None*
- given: *None*


### typerel/trectype.nim
- backend: c
- argv: `c`
- category: typerel
- action: reject
- expected: *None*
- given: *None*




reMsgsDiffer
==============
### range/tcompiletime_range_checks.nim
- backend: c
- argv: `c`
- category: range
- action: reject
- expected:   
  ```
  tcompiletime_range_checks.nim(36, 21) Error: 2147483648 can't be converted to int32
  tcompiletime_range_checks.nim(38, 34) Error: 255 can't be converted to FullNegativeRange
  tcompiletime_range_checks.nim(39, 34) Error: 18446744073709551615 can't be converted to HalfNegativeRange
  tcompiletime_range_checks.nim(40, 34) Error: 300 can't be converted to FullPositiveRange
  tcompiletime_range_checks.nim(41, 30) Error: 101 can't be converted to UnsignedRange
  tcompiletime_range_checks.nim(42, 32) Error: -9223372036854775808 can't be converted to SemiOutOfBounds
  tcompiletime_range_checks.nim(44, 22) Error: nan can't be converted to int32
  tcompiletime_range_checks.nim(46, 23) Error: 1e+100 can't be converted to uint64
  tcompiletime_range_checks.nim(49, 22) Error: 18446744073709551615 can't be converted to int64
  tcompiletime_range_checks.nim(50, 22) Error: 18446744073709551615 can't be converted to int32
  tcompiletime_range_checks.nim(51, 22) Error: 18446744073709551615 can't be converted to int16
  tcompiletime_range_checks.nim(52, 21) Error: 18446744073709551615 can't be converted to int8
    
  ```
- given:   
  ```
  tcompiletime_range_checks.nim(36, 21) Error: 2147483648 can't be converted to int32
  tcompiletime_range_checks.nim(38, 34) Error: 255 can't be converted to FullNegativeRange
  tcompiletime_range_checks.nim(39, 34) Error: 18446744073709551615 can't be converted to HalfNegativeRange
  tcompiletime_range_checks.nim(40, 34) Error: 300 can't be converted to FullPositiveRange
  tcompiletime_range_checks.nim(41, 30) Error: 101 can't be converted to UnsignedRange
  tcompiletime_range_checks.nim(42, 32) Error: -9223372036854775808 can't be converted to SemiOutOfBounds
  tcompiletime_range_checks.nim(44, 22) Error: nan can't be converted to int32
  tcompiletime_range_checks.nim(49, 22) Error: 18446744073709551615 can't be converted to int64
  tcompiletime_range_checks.nim(50, 22) Error: 18446744073709551615 can't be converted to int32
  tcompiletime_range_checks.nim(51, 22) Error: 18446744073709551615 can't be converted to int16
  tcompiletime_range_checks.nim(52, 21) Error: 18446744073709551615 can't be converted to int8
  ```




