Windows功能：Hyper-V（控制面板-程序和功能-windows功能，win家庭版没有这个选项）

启动服务：HV主机服务（win+R中输入services.msc）

powershell：bcdedit /set hypervisorlaunchtype auto


VMware不支持Hyper-V

GNS3：需要关闭Hyper-V, HV主机服务，bcdedit /set hypervisorlaunchtype off，VMware中关闭虚拟化引擎：虚拟化Intel VT-x/EPT 或AMD-I/RVI(V)

GNS3配置之后，
1. DockerDesktop会报错：Hardware assisted virtualization and data execution protection must be enabled in the BIOS. Refer to https://docs.docker.com/desktop/windows/troubleshoot/#virtualization

Docker官网提供的Virtualization出错解决方案：
Step1: 打开Windows功能中的“虚拟机平台”和“适用于Linux的Windows子系统”
Step2：如果是Win专业版，还可以打开Hyper-V
Step3：

2. WSL会报错(通过powershell打开wsl)：请启用虚拟机平台Windows功能并确保在BIOS中启用虚拟化。


<img src="image-20211018092941619.png" alt="image-20211018092941619" style="zoom:50%;" />
