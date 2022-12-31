# XeroLinux "G" Dev ISO Repo

Repo for the **Xero-G** Dev Project. Feel free to go through files and learn how it's all done. To build ISO need to use **ABS** Script via guide below.

### Note
> This is the Dev version of XeroG. It's intended for the XeroLinux Team
> For testing new features and fixes only !
-----------------------------------------------------------------

![XeroLinux-Calamares](https://i.imgur.com/tJ64aOY.png)

### Step 1 - Get Repo in to build :

Before we get started we will need to get the **ABS** repo in, that's where the new build tool is located. To do so need to edit the "pacman.conf" :

```
sudo nano /etc/pacman.conf
```

Now we need to add the repo at the end of the file, so add this,
```
# Valen Repository
[valen_repo]
SigLevel = Never
Server = https://keyaedisa.github.io/$repo/$arch
```
Now install the tool via,
```
sudo pacman -S abs
```
### Step 2 - Clone Build Repo :

Once you got Repos in, time to grab the build environment that you will be building from. Just note that you will need Git installed in order to do that.

**Install Git with :**
```
sudo pacman -S git
```
**Grab Build Env.**
```
cd ~ && git clone https://github.com/xerolinux/xero_g_dev_iso.git
```

### Step 3 - Building the Xero ISO :

Now that we have build environment on our system, it's time to build it.

**Build ISO :**
```
cd ~/xero_iso/ && abs XeroG
```

I hope this helps.. In case of other issues kindly find me on [**Discord**](https://discord.gg/Xg6T78ahtK)

Happy building
