<h1>Active Directory Password Reset Guide Lab</h1>

<h2>Description</h2>
Quick guide on how to reset a user password in Active Directory
<br />

<h2>Software & Tools Used</h2>

- <b>Active Directory</b> 
- <b>PowerShell</b>
- <b>Virtualbox</b>
- <b>Windows Server 2019</b>
- <b>Windows 11</b>

<h2>Project walk-through</h2>

<h3>Network plan for project environment</h3> 
<br />
<img src="https://i.imgur.com/vpqGEXe.png" height="80%" width="80%" />

<h3>Virtualbox performance issues</h2>
I was creating a virtual machine to install Windows Server 2019 and ran into strong performance issues: The mouse was so slow it became impossible to click on things. When typing, the letters would show up only about a minute later. I had different theories about what could be the problem. I went through the troubleshooting process step-by-step:

 - Performance of my laptop: Ruled out because of i7 Intel processor and 8Gb RAM on my host device.
 - Hardware ressources allocated to virtual machine: Increased from 1Gb to 2Gb RAM and gave it 2 instead of 1 CPU core. No significant change in performance.
 - Virtualisation not activated in BIOS (UEFI in my laptop's case): This ended up to be the solution. However, I had to research the difference between Windows own Hyper-V technology which is definitely not what Virtualbox uses and Intel's VT-x which is what I needed. After activating VT-x Virtualbox performed as expected.
<br />
<img src="https://i.imgur.com/YSYWoaM.png" height="80%" width="80%" />
<br />
<br />
With Virtualbox now running as intended, I went ahead and created the first virtual machine to serve as our Windows Server 2019 and Active Directory Domain Services (DC on the Network plan). <br />
<br />
