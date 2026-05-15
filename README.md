# Mapa de Inserção Regional — PPGSND/UFOPA

Mapa interativo das teses e dissertações do PPGSND.

🔗 **Acesse em:** https://ahminervino-sketch.github.io/ppgsnd-mapa/

---

## Como adicionar projetos

Edite apenas o arquivo **`projetos.json`** pelo GitHub:

1. Acesse https://github.com/ahminervino-sketch/ppgsnd-mapa
2. Clique em `projetos.json`
3. Clique no ícone ✏️ (Edit)
4. Adicione um bloco seguindo o modelo abaixo
5. Clique em **Commit changes**
6. Aguarde ~1 minuto — o mapa atualiza sozinho

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
  "cor": "#1D9E75",
  "desc": "Resumo curto (2-3 frases).",
  "bbox": [-56.0, -4.0, -54.0, -2.0]
}
```

### Categorias (`cat`) e comportamento do mapa

| Valor | Descrição | Zoom do mapa |
|-------|-----------|--------------|
| `"local"` | Município | América do Sul |
| `"amazonia"` | Região amazônica | América do Sul |
| `"nacional"` | Outras regiões do Brasil | América do Sul |
| `"internacional"` | Fora do Brasil | Mundo inteiro |

### Cores sugeridas

| Cor | Código |
|-----|--------|
| Verde (Amazônia) | `#1D9E75` |
| Roxo (Local) | `#7C5CBF` |
| Laranja (Nacional) | `#e76f51` |
| Azul (Internacional) | `#457b9d` |

### Como encontrar as coordenadas (`bbox`)

Acesse https://boundingbox.klokantech.com, desenhe um retângulo sobre a área e copie no formato CSV.
A ordem é: `[lon_oeste, lat_sul, lon_leste, lat_norte]`

Ou pergunte ao Claude: *"Quais as coordenadas de bounding box para [área de estudo]?"*

---

## Arquivos

```
ppgsnd-mapa/
├── index.html      ← aplicação (não editar)
├── world.json      ← dados geográficos (não editar)
├── projetos.json   ← EDITE AQUI para adicionar teses
└── README.md       ← instruções
```
