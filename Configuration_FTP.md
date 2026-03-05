# Documentation sur la configuration de serveur FTP

## Introduction
Le FTP (File Transfer Protocol) est un protocole standard pour le transfert de fichiers entre un client et un serveur sur un réseau. Cette documentation couvre la configuration, l'installation, la sécurité et les meilleures pratiques pour un serveur FTP.

## Configuration du serveur FTP
1. **Choisir un logiciel de serveur FTP**: Il existe plusieurs options de logiciels de serveur FTP, tels que vsftpd, ProFTPD et FileZilla Server. Sélectionnez celui qui convient à vos besoins.

2. **Installation**: 
   - Sur Ubuntu, vous pouvez installer vsftpd avec la commande suivante :  
     ```bash  
     sudo apt-get install vsftpd  
     ```  
   - Sur CentOS, utilisez :  
     ```bash  
     sudo yum install vsftpd  
     ```  

3. **Configuration du fichier vsftpd.conf**: Ce fichier contient les paramètres de configuration du serveur FTP. Les éléments clés à configurer incluent :  
   - `listen=YES`: Permet au serveur de fonctionner en mode standalone.  
   - `anonymous_enable=NO`: Désactive l'accès anonyme.  
   - `local_enable=YES`: Permet aux utilisateurs locaux de se connecter.  
   - `write_enable=YES`: Permet les opérations d'écriture.  

## Sécurité
1. **Utiliser FTPS**: Pour sécuriser le transfert de fichiers, activez FTPS pour chiffrer les données échangées entre le client et le serveur.

2. **Configurer un pare-feu**: Assurez-vous que le pare-feu autorise les connexions sur le port FTP (21) et, si vous utilisez FTPS, les ports supplémentaires pour le mode passif.

3. **Gestion des utilisateurs**: Créez des utilisateurs avec des mots de passe forts et limitez les permissions d'accès aux répertoires nécessaires uniquement.

## Meilleures Pratiques
1. **Mises à jour régulières**: Maintenez le logiciel de votre serveur FTP à jour pour bénéficier des dernières fonctionnalités et correctifs de sécurité.

2. **Surveillance des journaux**: Vérifiez régulièrement les journaux d'accès pour détecter toute activité suspecte ou non autorisée.

3. **Sauvegardes fréquentes**: Assurez-vous d'effectuer régulièrement des sauvegardes des données pour éviter toute perte de données en cas de défaillance du serveur.

## Conclusion
La configuration d'un serveur FTP nécessite une attention particulière à la fois sur la configuration technique et sur la sécurité. En suivant les meilleures pratiques, vous pouvez assurer une transmission de fichiers sécurisée et efficace.