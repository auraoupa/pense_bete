# Penses Bete

## Les commandes utiles

### Sur occigen :
* état de la consommation en heure pour le groupe et par utilisateurs : https://reser.cines.fr/user/login

### Faire des transferts avec tunnel :

* tunnel vers occigen via meolkerg : ssh -f -N -L 8383:occigen.cines.fr:22 albert6a@meolkerg.hmg.inpg.fr -CX (cf script ~/bin/occid)

* scp via tunnel : scp -P 8383 CDFTOOLS-master.zip albert6a@localhost:~/.

* rsync via tunnel : rsync -e 'ssh -p 8383' -arv albert6a@localhost:/store/albert6a/NATL60/NATL60-CJM165-S/AURELIEN/gridU_20130${m}.tar .

### Trucs bash

* rajouter un 0 devant $m 

      mm=$(printf "%02d" $m)
    
* lister et ranger par ordre croissant de taille de dossiers    

      du -sh | sort -n -r
      
* avoir des infos sur les commandes en cours

      ps -rf | grep rsync
      
* chercher un fichier dans un répertoire

      find . -name "*truc*"

### Trucs netcdf :

* pour transformer un fichier netcdf4 en pas netcdf4 : nccopy -k '64-bit offset' NATL12ext_bathymetry.nc NATL12ext_bathymetry_nonetcdf4.nc


### Trucs Gimp

* rendre une image transparente :
  * clic droit -> calques -> ajouter canal alpha
  * (selectionner zone) clic droit -> édition -> effacer
  * edition -> fondu effacer ... (réglage % transparence)
  
### Trucs open-office

#### Presentation

* mettre une image en fond de slide :
  * format -> remplissage -> bitmaps -> import
  * format -> page -> arrière-plan -> bitmap

### Trucs conda

 * proxy_servers https: https://www-cache.ujf-grenoble.fr:3128 dans ~/.condarc

 * myenv environment : in ~/anaconda2/conda-env
    * conda list --explicit > spec-file.txt
    * conda create --name myenv --file spec-file.txt
    
 * pandoc environment :
    * conda create --name pandoc-env python=3.5
    * source activate pandoc-env
    * append PATH : /home/albert/anaconda2/lib/ where ligmp.so.3 is
 
### Trucs vi

 *  error `E576: viminfo: Missing '>' in line: [file names]` ->  in `~/.viminfo` delete everything in the section labeled `# History of marks within files (newest to oldest):`.
