<h1 align="center"> Opside Pre-Alpha Testnet </h1>


![image](https://mirror-media.imgix.net/publication-images/264V2J4Zoi9uiQk9NIK4k.png?height=640&width=1280&h=640&w=1280&auto=compress)

# Sistem Gereksinimleri

```
4 CPU 16 RAM 500 GB SSD
```
# Güncelleme yapalım

``` 
sudo apt-get update -y && sudo apt-get upgrade -y 

```
# Kütüphaneleri Kuralım

``` 
sudo apt install -y build-essential libssl-dev cmake screen git htop

```
Burada dikkat etmeniz gereken Opside normal kurulum ile Genesis kurulumundan birini yapmanız yeterli olacaktır. 

# Opside normal yükleme:

``` 
wget -c https://pre-alpha-download.opside.network/testnet-auto-install-v2.tar.gz 
tar -C ./ -xzf testnet-auto-install-v2.tar.gz
chmod +x -R ./testnet-auto-install-v2
cd ./testnet-auto-install-v2

```
# Genesis yüklemesi:

```
wget -c https://pre-alpha-download.opside.network/testnet-auto-install.tar.gz 
tar -C ./ -xzf testnet-auto-install.tar.gz
chmod +x -R ./testnet-auto-install
cd ./testnet-auto-install

```
# Node'u başlatalım

``` 
./install-ubuntu-en-1.0.sh

```
Yukarıdaki Node başlatma komutundan sonra sırasıyla
* Metamask cüzdan adresinizi girin
* Şifre oluşturun
* Metamask cüzdan adresinizi tekrar girin
* Şifrenizi tekrar girin. Bu adımda ekrana hiçbir şey yazmaz gibi görünür güvenlik açısından
* Size vereceği memonicleri kayıt etin. bir sonraki adımda memonicleri isteyecek kayıt ettiğiniz memonicleri yapıştırın.

# Log kontrol edelim.

* execution client logları
```
opside-chain/show-geth-log.sh
```

* consensus client logları
```
opside-chain/show-beaconChain-log.sh
```
* validatör logları
```
opside-chain/show-validator-log.sh

```

# Validatör oluşturma
* Node sync olup olmadığını kontrol edin aşağıdaki log komutlari ile Explorer dan karşılaştırın. [Buradan](https://pre-alpha-beacon.opside.info/blocks)

* Node sync olduktan sonra [Buraya](https://opside.network/validator/deposit) gidelim.

* Resimdeki gibi continue veya I agree diyelim sürekli 2. resime kadar
![image](https://github.com/mcw00/Opside/assets/84830960/89309cd5-7d05-4a7c-97a6-789a53da63d9)

* İkinci Resim
![image](https://github.com/mcw00/Opside/assets/84830960/6165eb9b-d7a2-4d91-9979-14d311ac7830)

* Burada iki şekilde dosya yüklemesi yapacağız. 2. resimde gördüğünüz `Upload` kısmını seçerseniz `Winscp` gibi bir program ile sunucunuza girip `deposit_data-[timestamp].json` dosyanızı bilgisayara indirip bu sayfadan yüklemeniz gerekmektedir.
* `deposit_data-[timestamp].json` dosyanız normal Opside kurulumu normal yaptıysanız `./testnet-auto-install-v2/validator_keys` klasörünün altındadır. Yok eğer Genesis kurulumu yaptıysanız `./testnet-auto-install/validator_keys` klasörünün altındadır. Not: deposit dosyasındaki  `[timestamp]` kısmında rakamlar yazar.
* Diğer Yönten ise 2. resimde gösterdiğim  `Input ` kısmını seçip Opside kurulumu normal yaptıysanız  `cat ./testnet-auto-install-v2/validator_keys/deposit_data-[timestamp].json ` dosyasının içini kopyalayıp sitede yapıştırmanız gerekmektedir. Yok eğer Genesis kurulumu yaptıysanız  `cat ./testnet-auto-install/validator_keys/deposit_data-[timestamp].json ` dosyasının içini kopyalayıp sitede yapıştırmanız gerekmektedir.
* Son adımda ise cüzdan bağlayıp  `deposit ` yapınca  `Complete ` yazısını gördüktetn sonra işlem tamamdır. Tüm kutuları tıklamayı unutmayın.
* 12-24 saat içerisinde validatorunuz aktif olacaktır.
