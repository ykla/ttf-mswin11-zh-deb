# Windows 11 中文字体包：适用于 Debian/Ubuntu

MS Windows 11 Fonts for Debian/Ubuntu

## 版本

Windows 11 24H2 zh-cn

## 安装教程

```
$ sudo apt install git
$ git clone https://github.com/ykla/ttf-mswin11-zh-deb
$ cd ttf-mswin11-zh-deb
$ sudo dpkg -i ttf-ms-win11-*.deb
```

## 制作方法

```sh
$ mkdir -p extract/DEBIAN
$ mkdir build
$ dpkg -X package.deb extract/ # 将主要资源解压到 extract/
$ dpkg -e package.deb extract/DEBIAN # 然后对 extract/ 和 extract/DEBIAN 进行修改
$ dpkg-deb -Zgzip -b extract/ build/package.deb # 压缩回 deb，主要不要用 zstd
```
