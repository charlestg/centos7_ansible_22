## RUN

```
docker run --rm -it \
    --name ansible \
    -v `pwd`:/data \
    charlestg/centos7_ansible ansible --help
```

## Alias

```
# Create Alias
alias ansible='docker run --rm -it --name ansible -v `pwd`:/data charlestg/centos7_ansible_2.2 ansible'

# Run with Alias
ansible --help
ansible all -i hosts -m shell -a 'echo hello world'
ansible all -i "10.10.10.10," -m shell -a 'echo hello world'
```