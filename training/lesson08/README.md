# Ansible Vault

## Goals

-   Create an inventory file named "inventory" with a group named "myinstance" and your internal instance IP assigned included
-   Crate a vault variables file named "vault-vars.yml" in a new folder named "vars" with password "vault" and the following variables:
    -   String variable called "new_user_name" with a name "test01"
    -   String variable called "new_user_pass" with a password "test01"
-   Create a playbook named "vault-playbook.yml". The playbook should use tasks to ensure that the following conditions are met on the managed hosts:
    -   Generate a password hash in sha512 using "new_user_pass" and "123qweasdzxc" secret in a new variable named "new_hash_pass"
    -   Create a new user using "new_user_name" and "new_hash_pass" variables
-   Import "vault-vars.yml" file into the playbook
-   Before running your playbook, run the ansible-playbook --syntax-check site.yml command to verify that its syntax is correct
-   Run the playbook!
-   Test the new user
-   Modify "vault-vars.yml" file to include a string variable named "new_user_secret" with the previous secret content "123qweasdzxc"
-   Modify "vault-playbook.yml" playbook in order to include "new_user_secret" variable instead of then plain text secret
-   Run the playbook!
-   Test the user again

## Useful Links

For more information, please visit:

-   https://docs.ansible.com/ansible/latest/reference_appendices/faq.html#how-do-i-generate-encrypted-passwords-for-the-user-module
-   https://docs.ansible.com/ansible/latest/user_guide/playbooks.html
-   https://docs.ansible.com/ansible/latest/user_guide/vault.html
-   https://docs.ansible.com/ansible/latest/modules/modules_by_category.html