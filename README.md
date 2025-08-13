# LAB-8-TROUBLE-SHOOTING
13 agustus 2025
# TROUBLESHOOTING LOGGING DI MIKROTIK [BASIC CONFIGURATION] 

**Siswa mampu melakukan troubleshooting pada mikrotik :**    
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
 Router corrupt dan tidak bisa booting. memungkinkan salah satu Penyebabnya yaitu, Komponen seperti chip switch, RAM, 
atau board rusak karena overheat, petir, korsleting, dll.  
**Solusi**: 
      - Bongkar casing (jika memungkinkan dan aman) lalu periksa PCB, chip, kapasitor bengkak, bekas terbakar, atau jalur putus,   
      setelah itu verifikasi suplai daya dapat mengembalikan fungsi normal perangkat.
         
# F. Mikrotik selalu restart
Salah satu Penyebabnya mungkin Firmware rusak (corrupted).  
Solusi: Flash ulang firmware via netinstall  

                langkah-langkahnya:  
                    1. Unduh Netinstall dan file firmware sesuai tipe perangkat dari situs resmi Mikrotik.  
                    2. Buka Control Panel → Network & Sharing Center → Change Adapter Settings.  
                    3. Pilih adapter ethernet → Properties → IPv4.  
                    4. Atur IP manual:  
                        IP: 192.168.100.2 
                        Subnet: otomatis (255.255.255.0).  
                    5. Klik kanan netinstall.exe → Run as Administrator.  
                    6. Atur Net Booting ke 192.168.1.1.  
                    7. Hubungkan kabel LAN dari port ethernet Mikrotik ke laptop.  
                    8. Tekan dan tahan tombol reset di Mikrotik.  
                    9. Sambil menahan tombol reset, colokkan kabel power.  
                    10. Tunggu sampai perangkat terdeteksi di Netinstall.  
                    11. Pilih perangkat di Netinstall.  
                    12. Klik Browse → pilih file firmware (.npk) yang sudah diunduh.  
                    13. Klik Install dan tunggu proses selesai.   
                    14. Cabut kabel, hubungkan kembali Mikrotik ke laptop/Winbox. 
                    15. Pastikan sudah terdeteksi dan tidak restart berulang.    
                    16. Lakukan konfigurasi ulang sesuai kebutuhan.    

# kesimpulan
cara menyelesaikan troubleshoot mungkin berbeda-beda sesui dengan jenis masalahnya ada software dan hardware,     
yang pasti sebelum melakukan connecting, alangkah baiknya untuk melakukan pengecekan terhadap alat-alat terlebih dahulu.     
# Sumber
DK SRY - Youtube: https://youtu.be/XKTOdTjqzOs?si=qgZgb_gYCMMtbyO9  
ARRIE CELLULAR - Youtube: https://www.youtube.com/watch?v=bDO-ZBAeV9c  
ahnaf-p - Github: https://github.com/ahnaf-p/LAB-8-Troubleshooting.git  
