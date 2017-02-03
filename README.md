# Pense Bete

## Les commandes utiles

### Sur occigen :
* état de la consommation en heure pour le groupe et par utilisateurs : https://reser.cines.fr/user/login

### Faire des transferts avec tunnel :

* tunnel vers occigen via meolkerg : ssh -f -N -L 8383:occigen.cines.fr:22 albert6a@meolkerg.hmg.inpg.fr -CX (cf script ~/bin/occid)

* scp via tunnel : scp -P 8383 CDFTOOLS-master.zip albert6a@localhost:~/.

* rsync via tunnel : rsync -e 'ssh -p 8383' -arv albert6a@localhost:/store/albert6a/NATL60/NATL60-CJM165-S/AURELIEN/gridU_20130${m}.tar .
