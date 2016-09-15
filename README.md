---

Ansible-Flask
===

Will run a provided Flask app repository using Gunicorn.

The basic variables can be found inside `defaults/main.yml`

Usage
---

Hosts roles:

```
- hosts: myserver
  roles:
    - { role: flask }
```

Variables for host:


`flask_server_user`: Name of the user that will run the app.
`flask_server_group`: Name of the group to own the necesary folders
`flask_repo`: URL to a git repo containing the code
`flask_app_name`: Name of the app to run. Default `hello`
`flask_workers`: Number of workers to use to run gunicorn. Default `4`.
`flask_host`: Host that will contain the app. Default `0.0.0.0`
`flask_port`: Port to run the app `8000`
`flask_git_priv_key_path`: If you will use a private repo, you need to specify where the key to use.
