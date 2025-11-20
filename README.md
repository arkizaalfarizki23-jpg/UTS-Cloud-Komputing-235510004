1.Jelaskan keterkaitan antara SaaS, PaaS, dan IaaS dalam _cloud computing_
:
Keterkaitan SaaS, PaaS, dan IaaS dalam Cloud Computing
SaaS (Software as a Service), PaaS (Platform as a Service), dan IaaS (Infrastructure as a Service) adalah tiga model layanan utama di cloud computing yang saling berhubungan dalam satu ekosistem layanan TI berbasis cloud.​
1.IaaS menyediakan infrastruktur komputasi inti seperti server, storage, dan jaringan secara virtual. Pengguna bisa mengelola dan mengatur sendiri kebutuhan infrastruktur tanpa membeli perangkat fisik.​
2.PaaS membangun lapisan di atas IaaS, menawarkan platform pengembangan aplikasi (runtime, basis data, middleware, SDK), sehingga pengembang cukup fokus pada logika aplikasi tanpa perlu mengurus aspek infrastruktur atau sistem operasi yang mendasari.​
3.SaaS adalah aplikasi siap pakai yang berjalan di atas infrastruktur dan platform yang sudah dikelola sepenuhnya oleh penyedia layanan cloud. Pengguna tinggal menggunakan aplikasi tanpa memikirkan deployment, patching ataupun maintenancenya.​
Ketiganya membentuk piramida layanan: IaaS di bagian terbawah sebagai fondasi, PaaS sebagai lapisan pengembangan, dan SaaS sebagai aplikasi siap-pakai di puncak piramida

2.
          +------------------------+
           |        SaaS            |
           |  (Aplikasi untuk user) |
           +-----------▲------------+
                       |
                       |
          +------------+------------+
          |           PaaS         |
          | (Platform menjalankan  |
          |  container & services) |
          +------------▲------------+
                       |
                       |
          +------------+------------+
          |      Container          |
          |   (Runtime untuk app)   |
          +------------▲------------+
                       |
                       |
          +------------+------------+
          |   Cloud-Native App      |
          | (Microservices, CI/CD)  |
          +--------------------------+

3.


| Program           | Waktu (detik) |
|-------------------|--------------|
| Asyncio           | 0.21         |
| Multiprocessing   | 2.46         |


Pada Python 3.14 free-threaded, kedua metode (asyncio dan multiprocessing) cukup efisien untuk pengambilan data paralel dari endpoint JSON. Multiprocessing memberikan performa optimal jika jumlah core banyak dan task I/O tinggi, sedangkan asyncio unggul untuk banyak permintaan network yang bersifat non-blocking.


# Workspace GIL-enabled

## Hasil Uji Pengambilan Data JSON

| Program           | Waktu (detik) |
|-------------------|--------------|
| Asyncio           | 0.50         |
| Multiprocessing   | 2.79         |

Pada Python 3.14 dengan GIL, multiprocessing mengalami bottleneck pada I/O dan pembuatan proses baru, sehingga waktu bisa lebih lama dibandingkan asyncio. Asyncio cocok untuk komunikasi HTTP paralel dalam satu proses tanpa overhead proses baru.

