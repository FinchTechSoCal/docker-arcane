> [!IMPORTANT]
> Arcane: `ghcr.io/getarcaneapp/arcane`
>
> Arcane Agent: `ghcr.io/getarcaneapp/arcane-headless`

<div align="center">

  <img src="https://github.com/getarcaneapp/arcane/blob/main/.github/assets/img/PNG-3.png" alt="Arcane Logo" width="500" />
  <p>Modern Docker Management, Designed for Everyone.</p>

</div>

<br />
---

Generate an encryption key:
```bash
openssl rand -base64 32
```

Generate a JWT secret:
```bash
openssl rand -hex 32
```


**Use**
```bash
rm -fr ~/appdata/docker_files/arcane
git clone https://github.com/FinchTechSoCal/docker-arcane.git ~/appdata/docker_files/arcane
```

**Modify .env**
```bash
nano ~/appdata/docker_files/arcane/.env
```

**Run**
```bash
docker compose -f ~/appdata/docker_files/arcane/docker-compose.yml up -d
```