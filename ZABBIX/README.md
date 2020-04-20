# ZABBIX
[![N|Solid](https://assets.zabbix.com/img/logo/zabbix_logo_black_and_white.png)](https://docs.ansible.com/ansible/latest/index.html)

Repositório destinado a playbooks e códigos feito em Ansible.

  - Debian 8 e 9
  - Ansible
  - Zabbix

### Destalhes antes de proseguir:
O documento e estinado a pessoas que estão em busca de melhorar os seus playbooks de ansible ou que precisam
automatizar a instalação de agents zabbix no ambiente.

#### Entendendo alguns parametros do ansible-playbook

```sh
# -e version_zbx=4.4  # versão do zabbix. O código suporta versão 3.4 e 4.4 
# -e l_user=giovani # variavel responsável pelo usuário de conexão no servidor via ssh
# -e server_proxy=ip.do.proxy # Informe o IP do zabbix-proxy, o mesmo será processado no arquivo de config em zbxconfig
# -e cli_tag=tagdocliente # informação referente ao hostmedatadata no arquivo de config em zbx.config 
# -e cli_host=hostsdocliente # Nome dos hosts do cliente. Deve ser o mesmo nome existente em 
# -i hosts/hosts_install_zabbix_agent.yml  # arquivo que conterá a estrutura de hosts para fazer a instalação

```
### Como Executar o playbook:

```sh
$ ansible-playbook main.yml -e version_zbx=4.4 -e l_user=giovani -e server_proxy=ip.do.proxy -e cli_tag=tagdocliente -e cli_host=hostsdocliente -i hosts/hosts_install_zabbix_agent.yml
```

## Melhorias? Submeta uma Issue ou faça uma PR
![N|Solid](https://www.imagensanimadas.com/data/media/1618/tux-imagem-animada-0136.gif)

### Documentação
[Ansible Install] https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html