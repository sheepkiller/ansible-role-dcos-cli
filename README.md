dcos-cli
=========

Install DC/OS CLI.

Requirements
------------

`virtualenv` on the remote host

Role Variables
--------------
| variable|default|comment
|-------|------|------|
|dcos_cli_ssl_verify| "false"|verify SSL connection
|dcos_cli_reporting| "true"|Report usage|
|dcos_cli_timeout| 5| Timeout |
|dcos_cli_url: "http|//localhost"| DC/OS  URL|
|dcos_cli_user| "{{ ansible_user_id }}"|Owner of this installation|
|dcos_cli_installpath| "{{ ansible_user_dir }}/dcos/"| installation path|
|dcos_cli_version| 0.4.4|version|
|dcos_cli_virtualenv_command||alternative virtualenv|



Example Playbook: install on your box
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Install DC/OS CLI on my laptop, in my homedir
      hosts: localhost
      connection: local
      gather_facts: True
      roles:
       - {
            role: dcos-cli,
            dcos_cli_url: "http://my.mesos.url",
            dcos_cli_virtualenv_command: /usr/bin/virtualenv2
         }

License
-------

BSD
