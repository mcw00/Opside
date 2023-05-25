<h1 align="center"> Opside </h1>
> Pre-Alpha Testnet

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
# Genesisi yüklemesi:

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

# Validatör oluşturma
* Node sync olup olmadığını kontrol edin aşağıdaki log komutlari ile Explorer dan karşılaştırın. [Buradan](https://pre-alpha-beacon.opside.info/blocks)

* Node sync olduktan sonra (6-8 saat) [Buraya](https://opside.network/validator/deposit) gidelim.

* Resimdeki gibi continue veya I agree diyelim sürekli 2. resime kadar
![image](https://github.com/mcw00/Opside/assets/84830960/89309cd5-7d05-4a7c-97a6-789a53da63d9)

* İkinci Resim
![image](https://github.com/mcw00/Opside/assets/84830960/6165eb9b-d7a2-4d91-9979-14d311ac7830)

* Burada iki şekilde dosya yüklemesi yapacağız. 2. resimde gördüğünüz Upload kısmını seçerseniz Winscp gibi bir program ile sunucunuza girip deposit_data-[timestamp].json dosyanızı bilgisayara indirip bu sayfadan yüklemeniz gerekmektedir.
* deposit_data-[timestamp].json dosyanız normal Opside kurulumu normal yaptıysanız cd ./testnet-auto-install-v2/validator_keys klasörünün altındadır. Yok eğer Genesis kurulumu yaptıysanız cd ./testnet-auto-install/validator_keys klasörünün altındadır.  
* Diğer Yönten ise 2. resimde gösterdiğim Input kısmını seçip Opside kurulumu normal yaptıysanız cat ./testnet-auto-install-v2/validator_keys/deposit_data-[timestamp].json dosyasının içini kopyalayıp sitede yapıştırmanız gerekmektedir. Yok eğer Genesis kurulumu yaptıysanız cat ./testnet-auto-install/validator_keys/deposit_data-[timestamp].json dosyasının içini kopyalayıp sitede yapıştırmanız gerekmektedir.
* Son adımda ise cüzdan bağlayıp deposit yapınca Complete ettikten sonra işlem tamamdır. 12-24 saat içerisinde validatorunuz aktif olacaktır.
