Role Name
=========

Deploy a docker compose stack with one or multiple file

<!-- Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required. -->

Role Variables
--------------

  src: Docker_stack
  name: freeipa
  files:
    - docker-compose.0.yml
    - docker-compose.1.yml
  down_stack: False
  remove_artifcat: True
  command_before_build:
  command_on_build:
  command_build:
  command_before_start:
  command_on_start:
  command_start:
  command_after_start:
    - destination: local|machine/containeur name
      specific_command_environment:
        envar: overight
      command: "string"
    - ls
  command_down:
  command_clean:
  command_environment:
    envvar: value
    envvar1: value

<!-- Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles. -->

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts:
    - docker_compose
  roles:
    - role: deploy_docker_compose
      vars:
        src: Docker_stack
        name: freeipa
        files:
          - docker-compose.0.yml
          - docker-compose.1.yml
        down_stack: False
        remove_artifcat: True
        command_before_build:
        command_on_build:
        command_build:
        command_before_start:
        command_on_start:
        command_start:
        command_after_start:
          - destination: local|machine/containeur name
            specific_command_environment:
              envar: overight
            command: "string"
          - ls
        command_down:
        command_clean:
        command_environment:
          envvar: value
          envvar1: value

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
