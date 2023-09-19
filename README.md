# README

## Nama    : Resanda Dezca Asyam

## NPM     : 2206082682

## Kelas   : PBP C


## Soal Tugas 1

Penjelasan Dari Soal-Soal:
1. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).

    **a.  Membuat sebuah project Django awal**

        Saya memulai proyek pengelolaan inventori game pada karakter LightReborn dengan langkah-langkah yang terstruktur. Pertama-tama, 
        saya memulai dengan menginisiasi repositori baru menggunakan perintah "git init" Ini secara otomatis membuat repositori Git 
        kosong di dalam direktori yang sebelumnya telah saya buat, yaitu "resa_lightreborn." Langkah berikutnya adalah menginisiasi 
        repositori di GitHub untuk memulai pelacakan perubahan proyek "resa_lightreborn" secara daring. Setelah itu, saya menghubungkan 
        repositori lokal dengan repositori di GitHub, memastikan bahwa semua perubahan dapat disimpan secara online.

        Langkah selanjutnya adalah menginstalasi Django dan menginisiasi proyek Django. Untuk menjaga lingkungan yang terisolasi, saya    
        mengaktifkan Virtual Environment di dalam direktori "resa_lightreborn." Setelah itu, saya menyiapkan semua dependensi yang 
        diperlukan dan membuat proyek Django. Selanjutnya, saya melakukan konfigurasi proyek dengan mengizinkan akses dari semua host, 
        memastikan bahwa aplikasi dapat diakses secara luas. Untuk memverifikasi apakah proyek Django berhasil dibuat, saya menjalankan 
        server lokal.Terakhir, saya mengunggah proyek "resa_lightreborn" ke repositori GitHub dengan membuat berkas ".gitignore" untuk 
        menentukan berkas-berkas dan direktori-direktori yang harus dikecualikan oleh Git. Setelah itu, saya menjalankan proses "add," 
        "commit," dan "push" dari direktori repositori lokal, sehingga proyek saya dapat terus berkembang.
        
    **b.  Membuat aplikasi bernama main pada project yang telah dibuat** 

        Selanjutnya, saya menjalankan instruksi "python manage.py startapp main" untuk menciptakan direktori baru yang diberi nama 
        "main." Di dalam direktori ini, saya memulai proses pembangunan struktur awal aplikasi, yang akan digunakan untuk menampilkan 
        informasi inventori karakter pada app lightreborn.    

    **c.  Melakukan routing pada proyek agar dapat menjalankan aplikasi main**

        Setelah berhasil membuat aplikasi "main," langkah selanjutnya adalah mendaftarkannya ke dalam proyek Django agar dapat diakses 
        dan digunakan. Tahap ini melibatkan penambahan 'main' ke dalam daftar aplikasi yang telah terdaftar dalam variabel 
        "INSTALLED_APPS" yang ada di berkas "settings.py". Berkas "settings.py" tersebut terletak di dalam direktori proyek 
        "resa_lightreborn". Setelah itu, saya menciptakan sebuah folder bernama template yang berisi "main.html" dalam direktori 
        "templates" yang telah dibuat sebelumnya dalam  aplikasi "main." Template ini memiliki peran krusial dalam tampilan inventori 
        karakter lightreborn. Dalam proses pembuatan "main.html," saya mengisi template tersebut dengan kode HTML yang sederhana, 
        termasuk elemen-elemen seperti judul(application), nama, dan class. Tujuannya adalah untuk memeriksa tampilan dasar halaman HTML 
        yang akan digunakan untuk menampilkan informasi inventori karakter lightreborn.
    
    **d.  Mulai membuat model pada aplikasi main dengan nama Item dan memiliki atribut wajib seperti pada tugas 2**

        Tahap berikutnya dari project Inventori Karakter LightReborn, saya melakukan beberapa perubahan dalam berkas "models.py" yang 
        terletak dalam direktori aplikasi "main." Perubahan ini dimaksudkan untuk mengintroduksi model baru yang diberi nama "Item." 
        Model ini mengandung beberapa bidang, termasuk "name" untuk menyimpan nama item dengan tipe data CharField, "amount" untuk 
        menyimpan jumlah item dengan tipe data IntegerField, dan "description" untuk menyimpan deskripsi item dengan tipe data TextField, 
        yang memungkinkan penyimpanan teks yang lebih panjang. Setelah model "Item" didefinisikan, langkah berikutnya adalah menciptakan 
        dan menerapkan migrasi model. Ini merupakan langkah kunci dalam melacak perubahan pada model basis data.

    **e.  Membuat sebuah fungsi di views.py yang akan menghasilkan output ke dalam sebuah template HTML. Output tersebut akan menampilkan nama aplikasi dan juga nama serta kelas yang dibuat**
 
        Lalu, saya melanjutkan dengan mengintegrasikan komponen MVT (Model-View-Template) dalam kerangka kerja Django. Pertama, saya 
        mengimpor modul yang diperlukan dan membuat sebuah fungsi view yang dinamakan "show_main". Fungsi "render" yang berasal dari 
        modul "django.shortcuts" digunakan untuk merender tampilan HTML dengan data yang diberikan.

        Fungsi "show_main" menerima parameter "request" yang merupakan objek permintaan HTTP dari pengguna. Fungsi ini berperan dalam 
        mengatur permintaan tersebut dan mengembalikan tampilan yang sesuai. Dalam fungsi "show_main," saya menggunakan dictionary 
        "context" untuk mengemas data yang akan disampaikan ke tampilan. Data yang dimasukkan meliputi nama aplikasi, serta nama dan 
        kelas yang relevan dengan proyek.

        Saya menggunakan fungsi "render" dengan tiga argumen: "request" sebagai objek permintaan HTTP, "main.html" sebagai nama berkas 
        template, dan "context" sebagai dictionary yang berisi data untuk membuat tampilan menjadi dinamis. Selama proses ini, saya juga 
        mengubah judul (nama aplikasi), nama, dan kelas yang sebelumnya statis dalam tampilan HTML menjadi kode Django yang memungkinkan 
        nilai-nilainya berasal dari variabel-variabel yang telah didefinisikan dalam "context".

    **f.  Menyiapkan routing dalam berkas "urls.py" aplikasi "main" untuk mengaitkan fungsi yang telah saya buat dalam "views.py".**

        Pertama-tama, saya melakukan konfigurasi routing URL untuk aplikasi "main" dengan membuat berkas baru yang dinamakan "urls.py" di 
        dalam direktori "main". Fungsi dari berkas "urls.py" ini adalah mengatur bagaimana rute URL terkait langsung dengan aplikasi 
        "main" akan ditangani.

        Selanjutnya, saya melanjutkan dengan mengonfigurasi routing URL pada tingkat proyek secara keseluruhan. Ini dilakukan dengan 
        menambahkan rute URL yang akan mengarahkan pengguna ke tampilan yang ada di aplikasi "main." Rute URL ini kemudian dimasukkan ke 
        dalam variabel "urlpatterns" yang terdapat dalam berkas "urls.py" yang berada di dalam direktori proyek "resa_lightreborn."

        Dengan konfigurasi ini, proyek sekarang memiliki mekanisme yang jelas untuk mengarahkan permintaan URL pengguna ke tampilan yang 
        sesuai dalam aplikasi "main."

    **g.  *Unit Testing*, membuat berkas README.md, dan melakukan proses deployment aplikasi yang sudah dibuat agar dapat diakses oleh teman-teman melalui internet.**

        Pertama-tama, saya telah membuat serangkaian unit testing untuk memverifikasi bahwa kode yang telah saya tulis berfungsi sesuai 
        dengan yang diharapkan. Salah satu pengujian adalah "test_main_url_is_exist," yang berfungsi untuk memeriksa apakah alamat URL 
        "/main/" dapat diakses dengan sukses. Pengujian lainnya adalah "test_main_using_main_template," yang bertujuan untuk memastikan 
        bahwa halaman "/main/" dirender dengan benar menggunakan template "main.html." Terakhir, ada pengujian "test_item_model" yang 
        mengonfirmasi kemampuan aplikasi dalam menyimpan dan mengambil data dengan benar dari basis data menggunakan model "Item" yang 
        telah saya definisikan. Semua pengujian ini telah berhasil dilakukan, menunjukkan bahwa kode yang saya tulis berjalan sesuai 
        harapan.

        Langkah terakhir dalam proyek ini adalah memastikan repositori GitHub saya terbarui. Saya telah membuat berkas "README.md" dan 
        melakukan proses "add," "commit," dan "push" ke GitHub. Selanjutnya, saya melakukan proses deployment project "resa_lightreborn" 
        ke platform Adaptable. Saya memilih template "Python App" dengan menggunakan "PostgreSQL" sebagai basis data, serta Python 3.11 
        sebagai lingkungan pelaksanaan. Perintah "python manage.py migrate && gunicorn resa_lightreborn.wsgi" digunakan sebagai perintah 
        awal untuk menjalankan aplikasi. Situs web dapat diakses melalui domain "resalightreborn" dengan menggunakan HTTP Listener yang 
        telah diatur pada PORT. Dengan demikian, proyek saya telah berhasil di-deploy dan siap digunakan secara online.

2. Buatlah bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya dan jelaskan pada bagan tersebut kaitan antara urls.py, views.py, models.py, dan berkas html.

    ![Bagan Resa](bagan_resa.png)

3. Jelaskan mengapa kita menggunakan virtual environment? Apakah kita tetap dapat membuat aplikasi web berbasis Django tanpa menggunakan virtual environment?

    Kita menggunakan virtual environment dalam pengembangan aplikasi web berbasis Django karena itu memungkinkan kita untuk menciptakan lingkungan terisolasi yang mengelola dependensi proyek secara efisien. Ini sangat penting karena setiap proyek mungkin memerlukan versi paket Python dan dependensi yang berbeda, sehingga virtual environment membantu menghindari konflik dan masalah kompatibilitas. Tanpa virtual environment, kita dapat membuat aplikasi Django, tetapi akan terbatas dalam pengelolaan dependensi, rentan terhadap konflik, dan lebih sulit untuk menjaga kebersihan sistem. Oleh karena itu, meskipun memungkinkan, sebaiknya kita selalu menggunakan virtual environment dalam pengembangan aplikasi web Django untuk menjaga isolasi dan manajemen dependensi yang efektif.

4. Jelaskan apakah itu MVC, MVT, MVVM dan perbedaan dari ketiganya.

    MVC (Model-View-Controller), MVT (Model-View-Template), dan MVVM (Model-View-ViewModel) adalah pola desain yang digunakan dalam pengembangan perangkat lunak.

    1. MVC: Terdiri dari Model (data dan logika bisnis), View (tampilan yang diberikan kepada pengguna), dan Controller (pengendali alur aplikasi). Controller menghubungkan Model dan View.

    2. MVT: Ini adalah varian dari MVC yang digunakan dalam Django. Model sama, View mengatur logika tampilan, dan Template mengatur tampilan. "Controller" diatur oleh Django secara internal.

    3. MVVM: Digunakan dalam pengembangan aplikasi antarmuka pengguna (UI). Model adalah data dan logika, View menampilkan tampilan, dan ViewModel berperan sebagai perantara. ViewModel mengubah data dari Model agar sesuai dengan tampilan.

    Perbedaannya adalah bagaimana komponen-komponen ini berinteraksi. MVC menggunakan Controller, MVT memiliki tugas Controller internal di Django, sementara MVVM menggunakan ViewModel sebagai perantara. MVC adalah pola desain umum, MVT adalah variasi untuk Django, dan MVVM cocok untuk pengembangan aplikasi UI modern.

## Soal Tugas 2
1. Apa perbedaan antara form POST dan form GET dalam Django?

    Perbedaan antara metode form POST dan GET dalam Django, serta dalam pengembangan web secara umum adalah:

    **Form GET:**

* Pengiriman Data
    * Data dari form dikirimkan sebagai bagian dari URL.
* Visibilitas Data
    * Data yang dikirimkan dengan metode GET terlihat di URL browser.
* Keamanan
    * Kurang aman karena data terbuka dan bisa dilihat oleh siapa saja.
* Pemakaian
    * Biasanya digunakan ketika Anda ingin mendapatkan atau mengakses data tanpa mengubahnya, seperti pencarian atau filter data.
* Contoh
    * Ketika Anda mencari sesuatu di mesin pencari, kata kunci pencarian ditampilkan di URL sebagai query string.

    **Form POST:**

* Pengiriman Data
    * Data dari form dikirimkan secara tersembunyi dalam tubuh permintaan HTTP.
* Visibilitas Data
    * Data tidak terlihat di URL dan lebih aman karena tidak dapat dengan mudah diakses oleh orang lain.
* Keamanan
    * Lebih aman karena data tersembunyi.
* Pemakaian
    * Digunakan ketika Anda ingin mengirim data ke server untuk diproses, seperti ketika Anda mengisi formulir pendaftaran atau mengirim komentar ke situs web.
* Contoh
    * Ketika Anda mengisi formulir pendaftaran online, data yang Anda masukkan (seperti nama, alamat email, dan kata sandi) tidak terlihat di URL.

    Jadi, perbedaan utama antara metode GET dan POST adalah bagaimana data dari formulir disampaikan dan dikelola. GET digunakan untuk mengambil data dari server tanpa mengirim data yang signifikan, sementara POST digunakan untuk mengirim data ke server untuk melakukan tindakan tertentu, seperti menambahkan data ke database atau mengirim pesan. Selain itu, POST lebih aman karena data tidak terlihat di URL, sementara GET memiliki visibilitas data yang lebih tinggi.

2. Apa perbedaan utama antara XML, JSON, dan HTML dalam konteks pengiriman data?

    Perbedaan utama antara XML, JSON, dan HTML dalam konteks pengiriman data adalah:

    **XML (eXtensible Markup Language):**

    * Tujuan Utama
        * Digunakan untuk menyusun dan mentransmisikan data terstruktur antara aplikasi dan platform yang berbeda.
    * Format
        * Teks yang diorganisasi dengan tag yang mendefinisikan struktur data.
    * Kelebihan
        * Fleksibel dan kuat untuk mendefinisikan struktur data yang kompleks.
    * Kekurangan
        * Lebih berat dan rumit daripada format lain seperti JSON.

    **JSON (JavaScript Object Notation):**

    * Tujuan Utama
        * Digunakan untuk pertukaran data antara aplikasi yang sering kali ditulis dalam bahasa pemrograman yang berbeda.
    * Format
        * Teks yang menggambarkan objek dan array dalam bahasa pemrograman.
    * Kelebihan
        * Mudah dibaca oleh manusia dan mudah diolah oleh komputer. Ringan dan efisien.
    * Kekurangan
        * Kurang fleksibel dalam hal mendefinisikan struktur data yang kompleks dibandingkan dengan XML.

    **HTML (HyperText Markup Language):**
    * Tujuan Utama
        * Digunakan untuk merender konten web dalam bentuk yang dapat diinterpretasi oleh peramban web.
    * Format
        * Teks yang diorganisasi dengan tag yang mendefinisikan struktur dan tampilan konten web.
    * Kelebihan
        * Digunakan untuk membuat tampilan dan struktur halaman web. Mendukung tautan hypertext dan media.
    * Kekurangan
        * Terutama digunakan untuk tampilan, bukan pertukaran data terstruktur.

    Jadi, perbedaan utama antara ketiga format ini adalah tujuan penggunaannya. XML dan JSON digunakan untuk pertukaran data terstruktur antara aplikasi, sementara HTML digunakan untuk membuat tampilan dan struktur halaman web. XML cenderung lebih fleksibel tetapi kompleks, JSON ringan dan mudah dibaca, sedangkan HTML digunakan untuk mengatur tampilan konten web.

3. Mengapa JSON sering digunakan dalam pertukaran data antara aplikasi web modern?

    JSON sering digunakan dalam pertukaran data antara aplikasi web modern karena format datanya yang mudah dibaca dan ditulis, ringan, dan mendukung struktur data terstruktur, mirip dengan objek dan array dalam bahasa pemrograman. Hal ini memungkinkan pengembang untuk dengan mudah mengirim, menerima, dan memproses data antar-aplikasi tanpa perlu memikirkan banyak overhead atau kompleksitas. JSON juga mendukung banyak bahasa pemrograman dan diintegrasikan dengan baik dalam lingkungan pengembangan web, membuatnya menjadi pilihan alami untuk berkomunikasi dan berbagi data antar-aplikasi web yang berbeda.

4. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).

    1. Membuat input form untuk menambahkan objek model pada app sebelumnya.
        1. Langkah pertama yang saya lakukan adalah menciptakan sebuah template dasar yang bertindak sebagai kerangka umum untuk halaman web dalam proyek ini. Saya menaruh template ini di dalam direktori 'templates' yang terletak di root folder proyek. Setelah itu, saya melakukan penyesuaian pada konfigurasi berkas 'settings.py' yang berada dalam subdirektori 'resa_lightreborn' agar template 'base.html' dapat dikenali sebagai sebuah template. Selanjutnya, dalam subdirektori templates yang ada di dalam direktori 'main', saya melakukan perubahan pada kode berkas 'main.html' agar menggunakan 'base.html' sebagai template utama.
        2. Kemudian, saya membuat sebuah formulir sederhana yang memungkinkan pengguna untuk memasukkan data produk yang akan ditampilkan di halaman utama. Untuk langkah ini, saya menciptakan sebuah berkas baru yang dinamakan 'forms.py' di dalam direktori 'main' untuk merancang struktur formulir. Di dalam 'forms.py', saya melakukan definisi terhadap model yang akan digunakan oleh formulir, yakni 'Item'. Ketika pengguna mengisi formulir dan mengirimkannya, data yang dimasukkan akan disimpan sebagai objek 'Item'. Selain itu, saya juga menentukan field-field yang akan digunakan dalam model 'Item' dalam formulir ini, seperti "name", "amount", dan "description".
        3. Setelah itu, saya melakukan penambahan beberapa impor yang dibutuhkan pada berkas 'views.py' di dalam direktori 'main'. Setelahnya, saya membuat sebuah fungsi baru yang diberi nama 'create_item' dalam berkas tersebut. Fungsi ini menerima parameter 'request' dan berisikan kode yang bertujuan untuk menghasilkan sebuah formulir secara otomatis ketika data dari formulir tersebut di-submit. Di dalam fungsi 'create_item', saya memanfaatkan 'ItemForm' untuk menciptakan sebuah objek formulir yang didasarkan pada data yang diterima dari 'request.POST'. Selanjutnya, saya melakukan validasi terhadap isi input yang dimasukkan ke dalam formulir tersebut dengan menggunakan 'form.is_valid()', dan apabila data yang dimasukkan valid, saya menyimpan informasi dari formulir ke dalam database dengan menggunakan 'form.save()'. Terakhir, setelah data formulir berhasil disimpan, saya mengarahkan pengguna kembali ke halaman utama dengan menggunakan 'HttpResponseRedirect(reverse('main:show_main'))'.
        4. Setelah itu, saya melakukan perubahan pada fungsi 'show_main' yang telah ada dalam berkas 'views.py' dengan menambahkan 'item': item ke dalam dictionary konteks. Untuk mengambil semua objek 'Item' yang telah disimpan dalam database, saya menjalankan perintah 'item = Item.objects.all()'.
        5. Saya menciptakan sebuah berkas HTML yang baru dengan nama 'create_item.html' dan menempatkannya di dalam direktori 'main/templates'. Di dalam berkas ini, saya menggunakan kode berikut:
            * &lt;form method="POST">: Ini digunakan untuk menetapkan blok form dengan menggunakan metode POST.
            * {% csrf_token %}: Ini adalah token keamanan yang selalu di-generate secara otomatis secara berkala oleh Django untuk mencegah dari serangan berbahaya.
            * {{ form.as_table }}: Ini digunakan untuk menampilkan field-field form yang telah didefinisikan dalam 'forms.py' sebagai tabel.
            * &lt;input type="submit" value="Add Item"/>: Ini untuk membuat tombol submit yang akan mengirimkan permintaan ke view 'create_item(request)'.

        6. Terakhir, saya kembali ke halaman 'main.html' dan memasukkan kode ke dalam bagian {% block content %} dengan tujuan untuk menampilkan data produk dalam format tabel serta menambahkan tombol "Add New Item" yang akan mengalihkan pengguna ke halaman formulir.<br><br>
    2. Tambahkan 5 fungsi views untuk melihat objek yang sudah ditambahkan dalam format HTML, XML, JSON, XML by ID, dan JSON by ID.
        1. Pertama-tama, saya membuka berkas views.py dalam direktori 'main'. Di dalamnya, saya menambahkan import untuk HttpResponse dan Serializer.
        2. Setelah itu, saya menciptakan sebuah fungsi baru yang dinamakan show_xml dan menerima parameter request. Dalam fungsi show_xml ini, saya membuat sebuah variabel untuk menyimpan hasil dari kueri data dari seluruh objek yang ada dalam model Item. Kemudian, saya menghasilkan respons HttpResponse dengan mengatur data yang berisi hasil kueri tersebut yang telah di-serialisasi ke dalam format XML, dan menentukan content_type sebagai "application/xml" untuk menandakan bahwa data yang dikirimkan berformat XML.
        3. Setelah itu, saya membuat sebuah fungsi baru yang saya beri nama show_json. Fungsi ini juga menerima parameter request. Dalam implementasinya, saya menjalankan tugas yang serupa dengan fungsi show_xml, yaitu menghasilkan hasil kueri dari seluruh data yang ada dalam model Item. Kemudian, respons HttpResponse dihasilkan dengan mengatur parameter data yang berisi hasil kueri tersebut yang telah di-serialisasi ke dalam format JSON, dan content_type ditetapkan sebagai "application/json" untuk menunjukkan bahwa data yang dikirimkan dalam bentuk JSON.
        4. Terakhir, saya menciptakan dua fungsi baru, yakni show_xml_by_id dan show_json_by_id, yang menerima parameter request dan id. Di dalam kedua fungsi ini, saya melakukan pencarian data dengan ID tertentu dari model Item. Selanjutnya, saya menghasilkan respons HttpResponse dengan menentukan parameter data yang berisi hasil pencarian tersebut yang telah di-serialisasi entah dalam format XML atau JSON, bergantung pada fungsi yang dipanggil. Saya juga menetapkan content_type sesuai dengan format yang diinginkan, yaitu "application/xml" untuk XML atau "application/json" untuk JSON.<br><br>
        
    3. Membuat routing URL untuk masing-masing views yang telah ditambahkan pada poin 2.
        1. Pertama-tama, saya membuka berkas urls.py dalam direktori 'main'. Di dalamnya, saya melakukan impor fungsi-fungsi yang telah saya buat sebelumnya di views.py. Kemudian, saya menambahkan beberapa path URL ke dalam urlpatterns. Inilah setiap path URL yang saya tambahkan:
            * path('create-item', create_item, name='create_item'),
            * path('xml/', show_xml, name='show_xml'),
            * path('json/', show_json, name='show_json'),
            * path('xml/&lt;int:id>/', show_xml_by_id, name='show_xml_by_id'),
            * path('json/&lt;int:id>/', show_json_by_id, name='show_json_by_id'), 

5. Mengakses kelima URL di poin 2 menggunakan Postman, membuat screenshot dari hasil akses URL pada Postman, dan menambahkannya ke dalam README.md.

    **Gambar**

    ![Gambar-1](gambar-1.png)

    ![Gambar-2](gambar-2.png)

    ![Gambar-3](gambar-3.png)

    ![Gambar-4](gambar-4.png)
    
    ![Gambar-5](gambar-5.png)