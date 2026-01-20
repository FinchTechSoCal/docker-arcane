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
ARCENC=$(openssl rand -base64 32)
```

Generate a JWT secret:
```bash
ARCJWT=$(openssl rand -hex 32)
```


**Use**
```bash
rm -fr ~/appdata/docker_files/arcane
git clone https://github.com/FinchTechSoCal/docker-arcane.git ~/appdata/docker_files/arcane
```


**Modify .env**
```bash
sed -i 's;your_own_encryption_key;'$ARCENC';g' ~/appdata/docker_files/arcane/.env
sed -i 's;your_own_jwt_secret;'$ARCJWT';g' ~/appdata/docker_files/arcane/.env
sed -i 's;/path/to/appdata/;'$HOME'/appdata/;g' ~/appdata/docker_files/arcane/.env
nano ~/appdata/docker_files/arcane/.env
```

**Run**
```bash
docker compose -f ~/appdata/docker_files/arcane/docker-compose.yml up -d
```

---

## OIDC
* Issuer URL: https://accounts.google.com
* Scopes: openid email profile
* Admin Claim: email
* Requires Value(s): <your gmail address>