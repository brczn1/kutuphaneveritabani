📚 Kütüphane Yönetim Sistemi Veritabanı Projesi
📋 Proje Hakkında
Bu proje, bir kütüphane yönetim sisteminin veritabanı yapısını ve işlevlerini içermektedir. PostgreSQL veritabanı kullanılarak geliştirilmiştir.

🗃️ VERİTABANI TABLOLARI VE VERİ SAYILARI
📊 Tablo İstatistikleri
No	Tablo Adı	Kayıt Sayısı	Açıklama
1	yazarlar	10 kayıt	Türk edebiyatından ünlü yazarlar
2	yayinevleri	5 kayıt	Büyük Türk yayınevleri
3	kategoriler	8 kayıt	Kitap türleri
4	uyeler	15 kayıt	Kütüphane üyeleri
5	kitaplar	20 kayıt	Gerçek Türk edebiyatı kitapları
6	odunc_kayitlari	28 kayıt	Ödünç alma kayıtları
7	rezervasyonlar	8 kayıt	Kitap rezervasyonları
8	ceza_kayitlari	3 kayıt	Gecikme cezaları

1. Fonksiyonlar (3 adet)
●	calculate_fine(loan_id) - Gecikme cezasını hesaplayan fonksiyon
●	book_availability(book_id) - Kitabın müsaitlik durumunu kontrol eden
●	member_borrowed_count(member_id) - Üyenin ödünç aldığı toplam kitap sayısı
2. Triggerlar (3 adet)
●	Kitap ödünç alındığında stok miktarını düşüren trigger
●	İade yapıldığında gecikme varsa otomatik ceza kaydı oluşturan trigger
●	Kitap teslim edildiğinde stokları güncelleyen trigger
3. Stored Procedure'ler (2 adet)
●	sp_borrow_book() - Kitap ödünç alma işlemi
●	sp_return_book() - Kitap iade işlemi (ceza hesaplama dahil)
4. View'lar (2 adet)
●	En çok ödünç alınan kitaplar ve yazarları
●	Üyelerin ödünç alma istatistikleri
5. Kompleks Sorgular
●	Kategorilere göre kitap sayıları ve ödünç alınma oranları
●	Yazarlara göre toplam ödünç alınma sayıları
●	Subquery ile: Ortalamadan fazla gecikmesi olan üyeler
