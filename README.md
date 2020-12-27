Custom scripts
=========

This playbook allows you to install and configure custom scripts

TODO
----

No to do's

Requirements
------------

There are no requirements for this role


Role Variables
--------------

This is an example of a full script install

    scripts:
      - name: mysqlbackup # Name of script on the server
        ext: sh # extension that should be used
        mode: 0611 # Or like 'u=rw,g=r,o=r, a+x'
        source: "{{ playbook_dir }}/scripts/" # Source folder location from local or server
        destination: "/usr/local/bin" # target folder location
        owner: "root" # default root unless filled
        group: "root" # default root unless filled

Dependencies
------------

There are no Dependecies for this role

Example Playbook
----------------

    - name: Configure scripts
      hosts: all
      roles:
        - ggiinnoo.scripts

License
-------

BSD

Author Information
------------------

    Creator: Gino Jansen
    Website: www.ginojansen.nl
