FROM wordpress:latest
RUN apt update && apt upgrade -y
RUN apt install netcat wget vim python sudo -y
RUN useradd john -m -s /bin/bash
RUN echo "john:DmTr5MdH" | chpasswd
RUN useradd tayo -m -s /bin/bash
RUN echo "tayo:YgzSJf4A" | chpasswd
COPY maintain.sh /home/tayo/
RUN chown tayo:tayo /home/tayo/maintain.sh
RUN chmod 757 /home/tayo/maintain.sh
COPY tayo-to-do-list.txt /home/tayo/
RUN chown tayo:tayo /home/tayo/tayo-to-do-list.txt
COPY flag1.txt /home/
COPY flag2.txt /home/john/
RUN chown john:john /home/john/flag2.txt
RUN chmod 700 /home/john/flag2.txt
COPY flag3.txt /home/tayo/
RUN chown tayo:tayo /home/tayo/flag3.txt
RUN chmod 700 /home/tayo/flag3.txt
COPY flag4.txt /root/
RUN echo It works >> /home/log
RUN echo 'john	ALL=(tayo)NOPASSWD:/home/tayo/maintain.sh' >> /etc/sudoers
RUN echo 'tayo	ALL=(root)NOPASSWD:/usr/bin/python' >> /etc/sudoers
EXPOSE 80
