# yggdrasil-openwrt 25.12+

### Install trust key once

```sh
wget -qO "/etc/apk/keys/yggdrasil-feed.pem" "https://makishimuakuma.github.io/yggdrasil-openwrt/25.12/yggdrasil-feed.pub.pem"
```

### Add repository

```sh
echo "https://makishimuakuma.github.io/yggdrasil-openwrt/25.12/$(cat /etc/apk/arch)/packages.adb" > "/etc/apk/repositories.d/yggdrasil.list"
apk update
apk add yggdrasil
apk add luci-proto-yggdrasil
```

### Update yggdrasil

```sh
apk update
apk upgrade yggdrasil
apk upgrade luci-proto-yggdrasil
```
