FROM martynas/archlinux:latest

COPY entrypoint.sh /entrypoint.sh

USER root

RUN pacman -Syy --noconfirm --needed \
	&& pacman -S linux-lts-headers --noconfirm \
	&&  ln -s /lib/modules/`ls /lib/modules/`/ /lib/modules/$(uname -r)


ENTRYPOINT ["/entrypoint.sh"]
