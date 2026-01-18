# 修复版 AIC8800 Linux DKMS 驱动

个人自用。

修复了在 Slackware 15.0 和 Linux Kernel 6.12.47 的情况下，`rwnx_main.c` 无法通过编译的问题。

问题发生在 5631 行（原仓库的 5630 行），实际上原作者应该是没做完高版本 Kernel 的适配。

以下是原仓库的 README。

~~小小吐槽一句：这驱动写的好烂啊~~

---

## Dependencies 
 - dkms

## Installing
```shell
git clone https://github.com/fqrious/aic8800-dkms
cd aic8800-dkms
sudo cp -r src /usr/src/aic8800-1.0.5
sudo cp -r blobs/* /usr/lib/firmware/
dkms install aic8800/1.0.5
```
