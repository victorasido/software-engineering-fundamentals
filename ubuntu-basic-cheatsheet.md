# 🐧 Ubuntu Basic Command Cheat Sheet

## 📁 1. Navigasi Folder (Filesystem)

``` bash
ls
ls -l
ls -a
cd folder/
cd ..
cd ~
pwd
```

## 📦 2. File & Folder Management

``` bash
mkdir nama_folder
mkdir -p a/b/c

touch file.txt

cp file.txt backup.txt
cp -r folder/ backup/

mv file.txt /path/
mv lama.txt baru.txt

rm file.txt
rm -r folder/
rm -rf folder/
```

## 🔐 3. Permission & Ownership

``` bash
chmod 755 file
chmod +x script.sh

chown user:group file
sudo chown -R user:user folder/
```

## 🧾 4. Lihat Isi File

``` bash
cat file.txt
tac file.txt
nl file.txt
less file.txt
head -n 20 file.txt
tail -f logfile.log
```

## 🧩 5. Process Management

``` bash
ps aux
top
htop

kill 1234
kill -9 1234

pkill nama_process
```

## 🔧 6. Service Management (systemctl)

``` bash
sudo systemctl start nama_service
sudo systemctl stop nama_service
sudo systemctl restart nama_service
sudo systemctl status nama_service

sudo systemctl enable nama_service
sudo systemctl disable nama_service
```

## 🌐 7. Network Commands

``` bash
ip a
ifconfig
ping google.com
curl http://localhost:3000
wget https://file.com

netstat -tulnp
ss -tulnp
```

## 📦 8. APT Package Manager

``` bash
sudo apt update
sudo apt upgrade
sudo apt install <package>
sudo apt remove <package>
sudo apt purge <package>
sudo apt autoremove
```

## 🐳 9. Docker Basic

``` bash
docker ps
docker ps -a
docker images

docker pull nginx

docker run -p 8080:80 nginx

docker stop <id>
docker rm <id>
docker rmi <image_id>

docker logs -f <id>
```

## 🗃️ 10. Git

``` bash
git status
git add .
git commit -m "msg"
git push
git pull

git checkout -b feature/branch
git checkout main
```

## 🔍 11. Search

``` bash
grep -R "kata" .
grep -n "keyword" file.txt

find . -name "*.log"
```

## 📦 12. Tar & Zip

``` bash
tar -cvf file.tar folder/
tar -xvf file.tar

zip -r file.zip folder/
unzip file.zip
```

## 📝 13. System Info

``` bash
uname -a
df -h
du -sh *
free -h
whoami
```
