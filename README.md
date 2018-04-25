# CPanel-To-Google-Drive
Backup Cpanel to Google Drive


tenho ideia como funciona o github


Mas vamos lá.  Esse script é para fazer o backup cpmove em servidor com cpanel instalado
  Instalei o MUTT

E criei a rotina de backup como a seguir:
Não
#!/bin/sh
## /fazer backup site

/scripts/pkgacct meuteste
/scripts/pkgacct sf

# upload to google drive
gdrive upload cpmove-meuteste.tar.gz
gdrive upload cpmove-sf.tar.gz

# remove the original tar
rm -rf cpmove-meuteste.tar.gz
rm -rf cpmove-sf.tar.gz

# Nome do Remetente
set realname="Nome do administrador da conta no server"

# Email do Remetente
set from="meuemail@gmail.com;"

# Usuario da conta de email
set my_user=mgmail.com

# Senha da conta de email
set my_pass='your password'

# Autenticacao no servidor smtp de email, nesse caso do gmail.com
set smtp_url=smtps://$:$my_pass@smtp.gmail.com

# Camada de segurança, requerida pelo gmail.com
set ssl_force_tls = yes

exit 0

Salvei-o como bkp.sh


Depois executei ./bkp.sh
