# My Personal Package Archives (PPA) and Repository

Here's where I host my publicly available packages. You can find me on [𝕏 as @viktorplaga](https://x.com/viktorplaga)
and on [LinkedIn as Wiktor Plaga](https://www.linkedin.com/in/wiktor-plaga-7a353a106).

## Use `apt` packages

To define this PPA as an installation source, run the following commands:

```bash
curl -s --compressed "https://wscourge.github.io/ppa/public.gpg" | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/wscourge.gpg >/dev/null
sudo curl -s --compressed -o /etc/apt/sources.list.d/wscourge.list "https://wscourge.github.io/ppa/apt/wscourge.list"
```

Then, install the package(s):

```bash
sudo apt update
sudo apt install safe-utils
```

Resources:

- [Hosting your own PPA repository on GitHub](https://assafmo.github.io/2019/05/02/ppa-repo-hosted-on-github.html)
- [Athrunsun's self-hosted Github PPA example](https://github.com/athrunsun/ppa)

<!-- ## Use `yum` packages

To define this Repository as an installation source, create a `/etc/yum.repos.d/wscourge.repo` file:

```
[wscourge]
name=Wscourge GitHub Repository
baseurl=https://wscourge.github.io/ppa/yum
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://wscourge.github.io/ppa/public.gpg
```

Then, install the package(s):

```bash
yum install safe-utils
```

Resources:

- [Guide to Establishing and Hosting a Remote Yum Repository on GitHub](https://medium.com/debugging-diaries/guide-to-establishing-and-hosting-a-remote-yum-repository-on-github-b8326b60ac68)
- [HOWTO: GPG sign and verify RPM packages and yum repositories](https://blog.packagecloud.io/how-to-gpg-sign-and-verify-rpm-packages-and-yum-repositories/)

## Use `dnf` packages

To define this Repository as an installation source, create a `/etc/yum.repos.d/wscourge.repo` file:

```
[wscourge]
name=Wscourge GitHub Repository
baseurl=https://wscourge.github.io/ppa/yum
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://wscourge.github.io/ppa/public.gpg
```

Then, install the package(s):

```bash
dnf install safe-utils
```

Resources:

- [Guide to Establishing and Hosting a Remote Yum Repository on GitHub](https://medium.com/debugging-diaries/guide-to-establishing-and-hosting-a-remote-yum-repository-on-github-b8326b60ac68)
- [HOWTO: GPG sign and verify RPM packages and yum repositories](https://blog.packagecloud.io/how-to-gpg-sign-and-verify-rpm-packages-and-yum-repositories/)

## Use `pacman` packages

To define this Repository as an installation source, add the following to a `/etc/pacman.conf` file:

```
[wscourge]
SigLevel = Optional
Server = https://wscourge.github.io/ppa/pacman/repo
```

Then update the repository:

```
sudo pacman -Sy
```

Resources:
- [KSXGitHub's self-hosted Github pacman repo example](https://github.com/KSXGitHub/pacman-repo)

 -->
