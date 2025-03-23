# metro_agi
*Metro Simülasyonu (Rota Optimizasyonu)*
Bu proje, bir metro ağında iki istasyon arasındaki en hızlı ve en az aktarmalı rotayı belirleyen bir simülasyon geliştirmeyi amaçlamaktadır.

*Proje İçeriği*
Bu proje, bir graf veri yapısını kullanarak metro istasyonları arasındaki bağlantıları temsil eder ve aşağıdaki algoritmaları kullanarak optimal rotayı belirler:

BFS (Breadth-First Search): En az aktarma ile gidilecek rotayı bulur.

A* (A-Star) Algoritması: En hızlı rotayı bulur.

*Kullanılan Teknolojiler ve Kütüphaneler*

Projede aşağıdaki Python kütüphaneleri kullanılmıştır:

collections.deque: BFS algoritması için kuyruk veri yapısını kullanır.

heapq: A* algoritması için öncelikli kuyruk uygular.

defaultdict: Metro hatlarını gruplamak için kullanılır.

typing: Tür ipuçları sağlar.

*Algoritmaların Çalışma Mantığı*

1. BFS Algoritması (en_az_aktarma_bul)

Amaç: Başlangıç istasyonundan hedef istasyona giderken en az aktarma yaparak rotayı bulmak.

Kuyruk (deque) kullanılır.

Ziyaret edilen istasyonlar takip edilir.

Komşu istasyonlar keşfedilerek en kısa yol belirlenir.

BFS algoritması, genişlik öncelikli arama (Breadth-First Search) olarak çalışır ve en az aktarma gerektiren rotayı garanti eder.

2. A* Algoritması (en_hizli_rota_bul)

Amaç: En kısa sürede gidilebilecek en hızlı rotayı belirlemek.

Öncelik kuyruğu (heapq) kullanılır.

Toplam seyahat süresi hesaplanır.

Hedefe ulaşana kadar en düşük maliyetli (süre) rota takip edilir.

A* algoritması, Dijkstra algoritması gibi çalışır, ancak öncelikli kuyruk kullanarak daha verimli hale getirilmiştir.

*Örnek Kullanım*

Örnek metro ağı aşağıdaki hatlardan oluşmaktadır:

Kırmızı Hat: Kızılay, Ulus, Demetevler, OSB

Mavi Hat: AŞTİ, Kızılay (aktarma), Sıhhiye, Gar

Turuncu Hat: Batıkent, Demetevler (aktarma), Gar (aktarma), Keçiören

*Örnek Test Sonuçları*
AŞTİ'den OSB'ye Gitme Senaryosu

En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

En hızlı rota (17 dakika): AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

Batıkent'ten Keçiören'e Gitme Senaryosu

En az aktarmalı rota: Batıkent -> Demetevler -> Gar -> Keçiören

En hızlı rota (21 dakika): Batıkent -> Demetevler -> Gar -> Keçiören

Keçiören'den AŞTİ'ye Gitme Senaryosu

En az aktarmalı rota: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ

En hızlı rota (19 dakika): Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ

*Proje Geliştirme Fikirleri*

Projeye eklenebilecek bazı geliştirme fikirleri:

Grafiksel Arayüz (GUI) eklenerek etkileşimli harita oluşturulabilir.

Gerçek zamanlı trafik verisi eklenerek metro yoğunluğuna göre dinamik rota önerileri yapılabilir.

Farklı hat renkleri ve mesafe uzunlukları eklenerek görselleştirme geliştirilebilir.

*Projeyi Çalıştırma*

Projeyi çalıştırmak için aşağıdaki adımları izleyin:

Python 3 yüklü olduğundan emin olun.

metro_simulation.py dosyasını çalıştırın

Test sonuçlarını terminalde görüntüleyebilirsiniz.
