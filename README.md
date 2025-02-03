# Ansible

This repository contains multiple Ansible playbooks and supporting files designed to manage system operations across multiple hosts. The playbooks cover tasks such as:

- **Backup and Archive**  
  - [backup_tar.yaml](backup_tar.yaml): Archives a directory, moves the tar file to a destination, and sets file ownership.

- **User Management**  
  - [createuser_with_encrypted_pass.yaml](createuser_with_encrypted_pass.yaml): Creates groups and users with encrypted passwords and assigns group memberships.  
  - [createuser_with_sshkeys.yaml](createuser_with_sshkeys.yaml): Creates users and sets up authorized SSH keys.  
  - [deleteuser.yaml](deleteuser.yaml): Removes users defined in the variable file.

- **Security and Monitoring**  
  - [deploy_cronjob_trivy.yaml](deploy_cronjob_trivy.yaml): Installs Trivy, configures a cron job for vulnerability scans, and sends notifications on scan results.  
  - [deploy_filebeat.yaml](deploy_filebeat.yaml): Installs and configures Filebeat to collect logs and ship them to Logstash.  
  - [deploy_metricbeat.yaml](deploy_metricbeat.yaml): Installs and configures Metricbeat to collect system metrics and dispatch them to Kafka.

- **System and Storage Configuration**  
  - [lvm_automate.yaml](lvm_automate.yaml): Sets up partitions, volume groups, and logical volumes, formats filesystems, and mounts storage.  
  - [vm_setup.yaml](vm_setup.yaml): Installs Docker and Kubernetes packages, configures repositories, updates system settings, and adjusts network parameters.

Additionally, the workspace includes:
- An inventory file ([hosts](hosts))
- Variable files ([users](users), [vars](vars), [vars-lvm](vars-lvm))