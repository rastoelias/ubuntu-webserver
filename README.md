# Ubuntu 18.04 Webserver
Ansible playbook for initial Ubuntu 18.04 webserver setup.

* Ubuntu server 18.04
* Apache 2
* PHP 7.2

## Requirements
* SSH Keys on the client machine.
* A machine with the [Ubuntu server](http://cdimage.ubuntu.com/releases/18.04.2/release/) installed.
* SSH Key-Based Authentication your server.
* Ansible 2.7+ on your local machine.

## Roles
* Set timezone to `TIMEZONE`

## Usage
1. Clone this repository:
    ```
    git clone https://github.com/rastoelias/ubuntu-webserver.git ubuntu-webserver
    ```
2. Copy the `hosts.example` file to the `hosts` file.
    ```
    cp hosts.example hosts
    ```
3. Open the `hosts` file and replace `SERVER-IP-ADDRESS` with the public IP address of your server.
    ```
    [server]
    111.111.111.111
    ```
4. Copy the `config.example.yml` to the `config.yml` file.
    ```
    cp config.example.yml config.yml
    ```
5. Open the `config.yml` file, make desired changes and save changes.
6. Run playbook
    ```
    ansible-playbook provision.yml -u USER --become -K -e ansible_port=PORT
    ```
