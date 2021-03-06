<p align="center">
<a href="https://packagist.org/packages/znframework/shared-extension" rel="nofollow">
	<img src="https://img.shields.io/packagist/dt/znframework/shared-extension?style=flat-square" style="max-width:100%;"></a>
<a href="//packagist.org/packages/znframework/shared-extension" rel="nofollow">
	<img src="https://img.shields.io/github/v/release/znframework/shared-extension?style=flat-square&color=00BFFF" style="max-width:100%;"></a>
<a href="//packagist.org/packages/znframework/shared-extension" rel="nofollow">
	<img src="https://img.shields.io/github/release-date/znframework/shared-extension?style=flat-square" style="max-width:100%;"></a>
<a href="//packagist.org/packages/znframework/shared-extension" rel="nofollow">
	<img src="https://img.shields.io/github/license/znframework/shared-extension?style=flat-square" style="max-width:100%;"></a>
</p>

<h2>ZN Framework Shared Extension</h2>
<p>
Allows you to create a shared working directory. For this use, this directory must be shown in DocumentRoot as the working directory.
</p>

<h3>Installation</h3>
<p>
You only need to run the following code for the installation.
</p>

```
composer create-project znframework/shared-extension public
```

<h3>Configuration</h3>
<p>
For configuration, edit the .conf file as follows.
</p>

```
<VirtualHost *:80>

    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/html/public

    <Directory /var/www/html/public>
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
    
</VirtualHost>
```