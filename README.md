tenantcloud.ansible_role_dashboard
=========

Ansible role for install dashboard project.

  - tenantcloud_dashboard
  - keller_dashboard

Requirements
------------

Install tenantcloud.ansible_role_software_common
Install tenantcloud.ansible_role_software_dev

Role Variables
--------------

work_user: "user"
work_dir: "work"
dashboard_git:
dashboard_dir:
docker_git:
docker_dir:
work_domain:
database:
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
websockets_dir:
websockets_image_aws:

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
        work_user: "user"
        work_dir: 
        dashboard_git:
        dashboard_dir:
        docker_dir:
        docker_git:
        work_domain:
        database:
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
        websockets_dir:
        websockets_image_aws:
      roles:
        - tenantcloud.ansible_role_dashboard

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
