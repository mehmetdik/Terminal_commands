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

<dt>9-sudo apt-get install ethtool <dt/>  ==>ethtool gibi oto-müzakere, port hızı, dubleks modu, ve Wake-on-LAN gibi ethernet kartı ayarlarını görüntüler ve değiştiren bir programdır. Bu varsayılan olarak yüklenen, ama depolarda yükleme için kullanılabilir değil

<dt>10-sudo ifconfig eth0 10.0.0.100 netmask 255.255.255.0 <dt/>==geçici olarak ip adresinideğiştirme

<dt>11-sudo route add default gw 10.0.0.1 eth0 <dt/>==

<dt>12-iptables -L <dt/>==>iptables -L komutu ile daha önceden girilmiş iptables kurallarını görüntüleyebilirsiniz

<dt>13-ssh hostname@10.111.1.40<dt/> ==>

<dt>14-subl dosyaadi.uzantı <dt/>==>sublime texti acar

gcc -c deneme2.c   ==>derleme
gcc deneme2.o -o deneme2
./deneme2

<dt>15-netstat<dt/>  ==>kendi açık portlarını görürsün

<dt>16-ssh ile bağlandığın bilgisayarda 4 saat boyunca root şifresi istemez.<dt/>
ControlMaster auto
ControlPath /tmp/ssh_mux_%h_%p_%r
ControlPersist 4h 


<dt>17-sudo unzip ubuntu-logo.zip -d /usr/share/unity/5/ && rm ubuntu-logo.zip <dt/> ==>dash home daki logoyu değiştirir
	wget -O ubuntu-logo.zip http://goo.gl/V6mea       ==>logoyu indirir

<dt>18-sensors<dt/>=Bilgisayarın sıcaklığını ölçme

<dt>19-netstat -an | grep "LISTEN"<dt/> ==>dinlenen portları gösterir

<dt>20-sudo ufw enable  <dt/>  ==>firewall aktif hale etirmek için

<dt>21-sudo ufw status  <dt/>  ==>Güvenlik duvarının aktif yada pasif olduğunu kontrol etmek için,Verilen kuralların listeler

<dt>22-sudo ufw disable <dt/>  ==>firewall pasif hale getirmek için

<dt>23-sudo ufw logging on<dt/> ==>Sistem kaydının tutulmasını isterseniz bu özelliğin açılması gerekiyor, bunun için ;

<dt>24-grep UFW /var/log/syslog<dt/> ==>sistem kayıtlarını görüntülemek için

<dt>25-sudo ufw logging off   <dt/>  ==>kaydı kapatmak için

<dt>26-sudo ufw allow    <dt/>   ==>İnternet erişimine izin vermek için;

<dt>27- sudo ufw deny port_no <dt/> ==>Belirli bir portun  internet erişimini kapatmak için

<dt>28-sudo ufw deny IP_no<dt/> ==>ıp adresini engellemk için

<dt>29- sudo ufw deny telnet <dt/> ==>  Telnet erişimini engellemek için

<dt>30- sudo ufw delete allow <dt/>==>ip engellemelerini iptal eder

<dt>31-sudo ufw deny ssh <dt/>  ==>ssh servisini engeller.

<dt>32-sudo ufw allow ssh<dt/> ==>ssh servisine izin verir.

<dt>33-netstat -plnt<dt/>==>açık portlarınızı görmek için


<dt>33-  Port Açma :<dt/>
     Kod:
     iptables -A INPUT -p tcp --dport -j ACCEPT
     iptables -A INPUT -p udp --dport -j ACCEPT

<dt>34-  Port Kapama :<dt/>
     Dışardan içeriye gelen istekleri kapatmak için :
     Kod:
     iptables -A INPUT -p tcp --dport -j REJECT
     iptables -A INPUT -p udp --dport -j REJECT

<dt>35-  İçerden dışarıya giden istekleri kapatmak için :<dt/>
     Kod:
     iptables -A OUTPUT -p tcp --dport -j REJECT
     iptables -A OUTPUT -p udp --dport -j REJECT


<dt>36-sudo iptables -A INPUT -p tcp -d 0/0 -s 0/0 --dport 8081 -j ACCEPT<dt/> ==>8081.portu açar

<dt>37-sudo iptables -A INPUT -p tcp -d 0/0 -s 0/0 --dport 8081 -j DROP <dt/>  ==>8081.portu kapatır

<dt>38-sudo ping -i 0.1 localhost<dt/>==ping atma


<dt>39-youtube-dl <dt/>YouTube-video-link




<dt>40-pacman -S sshuttle<dt/>

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



<dt>41-sudo apt-get install xvidcap<dt/> ==ekranın videosunu çeker


<dt>42-#sudo dpkg --list <dt/> sisteme yüklenen tüm paketlerin listesini verir.
Ii - kurulan paketlerdir.
un – yüklenmiş fakat sisteme kurulmamış paketlerdir.



<dt>43-#apt-cache search paket_adi  <dt/>Paket aramak için kullanılır.


<dt>44-netstat ==>netstat<dt/>komutu network arayüzünüzle ilgili bir çok bilgiyi sunmaktadır.

<dt/>netstat<dt/>
-p parametresi ile programların ilişkili olduğu socketleri görüntülersiniz.

<dt>netstat -p<dt/>
-s parametresi ile portların detaylı istatistiklerini görüntülersiniz.

<dt>netstat -s<dt/>




<dt>46-sudo lsof -i|grep LISTEN<dt/> == dinlenen portları gösterir


<dt>47-wget url <dt/>==>url indexini indirir

<dt>48-sudo nmap -sV -v 10.0.0.0-255<dt/> ==>aynı ağ üzerinde ki ip adres lerini gösterir

<dt>49-sudo apt-get install gufw<dt/> ==>firewall arayünü yükler

<dt>50-df<dt/>==>diskin kullanım miktarını gösterir


<dt>51-du dosyaismi<dt/> ==>dosyanın boyutunu verir

<dt>52-gzip dosyaadi<dt/>==>dosyanın sıkıştırılmasını sağlar

<dt>53-gunzip<dt/> ==>sıkıştırılmış dosyaların açılmasını sağlar



<dt>54-where dosyaismi<dt/>=dosyanın nerde olduğunun gösterir


<dt>55-sudo apt-get purge nginx<dt/> ==>ngnix'i siler.


<dt>56-nmap -sP 192.168.1.0/24<dt/> ==>tüm ağı tarar

<dt>57- cat dosyaismi<dt/>==dosya içindekleri gösterir

<dt>58-cat dosyaismi.log<dt/>==>.log okuyabilirsin

<dt>59-cat acces.log<dt/>==bize erişenleri gösterir/acces e gelmen lazım

<dt>60- apt-get moo<dt/>==inek figürü çıkarır.

<dt>61-echo "istediğiniyaz" > test.txt<dt/>==>  test dosyasının içine "   " içine yazar

<dt>62-sudo apt-get lynx<dt/>==>lynx yükler

<dt>63-lynx www.google.com<dt/>==>googlun terminal üzerinden gire bilirisn.

<dt>64-nano isim.sh<dt/>
  chmod +x isim.sh
  ./isim.sh

<dt>65-nautilus<dt/>==>dosya aç

  
</dl>
