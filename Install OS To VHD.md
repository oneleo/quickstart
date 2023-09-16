# Windows

- Download [Windows 10](https://www.microsoft.com/zh-tw/software-download/windows10ISO) or [Windows 11](https://www.microsoft.com/zh-tw/software-download/windows11) ISO

- Mount ISO (Assume Disk S:)

- Create new VHDX via Logical Disk Manager (Assume Disk X: at C:\vhd\MyVhd.vhdx)

- Install Windows to VHDX

```shell
> cmd
> Dism /Apply-Image /ImageFile:"S:\sources\install.esd" /index:1 /ApplyDir:X:\
```

- Change Windows version

```shell
### List
> Dism /Image:X: /Get-CurrentEdition
> Dism /Image:X: /Get-TargetEditions

### Change
> Dism /Image:X: /Set-Edition:Professional
```

- Add to boot menu

```shell
### Add
> bcdedit /copy {current} /d "Windows VHD"

### Boot from VHDX
> bcdedit /set <YOUR BCD ID> device "vhd=[C:]\vhd\MyVhd.vhdx"
> bcdedit /set {f5271ab7-94c1-11ea-9a2a-d37dc47c9f8e} osdevice "vhd=[C:]\vhd\MyVhd.vhdx"

### Set default
> bcdedit /default <YOUR BCD ID>

### Set timeout
> bcdedit /timeout 3
```

- Cancel need network when install Windows

```shell
### Press Shift + F10
> oobe\bypassnro
```

- Obtain [Windows KMS](https://learn.microsoft.com/zh-tw/windows-server/get-started/kms-client-activation-keys) authorization

```shell
> cmd
> %SYSTEMROOT%\system32\slmgr.vbs /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX
> %SYSTEMROOT%\system32\slmgr.vbs /skms <YOUR KMS SERVER URL>
> %SYSTEMROOT%\system32\slmgr.vbs /ato
> %SYSTEMROOT%\system32\slmgr.vbs /dlv
```
