
FROM alpine:latest 
LABEL matainer="NovaCaoFc" \
      role="bak" \
      project="etcd"
COPY etcdctl /usr/local/bin/ 
CMD ["/bin/sh","-c","etcdctl --endpoints=${ETCD_HOST}:${ETCD_PORT} --cacert=/certs/ca.crt --cert=/certs/peer.crt --key=/certs/peer.key snapshot save /backup/etcd-`date +%F-%T`.backup"]
