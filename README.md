








































nifi-project/
├── README.md               → Documentação do projeto (objetivo, instruções, etc.)
├── .gitignore              → Arquivos/pastas a ignorar no Git (logs, dados sensíveis, etc.)
├── drivers/                → Drivers JDBC (referenciar, não versionar JARs grandes)
├── flows/                  → Arquivos JSON exportados dos fluxos NiFi
│   ├── fluxo-nifi-v1.json  → Export do fluxo NiFi atual
│   └── ...
├── scripts/                → Scripts auxiliares (backup, restore, importação, etc.)
├── configs/                → Configurações extras do NiFi (nifi.properties, etc.)
└── docker/
    ├── docker-compose.yml  → Configuração para subir NiFi e serviços relacionados
    └── volumes/
        └── drivers/        → Pasta para mapear drivers no container Docker
