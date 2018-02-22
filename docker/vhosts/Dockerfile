FROM dzejson91/vhosts:latest

ENV UID 1000
ENV GID 50
ENV ROOT_PASS root
ENV USER_PASS user

RUN groupmod -og ${GID} user
RUN usermod -ou ${UID} user
RUN echo "root:${ROOT_PASS}" | chpasswd
RUN echo "user:${USER_PASS}" | chpasswd

ENTRYPOINT ["/bin/bash"]
CMD ["/docker-entrypoint.sh"]
