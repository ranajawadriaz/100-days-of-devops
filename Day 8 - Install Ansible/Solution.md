<pre>
thor@jumphost ~$ pip3 --version
pip 24.0 from /usr/local/lib/python3.9/site-packages/pip (python 3.9)
thor@jumphost ~$ ansible --version
bash: ansible: command not found
thor@jumphost ~$ sudo pip3 install ansible==4.9.0

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for thor: 
Collecting ansible==4.9.0
  Downloading ansible-4.9.0.tar.gz (36.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 36.6/36.6 MB 82.7 MB/s eta 0:00:00
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Collecting ansible-core<2.12,>=2.11.6 (from ansible==4.9.0)
  Downloading ansible-core-2.11.12.tar.gz (7.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 7.1/7.1 MB 125.2 MB/s eta 0:00:00
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Collecting jinja2 (from ansible-core<2.12,>=2.11.6->ansible==4.9.0)
  Downloading jinja2-3.1.6-py3-none-any.whl.metadata (2.9 kB)
Requirement already satisfied: PyYAML in /usr/lib64/python3.9/site-packages (from ansible-core<2.12,>=2.11.6->ansible==4.9.0) (5.4.1)
Requirement already satisfied: cryptography in /usr/lib64/python3.9/site-packages (from ansible-core<2.12,>=2.11.6->ansible==4.9.0) (36.0.1)
Collecting packaging (from ansible-core<2.12,>=2.11.6->ansible==4.9.0)
  Downloading packaging-25.0-py3-none-any.whl.metadata (3.3 kB)
Collecting resolvelib<0.6.0,>=0.5.3 (from ansible-core<2.12,>=2.11.6->ansible==4.9.0)
  Downloading resolvelib-0.5.4-py2.py3-none-any.whl.metadata (3.7 kB)
Requirement already satisfied: cffi>=1.12 in /usr/lib64/python3.9/site-packages (from cryptography->ansible-core<2.12,>=2.11.6->ansible==4.9.0) (1.14.5)
Collecting MarkupSafe>=2.0 (from jinja2->ansible-core<2.12,>=2.11.6->ansible==4.9.0)
  Downloading MarkupSafe-3.0.2-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.0 kB)
Requirement already satisfied: pycparser in /usr/lib/python3.9/site-packages (from cffi>=1.12->cryptography->ansible-core<2.12,>=2.11.6->ansible==4.9.0) (2.20)
Requirement already satisfied: ply==3.11 in /usr/lib/python3.9/site-packages (from pycparser->cffi>=1.12->cryptography->ansible-core<2.12,>=2.11.6->ansible==4.9.0) (3.11)
Downloading resolvelib-0.5.4-py2.py3-none-any.whl (12 kB)
Downloading jinja2-3.1.6-py3-none-any.whl (134 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 134.9/134.9 kB 25.4 MB/s eta 0:00:00
Downloading packaging-25.0-py3-none-any.whl (66 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 66.5/66.5 kB 18.2 MB/s eta 0:00:00
Downloading MarkupSafe-3.0.2-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (20 kB)
Building wheels for collected packages: ansible, ansible-core
  Building wheel for ansible (pyproject.toml) ... done
  Created wheel for ansible: filename=ansible-4.9.0-py3-none-any.whl size=60168827 sha256=2d2900c4c81b547e07dd1c47cb7d2935746e1b232738b7f2f426a445ee259deb
  Stored in directory: /root/.cache/pip/wheels/33/b7/3a/a0419b4a74d0493a7a17adb9b944b045ed8e81c6e5ec5f81d6
  Building wheel for ansible-core (pyproject.toml) ... done
  Created wheel for ansible-core: filename=ansible_core-2.11.12-py3-none-any.whl size=1961046 sha256=d3b954354fd16d2601c26b82c0685877356da096b882859d846e8363be9b186d
  Stored in directory: /root/.cache/pip/wheels/06/b5/3d/4a4a1b494bb61ba26534ba172b81d1972467ee6c792d737b78
Successfully built ansible ansible-core
Installing collected packages: resolvelib, packaging, MarkupSafe, jinja2, ansible-core, ansible
Successfully installed MarkupSafe-3.0.2 ansible-4.9.0 ansible-core-2.11.12 jinja2-3.1.6 packaging-25.0 resolvelib-0.5.4
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv

[notice] A new release of pip is available: 24.0 -> 25.2
[notice] To update, run: pip install --upgrade pip
thor@jumphost ~$ ansible --version
ansible [core 2.11.12] 
  config file = None
  configured module search path = ['/home/thor/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/lib/python3.9/site-packages/ansible
  ansible collection location = /home/thor/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/local/bin/ansible
  python version = 3.9.18 (main, Jan 24 2024, 00:00:00) [GCC 11.4.1 20231218 (Red Hat 11.4.1-3)]
  jinja version = 3.1.6
  libyaml = True
thor@jumphost ~$ ^C
thor@jumphost ~$ 
</pre>