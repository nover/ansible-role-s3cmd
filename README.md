# Ansible s3cmd

Install and configure s3cmd on your server.

## Requirements

An Amazon S3 bucket, an access key + secret key for an IAM user to upload into this bucket.


## Role Variables

These role variables have NO DEFAULT VALUE and hence you must specify them before using this role.
Please note that the given AWS IAM user needs to have _write access_ to S3.

Variable | Description | Example
--- | --- | ---
`s3cmd_access_key`| IAM User access key | `AKIAD3212FIFKI2`
`s3cmd_secret_key`| IAM User secret key | `0Xpgfj32fagjj24234t4gjkaka`
`s3cmd_bucket_location`| S3 bucket location | `EU`
`s3cmd_encryption_password`| s3cmd encryption key | `my_super_Awesomesauce_enc_password!`

## Example Playbook

Use the playbook as follows, creating a local file in `vars` with the above mentioned variables in place

```yml
- hosts: servers
  roles:
    - { role: nover.s3cmd }
  vars_files:
    - vars/your-s3cmd.yml
```

## License

The unlicense
