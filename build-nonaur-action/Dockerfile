FROM martynas/archlinux:latest

COPY entrypoint.sh /entrypoint.sh

USER root

RUN pacman -Syu --noconfirm --needed \
	&& pacman -S linux-lts-headers wget  --noconfirm \
	&&  ln -s /lib/modules/`ls /lib/modules/`/ /lib/modules/$(uname -r) \
	&& yay -Sy python-pip  rubygems ruby ghc8.10-bin --noconfirm \ 
	&& mkdir -p /root/.local/share/gem/ruby/3.0.0/bin \
	&& export PATH="/root/.local/share/gem/ruby/3.0.0/bin:$PATH" \
	&& gem install wayback_machine_downloader \
	&& ls  -lh /root/.local/share/gem/ruby/3.0.0/bin \
	&& chmod -R 777 /root/.local/ \
	&& uname -a 


ENTRYPOINT ["/entrypoint.sh"]
