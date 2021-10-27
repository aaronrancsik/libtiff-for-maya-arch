# libtiff for maya-arch 
## Install
### 1. Clone this source
#### Select a folder
`cd /tmp`
#### Choose one:
#### A. HTTPS 
`git clone https://github.com/aaronrancsik/libtiff-for-maya-arch.git`
#### B. SSH 
`git clone git@github.com:aaronrancsik/libtiff-for-maya-arch.git`
### 2. Download the official Arch PKGBUILD 
`cd /tmp/libtiff-for-maya-arch`

`curl -O https://raw.githubusercontent.com/archlinux/svntogit-packages/packages/libtiff/trunk/PKGBUILD`
### 3. Patch the PKGBUILD 

`cp PKGBUILD PKGBUILD.orig`

#### *Optionally take a look at the patch file.*

`vim pkg.patch`

#### Patch
*You may need to install the [patch](https://archlinux.org/packages/core/x86_64/patch/) package*

`patch PKGBUILD pkg.patch`

#### *Optionally take a look what changed in PKGBUILD.*

`vimdiff PKGBUILD PKGBUILD.orig`

### 4. Create & install the actual package.
`makepkg -s`

`sudo pacman -U libtiff-4.3.0-1-x86_64.pkg.tar.zst`

### 5. It's done.

