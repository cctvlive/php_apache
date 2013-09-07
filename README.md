php_apache
==========

#在 Windows 下配置 Apache 的方法:

找到 PHP 安装目录下的 libeay32.dll 和 ssleay32.dll，

把它们拷贝到 Apache 安装目录下的 bin 目录里。
和c/windows/ 安装目录下的 libeay32.dll 和 ssleay32.dll，

编辑 PHP 配置文件 php.ini，和c/windows/ php.ini 找到 “;extension=php_openssl.dll” 这行，

把前面的分号去掉；如果没有这行，就添加一行 “extension=php_openssl.dll”。
