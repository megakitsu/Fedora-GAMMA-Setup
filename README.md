# ☢️ My Fedora Linux Stalker G.A.M.M.A. Installation and Setup Guide

<p align="center">
  <img src="gamma_logo.png" alt="Stalker GAMMA Logo" width="400"/>
</p>

**Quick Disclaimer:**
- This is not meant to be an educational guide of any sorts, this is simply the steps I use to get Stalker GAMMA up and running on a Fedora Linux installation.
- I use GNOME, this *should* work on KDE.
- Although this was written with Fedora in mind, it may work with other distributions as I'm using the Flatpak version of Bottles.

---

## Install Bottles

Enter into a terminal:

```
flatpak install flathub com.usebottles.bottles
sudo flatpak override com.usebottles.bottles --filesystem=host
```

## Install gamma-launcher

Here we are creating a directory where you will install GAMMA and gamma-launcher, Enter into terminal:

```
mkdir -p ~/Games/Stalker
cd ~/Games/Stalker
sudo dnf install libunrar
git clone https://github.com/Mord3rca/gamma-launcher
python3 -m venv env
source env/bin/activate
pip install --upgrade pip
cd gamma-launcher/
pip install .
gamma-launcher --version
```

## Install Stalker GAMMA

Here we are doing a full installation of Stalker GAMMA using gamma-launcher, Enter into terminal:

```
cd ~/Games/Stalker
gamma-launcher full-install --anomaly ./AnomalyGAMMA --gamma ./GAMMA --cache-directory ./cache
```

## Bottles Settings

Create a new 'bottle' 
