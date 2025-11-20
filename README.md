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
