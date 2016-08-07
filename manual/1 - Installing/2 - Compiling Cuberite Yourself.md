---
sitemap: false
---
Compiling yourself takes longer and is more involved, but on modern processors can lead to a speed increase of up to 1.5 to 3x. If your operating system or hardware is not officially supported, compiling may be the only way to run Cuberite.

The automatic compilation script is recommended for *nix users. Windows users should see the [Other Systems](#other-systems) subsection for instructions. The automatic compilation script takes care of the compilation process for you. You only need to copy this command to your terminal:

<pre>sh -c "$(wget -O - https://compile.cuberite.org)"</pre>

The rest of this section is for those who prefer to manually compile.

<div class="warning-box">
	<div class="warning-box-body">
		This process requires use of the command line. If you are not familiar with it, it is recommended that you use the <a href="#pre-com">pre-compiled builds</a> instead.
	</div>
</div>

#### Linux/Mac/BSD
Compiling on Linux and related operating systems is easy and simple, although it does require some tools before you can get started. You need a C++ compiler (Clang++ or G++), a C compiler (Clang or GCC), Git, CMake and Make. A simple command to make sure these tools are installed (Ubuntu/Debian) is:

<pre>sudo apt-get install clang git cmake make</pre>

Once the tools are installed, you should clone the Git repo:

<pre>
git clone --recursive https://github.com/cuberite/cuberite.git<br/>
cd cuberite
</pre>

You should then run the CMake process and compile:

<pre>
cmake . -DCMAKE_BUILD_TYPE=RELEASE<br/>
make -j 2
</pre>

<div class="warning-box">
	<div class="warning-box-body">
		This step may take a while on slow hardware like Raspberry Pis, up to several hours in some cases. However, subsequent compiles will be faster.
	</div>
</div>

<div class="info-box">
	<div class="info-box-body">
		For a more detailed look at Build Flags and their utility (especially if you are compiling a build on a different machine than the one your are running it on), see <a href="#build-flags">below</a>.
	</div>
</div>

Once the compilation process is finished, the Cuberite executable will be placed inside the ***Server*** inside the repository that you downloaded. You can copy this folder anywhere you like, just make sure to copy the supporting files otherwise the server will not work properly.

#### Other Systems
For compiling on Windows or other systems, please see [COMPILING.md](https://github.com/cuberite/cuberite/blob/master/COMPILING.md) in the main repository.

#### Build Flags
Cuberite's build process supports a large number of flags for customising the builds. Use these flags by adding ***-DFlag_name=Value*** to the cmake configuration command. For example to enable test generation using the ***SELF_TEST*** flag add: ***-DSELF_TEST=ON***

##### BUILD_TOOLS
> Adds the Cuberite tools to the build. At the moment only MCADefrag and ProtoProxy are added. Define as ***ON*** to enable. Define as ***OFF*** to disable.

##### BUILD_UNSTABLE_TOOLS
> Adds tools that are not working yet to the build. Currently this is only the Generator Performance Test. Used for developing these tools. Define as ***ON*** to enable. Define as ***OFF*** to disable.

##### SELF_TEST
> Enables generation of tests and self-test startup code. Tests can be run with ***ctest*** and with makefiles ***make test***. Define as ***ON*** to enable. Define as ***OFF*** to disable.
		
##### FORCE_32
> Forces the build to use 32 bit builds on *nix systems. Define as ***ON*** to enable. Define as ***OFF*** to disable.

##### CROSSCOMPILE
> Disables optimizations for the build host. This is important when building on a different machine from the one you will run Cuberite on as the build machine may support instructions the final machine does not. This flag only has any effect on Linux. Define as ***ON*** to enable. Define as ***OFF*** to disable.
