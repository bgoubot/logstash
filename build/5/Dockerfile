FROM logstash:5.1.2

# Install additional logstash plugins.
RUN logstash-plugin install logstash-filter-translate
RUN logstash-plugin install logstash-input-jmx
RUN logstash-plugin install logstash-output-jira
RUN logstash-plugin install logstash-output-mongodb
RUN logstash-plugin install logstash-filter-aggregate
RUN logstash-plugin install logstash-filter-elapsed
RUN logstash-plugin install logstash-filter-environment

COPY docker-entrypoint.sh /
RUN chmod 755 /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["-e", ""]
