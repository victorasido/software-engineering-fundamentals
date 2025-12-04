# 🐧 Ubuntu Basic Command Cheat Sheet (With Inline Comments)

## 📁 1. Navigasi Folder (Filesystem)

``` bash
ls              # menampilkan daftar file & folder
ls -l           # list dengan detail (permission, size, owner)
ls -a           # tampilkan file hidden (.env, .git, dsb)
cd folder/      # masuk ke folder
cd ..           # naik 1 level folder
cd ~            # ke home directory
pwd             # menampilkan path saat ini
```

## 📦 2. File & Folder Management

``` bash
mkdir nama_folder          # membuat folder baru
mkdir -p a/b/c             # membuat nested folder sekaligus

touch file.txt             # membuat file kosong

cp file.txt backup.txt     # menyalin file
cp -r folder/ backup/      # menyalin folder

mv file.txt /path/         # memindahkan file
mv lama.txt baru.txt       # rename file

rm file.txt                # menghapus file
rm -r folder/              # menghapus folder (recursive)
rm -rf folder/             # force delete tanpa konfirmasi
```

## 🔐 3. Permission & Ownership

``` bash
chmod 755 file             # mengubah permission (rwxr-xr-x)
chmod +x script.sh         # membuat file menjadi executable

chown user:group file      # mengubah owner & group file
sudo chown -R user:user folder/   # ubah owner folder beserta isinya
```

## 🧾 4. Lihat Isi File

``` bash
cat file.txt               # menampilkan isi file
tac file.txt               # menampilkan isi file terbalik
nl file.txt                # menampilkan isi dengan nomor baris
less file.txt              # membuka file mode view (scroll)
head -n 20 file.txt        # melihat 20 baris pertama
tail -f logfile.log        # live tail log realtime
```

## 🧩 5. Process Management

``` bash
ps aux                     # menampilkan semua proses berjalan
top                        # real-time monitoring proses
htop                       # versi top yang lebih bagus (harus install)

kill 1234                  # menghentikan proses berdasarkan PID
kill -9 1234               # force kill jika tidak bisa dimatikan normal

pkill nama_process         # kill berdasarkan nama proses
```

## 🔧 6. Service Management (systemctl)

``` bash
sudo systemctl start service     # menjalankan service
sudo systemctl stop service      # menghentikan service
sudo systemctl restart service   # restart service
sudo systemctl status service    # cek status service

sudo systemctl enable service    # otomatis jalan saat boot
sudo systemctl disable service   # nonaktifkan auto-start
```

## 🌐 7. Network Commands

``` bash
ip a                      # melihat daftar interface & IP
ifconfig                  # (jika net-tools terinstall)
ping google.com           # test koneksi internet
curl http://localhost:3000   # request HTTP ke endpoint lokal
wget https://file.com     # download file dari internet

netstat -tulnp            # cek port yang sedang listening
ss -tulnp                 # versi modern netstat
```

## 📦 8. APT Package Manager

``` bash
sudo apt update           # update daftar package
sudo apt upgrade          # upgrade seluruh package
sudo apt install pkg      # install package
sudo apt remove pkg       # uninstall package
sudo apt purge pkg        # uninstall + hapus config
sudo apt autoremove       # hapus package tidak terpakai
```

## 🐳 9. Docker Basic

``` bash
docker ps                 # lihat container aktif
docker ps -a              # lihat semua container
docker images             # lihat list image

docker pull nginx         # download image

docker run -p 8080:80 nginx   # menjalankan container map port

docker stop id            # stop container
docker rm id              # hapus container
docker rmi image_id       # hapus image

docker logs -f id         # melihat log container realtime
```

## 🗃️ 10. Git

``` bash
git status                # cek status repo
git add .                 # add semua file
git commit -m "msg"       # commit perubahan
git push                  # kirim ke remote
git pull                  # ambil perubahan dari remote

git checkout -b feature/branch   # membuat branch baru
git checkout main                # pindah ke branch main
```

## 🔍 11. Search

``` bash
grep -R "kata" .          # cari teks dalam folder
grep -n "keyword" file.txt # cari teks dengan nomor baris

find . -name "*.log"      # mencari file berdasarkan nama
```

## 📦 12. Tar & Zip

``` bash
tar -cvf file.tar folder/     # membuat file .tar
tar -xvf file.tar             # extract file .tar

zip -r file.zip folder/       # membuat zip
unzip file.zip                # extract zip
```

## 📝 13. System Info

``` bash
uname -a                # info kernel & OS lengkap
df -h                   # melihat disk usage
du -sh *                # ukuran semua file/folder
free -h                 # melihat RAM
whoami                  # user saat ini
```
