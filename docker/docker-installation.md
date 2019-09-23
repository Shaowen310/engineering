# Docker installation

## Ubuntu 18.04

### Docker Community Edition

[Script](https://github.com/Shaowen310/scripts/blob/master/ubuntu/18.04/install-docker-ce.sh)

1. Remove any older installations of Docker that may be on the system

```
sudo apt remove docker docker-engine docker.io
```

2. Add Docker’s repository

```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

3. Add Docker’s GPG key:

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

4. Add the stable Docker repository

```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

5. Install Docker CE

```
sudo apt update
sudo apt install docker-ce
```

6. Get rid of sudo (takes effect after user logging out)

```
sudo usermod -aG docker $USER
```

7. Check that the installation was successful

```
docker run hello-world
```

## Windows 10

### WSL1 1809

#### Issue: Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?

1. Expose daemon on tcp://localhost:2375 without TLS

![https://medium.com/@sebagomez/installing-the-docker-client-on-ubuntus-windows-subsystem-for-linux-612b392a44c4](https://miro.medium.com/max/832/1*6XwT-oT7cbw63UFHLjQPzA.png)

Picture from https://medium.com/@sebagomez/installing-the-docker-client-on-ubuntus-windows-subsystem-for-linux-612b392a44c4

2. Add DOCKER_HOST environment variable to `.profile`

```
export DOCKER_HOST=localhost:2375
```

Drawback: not secure

Solutions:

1. [WSL Interoperability with Docker](https://devblogs.microsoft.com/commandline/cross-post-wsl-interoperability-with-docker/)

1. Wait for WSL2

## References

1. [Offical Document: Get Docker Engine - Community for Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

1. [Installing the Docker client on Windows Subsystem for Linux (Ubuntu)](https://medium.com/@sebagomez/installing-the-docker-client-on-ubuntus-windows-subsystem-for-linux-612b392a44c4)