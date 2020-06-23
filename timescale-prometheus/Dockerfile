FROM timescale/timescale-prometheus
FROM buildpack-deps
COPY --from=0 /timescale-prometheus /usr/local/bin/timescale-prometheus
COPY gitmodules/wait-for-it/wait-for-it.sh /usr/local/bin/wait-for-it.sh
