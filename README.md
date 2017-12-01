# Magento docker environment

### Install docker and docker-compose

```
curl -L https://get.docker.com/ | sh
sudo usermod -aG docker $(whoami)
sudo systemctl enable --now docker.service
sudo curl -L --fail https://github.com/docker/compose/releases/download/1.17.0/run.sh -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

### Clone repo

```
git clone https://github.com/abgmtr/docker-magento-env.git
cd docker-magento-env
```

### Up environment
```
docker-compose up -d --build
```

### Install magento
for install m1
```
docker-compose exec mage m1-install
```
for install m2
```
docker-compose exec mage m2-install
```
