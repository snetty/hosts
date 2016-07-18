# Hosts Editor

A custom hosts file manager.

#### Setup

1. Make the script executable ``chmod +x ~/path/hosts``
2. Add the start/default part of your current /etc/hosts file to hosts.origin, it will probably look something like this:
    
    ```#
    # Host Database
    #
    # localhost is used to configure the loopback interface
    # when the system is booting.  Do not change this entry.
    ##
    127.0.0.1		localhost
    255.255.255.255	broadcasthost
    ::1             localhost
    fe80::1%lo0		localhost
    ```

3. Add any existing custom mappings to hosts.base, this is where your mappings will be stored when you add/remove them through the script.
4. Add static files to ``static/somename.hosts`` and they will be included untouched

#### Usage

* ``sudo ~/path/hosts add mydevdomain.dev 8.8.8.8`` set the mapped ip for a domain
* ``sudo ~/path/hosts rm mydevdomain.dev 8.8.8.8`` removes the mapped ip for a domain
* ``sudo ~/path/hosts fetch mydevdomain.dev`` show the mapped ip for a domain
* ``sudo ~/path/hosts read`` display entire hosts file
