# Soket Programlama
Socket programlama, bir bilgisayar ağı üzerinden farklı cihazlar arasında iletişim kurmak için kullanılan bir programlama yöntemidir. Bu yöntem, bir bilgisayarın ağ üzerinden diğer bir bilgisayarla veya bir sunucuyla bağlantı kurmasına, veri alışverişi yapmasına ve iletişim kurmasına olanak tanır.

Socket programlama genellikle TCP/IP protokolünü kullanır ve bilgisayarlar arasındaki bağlantı, bir soket olarak adlandırılan bir bağlantı noktası üzerinden gerçekleştirilir. Bu soketler, bir sunucu uygulaması ve bir istemci uygulaması arasındaki iletişimi sağlar.

# İnternet Protokolleri 
## TCP
TCP (Transmission Control Protocol), İnternet Protokolü (IP) üzerinde çalışan bir iletişim protokolüdür. TCP, IP'nin üst katmanında çalışır ve uygulama katmanıyla birlikte çalışarak veri transferini yönetir.

TCP, güvenilir ve sıralı bir bağlantı sağlayarak verilerin kaybolmasını veya bozulmasını önler. Bu amaçla, verilerin doğru şekilde aktarıldığından emin olmak için bir dizi mekanizma kullanır. Örneğin, TCP, gönderilen her paket için bir onaylama (acknowledgement) paketi bekler ve eğer belirli bir süre içinde onaylama gelmezse, paketi yeniden gönderir.

TCP ayrıca, verilerin doğru sırayla alınmasını sağlamak için bir sıra numarası (sequence number) kullanır. Bu numaralar, gönderilen paketlerin hangi sırada alınması gerektiğini belirler ve böylece verilerin doğru şekilde yeniden oluşturulmasını sağlar.


## UDP
UDP (User Datagram Protocol), İnternet Protokolü (IP) üzerinde çalışan bir iletişim protokolüdür. UDP, IP'nin üst katmanında çalışır ve uygulama katmanıyla birlikte çalışarak veri transferini yönetir.

TCP gibi güvenilir bir bağlantı sağlamaz, ancak veri paketlerini hızlı bir şekilde aktarabilir. Bu nedenle, hızlı ve etkili veri transferi gerektiren uygulamalar için kullanılır. Örneğin, oyunlarda gerçek zamanlı etkileşimler için, ses ve video akışı için UDP tercih edilir.

UDP, gönderilen veri paketlerinin doğruluğunu veya sıralamasını sağlamak için bir mekanizma kullanmaz. Bu nedenle, veri paketleri kaybolabilir, bozulabilir veya farklı bir sırayla alınabilir. Ancak, bu tür durumlar için uygulama katmanında hata düzeltme ve kontrol mekanizmaları kullanılabilir.

UDP ayrıca, TCP'nin yaptığı gibi, bir bağlantı kurma veya bağlantıyı sonlandırma işlemleri yapmaz. Bu nedenle, bağlantı kurulduğunda veya kesildiğinde herhangi bir zaman gecikmesi olmaz. Bu özellik, UDP'nin hızlı veri transferi için tercih edilmesine neden olur.

![image](https://user-images.githubusercontent.com/75627147/236814147-a278bcf3-585f-4003-b1dc-76daa66a1428.png)


> Soket programlamada SOCK_STREAM TCP protokolünü; SOCK_DGRAM UDP protokolünü temsil eder. 

## IP 
Internet Protocol (IP), internet üzerindeki cihazların birbirleriyle iletişim kurmasını sağlayan bir protokoldür. IP, veri paketlerinin yönlendirilmesi ve hedef cihaza 
iletilmesi için kullanılır.

Internet Protocol version 4 (IPv4), ilk olarak 1983 yılında tanıtılan ve günümüzde hala yaygın olarak kullanılan bir IP protokolüdür. IPv4, 32 bitlik adresleri 
kullanır ve bu adresler, noktalarla ayrılan dört bölümden oluşan sayılardan oluşur (Örneğin: 192.168.0.1). Ancak IPv4 adresleri, internet kullanımının hızla artması 
nedeniyle tükenmeye başlamıştır.

> Soket programlamada AF_INET makrosu Internet Protocol v4'ü temsil eder.

IPv6, IPv4'ün yerine geçmesi amacıyla 1998 yılında tanıtılmış bir sonraki nesil IP protokolüdür. IPv6, 128 bitlik adresleri kullanır ve bu adresler, onaltılık sayı 
sistemine göre ayrılan sekiz bölümden oluşur (Örneğin: 2001:0db8:85a3:0000:0000:8a2e:0370:7334). IPv6, IPv4'ün aksine adreslerin tükenmesine izin vermez ve daha fazla 
cihazın internete bağlanabilmesini sağlar. IPv6 ayrıca, IPv4'ten daha güvenli ve daha hızlıdır.

Günümüzde, hem IPv4 hem de IPv6 ağlarda kullanılmaktadır. Ancak, IPv6'nın kullanımı hala IPv4'e göre oldukça sınırlıdır ve birçok cihaz hala IPv4 protokolünü 
kullanmaktadır.

> Soket programlamada AF_INET6 makrosu Internet Protocol v6'yı temsil eder.


# TCP/IP
TCP/IP protokolü, internet üzerinden veri transferi için kullanılan bir iletişim protokolüdür. Bu protokol, ağdaki cihazlar arasında veri transferi yapmak için tasarlanmış bir standarttır ve internetin temelini oluşturur.

TCP/IP protokolü, iki ayrı protokolün birleşmesiyle oluşur: Transmission Control Protocol (TCP) ve Internet Protocol (IP). IP protokolü, ağ üzerinden veri paketlerini yönlendirmek için kullanılırken, TCP protokolü, verilerin güvenilir bir şekilde aktarılmasını sağlamak için kullanılır.



### TCP vs TCP/IP
TCP, İnternet Protokolü (IP) üzerinde çalışan bir iletişim protokolüdür ve IP'nin üst katmanında çalışır. TCP, veri transferi sırasında güvenilir bir bağlantı sağlamak için bir dizi mekanizma kullanır ve verilerin doğru şekilde aktarıldığından emin olur.

TCP/IP ise, TCP'nin yanı sıra İnternet Protokolü'nü de içeren bir ağ protokolüdür. TCP/IP, internet bağlantılarının temelini oluşturur ve veri paketlerinin doğru şekilde yönlendirilmesini sağlar. TCP/IP, birçok farklı ağ protokolünün birleştirilmesine olanak tanır ve internet trafiğinin yönetimi için temel bir yapı sağlar.

Yani, TCP ve TCP/IP farklı şeylerdir, ancak TCP/IP, TCP'nin yanı sıra bir dizi diğer protokolü de içerir ve internet trafiğinin yönetimi için temel bir yapı sağlar.



