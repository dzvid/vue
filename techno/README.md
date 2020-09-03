# Techno app

## Execute the fake API
- Run the fake API, install json-server: 
```bash
npm install -g json-server
```

- Execute the fake api (keep it running in a terminal window):
```bash
cd techno-api
json-server --watch api.json -p 3000
```
---
## Execute frontend in dev environment:
Execute the following steps in another terminal window.

- Install dependencies: 
```bash
cd techno-cursos
npm install
```

- Execute frontend in development mode:
```bash
npm run serve
```

- Now check the frontend at: `http://localhost:8080/`