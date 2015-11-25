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

If nhc_github is set to False it installs it from a pre-configured yum-repo.
Default is True

nhc_github: True

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
