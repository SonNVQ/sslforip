# sslforip

# Step 1: Issue SSL
Issue SSL for IP using acme.sh with HiCA

# Step 2: Config
## Config IP SSL for OLS Panel:
cd /usr/local/lsws/admin/conf

ln /root/.acme.sh/*.cer webadmin.crt

ln /root/.acme.sh/*.key webadmin.key

systemctl restart lsws

## Config IP SSL for CyberPanel:
cd /usr/local/lscp/conf

ln /root/.acme.sh/*.cer cer.pem

ln /root/.acme.sh/*.key key.pem

systemctl restart lscpd
