Descrizione Role
=========
* Installa un cron che giro ogni mattino alle 6.00 e cancella i file /home/reicom/core. * più vecchi di 3 giorni (se il playbook è stato lanciato senza parametri

* Installa un cron che giro ogni mattino alle 6.00 e cancella i file /home/reicom/stacktrace * più vecchi di 3 giorni (se il playbook è stato lanciato senza parametri

* il log di questa operazione sarà /var/log/ct6/delete_cron_stactrace.log

* Viene posizionato il file di logrotate che ruota il file (3 file da 2 MB)

Requisiti
------------
Nessuno in particolare.
Il Playbook agisce solo se sul server esiste la cartella /home/reicom (altrimenti non ci potranno mai essere file di core di nessun tipo)

Variabili
--------------
storicocore=<n>
storicostacktrace=<n>

Se si vuole personalizzare il default (3) dei giorni di storico dei core da tenere

Dipendenze
------------
Nessuna

Esempio di chiamata
----------------

ansible-playbook /home/playbook/bugs/6596/main.yml -l <elenco hosts/gruppo> -C (dry run)
ansible-playbook /home/playbook/bugs/6596/main.yml -l <elenco hosts/gruppo>

Informazioni Autore
------------------

Martino.Viganò
Martino.Vigano@enghouse.com

![alt text](http://www.accademianuovaitalia.it/images/gif/stati-persone/merkel/MERKEL-NETANIAU.gif)
