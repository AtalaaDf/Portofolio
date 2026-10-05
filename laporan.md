Halaman utama menggunakan tiga elemen section, setiap section memiliki id dan dipakai oleh tautan navigasi untuk menuju bagian tertentu, ada 3 section dibagian home yaitu section dengan id home, section dengan id skill yang berisi skill dan section yang berisi contact yang berisi contact

lalu di bagian project setiap project menggunakan tag article dengan class="project-card", yang dimana elemen atau tag article menandai satu project sebagai konten mandiri. Di dalamnya, class project-card dipakai oleh CSS untuk tampilan card


CSS

Pada about.html, konten profil berada di dalam article class="about-page", CSS untuk bagian ini mengatur susunan foto dan teks, bukan isi profilnya.

- .about-page menggunakan CSS Grid dengan dua kolom: kolom foto dan kolom teks. gap memberi jarak di antara keduanya, sedangkan align-items: center menyelaraskan isi kolom secara vertikal
- .about-page grid-column: 1 / -1 membuat judul membentang pada kedua kolom serta menggunakan h1 agar tulisannya membesar.
- .about-photo membuat foto memenuhi lebar kolom dengan batas tinggi maksimum. Border, radius, dan bayangan membingkai foto, object-fit: cover menjaga area foto tetap terisi tanpa mengubah rasio gambar.
- Pada media query layar dengan lebar maksimum 700px, .about-page berubah menjadi satu kolom. Judul kembali ke satu kolom, dan lebar foto dibatasi agar nyaman dilihat pada layar kecil.

CSS untuk project menggunakan class yang berbeda dari CSS About, karena susunan dan tujuan kedua bagian juga berbeda. About menampilkan satu profil, sedangkan halaman Project menampilkan beberapa project dalam bentuk kumpulan card.

- .projects-page memberi ruang di atas dan bawah seluruh bagian halaman project (hanya ada padding).
- .project-list menggunakan CSS Grid dengan dua kolom dan jarak antar-card.
- .project-card mengatur tampilan setiap elemen article sebagai card, dengan menggunakan Flexbox dengan arah kolom, border, border radius, shadow, dan overflow: hidden agar isi tidak keluar dari batas card.
- .project-card img menargetkan gambar yang menjadi anak langsung card. Lebar gambar memenuhi card, tingginya dibuat 13rem, dan object-fit: cover untuk menjaga area gambar tetap penuh tanpa mengubah rasio aslinya.

Jika .about-page hanya berisi 1 layout profil yang berbenduk grid 2 kolom yaitu foto di satu kolom dan teks di kolom lainnya maka .project-list adalah grid untuk banyak item setiap .project-card merupakan card mandiri walau sama sama menggunakan tag artikel didalam nya, meskipun bisa saja menggunakan div langsung sebagai wadah tetapi tag artikel ini lebih deskriptif sehingga dapat menjelaskan ke browser bahwa card nya berisi suatu informasi
