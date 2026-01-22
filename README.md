# AD-Infrastructure: Active Directory Domain Controller Setup in Azure
This project walks through setting up a basic Active Directory environment in Microsoft Azure. It includes creating a Domain Controller using Windows Server 2022 and a Windows 11 client VM, placing both systems on the same virtual network, and configuring DNS to enable proper communication. The lab finishes by verifying connectivity and DNS resolution through ping tests and PowerShell commands.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1cdf7503-564d-410d-8b8e-5c5ad5576bef" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/a2a299ac-42a3-4538-8149-c89a989cd812" />

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/c5e176e6-c6ae-448c-8aaf-d0b8ab924312" />

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/ecf45b0b-3805-497a-8159-f8b95200ca1b" />

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/201f081f-dedb-4f4d-af42-8fcb92dc14ce" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/ea15f78a-81dd-4a95-b14b-140591b95bab" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/085f0eea-2732-4470-a3da-7198c2c07ab3" />

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/a8741a5a-8278-46dd-91ba-5adc72fa8796" />

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/939fb738-6d53-4427-a3fb-5bc3da53347b" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/ea968afe-403e-4b2e-87e0-f0a034e8a384" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6ce69be1-3c02-4c29-945b-2583e341764e" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e14f822e-04dc-495a-9751-b4e04c92df5c" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/16c2d24b-ef7f-4602-8443-8375bd859aca" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/616a1575-5552-482e-9315-974e5226f98c" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2f988b90-fb19-4aea-80e4-231e06d64563" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/805ce7a8-1d6d-4661-ba55-2dfbc2a89cc4" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b73de035-cf43-4a2e-ab72-5c34eba28253" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/406c2bd7-e2e4-424e-9939-21007e9ec611" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/246eb014-c380-4fd6-8974-51b559b78ef0" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/894b7e4b-6673-4829-8aad-02115c64af2b" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dec9c976-e973-4395-b848-cba3ec2cd666" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/42d32087-25a3-498c-a5df-4221017bf6d4" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/54916d92-a51d-4078-aedf-3a1a7346a4ea" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b2c6a032-226b-4e80-a9ba-b66fe8d28636" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/53548424-538b-4761-a619-dae102db76dc" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d7b85306-0190-4c35-aacc-4a4031aed28e" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/46a7215d-4ea6-4ab4-be1c-aba5401e6975" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/86cfd3ac-3d72-48f7-a9b1-e36edae0c541" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/223286d9-ea3d-40a2-a84f-5df331395acb" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/609d4b39-7c4a-4bc7-8fb6-400f64ffdbd5" />

<h1>Deploying Active Directory
</h1>
Installing and Configuring Active Directory Domain Services
First, I log into DC-1 and install the Active Directory Domain Services (AD DS) role. After the installation completes, I promote the server to a Domain Controller by creating a new forest named mydomain.com. I restart the server and log back in to DC-1 using the domain account mydomain.com\labuser.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7b1648a5-7f73-4f21-aa10-6b41cdde7a74" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8697bec1-5de9-434e-940f-ce68f8a2052c" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1fcf7db6-dcd4-4be0-af10-bbe7ee5bcdef" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6d31fab2-f11d-4d22-b193-d8118e5b5cd2" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/928b6697-20da-478f-a9ea-2681d4b8ff4d" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c2054782-d301-4a6a-89c2-e146759631f8" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/37c649a5-8c55-44ed-b046-795e2e3e5e29" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/50febe71-77b8-420a-9438-76f35ceb91fb" />












































