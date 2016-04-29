[![Build Status](https://travis-ci.org/CSC-IT-Center-for-Science/ansible-role-nhc.svg?branch=master)](https://travis-ci.org/CSC-IT-Center-for-Science/ansible-role-nhc)
ansible-role-nhc
=========

Install Node Health Checker https://github.com/mej/nhc

Requirements
------------

 - A batch scheduler
 - Internet access to Github

Role Variables
--------------

See defaults/main.yml for a complete list

If nhc_github is set to False it installs it from a pre-configured yum-repo.
Default is True

nhc_github: True

If we set nhc_use_default_checks to True - then all the default checks in nhc.conf will not be added. Only the ones in nhc_checks list.
<pre>
nhc_use_default_checks: True

nhc_checks:
 - { match: "*", name: "check_reboot_slurm", arguments: "" }
 - { match: "{gpu[1-19]}", name: "check_hw_ib", arguments: "40" }
</pre>

nhc_rm: "slurm" # but can also be whatever else NHC supports like pbs or torque. 

<pre>
# setting nhc_rm to "" means we don't set the variable at all - autodetection
nhc_rm: ""
</pre>

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-nhc }

License
-------

MIT

Author Information
------------------
