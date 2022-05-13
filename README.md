# ansible-role-registry
Containerized Docker registry.

## Example Playbook

    - hosts: all
      become: true
    
      vars:
        registry_instances:
          - name: registry1
            hostname: registry.example.com
            users:
              - name: "username"
                password: "secure-password"
    
        tls_cert: "http:// or file: path"
        tls_key: "http:// or file: path"
        max_image_size: "2000M"
    
      roles:
        - name: registry
