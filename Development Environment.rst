=================================
Development Environment Setup
=================================

msys2 Installation
--------------------

1. Download the msys2 installer from its official website, http://www.msys2.org. Choose `msys2-x85_64-20161025.exe` in a 64-bit environment.

2. Install the software in the default location, which means `C:\msys64`.Modify msys2's mirrorlist files in `/etc/pacman.d` directory to use USTC servers. Concretely speaking, change the server part of `mirrorlist.ming32` to::
	
	Server = http://mirrors.ustc.edu.cn/msys2/mingw/i686
	
the server part of `mirrorlist.ming64` to::

	Server = http://mirrors.ustc.edu.cn/msys2/mingw/x86_64
	
and the corresponding part in mirrorlist.msys to::

	Server = http://mirrors.ustc.edu.cn/msys2/msys/$arch  
	
Run MSYS2 MinGW 64-bit shell, which is `C:\msys64\mingw64.exe` by default. Type the following command and follow the system's instruction.::

	Pacman –Syu
	Pacman –Su

Install the development toolchains and useful softwares using the following command.::

     pacman -S mingw-w64-x86_64-toolchain libraries development compression VCS sys-utils net-utils msys2-devel
     pacman –S base-devel
     pacman –S msys/cmake
     pacman –S mingw64/mingw-w64-x86_64-python3
     pacman –S mingw64/mingw-w64-x86_64-boost
     pacman –S mingw64/mingw-w64-x86_64-gtk2
     pacman –S msys/vim
     git clone https://github.com/amix/vimrc.git  ~/.vim_runtime
     source ~/.vim_runtime/ install_awesome_vimrc.sh


ConEmu Installation
-------------------------

1. Download the ConEmu from its official website, https://conemu.github.io.

2. Customize the default shell to be `{Bash::Msys2-64}`

Add the following statement into the `{Bash::msys2-64}` shell's startup script, which is located at  `Setting->StartUp->Task->{Bash:msys2-64}`.::

	set MSYSTEM=MINGW64&
