# 🎼 Gerador de Partituras Musicais

Uma aplicação web profissional para criar, editar e exportar partituras musicais com interface intuitiva e recursos avançados.

## 🌟 Características Principais

### ✅ Funcionalidades Completas
- **Interface Visual Intuitiva** - Canvas interativo para criação de partituras
- **Elementos Musicais Completos** - Notas, pausas, claves, assinaturas e alterações
- **Editor Interativo** - Arrastar e soltar, seleção múltipla, edição precisa
- **Playback de Áudio** - Toca as partituras criadas com síntese sonora
- **Exportação PDF** - Gera arquivos PDF profissionais das partituras
- **Salvamento Local** - Auto-save e persistência no navegador

### 🎵 Elementos Musicais Suportados
- **Claves**: Sol (Treble), Fá (Bass), Dó (Alto)
- **Notas**: Semínima, Mínima, Colcheia, Semicolcheia, Fusa
- **Pausas**: Todas as durações equivalentes
- **Alterações**: Sustenido (#), Bemol (b), Bequadro (♮)
- **Compassos**: 4/4, 3/4, 2/4, 6/8 e personalizados

### 🎨 Design Avançado
- **Design Responsivo** - Adaptável a todos os dispositivos
- **Tema Claro/Escuro** - Suporte a preferências do sistema
- **Interface Musical Temática** - Cores e estética musical
- **Animações Suaves** - Transições fluidas e feedback visual
- **Acessibilidade WCAG 2.1 AA** - Compatível com leitores de tela

### ⚡ Performance e Tecnologia
- **Web Audio API** - Síntese sonora de alta qualidade
- **Canvas 2D** - Renderização vetorial de precisão
- **ES6+ Modules** - Código moderno e modular
- **LocalStorage API** - Persistência local de dados
- **CSS Grid/Flexbox** - Layout moderno e eficiente

## 🚀 Começando

### Requisitos
- Navegador moderno (Chrome 80+, Firefox 75+, Safari 13+, Edge 80+)
- JavaScript habilitado
- Conexão com internet (para carregamento inicial)

### Instalação
1. Clone o repositório ou baixe os arquivos
2. Abra o arquivo `index.html` em seu navegador
3. Comece a criar música!

### Uso Básico
```javascript
// A aplicação inicia automaticamente ao carregar a página
// Acesse através de: window.scoreApp

// Obter status da aplicação
window.getAppStatus()

// Testar notificação
window.testNotification('Olá Músico!', 'success')
```

## 📖 Documentação de Uso

### Interface Principal

#### Toolbar Lateral
- **Claves**: Selecione o tipo de clave (Sol, Fá, Dó)
- **Notas**: Escolha a duração das notas a inserir
- **Pausas**: Insira pausas de diferentes durações
- **Alterações**: Adicione sustenidos, bemóis e bequadros
- **Compasso**: Defina a assinatura de compasso
- **Ferramentas**: Selecione, apague ou mova elementos

#### Área de Edição
- **Canvas Principal**: Clique para adicionar notas
- **Arrastar**: Segure e arraste para mover elementos
- **Zoom**: Use os controles de zoom para aproximar/afastar
- **Playback**: Clique em "Tocar" para ouvir a partitura

#### Barra Superior
- **Nova**: Cria uma nova partitura
- **Salvar**: Exporta a partitura como JSON
- **PDF**: Gera um PDF da partitura
- **Tocar/Parar**: Controla o playback de áudio

### Atalhos de Teclado
| Tecla | Ação |
|-------|------|
| `Ctrl+S` | Salvar partitura |
| `Ctrl+P` | Exportar PDF |
| `Espaço` | Tocar/Parar |
| `Delete` | Apagar seleção |
| `1-5` | Selecionar tipo de nota |
| `S` | Sustenido |
| `F` | Bemol |
| `N` | Bequadro |
| `Esc` | Limpar seleção |

### Trabalhando com Elementos

#### Adicionar Notas
1. Selecione o tipo de nota desejado na toolbar
2. Clique na posição desejada no canvas
3. A nota será inserida automaticamente

#### Mover Elementos
1. Selecione a ferramenta "Mover"
2. Clique e arraste o elemento desejado
3. Solte para posicionar

#### Editar Propriedades
1. Clique em um elemento para selecioná-lo
2. Use as ferramentas de alteração para modificar
3. As mudanças são aplicadas instantaneamente

## 🎯 Exemplos de Uso

### Criar uma Melodia Simples
```javascript
// A aplicação cria automaticamente uma estrutura básica
// Adicione notas clicando no canvas
// O sistema automaticamente:
// - Ajusta a altura das notas baseado na posição Y
// - Define a duração baseado na seleção atual
// - Alinha ao compasso atual
```

### Exportar para PDF
```javascript
// Clique no botão "PDF" na barra superior
// Ou use o atalho Ctrl+P
// O PDF será gerado com:
// - Alta resolução (300 DPI)
// - Fundo branco limpo
// - Elementos musicais vetoriais
// - Título e compositor
```

### Tocar a Partitura
```javascript
// Clique no botão "Tocar"
// A aplicação irá:
// - Sintetizar cada nota
// - Respeitar os tempos e durações
// - Usar timbre de piano padrão
// - Aplicar o andamento (BPM) configurado
```

## 🛠️ Desenvolvimento

### Estrutura de Arquivos
```
index.html              # Página principal
├── css/
│   ├── style.css       # Estilos principais
│   └── responsive.css  # Estilos responsivos
├── js/
│   ├── app.js          # Aplicação principal
│   ├── musicTheory.js  # Teoria musical
│   ├── scoreRenderer.js # Renderizador de partituras
│   ├── scoreEditor.js   # Editor interativo
│   └── audioPlayer.js   # Player de áudio
└── README.md          # Documentação
```

### Arquitetura
```
┌─────────────────────────────────────┐
│         Aplicação Principal       │
│  ┌───────────────────────────────┐  │
│  │     ScoreGeneratorApp        │  │
│  └─────────────┬───────────────┘  │
│                │                   │
│  ┌─────────────┴───────────────┐  │
│  │        ScoreEditor           │  │
│  ├─────────────────────────────┤  │
│  │      ScoreRenderer          │  │
│  ├─────────────────────────────┤  │
│  │      AudioPlayer            │  │
│  ├─────────────────────────────┤  │
│  │      MusicTheory            │  │
│  └─────────────────────────────┘  │
└─────────────────────────────────────┘
```

### APIs Utilizadas
- **Web Audio API** - Síntese e processamento de áudio
- **Canvas 2D API** - Renderização gráfica vetorial
- **LocalStorage API** - Persistência local de dados
- **File API** - Importação/exportação de arquivos
- **Media Queries** - Design responsivo

### Compatibilidade
- **Chrome 80+**: ✓ Completo
- **Firefox 75+**: ✓ Completo
- **Safari 13+**: ✓ Completo
- **Edge 80+**: ✓ Completo
- **Mobile**: ✓ Adaptado

## 🎨 Customização

### Temas de Cor
```css
:root {
    --color-primary: #2563eb;           /* Azul principal */
    --color-secondary: #64748b;       /* Cinza secundário */
    --color-bg-primary: #ffffff;      /* Fundo principal */
    --color-text-primary: #1e293b;    /* Texto principal */
    --color-staff-lines: #334155;   /* Linhas da pauta */
    --color-note-head: #1e293b;     /* Cabeça da nota */
}
```

### Configurações de Renderização
```javascript
const config = {
    staffLineSpacing: 10,      // Espaçamento entre linhas
    noteHeadRadius: 4,         // Raio da cabeça da nota
    noteStemWidth: 2,          // Largura da haste
    clefSize: 40,              // Tamanho da clave
    measureWidth: 200,        // Largura do compasso
    zoom: 1.0                  // Zoom inicial
};
```

### Configurações de Áudio
```javascript
const audioConfig = {
    masterVolume: 0.5,         // Volume mestre (0-1)
    waveform: 'sine',          // Forma de onda
    attackTime: 0.01,         // Tempo de ataque
    decayTime: 0.1,           // Tempo de decaimento
    sustainLevel: 0.7,        // Nível de sustain
    releaseTime: 0.3          // Tempo de release
};
```

## 🔧 Suporte e Troubleshooting

### Problemas Comuns

#### Canvas não renderiza
- Verifique se o navegador suporta Canvas 2D
- Limpe o cache do navegador
- Verifique o console por erros JavaScript

#### Áudio não funciona
- Verifique as permissões de áudio do navegador
- Certifique-se de interagir com a página antes de tocar
- Verifique se o Web Audio API é suportado

#### Exportação PDF falha
- Verifique se jsPDF está carregado
- Tente reduzir a qualidade da imagem
- Verifique o console por erros

#### Dados não salvam
- Verifique se LocalStorage está habilitado
- Verifique o limite de armazenamento
- Tente limpar os dados salvos

### Debug e Desenvolvimento
```javascript
// Obter status da aplicação
window.getAppStatus()

// Testar notificação
window.testNotification('Mensagem', 'success')

// Forçar atualização da UI
window.forceUIUpdate()

// Acessar componentes individualmente
window.scoreApp.audioPlayer
window.scoreApp.editor
window.scoreApp.renderer
```

## 📚 Recursos Adicionais

### Teoria Musical
- **Notas e Escalas**: Implementação completa de notas cromáticas
- **Intervalos**: Cálculo de distâncias entre notas
- **Acordes**: Criação de tríades e tétrades
- **Compassos**: Suporte a várias assinaturas de compasso

### Recursos Técnicos
- **Performance**: Otimizado para 60fps
- **Acessibilidade**: Suporte a leitores de tela e navegação por teclado
- **Internacionalização**: Suporte a múltiplos idiomas
- **Modularidade**: Código organizado em módulos ES6+

## 🤝 Contribuindo

### Estrutura de Desenvolvimento
1. **Fork** o repositório
2. **Clone** seu fork localmente
3. **Crie** uma branch para sua feature
4. **Commit** suas mudanças
5. **Push** para sua branch
6. **Abra** um Pull Request

### Diretrizes de Código
- Use **ES6+** e módulos JavaScript
- Siga o padrão **BEM** para CSS
- Mantenha **compatibilidade cross-browser**
- **Documente** funções complexas
- **Teste** em dispositivos móveis

### Padrões de Código
```javascript
// Use const/let em vez de var
const myVariable = 'value';

// Use arrow functions para callbacks
const myFunction = (param) => {
    return param * 2;
};

// Use template literals
const message = `Hello ${name}`;

// Use destructuring
const { x, y } = coordinates;
```

## 📄 Licença

Este projeto é licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## 🙏 Agradecimentos

- **Web Audio API** - Para síntese sonora de alta qualidade
- **Canvas 2D API** - Para renderização gráfica
- **Font Awesome** - Para ícones consistentes
- **Google Fonts** - Para tipografia de qualidade
- **jsPDF** - Para exportação PDF

## 📞 Suporte

Para suporte, abra uma issue no repositório ou entre em contato através das informações fornecidas.

---

**Desenvolvido com ❤️ por Arquiteto Web Sênior**  
*Criando experiências musicais na web*# gera-partitura
