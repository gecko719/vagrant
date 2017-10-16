# Vagrant 


#### 1. 建立資料匣

~~~
$ mkdir -p /Users/chungwei/Documents/work/vagrant/williamyeh-ubuntu-trusty64-docker-1
$ cd /Users/chungwei/Documents/work/vagrant/williamyeh-ubuntu-trusty64-docker-1
~~~

#### 2. 從Vagrant Cloud 安裝 Box 'boxwilliamyeh/ubuntu-trusty64-docker'

~~~
$ vagrant init williamyeh/ubuntu-trusty64-docker
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
[1]+  Done                    mkdir -p /Users/chungwei/Documents/work/vagrant/williamyeh-ubuntu-trusty64-docker-1

~~~

#### 3. 查看目錄下是否有產生Vagrantfile

~~~
$ ls
Vagrantfile

~~~

#### 4. 透過Vagrantfile檔案來啟動虛擬機。

~~~

$ vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Box 'williamyeh/ubuntu-trusty64-docker' could not be found. Attempting to find and install...
    default: Box Provider: virtualbox
    default: Box Version: >= 0
==> default: Loading metadata for box 'williamyeh/ubuntu-trusty64-docker'
    default: URL: https://vagrantcloud.com/williamyeh/ubuntu-trusty64-docker
==> default: Adding box 'williamyeh/ubuntu-trusty64-docker' (v1.12.1.20160830) for provider: virtualbox
    default: Downloading: https://vagrantcloud.com/williamyeh/boxes/ubuntu-trusty64-docker/versions/1.12.1.20160830/providers/virtualbox.box
==> default: Successfully added box 'williamyeh/ubuntu-trusty64-docker' (v1.12.1.20160830) for 'virtualbox'!
==> default: Importing base box 'williamyeh/ubuntu-trusty64-docker'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'williamyeh/ubuntu-trusty64-docker' is up to date...
==> default: Setting the name of the VM: williamyeh-ubuntu-trusty64-docker-1_default_1507940136633_24017
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default: 
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default: 
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: The guest additions on this VM do not match the installed version of
    default: VirtualBox! In most cases this is fine, but in rare cases it can
    default: prevent things such as shared folders from working properly. If you see
    default: shared folder errors, please make sure the guest additions within the
    default: virtual machine match the version of VirtualBox you have installed on
    default: your host and reload your VM.
    default: 
    default: Guest Additions Version: 5.0.24
    default: VirtualBox Version: 5.1
==> default: Mounting shared folders...
    default: /vagrant => /Users/chungwei/Documents/work/vagrant/williamyeh-ubuntu-trusty64-docker-1

~~~


#### 5. 登入虛擬機

~~~
$ vagrant ssh
Welcome to Ubuntu 14.04.5 LTS (GNU/Linux 4.2.0-42-generic x86_64)

 * Documentation:  https://help.ubuntu.com/
vagrant@localhost ~ $

~~~

#### 6. 確認OS資訊

~~~
vagrant@localhost ~ $ lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 14.04.5 LTS
Release:	14.04
Codename:	trusty 
~~~

#### 7. 關閉虛擬機

~~~
$ vagrant halt
==> default: Attempting graceful shutdown of VM...
~~~
