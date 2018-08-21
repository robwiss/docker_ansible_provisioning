# How to Provision Docker with Ansible

1. `docker build -t basecentos .`
2. `docker images`
3. `docker run -dit --name=mycentos basecentos bash`
4. `docker ps`
5. `ansible-playbook -i hosts playbook.yml`
   * See: https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#non-ssh-connection-types
6. `docker attach mycentos`
7. in docker: `vim`
8. in docker: ctrl+p ctrl+q
10. `docker commit mycentos provisioned_centos`
11. `docker images`
12. `docker stop mycentos && docker rm mycentos`
13. `docker run --rm provisioned_centos which vim`
14. `docker run --rm basecentos which vim`

