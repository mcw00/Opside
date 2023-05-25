# Sıkça sorulan Sorular

1. deposit_data-[timestamp].json dosyasını nasıl upload ederim. 
Cevap: Yöntem 1: Winscp veya benzeri bir program ile deposit_data-[timestamp].json dosyanızı bilgisayarınıza indirip yükleyebilirsiniz.
Yöntem 2: Cat komutu ile deposit_data-[timestamp].json dosyası açıp içindekini koplayarak upload sayfasına input kısmından yükleyebilirsiniz.

2. Bir Node u yeni bir sunucuya aktarırken yedekleme yapmak gerekli midir?
Cevap: Evet, yedekleme yapmanız gerekiyor. 
Düğümü önce eski sunucuda durdurun ve ardından klasörü yeni sunucuya kopyalayın. 
Durdurma komutu `opside-chain/stop-all.sh` 
Son olarak, zincir hizmetini başlatmak için yeni sunucuda aşağıdaki komut dosyalarını sırayla çalıştırın: 
testnet-auto-install-v2/opside-chain/start-geth.sh 
testnet-auto-install-v2/opside-chain/start- beaconChain.sh 
testnet-auto-install-v2/opside-chain/start-validator.sh 
Blokları en son Hatırlatıcıya senkronize etmeye başlamak için sabırla bekleyin
düğümlerin çalıştığını onaylayana kadar eski sunucudaki verileri silmemelisiniz. yeni sunucu düzgün çalışıyor. Ardından doğrulayıcı anahtar dosyasını kaydettiğinizden emin olun.
