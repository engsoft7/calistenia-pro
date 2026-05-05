# 💪 CALISTENIA PRO

> **App completo de treino calistênico para treinar em casa — sem equipamentos, sem academia.**

![Banner](https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=900&h=300&fit=crop&q=80)

---

## 📱 Demo

Abra o `index.html` no navegador do celular e adicione à tela inicial para usar como app.

---

## ✨ Funcionalidades

### 🏠 Tela Inicial
- Dashboard com **streak, treinos e kcal** queimadas
- **Treino do dia** com início rápido em 1 toque
- **Treinos rápidos** (Core, Upper Body, Leg Day, Cardio)
- Rastreador semanal de atividades

### 💪 Biblioteca de Exercícios (12 movimentos)
| Exercício | Categoria | Dificuldade | Músculos |
|-----------|-----------|-------------|----------|
| Flexão | Peito | Iniciante | Peitoral, Tríceps, Ombros |
| Agachamento | Pernas | Iniciante | Quadríceps, Glúteos |
| Barra Fixa | Costas | Avançado | Latíssimo, Bíceps |
| Prancha | Core | Iniciante | Core, Transverso |
| Burpee | Full Body | Intermediário | Full Body + Cardio |
| Afundo | Pernas | Iniciante | Quadríceps, Glúteos |
| Dips | Tríceps | Intermediário | Tríceps, Peitoral |
| Mountain Climber | Core | Intermediário | Core, Cardio |
| L-Sit | Core | Avançado | Core, Tríceps |
| Pistol Squat | Pernas | Avançado | Quadríceps, Equilíbrio |
| Handstand | Ombros | Avançado | Ombros, Core |
| Superman | Lombar | Iniciante | Lombar, Glúteos |

- ✅ **Imagens reais** de cada exercício (via Unsplash)
- ✅ Filtro por categoria
- ✅ Badge de dificuldade (Iniciante / Intermediário / Avançado)
- ✅ Músculos trabalhados com destaque colorido
- ✅ Instruções detalhadas de execução
- ✅ Dicas do coach
- ✅ Progressões (do mais fácil ao mais difícil)

### 📅 Programas Estruturados
| Programa | Duração | Frequência |
|----------|---------|------------|
| 🌱 Iniciante | 4 semanas | 3× por semana |
| 🔥 Intermediário | 6 semanas | 4× por semana |
| ⚡ Avançado | 8 semanas | 5× por semana |

### ⏱️ Treino Ativo
- Cronômetro em tempo real
- Controle de séries com barra de progresso visual
- **Timer de descanso** automático com barra de contagem
- Instrução do exercício na tela durante o treino
- Opção de pular descanso
- Tela de conclusão com resumo (tempo, exercícios, kcal)

### 📈 Progresso
- Streak de dias consecutivos
- Gráfico de atividade dos últimos 7 dias
- Barras de músculos mais trabalhados
- **8 conquistas** (achievements) desbloqueáveis
- Dados salvos no `localStorage` do navegador

---

## 🚀 Como Usar

### Opção 1 — Navegador (mais simples)
```bash
# Clone o repositório
git clone https://github.com/seu-usuario/calistenia-pro.git

# Abra o arquivo no navegador
open index.html
```

### Opção 2 — Servidor local
```bash
# Com Python
python3 -m http.server 8080

# Ou com Node.js
npx serve .

# Acesse: http://localhost:8080
```

### Opção 3 — Instalar no celular como app (PWA)
1. Abra o link no **Chrome para Android**
2. Toque no menu `⋮` → **"Adicionar à tela inicial"**
3. O app abre em tela cheia como um APK nativo ✅

### Opção 4 — Gerar APK real
Use o [PWA Builder](https://www.pwabuilder.com) (gratuito):
1. Acesse: https://www.pwabuilder.com
2. Cole a URL do seu app (hospedado no GitHub Pages, por exemplo)
3. Clique em **"Package for stores"** → Android
4. Baixe o `.apk` gerado 🎉

---

## 🌐 Deploy no GitHub Pages (Grátis)

```bash
# 1. Crie um repositório no GitHub
# 2. Faça push dos arquivos:
git init
git add .
git commit -m "🚀 Calistenia PRO - first commit"
git remote add origin https://github.com/SEU-USUARIO/calistenia-pro.git
git push -u origin main

# 3. Vá em Settings → Pages → Branch: main → Save
# 4. Acesse: https://SEU-USUARIO.github.io/calistenia-pro
```

---

## 📁 Estrutura do Projeto

```
calistenia-pro/
│
├── index.html       ← App completo (HTML + CSS + JS em um arquivo)
├── manifest.json    ← Configuração PWA (ícone, nome, cores)
└── README.md        ← Este arquivo
```

> **Design decision:** Toda a aplicação está em um único `index.html` para máxima portabilidade. Sem dependências externas além das fontes do Google.

---

## 🎨 Design

- **Dark theme** com tons de `#080810`
- **Accent color:** `#FF4500` (laranja vibrante)
- **Fontes:** Bebas Neue (títulos) + Barlow (texto)
- **Imagens reais** via Unsplash (carregam com internet)
- Layout **mobile-first**, otimizado para 375–430px de largura

---

## 🧱 Tecnologias

| Tech | Uso |
|------|-----|
| HTML5 | Estrutura |
| CSS3 | Estilização, animações, layout |
| JavaScript (Vanilla) | Lógica, estado, navegação |
| localStorage | Persistência dos dados de progresso |
| PWA (manifest.json) | Instalação no celular |
| Unsplash API | Imagens dos exercícios |
| Google Fonts | Bebas Neue + Barlow |

---

## 🔧 Personalização

### Adicionar exercícios
No `index.html`, localize o array `const EX = [...]` e adicione:
```javascript
{
  id: 13,
  name: 'Meu Exercício',
  cat: 'Core',              // Peito | Costas | Pernas | Core | Ombros | Tríceps | Full Body | Lombar
  diff: 'Iniciante',        // Iniciante | Intermediário | Avançado
  reps: '10–15',
  sets: 3,
  rest: 60,                 // segundos de descanso
  kcal: 7,                  // kcal por série
  img: 'https://sua-imagem.com/foto.jpg',
  muscles: ['Músculo 1', 'Músculo 2'],
  mc: ['#FF5722', '#6366F1'],  // cores dos músculos
  color: '#FF5722',
  desc: 'Descrição de como executar o exercício.',
  tips: ['Dica 1', 'Dica 2', 'Dica 3'],
  prog: ['Progressão 1', 'Progressão 2', 'Progressão 3']
}
```

### Criar um novo treino rápido
```javascript
const WORKOUTS = {
  // ...existentes...
  meuTreino: {
    name: 'Meu Treino',
    exIds: [1, 2, 4],  // IDs dos exercícios
    rest: 60           // segundos de descanso
  }
};
```

---

## 📸 Screenshots

| Home | Exercícios | Treino Ativo | Progresso |
|------|-----------|--------------|-----------|
| Dashboard com stats | Lista filtrada | Timer + séries | Gráficos + conquistas |

---

## 🗺️ Roadmap

- [ ] Exercícios com GIFs animados
- [ ] Cronômetro Tabata e AMRAP
- [ ] Planos personalizados pelo usuário
- [ ] Sincronização na nuvem (Firebase)
- [ ] Modo offline completo (Service Worker)
- [ ] Notificações de lembrete de treino
- [ ] Histórico detalhado por treino
- [ ] Compartilhar treino com amigos

---

## 📄 Licença

MIT License — use, modifique e distribua à vontade.

---

## 🙏 Créditos

- **Imagens:** [Unsplash](https://unsplash.com) (licença gratuita)
- **Fontes:** [Google Fonts](https://fonts.google.com)
- **Ícones:** Emojis nativos

---

<div align="center">

Feito com 💪 para quem treina em casa

**[⭐ Star no GitHub](https://github.com/seu-usuario/calistenia-pro)** · **[🌐 Ver Demo](https://seu-usuario.github.io/calistenia-pro)**

</div>
