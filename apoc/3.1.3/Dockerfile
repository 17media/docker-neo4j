FROM neo4j:3.1.3

MAINTAINER Sam Liu <sam@17.media>

ENV APOC_URI https://github.com/neo4j-contrib/neo4j-apoc-procedures/releases/download/3.1.3.6/apoc-3.1.3.6-all.jar

RUN mv plugins /plugins \
    && ln -s /plugins \
    && curl --fail --silent --show-error --location --output apoc-3.1.3.6-all.jar $APOC_URI \
    && mv apoc-3.1.3.6-all.jar /plugins

EXPOSE 7474 7473 7687

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ["neo4j"]
