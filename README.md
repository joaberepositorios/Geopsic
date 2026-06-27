# Geopsic — Geometria Analítica 3D em WebAR

Piloto de uma ferramenta **WebAR sem instalação** para ensino superior: visualiza
geometria analítica 3D (eixos, ponto/vetor, plano `ax+by+cz=d`) e a **cinemática de
projéteis como curva paramétrica** `x(t), y(t), z(t)`. Roda no navegador.

## Arquivos
- `index.html` — página inicial (descrição + marcador + acesso aos dois modos).
- `geometria.html` — visualizador **3D interativo** (Three.js). Funciona em qualquer aparelho, sem câmera. É o núcleo e o fallback.
- `ar.html` — **modo AR** (A-Frame + AR.js) com marcador Hiro.

## Como rodar localmente
A câmera (AR) e os módulos exigem servir por HTTP — não abra via `file://`.

```bash
# dentro da pasta do projeto:
python -m http.server 8000
# abra no PC:  http://localhost:8000
```
`localhost` é tratado como origem segura, então a câmera funciona no PC.

## Como testar no celular (recomendado para o piloto)
O celular precisa de **HTTPS**. Caminho mais fácil — deploy grátis:

- **Vercel:** `npm i -g vercel` → `vercel` (na pasta) → gera uma URL `https://...`.
- **ou GitHub Pages:** suba os arquivos num repositório → Settings → Pages → branch `main`.

Depois abra a URL no celular (ou gere um QR da URL) e:
1. **Modo AR** → permita a câmera → aponte para o **marcador Hiro** (mostre `index.html` em outra tela ou imprima).
2. Os eixos e o projétil aparecem sobre o marcador; ajuste `v₀`, `θ`, `φ`.

> Dica: WebXR de AR não funciona no iOS; por isso usamos **AR.js com marcador**, que roda no navegador de Android **e** iOS.

## Protocolo do piloto (para o artigo)
- **Participantes:** 5–8 estudantes de ensino superior (presencial).
- **Fluxo:** pré-teste (3–4 questões de geometria 3D / projétil) → uso livre ~10 min → pós-teste (questões equivalentes) → **SUS** (10 itens) + 2 itens Likert (“ajudou a entender?”).
- **Métricas:** nota SUS (0–100), ganho pré→pós, comentários abertos.
- **Limitação (declarar):** amostra pequena → resultado é **indício**, não prova. Estudo controlado maior = trabalho futuro.

## Tópicos no SVR
Sistemas/frameworks/kits VR/AR/MR · Jogos sérios / educação · Estudos e avaliação de usuários.
