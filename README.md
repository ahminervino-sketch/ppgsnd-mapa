# Mapa de Inserção Regional — PPGSND/UFOPA

Mapa interativo das teses e dissertações do PPGSND, com zoom automático para a área geográfica de cada pesquisa.

🔗 **Acesse em:** https://ahminervino-sketch.github.io/ppgsnd-mapa/

---

## Como adicionar ou editar projetos

Você não precisa mexer no código. Só edite o arquivo **`projetos.json`**.

### Passo a passo no GitHub:

1. Acesse o repositório: https://github.com/ahminervino-sketch/ppgsnd-mapa
2. Clique no arquivo `projetos.json`
3. Clique no ícone de lápis (✏️ Edit this file)
4. Adicione um novo bloco seguindo o modelo abaixo
5. Clique em **Commit changes** → **Commit changes** (verde)
6. Aguarde ~1 minuto e o mapa atualiza automaticamente

---

## Modelo de projeto

```json
{
  "id": 6,
  "titulo": "Título da tese ou dissertação",
  "autor": "Nome do Autor",
  "ano": 2025,
  "tipo": "Tese",
  "cat": "amazonia",
  "cor": "#1D9E75",
  "desc": "Resumo curto da pesquisa (2-3 frases).",
  "bbox": [-56.0, -4.0, -54.0, -2.0]
}
```

### Campos obrigatórios

| Campo | Descrição |
|-------|-----------|
| `id` | Número único — sempre incrementar o último |
| `titulo` | Título completo |
| `autor` | Nome do autor/a |
| `ano` | Ano de defesa |
| `tipo` | `"Tese"` ou `"Dissertação"` |
| `cat` | Categoria — ver opções abaixo |
| `cor` | Cor da mancha no mapa — ver paleta abaixo |
| `desc` | Descrição curta (aparece ao clicar) |
| `bbox` | Coordenadas da área: `[lon_oeste, lat_sul, lon_leste, lat_norte]` |

### Categorias (`cat`)

| Valor | Descrição |
|-------|-----------|
| `"local"` | Município ou área restrita |
| `"amazonia"` | Região amazônica |
| `"nacional"` | Outras regiões do Brasil |
| `"internacional"` | Fora do Brasil |

### Cores sugeridas (`cor`)

| Cor | Código | Uso |
|-----|--------|-----|
| Verde | `#1D9E75` | Amazônia (padrão) |
| Roxo | `#534AB7` | Local/Municipal |
| Laranja | `#993C1D` | Nacional |
| Azul | `#185FA5` | Internacional |

---

## Como encontrar as coordenadas (`bbox`)

1. Acesse https://boundingbox.klokantech.com
2. Desenhe um retângulo sobre a área de estudo
3. No campo "Copy & Paste", selecione **CSV**
4. A ordem é: `lon_oeste, lat_sul, lon_leste, lat_norte`

Ou peça ao Claude: *"Quais são as coordenadas de bounding box para [área de estudo]?"*

---

## Estrutura do repositório

```
ppgsnd-mapa/
├── index.html       ← aplicação do mapa (não editar)
├── world.json       ← dados geográficos do mundo (não editar)
├── projetos.json    ← lista de teses — EDITE AQUI
└── README.md        ← este arquivo
```

---

## Transferir para repositório institucional

Quando quiser mover para uma conta institucional da UFOPA:
1. Crie um repositório novo na conta institucional
2. Copie os 4 arquivos
3. Ative o GitHub Pages (Settings → Pages → main branch)
4. A nova URL será `https://[conta-ufopa].github.io/ppgsnd-mapa/`
