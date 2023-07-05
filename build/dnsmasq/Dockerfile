FROM alpine
RUN apk --no-cache add dnsmasq

# Expose ports: 53/tcp (DNS), 67/udp & 68/udp (DHCP)
EXPOSE 53/udp
EXPOSE 53/tcp

# Start dnsmasq, write log items to container console
ENTRYPOINT ["dnsmasq", "-k"]
