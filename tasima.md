# Node Taşıma

* Öncelikle Eski sunucudan `validator_keys` klasörünü ve `keystore` dosyanızı bilgisayara yedekleyin.
* validator_keys klasörü `/root/testnet-auto-install-v2/` dizininin altında bulunur.
* keystore dosyası ise `/root/testnet-auto-install-v2/opside-chain/prysm/validator/config/wallet/` dizinin altındadır.
* Yeni server'a Node sıfırdan kuruyoruz. Eski sunucudaki `şifre` ve aynı `cüzdan` ile.
* Eski ve yeni sunucuda node durdurun

```
cd
cd testnet-auto-install-v2
opside-chain/stop-all.sh

```

* Yedeklediğiniz dosyaları `(validator_keys klasörü ve keystore dosyası)` yeni sunucuda yukarıdaki dizinlerin için Winscp veya benzeri bir program ile aktarın.

## Yeni sunucuda terminale aşağıdaki komutları sırayla yazalım

```
cd
cd testnet-auto-install-v2
testnet-auto-install-v2/opside-chain/start-geth.sh
testnet-auto-install-v2/opside-chain/start-beaconChain.sh
testnet-auto-install-v2/opside-chain/start-validator.sh

```

son komutu da girdikten sonra aşağıdaki gibi bir yazı çıkacak

`Successfully imported 1 accounts, view all of them by running accounts list`

## Log kontrolü

```
cd
cd testnet-auto-install-v2/
opside-chain/show-geth-log.sh

```
