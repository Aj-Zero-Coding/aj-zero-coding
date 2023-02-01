# Install Terraform in windows.

in this blog we learn how to install terraform in windows.

**Terraform**

**Chocolatey** is a free and open-source package management system for Windows. Install the **Terraform package** from the command line.

*$ choco install terraform*

### Verify the installation

Verify that the installation worked by opening a new terminal session and listing Terraform’s available subcommands.

```
$ choco install terraform
```

.

```
$ terraform -help  
Usage: terraform [-version] [-help] <command> [args]
```

```
The available commands for execution are listed below.  
The most common, useful commands are shown first, followed by  
less common or more advanced commands. If you're just getting  
started with Terraform, stick with the common commands. For the  
other commands, please read the help and docs before usage.  
##...
```

Add any subcommand to `***terraform -help***` to learn more about what it does and available options.

```
$ terraform -help plan
```

### Troubleshoot

If you get an error that `***terraform***` could not be found, your `***PATH***` environment variable was not set up properly. Please go back and ensure that your `***PATH***` variable contains the directory where Terraform was installed.

### Enable tab completion

If you use either Bash or Zsh, you can enable tab completion for Terraform commands. To enable autocomplete, first ensure that a config file exists for your chosen shell.

BashZsh

```
$ touch ~/.bashrc
```

Then install the autocomplete package.

```
$ terraform -install-autocomplete
```

Once the autocomplete support is installed, you will need to restart your shell.

### Quick start tutorial

Now that you’ve installed Terraform, you can provision an NGINX server in less than a minute using [Docker](https://www.docker.com/products/docker-desktop) on Mac, Windows, or Linux. You can also follow the rest of this tutorial in your web browser.

Click on the tab(s) below relevant to your operating system.

Docker Desktop for MacDocker Desktop for WindowsDocker Engine for LinuxWeb Browser

To run Docker on your Windows 10 machine, you must use the Windows Subsystem for Linux (WSL2). [Download and install WSL2](https://docs.microsoft.com/en-us/windows/wsl/install-win10) before moving on.

Download [Docker Desktop for Windows](https://docs.docker.com/docker-for-windows/install).

After you install Terraform and Docker on your local machine, start Docker Desktop by searching for Docker from your Start Menu and select Docker Desktop in the search results. When the whale icon in the status bar stays steady, Docker Desktop is up-and-running, and is accessible from any terminal window.

For more information on Docker Desktop requirements for Windows, visit the Docker docs

Create a directory named `***learn-terraform-docker-container***`***.***

```
$ mkdir learn-terraform-docker-container
```

Then, navigate into it.

```
$ cd learn-terraform-docker-container
```

Paste the following Terraform configuration into a file and name it `***main.tf***`.

Mac or LinuxWindows

```
terraform {  
  required_providers {  
    docker = {  
      source  = "kreuzwerker/docker"  
      version = ">= 2.13.0"  
    }  
  }  
}
```

```
provider "docker" {  
  host    = "npipe:////.//pipe//docker_engine"  
}
```

```
resource "docker_image" "nginx" {  
  name         = "nginx:latest"  
  keep_locally = false  
}
```

```
resource "docker_container" "nginx" {  
  image = docker_image.nginx.latest  
  name  = "tutorial"  
  ports {  
    internal = 80  
    external = 8000  
  }  
}
```

Initialize the project, which downloads a plugin that allows Terraform to interact with Docker.

```
$ terraform init
```

Provision the NGINX server container with `apply`. When Terraform asks you to confirm type `yes` and press `ENTER`.

```
$ terraform apply
```

Verify the existence of the NGINX container by visiting [localhost:8000](http://localhost:8000/) in your web browser or running `***docker ps***` to see the container.

```
$ docker ps  
CONTAINER ID        IMAGE                     COMMAND                  CREATED             STATUS              PORTS                    NAMES  
425d5ee58619        e791337790a6              "nginx -g 'daemon of…"   20 seconds ago      Up 19 seconds       0.0.0.0:8000->80/tcp     tutorial
```

To stop the container, run `***terraform destroy***`.

```
$ terraform destroy
```

You’ve now provisioned and destroyed an NGINX webserver with Terraform.