FROM martynas/archlinux:latest

COPY entrypoint.sh /entrypoint.sh

USER root

RUN pacman -Syu --noconfirm --needed \
	&& pacman -S linux-lts-headers wget  --noconfirm \
	&&  ln -s /lib/modules/`ls /lib/modules/`/ /lib/modules/$(uname -r) \
	&& yay -Sy waybackpack --noconfirm \ 
	&& uname -a 


ENTRYPOINT ["/entrypoint.sh"]
