# linux-rootfs-amd64
debootstrap , linux , amd64 , docker , new os 

linux-rootfs https://www15.zippyshare.com/v/Qhyy36pv/file.html tutorial https://www.itworkroom.com/installing-a-rootfs-on-sd-card/ не забываем что если будет отказано в доступе использовать sudo или su , использовать можно и чуть разделенный диск то там уже будет sda / sda1 /sda2 /sda3 и так далее для разворачивания системы и последующей модификации и выпуска в продакшен естественно чем на большее развернуть тем будет лучше допустим гигабайт 20 и более если ещё и собираемся собирать на этой оси , а пока нету ядра бут пуст.

Пример как я распаковал себе переразмеченный раздел к тем что мало ещё понимает не рискуйте это для разработчиков!

sudo mkfs.ext2 /dev/sdb7 спросит если то жмем y думаю по логике прокатит и sudo mkfs.ext2 /dev/sdb7 -y команда

sudo mount /dev/sdb7 /mnt

sudo tar -xzvf linux-rootfs.tar.gz -C /mnt

sudo umount /dev/sdb7

Как то так как пример

https://www.youtube.com/watch?v=1bz4vSR-LXk


