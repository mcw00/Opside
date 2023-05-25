# Sıkça Sorulan Sorular

1. deposit_data-[timestamp].json dosyasını nasıl upload ederim. 
Cevap: Yöntem 1: Winscp veya benzeri bir program ile deposit_data-[timestamp].json dosyanızı bilgisayarınıza indirip yükleyebilirsiniz.
Yöntem 2: Cat komutu ile deposit_data-[timestamp].json dosyası açıp içindekini koplayarak upload sayfasına input kısmından yükleyebilirsiniz.

2. Bir Node u yeni bir sunucuya aktarırken yedekleme yapmak gerekli midir?
Cevap: Evet, yedekleme yapmanız gerekiyor. 
Düğümü önce eski sunucuda durdurun ve ardından klasörü yeni sunucuya kopyalayın. 
Durdurma komutu `opside-chain/stop-all.sh` 
Son olarak, zincir hizmetini başlatmak için yeni sunucuda aşağıdaki komut dosyalarını sırayla çalıştırın: 
`testnet-auto-install-v2/opside-chain/start-geth.sh` 
`testnet-auto-install-v2/opside-chain/start- beaconChain.sh` 
`testnet-auto-install-v2/opside-chain/start-validator.sh` 
Blokları en son Hatırlatıcıya senkronize etmeye başlamak için sabırla bekleyin
düğümlerin çalıştığını onaylayana kadar eski sunucudaki verileri silmemelisiniz. yeni sunucu düzgün çalışıyor. Ardından doğrulayıcı anahtar dosyasını kaydettiğinizden emin olun.

3. Sync olmadan önce Stake ettim bir problem olur mu?
Cevap: Sorun değil. Explorer ile günlük eşitlemenizi bekleyin. Belki validatorünüz ufak bir ceza alabilir.

4. Bir düğümün eşitlenmesi ne kadar sürer?
Cevap: Zaman belirsiz. Senkronizasyon normal şekilde büyüyorsa, sabırla bekleyin.

5. deposit dosyası hangi klasördedir?
Cevap: `testnet-auto-install/validator_keys/` veya `testnet-auto-install-v2/validator_keys/`

6. yüklemeye çalıştığımda ikinci şifreyi girdiğimde harfler çıkmadığı için düğümün donduğunu düşündüm, sonra yeni girdim ve kurulum başarılı oldu ama hiçbir hesap başarılı bir şekilde içe aktarılmadı. sonunda düğümü sildim ve birkaç kez daha kurdum. ve sonuncusu bir hesap oluşturmayı başardım, ancak adresin zaten kullanımda olduğuna dair bir hata oluştu. Ne yapmalıyım?
Cevap: Önce `opside-chain/stop-all.sh` çalıştırın. sonra sırayla aşağıdakileri çalıştırın. 
`testnet-auto-install-v2/opside-chain/start-geth.sh` 
`testnet-auto-install-v2/opside-chain/start-beaconChain.sh` 
`testnet-auto-install-v2/opside-chain/start-validator.sh`

7. Logda çok sayıda hata olduğunda, kullanıcılar düğümü yeniden başlatmayı seçebilir. Nasıl yapılır?
Cevap: Adım 1: Stop node `opside-chain/stop-all.sh` 
Adım 2: Restart chain servis: 
`testnet-auto-install-v2/opside-chain/start-geth.sh` 
`testnet-auto-install-v2/opside-chain/start-beaconChain.sh` 
`testnet-auto-install-v2/opside-chain/start-validator.sh`

Blokları en yenisiyle senkronize etmeye başlamak için sabırla bekleyin

