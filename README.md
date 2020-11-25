# create-sever-from-template-on-ovirt
## This git repository's Playbooks 
- create_vm _template.yml 

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
    
    # The variables to create the vm
        #template name to use
        template: rhel83  
        #the amount of memory of server
        vm_memory: 4GiB
        #The vm's name 
        vm_name: vm-001.yourdomain.domain
        #Do you like to use the ballooning fuction
        vm_ballooning_enabled: yes
        #Should it use high availability 
        vm_high_availability: yes



---

