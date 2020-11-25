# create-sever-from-template-on-ovirt

#### Branch - sitedevelopments.net  By Johan Sörell

## This git repository's Playbooks

- create_vm.yml 

    Variables that are used:

    ```yaml

    # variables for the hosted-engine connection
        #engine_fqdn the fqdn of hosted-engine
        engine_fqdn: hosted-engine.yourdomain.domain
        #username for the hosted-engine
        engine_user: admin@internal
        #the location of the ca.pem file
        engine_cafile: /etc/pki/ovirt-engine/ca.pem  
        #engine_password is encrypted in a varsfile with ansible-vault
        engine_password:
        # set insecure yes | no
        engine_insecure:

    # The variables to create the vm
        #template name to use
        template: rhel83  
        #the amount of memory of server
        vm_memory: 4GiB
        #The vm's name 
        vm_name: vm-001.yourdomain.domain
        #enable ballooning yes | no
        vm_ballooning_enabled: yes
        #enable high availability yes | no
        vm_high_availability: yes

- deploy_git_vm.yml

```yaml

  #extra variables that are defined in deploy_git_vm.yml playbook is:
  # set disk size defaut value is 100GiB
  vm_disk_size:
