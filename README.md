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


# Soket Programlama Aşamaları

## Server-Client Uygulaması

**SERVER**
1. Soket Oluşturmak (Create Socket)

İlk olarak, server ve client tarafında socket oluşturulması gerekir. Bu, socket tanımlayıcılarının oluşturulmasını ve ağa bağlanmalarını sağlar.
```c
        int server_socket = socket(AF_INET, SOCK_STREAM, 0);               
```
- İlk parametre olan "AF_INET", internet protokolü ailesinin (IPv4) kullanılacağını belirtir.

- İkinci parametre olan "SOCK_STREAM", TCP protokolü kullanılarak iletişim kurulacağını belirtir.

- Üçüncü parametre olan "0", protokolü belirlemede kullanılır ve genellikle sıfırlanarak varsayılan protokol kullanılır.

2. Bağlamak (Bind)

Server tarafında, socket'in bir IP adresi ve port numarası ile eşleştirilmesi gerekmektedir. Bu işlem, serverın belirli bir port numarasına dinleme modunda kalmasını 
sağlar ve clientların server'a bağlanabilmesini mümkün kılar.
```c
#define PORT 4700
#define SERVER_IP "127.0.0.1"

    struct sockaddr_in server_addr = { 0 };
    server_addr.sin_family = AF_INET;  
    server_addr.sin_addr.s_addr = INADDR_ANY;
    //server_addr.sin_addr.s_addr = SERVER_IP 
    server_addr.sin_port = htons(PORT);
```
- #define ile PORT ve SERVER_IP sabitleri tanımlanır. PORT, server tarafındaki soketin belirleneceği port numarasını tutar. SERVER_IP, serverın IP adresini belirtir. Bu durumda, 127.0.0.1, localhost olarak bilinen yerel bilgisayarın IP adresidir.
- struct sockaddr_in türündeki server_addr adres yapısı tanımlanır ve tüm elemanları sıfıra eşitlenir.
- server_addr.sin_family = AF_INET; ile, adres yapısının internet protokol ailesi (IPv4) olarak ayarlanması sağlanır.
- server_addr.sin_addr.s_addr = INADDR_ANY; ile, adres yapısının IP adresinin belirtilmemesi ve dinlemeye başlanacak tüm IP adreslerinden bağlantı isteklerini kabul etmesi sağlanır.
- server_addr.sin_port = htons(PORT); ile, adres yapısının belirtilen PORT numarasına bağlanması sağlanır. htons() fonksiyonu, byte düzenlemesi nedeniyle, port numarasını doğru sırayla yerleştirmek için kullanılır.

3. Dinlemek (Listen)

Server tarafında, belirli bir port üzerinden dinlemeye başlamak için listen() fonksiyonu çağrılır. Bu, serverın gelen bağlantıları kabul etmek için hazır olduğunu 
bildirir.

```c
    if (listen(server_socket, BACKLOG) == -1) {
        perror("listen() error");
        close(server_socket);
        return errno;
    }
    printf("Port Listening Successful! Port: %d\n", PORT);
```

- listen() fonksiyonu, server tarafındaki soketi belirtilen BACKLOG (dinlemeye hazır bekleme kuyruğu) boyutu ile dinlemeye başlar.

Eğer listen() fonksiyonu -1 dönerse, bir hata oluştuğu anlamına gelir ve hata mesajı ("listen() error") ve errno değeri kullanılarak hata nedeni belirtilir.

- close(server_socket) ile, soketin kapatılması sağlanır.

- printf() fonksiyonu ile, server tarafındaki soketin belirtilen PORT numarasında dinlemeye başarılı bir şekilde başladığı kullanıcıya bildirilir.

4. Accept (Kabul)

Server tarafında, gelen bağlantıları kabul etmek için accept() fonksiyonu çağrılır. Bu fonksiyon, bir client bağlantısı geldiğinde, o bağlantıya özgü bir socket 
tanımlayıcısı döndürür. Bu socket tanımlayıcısı, client ile iletişim kurmak için kullanılacaktır.

```c
    struct sockaddr_in client_addr = { 0 };
    socklen_t client_addr_len = sizeof(client_addr);
    
    int client_socket = accept(server_socket, (struct sockaddr*) &client_addr, &client_addr_len);
```

- struct sockaddr_in tipinde client_addr adres yapısı tanımlanır ve tüm elemanları sıfıra eşitlenir.
- socklen_t tipinde client_addr_len değişkeni, client_addr adres yapısının boyutunu tutar.
- accept() fonksiyonu, server tarafındaki sokete gelen bağlantı taleplerini kabul eder ve bir client soketi tanımlayıcısı döndürür. 
  - İlk parametre olarak server_socket kullanılır.
  - İkinci parametre olarak, struct sockaddr* tipindeki client_addr adresi kullanılır. accept() fonksiyonu, bu adres yapısına client tarafından gelen bağlantı isteğinin ayrıntılarını doldurur.
  - Üçüncü parametre olarak, socklen_t* tipindeki client_addr_len değişkeni kullanılır. Bu, accept() fonksiyonu tarafından doldurulan client_addr adres yapısının boyutunu tutar.

> accept() fonksiyonu, bir hata oluşursa -1 döner ve hata nedeni errno değişkeninde tutulur.


5. Bağlantı (Connect) //Client.c

```c
    if (connect(socket_fd, (struct sockaddr *)&server_addr, sizeof(server_addr)) == -1) {
        perror("connect() error");
        close(socket_fd);
        return errno;
    }
    printf("SUCCESSFUL | Connected to the server!\n");
```
Bu kod, client tarafında, sunucu ile bağlantı kurmak için kullanılır.

- connect() fonksiyonu, belirtilen sokete bağlanır. Bu, client tarafından sunucuya bağlanmak için kullanılır.
  - İlk parametre olarak socket_fd soketi kullanılır. Bu, bağlantının yapılacağı soketi temsil eder.
  - İkinci parametre olarak, sunucunun adresini tutan server_addr yapısının adresi kullanılır. Bu, bağlanılacak sunucunun adresini temsil eder.
  - Üçüncü parametre olarak, sizeof(server_addr) kullanılır. Bu, sunucunun adres yapısının boyutunu temsil eder.
- Eğer bağlantı başarısız olursa, connect() fonksiyonu -1 döndürür ve hata nedeni errno değişkeninde tutulur.
- perror() fonksiyonu, connect() fonksiyonundan dönen hatayı ekrana yazdırır.
- close() fonksiyonu, belirtilen soketi kapatır ve soketi artık kullanılamaz hale getirir.


6. Send/Receive

Server ve client arasında, veri alışverişi yapmak için send() ve receive() fonksiyonları kullanılır. Server, accept() fonksiyonu ile alınan socket tanımlayıcısını 
kullanarak gelen mesajları alır ve client tarafına send() fonksiyonuyla gönderir. Client, connect() fonksiyonu ile belirli bir servera bağlanır ve receive() fonksiyonu 
ile serverdan gelen mesajları alır ve send() fonksiyonu ile servera yanıt gönderir.

```c
  char client_message[MESSAGE_LENGTH] = { 0 };
    ssize_t recv_result = recv(client_socket, client_message, sizeof(client_message), 0);
```

- char tipinde, MESSAGE_LENGTH uzunluğunda client_message adlı bir karakter dizisi tanımlanır ve tüm elemanları sıfıra eşitlenir. Bu, alınacak mesajın depolanacağı bellek alanını temsil eder.
- ssize_t tipinde recv_result değişkeni, recv() fonksiyonunun dönüş değerini tutar.
- recv() fonksiyonu, client_socket soketinden gelen veriyi, client_message karakter dizisine okur. 
  - İkinci parametre olarak client_message kullanılır.
  - Üçüncü parametre olarak, sizeof(client_message) kullanılır. Bu, client_message karakter dizisinin boyutunu temsil eder.
  - Dördüncü parametre olarak, 0 kullanılır. Bu, özel bir bayrak değeridir ve verinin alınmasına yönelik özel bir işlem yapmaz.

> recv() fonksiyonu, veri alımı tamamlandığında, alınan bayt sayısını döndürür. Eğer bir hata oluşursa, -1 döner ve hata nedeni errno değişkeninde tutulur.


7. Close

İletişim sona erdiğinde, server ve client taraflarında kullanılan socketler kapatılır. Bu, kaynakların serbest bırakılmasını ve daha fazla iletişim için hazır hale 
getirilmesini sağlar.

```c
    close(client_socket);
    close(server_socket);
```

close() fonksiyonu, belirtilen soketi kapatır ve soketi artık kullanılamaz hale getirir.

İlk olarak, client_socket soketi kapatılır. Bu, client ile olan iletişimin sonlandırılması ve soketin serbest bırakılması için kullanılır.

Ardından, server_socket soketi kapatılır. Bu, server tarafındaki soketin serbest bırakılması için kullanılır.

Soketlerin kapatılması, programın sonlandırılması veya soketlerin yeniden kullanılmayacağı durumlarda önemlidir. Soketlerin serbest bırakılmaması, kaynak tüketimine ve potansiyel olarak sistem çökmesine neden olabilir.



























