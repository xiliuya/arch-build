FROM martynas/archlinux:latest

COPY entrypoint.sh /entrypoint.sh

USER root

RUN pacman -Syu --noconfirm --needed \
	&& pacman -S linux-lts-headers wget  --noconfirm \
	&&  ln -s /lib/modules/`ls /lib/modules/`/ /lib/modules/$(uname -r) \
	&& yay -Sy python-pip  rubygems ruby --noconfirm \ 
	&& export PATH="/root/.local/share/gem/ruby/3.0.0/bin:$PATH" \
	&& chmod 777 -R /root/.local/ \
	&& gem install wayback_machine_downloader \
	&& uname -a 


ENTRYPOINT ["/entrypoint.sh"]
