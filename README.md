keller.dashboard
=========

Ansible role for install dashboard project.

  - keller_dashboard

Ste-by-step
------------

  - Setup Kellermanagement docker containers project and pull images from https://github.com/KWXS/km-containers
  - Download needed ansible roles
  - Create ansible playbook and fill role variables
  - Setup awscli with keys for pulling images from AWS ECR
  - Add public ssh-key in guthub account for pull repository via ansible role
  - Run ansible playbook

Requirements
------------

```git
php@7.4
mysql@5.7
redis-server
nginx
docker
docker-compose
awscli
```

awscli must be installed and configured, AWS keys have permission to pulling images from AWS ECR.
Public ssh-key must be added on github account (https://github.com/settings/keys)

Role Variables
--------------

```git
ansible_user: "user" os username 
work_dir: "work"
dashboard_git:
dashboard_git_branch:
dashboard_dir:
docker_dir:
docker_git:
work_domain:
mysql_host:
mysql_admin_user:
mysql_admin_password:
mysql_database:
mysql_db_user:
mysql_db_user_pass:
pusher_app_id:
pusher_app_key:
pusher_app_secret:
app_key:
mysql_user:
minio_key:
minio_secret:
zencoder_key:
webhook_token:
rentrange_key:
aws_lambda_key:
aws_lambda_secret:
aws_lambda_region:
aws_lambda_s3:
aws_default_region:
php_api_version:
php_version:
app_env:
```

Dependencies
------------

  - homebrew
  - python@3
  - ansible

Example Playbook
----------------

    - hosts: localhost
      become: no
      vars:
        ansible_user: "user"
        work_dir: "work"
        dashboard_git:
        dashboard_git_branch:
        dashboard_dir:
        docker_dir:
        docker_git:
        work_domain:
        mysql_host:
        mysql_admin_user:
        mysql_admin_password:
        mysql_database:
        mysql_db_user:
        mysql_db_user_pass:
        pusher_app_id:
        pusher_app_key:
        pusher_app_secret:
        app_key:
        mysql_user:
        minio_key:
        minio_secret:
        zencoder_key:
        webhook_token:
        rentrange_key:
        aws_lambda_key:
        aws_lambda_secret:
        aws_lambda_region:
        aws_lambda_s3:
        aws_default_region:
        php_api_version:
        php_version:
        app_env:
      roles:
        - KWXS.dashboard

License
-------

BSD

Author Information
------------------

KWXS
