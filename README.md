This is a reproduction of the error I encountered trying to compile Boost with Hunter (May 19, 2016.) C++ file is empty placeholder, not needed to reproduce the error itself.

```
noob@noobstation ~/devel/hunter-repro $ cmake -H. -B_builds -DHUNTER_STATUS_DEBUG=ON -DCMAKE_TOOLCHAIN_FILE=$POLLY_ROOT/gcc.cmake
-- [hunter *** DEBUG *** 2016-05-22T19:20:37] HUNTER_ROOT detected by environment variable
-- [hunter *** DEBUG *** 2016-05-22T19:20:37] HUNTER_ROOT: /home/noob/devel/hunter-root
-- [hunter *** DEBUG *** 2016-05-22T19:20:37] Settings (initialize):
	-- [hunter *** DEBUG *** 2016-05-22T19:20:37]   HunterGate done (NO)
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37]   Cache init (YES)
	    -- [polly] Used toolchain: gcc / c++11 support
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37] List of cache servers:
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37]   * https://github.com/ingenue/hunter-cache
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37] Settings (finalize):
	-- [hunter *** DEBUG *** 2016-05-22T19:20:37]   HunterGate done (NO)
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37]   Cache init (YES)
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37] Variables from HunterGate:
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37]   HUNTER_GATE_ROOT: /home/noob/devel/hunter-root
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37]   HUNTER_GATE_VERSION: xxxxxxxxxx
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37]   HUNTER_GATE_SHA1: xxxxxxxxxx
	    -- [hunter] Calculating Config-SHA1
	    -- [hunter] Calculating Toolchain-SHA1
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:37] [/home/noob/devel/hunter-repro/_builds/_3rdParty/hunter/toolchain] > "/usr/bin/cmake" "-DTOOLCHAIN_INFO_FILE=/home/noob/devel/hunter-repro/_builds/_3rdParty/hunter/toolchain/toolchain.info" "-DCMAKE_TOOLCHAIN_FILE=/home/noob/devel/polly-root/gcc.cmake" "-DHUNTER_SELF=/home/noob/devel/hunter-root" "-GUnix Makefiles" "-H/home/noob/devel/hunter-repro/_builds/_3rdParty/hunter/toolchain" "-B/home/noob/devel/hunter-repro/_builds/_3rdParty/hunter/toolchain/_builds" "-DCMAKE_RELEASE_POSTFIX=" "-DCMAKE_DEBUG_POSTFIX=d"
	    -- [polly] Used toolchain: gcc / c++11 support
	    -- The C compiler identification is GNU 4.9.3
	    -- The CXX compiler identification is GNU 4.9.3
	    -- Check for working C compiler: /usr/bin/gcc
	    -- Check for working C compiler: /usr/bin/gcc -- works
	    -- Detecting C compiler ABI info
	    -- Detecting C compiler ABI info - done
	    -- Detecting C compile features
	    -- Detecting C compile features - done
	    -- Check for working CXX compiler: /usr/bin/g++
	    -- Check for working CXX compiler: /usr/bin/g++ -- works
	    -- Detecting CXX compiler ABI info
	    -- Detecting CXX compiler ABI info - done
	    -- Detecting CXX compile features
	    -- Detecting CXX compile features - done
	    -- Configuring done
	    -- Generating done
	    -- Build files have been written to: /home/noob/devel/hunter-repro/_builds/_3rdParty/hunter/toolchain/_builds
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Already exists: /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/toolchain.info
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Cache data is up-to-date
	    -- [hunter] HUNTER_ROOT: /home/noob/devel/hunter-root
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] HUNTER_TOOLCHAIN_ID_PATH: /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] HUNTER_CONFIGURATION_TYPES: Release;Debug
	    -- [hunter] [ Hunter-ID: xxxxxxx | Config-ID: 9774815 | Toolchain-ID: c05c545 ]
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] load: /home/noob/devel/hunter-root/cmake/projects/Boost/hunter.cmake
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.60.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.59.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.58.0-p1' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.58.0-p0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.58.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.57.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.56.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.55.0-patched-3' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.55.0-patched-2' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.55.0-patched' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.55.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.54.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.53.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.52.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.51.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.50.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Skip '1.49.0' (looking for '1.61.0')
	    -- [hunter *** DEBUG *** 2016-05-22T19:20:38] Boost versions available: [1.61.0;1.60.0;1.59.0;1.58.0-p1;1.58.0-p0;1.58.0;1.57.0;1.56.0;1.55.0-patched-3;1.55.0-patched-2;1.55.0-patched;1.55.0;1.54.0;1.53.0;1.52.0;1.51.0;1.50.0;1.49.0]
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Install to: /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Install
-- [hunter] BOOST_ROOT: /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Install (ver.: 1.61.0)
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Default arguments: 
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] User arguments: 
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Locking directory: /home/noob/devel/hunter-root/_Base/Download/Boost/1.61.0/f84b1a1
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Lock done
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Already locked: /home/noob/devel/hunter-root/_Base/Download/Boost/1.61.0/f84b1a1
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Locking directory: /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Lock done
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Locking directory: /home/noob/devel/hunter-root/_Base/Cache
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Lock done
	-- [hunter *** DEBUG *** 2016-05-22T19:20:38] Downloading file (try #0 of 10):
		-- [hunter *** DEBUG *** 2016-05-22T19:20:38]   https://raw.githubusercontent.com/ingenue/hunter-cache/master/c05c545/Boost/1.61.0/f84b1a1/da39a3e/d41f56c/da4b923/basic-deps.DONE
		    -- [hunter *** DEBUG *** 2016-05-22T19:20:38]   -> /home/noob/devel/hunter-root/_Base/Cache/meta/c05c545/Boost/1.61.0/f84b1a1/da39a3e/d41f56c/da4b923/basic-deps.DONE
	-- [hunter *** DEBUG *** 2016-05-22T19:20:39] File not found
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Cache miss (no basic dependencies info found: /home/noob/devel/hunter-root/_Base/Cache/meta/c05c545/Boost/1.61.0/f84b1a1/da39a3e/d41f56c/da4b923/basic-deps.DONE)
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Number of logical cores: 8
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] HUNTER_JOBS_NUMBER: 
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] HUNTER_JOBS_OPTION: 8
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Add package: Boost
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Download scheme: url_sha1_boost
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Url: https://downloads.sourceforge.net/project/boost/boost/1.61.0/boost_1_61_0.tar.bz2
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] SHA1: f84b1a1ce764108ec3c2b7bd7704cf8dfd3c9d01
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Configuration types: Release
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Internal dependencies ID: 2
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Scheme file used: /home/noob/devel/hunter-root/cmake/projects/Boost/schemes/url_sha1_boost.cmake.in
	     -- [hunter] Building Boost
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] [/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost] > "/usr/bin/cmake" "-C/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/cache.cmake" "-C/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/args.cmake" "-H/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost" "-B/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build" "-DCMAKE_TOOLCHAIN_FILE=/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/toolchain.cmake" "-GUnix Makefiles"
	     loading initial cache file /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/cache.cmake
	     loading initial cache file /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/args.cmake
	     -- [polly] Used toolchain: gcc / c++11 support
	     -- The C compiler identification is GNU 4.9.3
	     -- The CXX compiler identification is GNU 4.9.3
	     -- Check for working C compiler: /usr/bin/gcc
	     -- Check for working C compiler: /usr/bin/gcc -- works
	     -- Detecting C compile features
	     -- Detecting C compile features - done
	     -- Check for working CXX compiler: /usr/bin/g++
	     -- Check for working CXX compiler: /usr/bin/g++ -- works
	     -- Detecting CXX compile features
	     -- Detecting CXX compile features - done
	     -- [hunter *** DEBUG *** 2016-05-22T19:20:39] Scheme: url_sha1_boost
	     CMake Warning (dev) at /usr/share/cmake/Modules/ExternalProject.cmake:1880 (if):
		     Policy CMP0054 is not set: Only interpret if() arguments as variables or
		     keywords when unquoted.  Run "cmake --help-policy CMP0054" for policy
		     details.  Use the cmake_policy command to set the policy and suppress this
		     warning.

		     Quoted variables like "x" will no longer be dereferenced when the policy is
		     set to NEW.  Since the policy is not set the OLD behavior will be used.
		     Call Stack (most recent call first):
	/usr/share/cmake/Modules/ExternalProject.cmake:2459 (_ep_add_download_command)
	 CMakeLists.txt:119 (ExternalProject_Add)
	 This warning is for project developers.  Use -Wno-dev to suppress it.

	 -- Configuring done
	 -- Generating done
	-- Build files have been written to: /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build
-- [hunter *** DEBUG *** 2016-05-22T19:20:39] Configure step successful (dir: /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost)
	-- [hunter *** DEBUG *** 2016-05-22T19:20:39] [/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost] > "/usr/bin/cmake" "--build" "/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build"
	/usr/bin/cmake -H/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost -B/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build --check-build-system CMakeFiles/Makefile.cmake 0
	/usr/bin/cmake -E cmake_progress_start /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/CMakeFiles /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/CMakeFiles/progress.marks
	/usr/bin/gmake -f CMakeFiles/Makefile2 all
	gmake[1]: Entering directory '/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build'
	/usr/bin/gmake -f CMakeFiles/Boost.dir/build.make CMakeFiles/Boost.dir/depend
	gmake[2]: Entering directory '/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build'
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build && /usr/bin/cmake -E cmake_depends "Unix Makefiles" /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/CMakeFiles/Boost.dir/DependInfo.cmake --color=
	Scanning dependencies of target Boost
	gmake[2]: Leaving directory '/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build'
	/usr/bin/gmake -f CMakeFiles/Boost.dir/build.make CMakeFiles/Boost.dir/build
	gmake[2]: Entering directory '/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build'
	[ 12%] Creating directories for 'Boost'
	/usr/bin/cmake -E make_directory /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source
	/usr/bin/cmake -E make_directory /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source
	/usr/bin/cmake -E make_directory /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Install
	/usr/bin/cmake -E make_directory /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/tmp
	/usr/bin/cmake -E make_directory /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp
	/usr/bin/cmake -E make_directory /home/noob/devel/hunter-root/_Base/Download/Boost/1.61.0/f84b1a1
	/usr/bin/cmake -E touch /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/Boost-mkdir
	[ 25%] Performing download step (download, verify and extract) for 'Boost'
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost && /usr/bin/cmake -P /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/download-Boost.cmake
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost && /usr/bin/cmake -P /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/verify-Boost.cmake
	-- verifying file...
	file='/home/noob/devel/hunter-root/_Base/Download/Boost/1.61.0/f84b1a1/boost_1_61_0.tar.bz2'
	-- verifying file... done
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost && /usr/bin/cmake -P /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/extract-Boost.cmake
	-- extracting...
	src='/home/noob/devel/hunter-root/_Base/Download/Boost/1.61.0/f84b1a1/boost_1_61_0.tar.bz2'
	dst='/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source'
	-- extracting... [tar xfz]
	-- extracting... [analysis]
	-- extracting... [rename]
	-- extracting... [clean up]
	-- extracting... done
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost && /usr/bin/cmake -E touch /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/Boost-download
	[ 37%] No patch step for 'Boost'
	/usr/bin/cmake -E echo_append
	/usr/bin/cmake -E touch /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/Boost-patch
	[ 50%] No update step for 'Boost'
	/usr/bin/cmake -E echo_append
	/usr/bin/cmake -E touch /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/Boost-update
	[ 62%] Performing configure step for 'Boost'
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source && ./bootstrap.sh
	Building Boost.Build engine with toolset gcc... tools/build/src/engine/bin.linuxx86_64/b2
	Detecting Python version... 2.7
	Detecting Python root... /usr
	Unicode/ICU support for Boost.Regex?... /usr
	Generating Boost.Build configuration in project-config.jam...

	Bootstrapping is done. To build, run:

	./b2

	To adjust configuration, edit 'project-config.jam'.
	Further information:

	- Command line help:
	./b2 --help

	- Getting started guide: 
	http://www.boost.org/more/getting_started/unix-variants.html

	- Boost.Build documentation:
	http://www.boost.org/build/doc/html/index.html

	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source && /usr/bin/cmake -E touch /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/Boost-configure
	[ 75%] No build step for 'Boost'
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source && /usr/bin/cmake -E echo_append
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source && /usr/bin/cmake -E touch /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build/Boost-prefix/src/Boost-stamp/Boost-build
	[ 87%] Performing install step for 'Boost'
	cd /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source && ./b2 --layout=tagged -d0 install --without-atomic --without-chrono --without-container --without-context --without-coroutine --without-coroutine2 --without-date_time --without-exception --without-filesystem --without-graph --without-graph_parallel --without-iostreams --without-locale --without-log --without-math --without-metaparse --without-mpi --without-program_options --without-python --without-random --without-regex --without-serialization --without-signals --without-system --without-test --without-thread --without-timer --without-type_erasure --without-wave --prefix=/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Install
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/build/feature.jam:494: in feature.validate-value-string from module feature
	error: "none" is not a known value of feature <optimization>
	error: legal values: "off" "speed" "space"
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/build/property.jam:276: in validate1 from module property
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/build/property.jam:302: in property.validate from module property
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/tools/builtin.jam:381: in variant from module builtin
	/usr/share/boost-build/site-config.jam:9: in modules.load from module site-config
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/build-system.jam:249: in load-config from module build-system
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/build-system.jam:351: in load-configuration-files from module build-system
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/build-system.jam:524: in load from module build-system
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/kernel/modules.jam:295: in import from module modules
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/tools/build/src/kernel/bootstrap.jam:139: in boost-build from module
	/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Source/boost-build.jam:17: in module scope from module

	CMakeFiles/Boost.dir/build.make:76: recipe for target 'Boost-prefix/src/Boost-stamp/Boost-install' failed
	gmake[2]: *** [Boost-prefix/src/Boost-stamp/Boost-install] Error 1
	gmake[2]: Leaving directory '/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build'
	CMakeFiles/Makefile2:70: recipe for target 'CMakeFiles/Boost.dir/all' failed
	gmake[1]: *** [CMakeFiles/Boost.dir/all] Error 2
	gmake[1]: Leaving directory '/home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost/Build'
	Makefile:86: recipe for target 'all' failed
	gmake: *** [all] Error 2

	[hunter ** FATAL ERROR **] Build step failed (dir: /home/noob/devel/hunter-root/_Base/xxxxxxx/9774815/c05c545/Build/Boost
			[hunter ** FATAL ERROR **] [Directory:/home/noob/devel/hunter-root/cmake/projects/Boost]

			------------------------------ WIKI -------------------------------
			https://github.com/ruslo/hunter/wiki/error.external.build.failed
			-------------------------------------------------------------------

			CMake Error at /home/noob/devel/hunter-root/cmake/modules/hunter_wiki.cmake:12 (message):
			Call Stack (most recent call first):
			/home/noob/devel/hunter-root/cmake/modules/hunter_fatal_error.cmake:20 (hunter_wiki)
			/home/noob/devel/hunter-root/cmake/modules/hunter_download.cmake:484 (hunter_fatal_error)
			/home/noob/devel/hunter-root/cmake/projects/Boost/hunter.cmake:222 (hunter_download)
			/home/noob/devel/hunter-root/cmake/modules/hunter_add_package.cmake:87 (include)
			CMakeLists.txt:12 (hunter_add_package)


			-- Configuring incomplete, errors occurred!
			See also "/home/noob/devel/hunter-repro/_builds/CMakeFiles/CMakeOutput.log".

```
