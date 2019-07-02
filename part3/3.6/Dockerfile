FROM alpine

COPY script.sh /app/

RUN apk add --no-cache curl && \
    chmod +x /app/script.sh && \
    adduser -D app

USER app

CMD /app/script.sh