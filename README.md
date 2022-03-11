ansible-role-win2019-languagepack
=========

Add language packs to a Windows 2019.   


Role Variables
--------------
The default values for the variables are set in `defaults/main.yml`:

```yaml
language_experience_pack_download_dir: 'C:\temp'
language_experience_pack_isos:
  - url: 'https://software-download.microsoft.com/download/pr/17763.1.180914-1434.rs5_release_SERVERLANGPACKDVD_OEM_MULTI.iso'
    dest: '{{ language_experience_pack_download_dir }}\langpack.iso'

language_experience_packs:
  - de-de

language_experience_pack_isos_remove_when_finished: true
```

Example Playbook
----------------


```yaml
- hosts: win2019
  vars:
    language_experience_pack_download_dir: 'D:\temp'
    language_experience_packs:
      - de-de
      - nl-nl

  roles:
    - { role: ansible-role-win2019-languagepack }
```
