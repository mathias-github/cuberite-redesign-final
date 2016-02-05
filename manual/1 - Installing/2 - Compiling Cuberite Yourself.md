Compiling yourself takes longer and is more involved, but on modern processors can lead to a speed increase of up to 1.5 to 3x. If your operating system or hardware is not officially supported, compiling may be the only way to run Cuberite.

The automatic compilation script is recommended for *nix users. Windows users should see the [Other Systems](#other-systems) subsection for instructions. The automatic compilation script takes care of the compilation process for you. You only need to copy this command to your terminal:

    sh -c "$(wget -O - https://raw.githubusercontent.com/cuberite/cuberite/master/compile.sh)"

The rest of this section is for those who prefer to manually compile.

<aside class="warnbox">
	This process requires use of the command line. If you are not familiar with it, it is recommended that you use the [pre-compiled builds](#1.1) instead.
</aside>

#### Linux/Mac/BSD
Compiling on Linux and related operating systems is easy and simple, although it does require some tools before you can get started. You need a C++ compiler (Clang++ or G++), a C compiler (Clang or GCC), Git, CMake and Make. A simple command to make sure these tools are installed (Ubuntu/Debian) is:

    sudo apt-get install clang git cmake make

Once the tools are installed, you should clone the Git repo:

      git clone --recursive https://github.com/cuberite/cuberite.git
      cd cuberite

You should then run the CMake process and compile:

    cmake . -DCMAKE_BUILD_TYPE=RELEASE
    make . -j 2

<aside class="warnbox">
	This step may take a while on slow hardware like Raspberry Pis, up to several hours in some cases. However, subsequent compiles will be faster.
</aside>

<aside class="infobox">
	For a more detailed look at Build Flags and their utility (especially if you are compiling a build on a different machine than the one your are running it on), see [below](#build-flags).
</aside>

Once the compilation process is finished, the Cuberite executable will be placed inside the <code>Server</code> inside the repository that you downloaded. You can copy this folder anywhere you like, just make sure to copy the supporting files otherwise the server will not work properly.

#### Other Systems
For compiling on Windows or other systems, please see [COMPILING.md](https://github.com/cuberite/cuberite/blob/master/COMPILING.md) in the main repository.

#### Build Flags
Cuberite's build process supports a large number of flags for customising the builds. Use these flags by adding <code>-DFlag_name=Value</code> to the cmake configuration command. For example to enable test generation using the <code>SELF_TEST</code> flag add: <code>-DSELF_TEST=ON</code>

<dl>
	<dt>BUILD_TOOLS</dt>
	<dd>
		Adds the Cuberite tools to the build. At the moment only MCADefrag and ProtoProxy are added. Define as <code>ON</code> to
		enable. Define as <code>OFF</code> to disable.
	</dd>
	<dt>BUILD_UNSTABLE_TOOLS</dt>
	<dd>
		Adds tools that are not working yet to the build. Currently this is only the Generator Performance Test. Used for developing these
		tools. Define as <code>ON</code> to enable. Define as <code>OFF</code> to disable.
	</dd>
	<dt>SELF_TEST</dt>
	<dd>
		Enables generation of tests and self-test startup code. Tests can be run with <code>ctest</code> and with makefiles
		<code>make test</code>. Define as <code>ON</code> to enable. Define as <code>OFF</code> to disable.
	</dd>
	<dt>FORCE_32</dt>
	<dd>
		Forces the build to use 32 bit builds on *nix systems. Define as <code>ON</code> to enable. Define as <code>OFF</code> to
		disable.
	</dd>
	<dt>CROSSCOMPILE</dt>
	<dd>
		Disables optimizations for the build host. This is important when building on a different machine from the one you will
		run Cuberite on as the build machine may support instructions the final machine does not. This flag only has any effect
		on linux. Define as <code>ON</code> to enable. Define as <code>OFF</code> to disable.
	</dd>
</dl>
