pkgname=PID37
pkgver=r8.601f58b
pkgrel=1
pkgdesc="Walmart Kivy MD Interface for PRD4"
arch=('any')
url="https://github.com/DamianoGlobal/DGnet_Program_ID37"
license=('')

source=("$pkgname::git+ssh://git@github.com:DamianoGlobal/DGnet_Dist_PID4.git")

md5sums=('SKIP')

prepare() {
  cd $pkgname
  #git clone https://github.com/DamianoGlobal/DGnet_Dist_PID4
}


pkgver() {
        cd "$srcdir/${pkgname}"
        printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}


package() {
  mkdir -p $pkgdir/home/dgnet/dgnet_programs/PID37
  mkdir -p $pkgdir/home/dgnet/dgnet_settings/PID37
  cd $pkgdir/home/dgnet/dgnet_programs/PID37
  python3 -m venv ./venv
  source ./venv/bin/activate
  pip install --upgrade pip
  pip install wheel
  cd "$srcdir/$pkgname"
  #pip wheel . -w wheels -r requirements.txt
  #python -m pip install --force-reinstall ./wheels/*.whl
}



