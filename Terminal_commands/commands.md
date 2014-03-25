<dl>
 <dt>1-sudo apt-get install mailutils</dt>
   top yaz çalışanları göster çalışanı durdurmak için killer yaz top da

<dt>2-dpkg --get selections</dt> ==>kurulan programların gösterir.

<dt>3-sudo apt-get autoremove </dt>==>fazlalıkları siler

<dt>4-youtube-dl "link"         </dt>==>youtubeden video indirme

<dt>5-iptables -A INPUT -p tcp –dport <PORTNUMARASI> -j ACCEPT</dt>==port açmak için
<dt>örnek</dt>==>	sudo iptables -A INPUT -p tcp --dport 25 -j ACCEPT


<dt>6-ifconfig -a | grep eth  </dt>   ==>

<dt>7-sudo lshw -class network  </dt> ==>Sisteminizde mevcut tüm ağ arayüzleri belirlemenize yardımcı olabilir başka bir uygulama lshw komut. Aşağıdaki örnekte, lshw otobüs bilgi, sürücü ayrıntıları ve tüm desteklenen yetenekleri ile birlikte eth0 mantıksal adıyla tek bir Ethernet arabirimi gösterir.


<dt>8-cd /var   </dt> ==>log kayıtlarını gösterir log sistemde ne yapıldığını gösterir
  <dt>cd log</dt>

9-sudo apt-get install ethtool   ==>ethtool gibi oto-müzakere, port hızı, dubleks modu, ve Wake-on-LAN gibi ethernet kartı ayarlarını görüntüler ve değiştiren bir programdır. Bu varsayılan olarak yüklenen, ama depolarda yükleme için kullanılabilir değil

10-sudo ifconfig eth0 10.0.0.100 netmask 255.255.255.0 ==geçici olarak ip adresinideğiştirme

11-sudo route add default gw 10.0.0.1 eth0 ==

12-iptables -L ==>iptables -L komutu ile daha önceden girilmiş iptables kurallarını görüntüleyebilirsiniz

13-ssh hostname@10.111.1.40  ==>

14-subl dosyaadi.uzantı ==>sublime texti acar

gcc -c deneme2.c   ==>derleme
gcc deneme2.o -o deneme2
./deneme2

15-netstat  ==>kendi açık portlarını görürsün

16-ssh ile bağlandığın bilgisayarda 4 saat boyunca root şifresi istemez.
ControlMaster auto
ControlPath /tmp/ssh_mux_%h_%p_%r
ControlPersist 4h 


17-sudo unzip ubuntu-logo.zip -d /usr/share/unity/5/ && rm ubuntu-logo.zip  ==>dash home daki logoyu değiştirir
	wget -O ubuntu-logo.zip http://goo.gl/V6mea       ==>logoyu indirir

18-sensors=Bilgisayarın sıcaklığını ölçme

19-netstat -an | grep "LISTEN" ==>dinlenen portları gösterir

20-sudo ufw enable    ==>firewall aktif hale etirmek için

21-sudo ufw status    ==>Güvenlik duvarının aktif yada pasif olduğunu kontrol etmek için,Verilen kuralların listeler

22-sudo ufw disable   ==>firewall pasif hale getirmek için

23-sudo ufw logging on ==>Sistem kaydının tutulmasını isterseniz bu özelliğin açılması gerekiyor, bunun için ;

24-grep UFW /var/log/syslog  ==>sistem kayıtlarını görüntülemek için

25-sudo ufw logging off     ==>kaydı kapatmak için

26-sudo ufw allow       ==>İnternet erişimine izin vermek için;

27- sudo ufw deny port_no  ==>Belirli bir portun  internet erişimini kapatmak için

28-sudo ufw deny IP_no ==>ıp adresini engellemk için

29- sudo ufw deny telnet  ==>  Telnet erişimini engellemek için

30- sudo ufw delete allow ==>ip engellemelerini iptal eder

31-sudo ufw deny ssh   ==>ssh servisini engeller.

32-sudo ufw allow ssh ==>ssh servisine izin verir.

33-netstat -plnt==>açık portlarınızı görmek için


33-  Port Açma :
     Kod:
     iptables -A INPUT -p tcp --dport -j ACCEPT
     iptables -A INPUT -p udp --dport -j ACCEPT

34-  Port Kapama :
     Dışardan içeriye gelen istekleri kapatmak için :
     Kod:
     iptables -A INPUT -p tcp --dport -j REJECT
     iptables -A INPUT -p udp --dport -j REJECT

35-  İçerden dışarıya giden istekleri kapatmak için :
     Kod:
     iptables -A OUTPUT -p tcp --dport -j REJECT
     iptables -A OUTPUT -p udp --dport -j REJECT


36-sudo iptables -A INPUT -p tcp -d 0/0 -s 0/0 --dport 8081 -j ACCEPT ==>8081.portu açar

37-sudo iptables -A INPUT -p tcp -d 0/0 -s 0/0 --dport 8081 -j DROP   ==>8081.portu kapatır

38-sudo ping -i 0.1 localhost==ping atma


39-youtube-dl YouTube-video-link




40-pacman -S sshuttle

Debian/Ubuntu ve benzeri dağıtımlarda:

apt-get install sshuttle

Fedora kullanıcıları ise EPEL deposunu ekleyip şu şekilde kurabilirler:

yum install sshuttle

Çalıştırmak için ise aşağıdaki komut yetiyor (root olarak veya sudo ile):

sshuttle --dns -r kullanıcı@makine 0/0 -D

Parametrelerin neler yaptığını da açıklayalım:

-r parametresi: remote anlamı taşıyor; yani bağlanacağınız ssh sunucusu
0/0: hedef ağ, 0.0.0.0/0′ın kısaltması. 0/0 tüm internet bağlantısını ifade ediyor. Belirli bir subnete bağlanmak istiyorsanız 0/0 yerine subneti verebilirsiniz.
--dns: DNS sorgularını ssh üzerinden yapmanızı sağlıyor.
-D: sshuttle’ın arkaplanda (daemonize) çalışmasını sağlıyor.

Ne diyelim, zalimin yasakları varsa garibanın da sshuttle’ı var!



41-sudo apt-get install xvidcap ==ekranın videosunu çeker


42-#sudo dpkg --list à sisteme yüklenen tüm paketlerin listesini verir.
Ii - kurulan paketlerdir.
un – yüklenmiş fakat sisteme kurulmamış paketlerdir.



43-#apt-cache search paket_adi à Paket aramak için kullanılır.


44-netstat komutu network arayüzünüzle ilgili bir çok bilgiyi sunmaktadır.

netstat
-p parametresi ile programların ilişkili olduğu socketleri görüntülersiniz.

netstat -p
-s parametresi ile portların detaylı istatistiklerini görüntülersiniz.

netstat -s




46-sudo lsof -i|grep LISTEN == dinlenen portları gösterir


47-wget url ==>url indexini indirir

48-sudo nmap -sV -v 10.0.0.0-255 ==>aynı ağ üzerinde ki ip adres lerini gösterir

49-sudo apt-get install gufw ==>firewall arayünü yükler

50-df==>diskin kullanım miktarını gösterir


51-du dosyaismi ==>dosyanın boyutunu verir

52-gzip dosyaadi==>dosyanın sıkıştırılmasını sağlar

53-gunzip ==>sıkıştırılmış dosyaların açılmasını sağlar



54-where dosyaismi=dosyanın nerde olduğunun gösterir


55-sudo apt-get purge nginx ==>ngnix'i siler.


56-nmap -sP 192.168.1.0/24. ==>tüm ağı tarar

57- cat dosyaismi==dosya içindekleri gösterir

58-cat dosyaismi.log==>.log okuyabilirsin

59-cat acces.log==bize erişenleri gösterir/acces e gelmen lazım

60- apt-get moo==inek figürü çıkarır.

61-echo "istediğiniyaz" > test.txt==>  test dosyasının içine "   " içine yazar

62-sudo apt-get lynx==>lynx yükler

63-lynx www.google.com==>googlun terminal üzerinden gire bilirisn.

64-nano isim.sh
  chmod +x isim.sh
  ./isim.sh

65-nautilus==>dosya aç

  
</dl>
