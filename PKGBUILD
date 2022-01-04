pkgname=PID37
pkgver=1
pkgrel=1
pkgdesc="Walmart Kivy MD Interface for PRD4"
arch=('any')
url="https://github.com/DamianoGlobal/DGnet_Program_ID37"
license=('')

source=($pkgname::git+ssh://git@github.com/DamianoGlobal/DGnet_Program_ID37.git)

md5sums=('SKIP')



package() {

  mkdir -p $pkgdir/home/dgnet/dgnet_programs/PID37
  mkdir -p $pkgdir/home/dgnet/dgnet_settings/PID37
  cd $pkgdir/home/dgnet/dgnet_programs/PID37
  python3 -m venv ./venv
  source ./venv/bin/activate
  pip install --upgrade pip
  pip install wheel

  cd "$srcdir/$pkgname"
  git clone git@github.com:DamianoGlobal/DGnet_Dist_PID4.git
  cd ./DGnet_Dist_PID4/B2.0.0.210727
  python -m pip install ./*.whl
  deactivate
  python -m pip install ./*.whl

  cd $pkgdir/home/dgnet/dgnet_programs/PID37
  source ./venv/bin/activate
  cd "$srcdir/$pkgname"

  git clone git@github.com:DamianoGlobal/KivyDG.git
  cd ./KivyDG/
  pip install .
  
  cd $pkgdir/home/dgnet/dgnet_programs/PID37
  pip install websocket

  git clone git@github.com:DamianoGlobal/DGnet_Program_ID37.git
  cd ./DGnet_Program_ID37
  pip install .

}



