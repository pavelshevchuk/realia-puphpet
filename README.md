# Realia PuPHPet

HOW TO INSTALL
=====================
Up and Run Vagrant
```bash
$ git clone https://github.com/pavelshevchuk/realia-puphpet.git
$ cd realia-puphpet
$ vagrant up
```

Connect to vagrant using ssh
```bash
$ vagrant ssh
```

Download Drupal 8 Core (currently supported version is *8.0.0-beta12*)
```bash
$ cd /var/www
$ drush dl drupal-8.0.0-beta12 --drupal-project-rename="realia" -y
```

Download Realia Drupal installation profile
```bash
$ cd /var/www/realia
$ git clone https://github.com/pavelshevchuk/realia-drupal-profile.git /var/www/realia/profiles/realia
```

Install Drupal core with Realia profile
```bash
$ drush si realia --db-url=mysql://admin:admin@localhost/realia --account-pass=admin -y
```
