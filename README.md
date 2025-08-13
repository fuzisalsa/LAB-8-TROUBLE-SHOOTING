# LAB-8-TROUBLE-SHOOTING
13 agustus 2025
# Troubleshooting logging di mikrotik [basic configuration]  

Siswa mampu melakukan troubleshooting pada mikrotik :    
# A. Tidak bisa login ke mikrotik    
    1. periksa perkabelan, pastikan tida ada kabel yang terputus atau longgar.  
    2. periksa router board pastikan dalam kondisi baik dan tidak cacat.   
    3. atau dengan cara reset router board 
      - hard reset 
        Lepas power adaptor.  
        Tekan tombol reset yang biasanya terletak di dekat power jack dengan keterangan "RES".     
        Ada juga yang terletak dibalakang board seperti RB2011series.   
        
        Sambil tetap ditahan tombol resetnya, tancapkan power adaptornya.    
        Tunggu kurang lebih 5 detik, atau indikator LED ACT blink sekali, dan lepaskan tombol resetnya.    
        Biarkan router melanjutkan proses booting, dan router anda sudah kembali ke default konfigurasi.    
# B. Tidak bisa akses menggunakan winbox 
    -  disebled jaringan yang mengganggu seperti, interface virtualbox.
    -  Coba ganti kabel ethernet dan coba port lain
# C. Tidak bisa akses melalui telnet
    - pastikan memiliki ip default mikrotik 192.168.88.1/24, jika belum, bisa buat ip static via winbox.  
    - pastikan port yang di masukan benar yaitu port 23.
# D. Tidak bisa akses melalui ssh
     - pastikan memiliki ip default mikrotik 192.168.88.1/24. jika belum, bisa buat ip static via winbox.  
     - pastikan port yang di masukan benar yaitu port 22.
# E. Perangkat mikrotik/RB error [indikator lampu port ethernet menyala semuanya]
    
# F. Mikrotik selalu restart
