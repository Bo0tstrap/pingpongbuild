Pingpong için OG + GRASS kurulumları aşağıdaki gibidir.

--------------------------------------------- 0G Kurulumu -------------------------------------------------------------------------

İlk önce çalıştırmış olduğunuz screen içerisine giriyoruz.
```console
screen -r pin
```

Ctrl + C ile çalışan sürümü durduruyoruz ve ardından aşağıdaki kodları giriyoruz.
```console
sudo rm PINGPONG

wget https://pingpong-build.s3.ap-southeast-1.amazonaws.com/linux/latest/PINGPONG

chmod +x ./PINGPONG && ./PINGPONG --key <KEY>
```
Ardından çalışır halde bırakıyoruz ve Ctrl A + D  yapıp screenden çıkıyoruz.

Açılan ekranda OG için kullandığınız adresin Private Keyini girmeniz gerekecek. OG için bir adet Matemask üzerinden bir cüzdan oluşturun eğer yoksa ve sonra [OG Faucet](https://faucet.0g.ai/)'den test tokeninizi alın. Token geldikten sonra aşağıdaki kodu sunucumuza girelim.
```console
./PINGPONG config set --0g=***
```
*** olan yere Private key giriyoruz ve ENTER yapıyoruz. Bize succes olacak bir ibare verecek ve tekrar Screen içierisine girip Ctrl + C yapıp durduruyoruz ve ardından tekrar başlatıyoruz.

0G için bazı komutlar aşağıdaki gibidir. Başlatmak ve durdurmak için. Bunları bilmeniz için EKLEDİM.
```console
./PINGPONG stop --depins=0g
./PINGPONG start --depins=0g
```


------------------------------------------- GRASS Kurulumu ------------------------------------------------------------------------

- Öncelikle Pingpong sunucumuzun güncellemesini üstte yapmıştık. Ardından Grass için daha öncede çalıştırdığınız ya da kayıt olmak için [buradan](https://app.getgrass.io/register/?referralCode=SPXaO1HbZhr9DPP) kaydolup giriş yapıyoruz.
- Giriş yaptıktan sonra F12 tuşuna basıp kontrol panelini açalım ve ardından aşağıdaki gibi APPLİCATİON yazan yere girelim ve görseli takip edip USERID olan yerden "" işaretleri olmadan ID'mizi alalım.

![Grass](https://docs.pingpong.build/~gitbook/image?url=https%3A%2F%2F4218866956-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FL3pmMG28FGN0WFBuuVhL%252Fuploads%252FbNcVe180xJSDRXk3dexe%252FGroup%25201912056010.png%3Falt%3Dmedia%26token%3D2f8745c1-7546-4374-ad13-40a8516f5781&width=768&dpr=1&quality=100&sign=bc8bd63c&sv=1)


Bu işlemin ardından sunucumuzu açalım ve SCREEN içerisine giriş yapmadan önce direkt aşağıdaki kodu girelim.
```console
./PINGPONG config set --grass=***
```
*** olan yere USERID yazmamız gerekiyor ve ENTER yapıyoruz. Sonrasında succes olacak çıktı alacağız. Ardından SCREEN içerisine girip tekrar durduruyoruz ve PINGPONG'umuzu tekrardan başlatıyoruz. Website üzerinden kotrol ediyoruz. Bu kadardı teşekkürler.

GRASS için bazı komutlar aşağıdaki gibidir. Başlatmak ve durdurmak için. Bunları bilmeniz için EKLEDİM.
```console
./PINGPONG stop --depins=grass
./PINGPONG start --depins=grass
```
