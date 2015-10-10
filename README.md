rpm-python27
============

An RPM spec file build and alt-install Python 2.7 on RHEL.

To Build:

`sudo yum -y install rpmdevtools && rpmdev-setuptree`

`sudo yum -y install tk-devel tcl-devel expat-devel db4-devel gdbm-devel sqlite-devel bzip2-devel openssl-devel ncurses-devel readline-devel`

`wget https://raw.github.com/nmilford/rpm-python27/master/python27.spec -O ~/rpmbuild/SPECS/python27.spec`

`wget https://www.python.org/ftp/python/2.7.10/Python-2.7.10.tgz -O ~/rpmbuild/SOURCES/Python-2.7.10.tar.bz2`

`QA_RPATHS=$[ 0x0001|0x0010 ] rpmbuild -bb ~/rpmbuild/SPECS/python27.spec`
