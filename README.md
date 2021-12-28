# Linux Kernel Configs for Popular distros

I frequently needed a way to check a kernel config and other configuration for popular distributions so that I can make a dev/design decision.

**My specific use-case**:
I was working on supporting [KubeArmor](https://github.com/kubearmor/kubearmor) on popular distros. KubeArmor leverages LSMs (Linux Security Modules) and eBPF for in kernel policy controls. We had to refer to kernel configs for making design/dev decisions regarding whether we can depend on a certain kernel primitive. The boot configs part of this repo helped for making an informed choice.

## How to get the details and raise a PR for new OS/Distro?

Use following command to create a Distro/Kernel specific folder with the corresponding markdowns:
```
curl -s https://raw.githubusercontent.com/nyrahul/linux-kernel-configs/main/lk-config-get.sh | bash -s
```
if `curl` is not available, use `wget` ...
```
wget -q -O- https://raw.githubusercontent.com/nyrahul/linux-kernel-configs/main/lk-config-get.sh  | bash -s
```
Copy the folder to your github fork and raise a PR.
# Distro Details
| Distro | Arch | Kernel | Boot Config | hostnamectl | os-release |
|:------:|:----:|:------:|:-----------:|:-----------:|:----------:|
| Amazon Linux 2022 | x86_64 | 5.10.75 | [config](<./Amazon Linux 2022/5.10.75-82.359.amzn2022.x86_64/bootconfig.md>) | [hostnamectl](<./Amazon Linux 2022/5.10.75-82.359.amzn2022.x86_64/hostnamectl.md>) | [os-release](<./Amazon Linux 2022/5.10.75-82.359.amzn2022.x86_64/os-release.md>) |
| Amazon Linux 2 | x86_64 | 4.14.252 | [config](<./Amazon Linux 2/4.14.252-195.483.amzn2.x86_64/bootconfig.md>) | [hostnamectl](<./Amazon Linux 2/4.14.252-195.483.amzn2.x86_64/hostnamectl.md>) | [os-release](<./Amazon Linux 2/4.14.252-195.483.amzn2.x86_64/os-release.md>) |
| Amazon Linux 2 | x86_64 | 5.10.75 | [config](<./Amazon Linux 2/5.10.75-79.358.amzn2.x86_64/bootconfig.md>) | [hostnamectl](<./Amazon Linux 2/5.10.75-79.358.amzn2.x86_64/hostnamectl.md>) | [os-release](<./Amazon Linux 2/5.10.75-79.358.amzn2.x86_64/os-release.md>) |
| CentOS Linux 7 (Core) | x86_64 | 3.10.0 | [config](<./CentOS Linux 7 (Core)/3.10.0-1127.el7.x86_64/bootconfig.md>) | [hostnamectl](<./CentOS Linux 7 (Core)/3.10.0-1127.el7.x86_64/hostnamectl.md>) | [os-release](<./CentOS Linux 7 (Core)/3.10.0-1127.el7.x86_64/os-release.md>) |
| CentOS Linux 8 | x86_64 | 4.18.0 | [config](<./CentOS Linux 8/4.18.0-240.1.1.el8_3.x86_64/bootconfig.md>) | [hostnamectl](<./CentOS Linux 8/4.18.0-240.1.1.el8_3.x86_64/hostnamectl.md>) | [os-release](<./CentOS Linux 8/4.18.0-240.1.1.el8_3.x86_64/os-release.md>) |
| Container-Optimized OS from Google | x86_64 | 5.4.144 | [config](<./Container-Optimized OS from Google/5.4.144+/bootconfig.md>) | [hostnamectl](<./Container-Optimized OS from Google/5.4.144+/hostnamectl.md>) | [os-release](<./Container-Optimized OS from Google/5.4.144+/os-release.md>) |
| Debian GNU/Linux 10 (buster) | x86 | 4.19.181 | [config](<./Debian GNU_Linux 10 (buster)/4.19.0-16-cloud-amd64/bootconfig.md>) | [hostnamectl](<./Debian GNU_Linux 10 (buster)/4.19.0-16-cloud-amd64/hostnamectl.md>) | [os-release](<./Debian GNU_Linux 10 (buster)/4.19.0-16-cloud-amd64/os-release.md>) |
| Fedora CoreOS 35.20211203.3.0 | x86_64 | 5.15.6 | [config](<./Fedora CoreOS 35.20211203.3.0/5.15.6-200.fc35.x86_64/bootconfig.md>) | [hostnamectl](<./Fedora CoreOS 35.20211203.3.0/5.15.6-200.fc35.x86_64/hostnamectl.md>) | [os-release](<./Fedora CoreOS 35.20211203.3.0/5.15.6-200.fc35.x86_64/os-release.md>) |
| Flatcar Container Linux by Kinvolk 3033.2.0 (Oklo) | x86 | 5.10.84 | [config](<./Flatcar Container Linux by Kinvolk 3033.2.0 (Oklo)/5.10.84-flatcar/bootconfig.md>) | [hostnamectl](<./Flatcar Container Linux by Kinvolk 3033.2.0 (Oklo)/5.10.84-flatcar/hostnamectl.md>) | [os-release](<./Flatcar Container Linux by Kinvolk 3033.2.0 (Oklo)/5.10.84-flatcar/os-release.md>) |
| k3OS v0.21.5-k3s2r1 | x86 | 5.4.0 | [config](<./k3OS v0.21.5-k3s2r1/5.4.0-88-generic/bootconfig.md>) | [hostnamectl](<./k3OS v0.21.5-k3s2r1/5.4.0-88-generic/hostnamectl.md>) | [os-release](<./k3OS v0.21.5-k3s2r1/5.4.0-88-generic/os-release.md>) |
| Pop!_OS 21.04 | x86 | 5.11.0 | [config](<./Pop!_OS 21.04/5.11.0-7633-generic/bootconfig.md>) | [hostnamectl](<./Pop!_OS 21.04/5.11.0-7633-generic/hostnamectl.md>) | [os-release](<./Pop!_OS 21.04/5.11.0-7633-generic/os-release.md>) |
| Pop!_OS 21.10 | x86 | 5.15.5 | [config](<./Pop!_OS 21.10/5.15.5-76051505-generic/bootconfig.md>) | [hostnamectl](<./Pop!_OS 21.10/5.15.5-76051505-generic/hostnamectl.md>) | [os-release](<./Pop!_OS 21.10/5.15.5-76051505-generic/os-release.md>) |
| RancherOS v1.5.8 | x86 | 4.14.138 | [config](<./RancherOS v1.5.8/4.14.138-rancher/bootconfig.md>) | [hostnamectl](<./RancherOS v1.5.8/4.14.138-rancher/hostnamectl.md>) | [os-release](<./RancherOS v1.5.8/4.14.138-rancher/os-release.md>) |
| Raspbian GNU/Linux 10 (buster) | arm | 5.10.17 | [config](<./Raspbian GNU_Linux 10 (buster)/5.10.17-v7l+/bootconfig.md>) | [hostnamectl](<./Raspbian GNU_Linux 10 (buster)/5.10.17-v7l+/hostnamectl.md>) | [os-release](<./Raspbian GNU_Linux 10 (buster)/5.10.17-v7l+/os-release.md>) |
| Red Hat Enterprise Linux 8.4 (Ootpa) | x86_64 | 4.18.0 | [config](<./Red Hat Enterprise Linux 8.4 (Ootpa)/4.18.0-305.el8.x86_64/bootconfig.md>) | [hostnamectl](<./Red Hat Enterprise Linux 8.4 (Ootpa)/4.18.0-305.el8.x86_64/hostnamectl.md>) | [os-release](<./Red Hat Enterprise Linux 8.4 (Ootpa)/4.18.0-305.el8.x86_64/os-release.md>) |
| SUSE Linux Enterprise Server 12 SP5 | x86_64 | 4.12.14 | [config](<./SUSE Linux Enterprise Server 12 SP5/4.12.14-122.54-default/bootconfig.md>) | [hostnamectl](<./SUSE Linux Enterprise Server 12 SP5/4.12.14-122.54-default/hostnamectl.md>) | [os-release](<./SUSE Linux Enterprise Server 12 SP5/4.12.14-122.54-default/os-release.md>) |
| SUSE Linux Enterprise Server 15 SP3 | x86 | 5.3.18 | [config](<./SUSE Linux Enterprise Server 15 SP3/5.3.18-59.24-default/bootconfig.md>) | [hostnamectl](<./SUSE Linux Enterprise Server 15 SP3/5.3.18-59.24-default/hostnamectl.md>) | [os-release](<./SUSE Linux Enterprise Server 15 SP3/5.3.18-59.24-default/os-release.md>) |
| Ubuntu 18.04.6 LTS | x86_64 | 5.4.0 | [config](<./Ubuntu 18.04.6 LTS/5.4.0-1060-aws/bootconfig.md>) | [hostnamectl](<./Ubuntu 18.04.6 LTS/5.4.0-1060-aws/hostnamectl.md>) | [os-release](<./Ubuntu 18.04.6 LTS/5.4.0-1060-aws/os-release.md>) |
| Ubuntu 20.04.3 LTS | x86_64 | 5.11.0 | [config](<./Ubuntu 20.04.3 LTS/5.11.0-1022-aws/bootconfig.md>) | [hostnamectl](<./Ubuntu 20.04.3 LTS/5.11.0-1022-aws/hostnamectl.md>) | [os-release](<./Ubuntu 20.04.3 LTS/5.11.0-1022-aws/os-release.md>) |
| VMware Photon OS/Linux | x86_64 | 5.10.61 | [config](<./VMware Photon OS_Linux/5.10.61-1.ph4/bootconfig.md>) | [hostnamectl](<./VMware Photon OS_Linux/5.10.61-1.ph4/hostnamectl.md>) | [os-release](<./VMware Photon OS_Linux/5.10.61-1.ph4/os-release.md>) |
