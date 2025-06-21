# Active-Directory-Environment

📋 Contents
1.Features

2.Requirements

3.Setup Guide

4.Usage Examples

5.Screenshots

✨ Features

✅ Automated domain controller setup

✅ Sample OU structure

✅ Test users and groups

✅ Security policies pre-configured


🛠️ Requirements

Hardware: 4GB RAM, 2vCPU, 50GB storage

Software: Windows Server ISO, window 11 pro




![VirtualBox_Window Server 2022 _21_06_2025_21_58_34](https://github.com/user-attachments/assets/c9e1b027-4f3b-44fa-9cc5-2711caf2461e)


⚡ Setup Guide

1.Install AD Domain Services

powershell

command - Install-WindowsFeature AD-Domain-Services -IncludeManagementTools

2.Promote to Domain Controller

powershell

command - Install-ADDSForest -DomainName "lab.local" -InstallDNS -SafeModePassword (ConvertTo-SecureString "SafePass123!" -AsPlainText -Force)

🖥️ Usage Examples
Create Organizational Units

powershell
command - New-ADOrganizationalUnit -Name "Departments" -Path "DC=lab,DC=local"



Manage Group Policy

powershell
command - New-GPO -Name "Security Baseline" | New-GPLink -Target "DC=lab,DC=local"

📸 Screenshots

![ad](https://github.com/user-attachments/assets/595bf804-41ac-486c-a6de-c215c8accf54)




![ad](https://github.com/user-attachments/assets/79f9e875-f376-4591-89e2-966c654a8f22)


![dns](https://github.com/user-attachments/assets/f2fc804e-92a7-4f53-ac14-ff1c6c0e5d33)


![group1](https://github.com/user-attachments/assets/608512cd-4a38-4a7f-9596-f30aa01f0c61)


![group2](https://github.com/user-attachments/assets/2a1fba72-1fec-4b07-bb6e-2a5c0078525f)

⚠️ Safety Reminder

Use only in isolated VMs

Never use production credentials

Take regular snapshot
