FROM gitlab.lampiris.be:4567/docker/liquibase:3.5.3

ENV WAIT_HOST localhost
ENV WAIT_PORT 5432
ENV TIMEOUT 60

RUN curl -o /bin/wait-for-it.sh https://raw.githubusercontent.com/jgsqware/wait-for-it/master/wait-for-it.sh && \
    chmod +x /bin/wait-for-it.sh

ENTRYPOINT ["/bin/wait-for-it.sh", "$WAIT_HOST:$WAIT_PORT", "-s","--","/opt/docker/bin/entrypoint.sh"]
