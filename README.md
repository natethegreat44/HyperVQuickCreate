# Additional Hyper-V QuickCreate options.

This code is NOT endorsed nor supported by Microsoft or Canonical. I think it's safe and use it on my own systems. However, your mileage may vary and should only USE THIS CODE AT YOUR OWN RISK (and make sure you have a good backup!).

PRs and feedback are welcomed.

# Current Images

Currently, this adds options for:
- Ubuntu 24.04 LTS
- Ubuntu 24.10 (not recommended - remarkably out of date)
- Ubuntu 26.04 LTS

# Getting started

The most important step here is to install the `GalleryLocations.reg` file from this repository. This will create or overwrite the `GalleryLocations` registry value stored at `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Virtualization`. Because it's a multi-string value, the data is encoded and hard to read. The values being installed are:

```
https://go.microsoft.com/fwlink/?linkid=851584
https://raw.githubusercontent.com/natethegreat44/HyperVQuickCreate/refs/heads/main/UbuntuGalleryHyperV.json
```

The first one is the default used by Hyper-V QuickCreate and the second one contains the new Ubuntu options that are housed in this repo. You can use a local file path here, too, such as `C:\Users\me\MyCustomGallery.json`.

If you make changes to the JSON file, you'll also need to update your registry value to point to it.

# Creating a new VM

After the registry entry is created, you simply need to open up Hyper-V QuickCreate and choose the VM you want. For the Ubuntu VMs, the setup will create a new VM with all the display goodness you'd expect.

# References and Troubleshooting

https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/user-guide/custom-gallery
