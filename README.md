# Mapa de Inserção Regional — PPGSND/UFOPA

Mapa interativo das teses e dissertações do PPGSND, usando Mapbox GL JS.

🔗 **Acesse em:** https://ahminervino-sketch.github.io/ppgsnd-mapa/

---

## Como adicionar projetos

Edite apenas o arquivo **`projetos.json`** pelo GitHub:

1. Acesse https://github.com/ahminervino-sketch/ppgsnd-mapa
2. Clique em `projetos.json` → ✏️ Edit
3. Adicione um bloco seguindo o modelo abaixo
4. **Commit changes** — o mapa atualiza em ~1 minuto

---

## Modelo de projeto

```json
{
  "id": 6,
  "titulo": "Título da tese",
  "autor": "Nome do Autor",
  "ano": 2025,
  "tipo": "Tese",
  "cat": "amazonia",
  "cor": "#2a9d8f",
  "desc": "Resumo curto (2-3 frases).",
  "bbox": [-56.0, -4.0, -54.0, -2.0]
}
```

### Categorias e zoom do mapa

| `cat` | Zoom |
|-------|------|
| `"local"` | América do Sul |
| `"amazonia"` | América do Sul |
| `"nacional"` | América do Sul |
| `"internacional"` | Mundo inteiro |

### Cores sugeridas

| Categoria | Cor |
|-----------|-----|
| Local | `#7b61c9` |
| Amazônia | `#2a9d8f` |
| Nacional | `#e76f51` |
| Internacional | `#457b9d` |

### Coordenadas (`bbox`)

Acesse https://boundingbox.klokantech.com, desenhe a área e copie no formato CSV.
Ordem: `[lon_oeste, lat_sul, lon_leste, lat_norte]`

---

## Arquivos

```
ppgsnd-mapa/
├── index.html      ← aplicação (não editar)
├── projetos.json   ← EDITE AQUI
└── README.md       ← instruções
```
