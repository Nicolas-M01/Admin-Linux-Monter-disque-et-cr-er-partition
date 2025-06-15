# Admin-Linux-Monter-disque-et-creer-partition

![Capture d'écran 2025-06-15 155803](https://github.com/user-attachments/assets/f964b9c5-c8c0-4393-8e48-6884cdf53f9f)  

![Capture d'écran 2025-06-15 155817](https://github.com/user-attachments/assets/70643438-6ca5-4cef-ad41-51d364bd8b8e)  

![Capture d'écran 2025-06-15 160220](https://github.com/user-attachments/assets/6819e7ae-0667-42ca-a2a6-637820a40af7)  
![Capture d'écran 2025-06-15 160227](https://github.com/user-attachments/assets/a2977e27-2a57-4498-b6e2-d11451a6c40b)  
![Capture d'écran 2025-06-15 160242](https://github.com/user-attachments/assets/49aed69f-ca9e-4660-acae-efdd78f7020b)  
![Capture d'écran 2025-06-15 160401](https://github.com/user-attachments/assets/033f81e5-b9d1-4d73-bf47-59f682c91217)  
![Capture d'écran 2025-06-15 160459](https://github.com/user-attachments/assets/db577207-2fe2-4bf4-a64c-c0a3b83c979e)

Le disque est créé et "branché". On  peut démarrer la machine.  
Avec `lsblk` on voit qu'il est "physiquement existant"  

![Capture d'écran 2025-06-15 160703](https://github.com/user-attachments/assets/71ab4fc8-8a9e-4680-9b62-87e1e383dde9)  

Puis avec `cfdisk`, donc en mode "semi graphique" on va le partitionner :  
![Capture d'écran 2025-06-15 161024](https://github.com/user-attachments/assets/2bbd8ca3-a9ce-4aaa-b5ec-ae205604b80f)  

On choisit notre table de partition. Ici on prend "GPT", car c'est le nouveau standard, plus fiable, utilisé avec les systèmes modernes (Windows 10/11, Linux, macOS).
( => MBR (aussi appelé "DOS partition table") : ancien standard, limité à 4 partitions primaires et 2 To de disque.)  
![Capture d'écran 2025-06-15 161034](https://github.com/user-attachments/assets/472a23f4-cd65-4dcf-8457-f7c6262d3f91)  

On écrit sur toute la partition dans notre cas :  
![Capture d'écran 2025-06-15 161049](https://github.com/user-attachments/assets/db0266af-9fb6-48de-9793-b242ec28b850)  


![Capture d'écran 2025-06-15 161231](https://github.com/user-attachments/assets/8df43488-2751-4718-a096-1df0041edc78)  

Puis on enregistre  
![Capture d'écran 2025-06-15 161242](https://github.com/user-attachments/assets/ccc2303b-aa94-4977-839d-2bc729d68f1d)  

![Capture d'écran 2025-06-15 161257](https://github.com/user-attachments/assets/97aaf206-cf1d-424b-b4ff-46da80fae1ef)  


On verifie que notre disque est bien présent :  
![Capture d'écran 2025-06-15 161318](https://github.com/user-attachments/assets/683fab94-ccd3-4467-a193-67c952d1832c)  

On crée notre système de fichiers et on lui attribue une "étiquette". en `ext4`, qui est le dernier format de fichiers sur linux.  
![Capture d'écran 2025-06-15 162500](https://github.com/user-attachments/assets/82613663-aaf9-4243-aa2f-bccdefffc7fe)
