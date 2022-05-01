FROM martynas/archlinux:latest

COPY entrypoint.sh /entrypoint.sh

USER root

RUN pacman -Syu --noconfirm --needed \
	&& pacman -S linux-lts-headers --noconfirm \
	&&  ln -s /lib/modules/`ls /lib/modules/`/ /lib/modules/$(uname -r) \
	&& uname -a 


ENTRYPOINT ["/entrypoint.sh"]
