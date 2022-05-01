FROM martynas/archlinux:latest

COPY entrypoint.sh /entrypoint.sh

USER root

RUN yay -Syy --noconfirm --needed && yay -S linux-lts-headers --noconfirm 
RUN ln -s /lib/modules/$(uname -r) /lib/modules/`ls /lib/modules/`/


ENTRYPOINT ["/entrypoint.sh"]
