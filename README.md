# kenobyn3final

## Organização do repositório:
```
.
├── data
│   ├── logs => Nginx logs.
│   └── mysql => Arquivo de banco MySQL.
├── mysql => Folder com Dockfile, schema e configuração do MySQL.
├── nginx => Folder com Dockfile e arquivos de configurações do Nginx.
├── node => Folder com Dockfile e código fonte da aplicação em NodeJS.
├── playbooks => Playbooks para execução das roles.
└── roles => Roles para instalação do Docker, docker-compose e direnv
```

## Dependencias:
- ansible
- docker
- docker-compose

## Para executar

### Instalando as dependencias:
```
ansible-playbook playbooks/main.yml --ask-sudo-pass
```

### Executando o ambiente
```
docker-compose up --build -d
```

### Adicionando uma nota
```
curl -X POST http://localhost/notes -d 'Nota a ser adicionada'    
Ok%
```

#### Consultando as notas registradas
```
curl -X GET http://localhost/notes
[{"Id":5,"Text":"`adicionando nota #nkfl123` = ''","CreateDate":"2019-09-17T03:27:09.000Z"}]%
```
### Apagando uma nota (As notas são removidas pelo ID gerado)
```
curl -X DELETE http://localhost/notes/5
Ok%
