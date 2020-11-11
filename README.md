__데이터몬 자빅스 ANSIBLE PLAYBOOK__
=================================

## 설치

```
ansible-playbook -vvv install.yml -i example/inventory.yaml
```

## 삭제

```
ansible-playbook -vvv uninstall.yml -i example/inventory.yaml
```

## DIRECTORY 구조

| example/inventory.yaml | 테스트를 위하여 생성한 인벤토리 |
| hosts                  | 호스트 정보: 현재 사용하지 않음 |
| install.yml            | 설치 설정 파일 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static | 설치에 필요한 파일을 저장해 놓은 폴더 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static/bin/zabbix_get | 자빅스 파일 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static/bin/zabbix_sender | 자빅스 파일 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static/conf/zabbix_agentd/userparameter_examples.conf | 자빅스 파일 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static/conf/zabbix_agentd/userparameter_mysql.conf | 자빅스 파일 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static/sbin/zabbix_agentd | 자빅스 파일 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static/service/zabbix-agent.service | 자빅스 파일 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static.original.tar.gz | 원본 자빅스 에이젼트 파일 |
| rpms/zabbix_agent-5.0.5-linux-3.0-amd64-static.tar.gz | 원본 자빅스 에이젼트 파일: 데이터빈 |
| tasks/autoadd_tasks.yml | 사용하지 않음 |
| tasks/install_tasks.yml | 사용중 (설치) |
| tasks/managepkgs_tasks.yml | 시용하지 않음 |
| tasks/remove.yml | 사용중 (삭제) |
| templates/zabbix_agentd.conf.j2 | 에이젼트 설정 템플릿 |
| templates/zabbix_sudoers.j2 | 사용하지 않음 |
| uninstall.yml | 삭제 파일 |
| vars/zabbix_variables.yml | 자빅스 변수 |

```
├── example
│   └── inventory.yaml
├── hosts
├── install.yml
├── README.md
├── rpms
│   ├── zabbix_agent-5.0.5-linux-3.0-amd64-static
│   │   ├── bin
│   │   │   ├── zabbix_get
│   │   │   └── zabbix_sender
│   │   ├── conf
│   │   │   ├── zabbix_agentd
│   │   │   │   ├── userparameter_examples.conf
│   │   │   │   └── userparameter_mysql.conf
│   │   │   └── zabbix_agentd.conf
│   │   ├── sbin
│   │   │   └── zabbix_agentd
│   │   └── service
│   │       └── zabbix-agent.service
│   ├── zabbix_agent-5.0.5-linux-3.0-amd64-static.original.tar.gz
│   └── zabbix_agent-5.0.5-linux-3.0-amd64-static.tar.gz
├── tasks
│   ├── autoadd_tasks.yml
│   ├── install_tasks.yml
│   ├── managepkgs_tasks.yml
│   └── remove.yml
├── templates
│   ├── zabbix_agentd.conf.j2
│   └── zabbix_sudoers.j2
├── uninstall.yml
└── vars
    └── zabbix_variables.yml
```

* Reference: 
  * R1: https://github.com/hvaithia/Ansible-zabbix-agent-installation