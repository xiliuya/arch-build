FROM archlinux:latest

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN date
RUN pacman -Syu --noconfirm
RUN pacman -S base-devel ruby wget fuse 'cmake' 'clang' 'dkms' 'bison' 'flex' 'pkg-config' 'fontconfig' 'binutils>=2.28' 'libpng' 'cairo' 'libtiff' 'glu' 'libbsd' 'python' 'mesa' 'libxkbfile' 'libxcursor' 'libxext' 'libxkbcommon' 'libxrandr' 'ffmpeg' 'lib32-gcc-libs' 'linux-headers' --noconfirm
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"] 
