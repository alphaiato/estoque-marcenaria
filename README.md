# Sistema de Controle de Estoque - Marcenaria

Sistema completo de controle de estoque para marcenaria desenvolvido em HTML, CSS e JavaScript puro. Agora com suporte a **Firebase Firestore** para persistência de dados na nuvem e hospedagem no **GitHub Pages**.

## 🚀 Funcionalidades

- **Dashboard** com visão geral e gráficos
- **Gerenciamento de Ferramentas** com controle de condição e empréstimos
- **Controle de Materiais** com fornecedores e ajustes de estoque
- **Gestão de Produtos** com datas de validade
- **Sistema de Usuários** com permissões (Admin/Usuário)
- **Logs de Movimentações** completos
- **Previsões IA** para compras automáticas
- **Assinatura Digital** para empréstimos de ferramentas
- **Interface Responsiva** para desktop e mobile
- **Sincronização na Nuvem** com Firebase Firestore

## 📱 Como Usar

### Opção 1: Local (Sem Firebase)
1. **Acesse:** Abra o arquivo `index.html` em qualquer navegador moderno
2. **Login:** Use usuário `admin` e senha `admin`
3. **Explore:** Navegue pelas abas para gerenciar seu estoque

### Opção 2: Com Firebase (Dados na Nuvem)
1. **Configure o Firebase** (veja instruções abaixo)
2. **Acesse:** Abra o arquivo `index.html` em qualquer navegador
3. **Login:** Use usuário `admin` e senha `admin`
4. **Dados Sincronizados:** Todas as alterações são salvas automaticamente na nuvem

## � Configuração do Firebase (Opcional)

Para usar persistência de dados na nuvem:

### 1. Criar Projeto no Firebase
1. Acesse [Firebase Console](https://console.firebase.google.com/)
2. Clique em "Criar um projeto" ou "Add project"
3. Dê um nome ao projeto (ex: "estoque-marcenaria")
4. Siga os passos para criar o projeto

### 2. Configurar Firestore
1. No menu lateral, clique em "Firestore Database"
2. Clique em "Criar banco de dados"
3. Escolha "Iniciar no modo de produção" ou "Iniciar no modo de teste"
4. Selecione uma localização para o banco de dados

### 3. Obter Configuração do Firebase
1. Clique no ícone de engrenagem (Configurações do projeto)
2. Vá para "Configurações gerais"
3. Role para baixo até "Seus apps"
4. Clique em "Adicionar app" > Web app (</>)
5. Registre o app com um nome (ex: "Estoque Web")
6. Copie a configuração JavaScript

### 4. Atualizar o Código
1. Abra o arquivo `index.html`
2. Localize a seção de configuração do Firebase (linha ~15)
3. Substitua os valores placeholder pelos seus dados reais:

```javascript
const firebaseConfig = {
    apiKey: "SUA_API_KEY_AQUI",
    authDomain: "SEU_PROJETO.firebaseapp.com",
    projectId: "SEU_PROJECT_ID",
    storageBucket: "SEU_PROJETO.appspot.com",
    messagingSenderId: "SEU_SENDER_ID",
    appId: "SEU_APP_ID"
};
```

### 5. Configurar Regras de Segurança (Opcional)
Para produção, configure as regras do Firestore no Console do Firebase:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    // Permitir leitura/escrita para usuários autenticados
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

## 🌐 Hospedagem no GitHub Pages

### 1. Criar Repositório no GitHub
1. Acesse [GitHub](https://github.com) e faça login
2. Clique em "New repository"
3. Dê um nome (ex: "estoque-marcenaria")
4. Deixe público ou privado
5. **Não** inicialize com README, .gitignore ou license
6. Clique em "Create repository"

### 2. Fazer Upload dos Arquivos
1. No repositório criado, clique em "uploading an existing file"
2. Arraste os arquivos `index.html` e `README.md` para a área de upload
3. Clique em "Commit changes"

### 3. Ativar GitHub Pages
1. Vá para "Settings" do repositório
2. No menu lateral, clique em "Pages"
3. Em "Source", selecione "Deploy from a branch"
4. Em "Branch", selecione "main" e "/ (root)"
5. Clique em "Save"

### 4. Acessar o Site
- Aguarde alguns minutos para o deploy
- O site estará disponível em: `https://SEU_USUARIO.github.io/NOME_DO_REPOSITORIO`
- Exemplo: `https://johndoe.github.io/estoque-marcenaria`

## 💾 Persistência de Dados

### Local (Padrão)
- Dados salvos no **localStorage** do navegador
- Funciona **offline** após carregamento inicial
- Dados ficam no dispositivo do usuário

### Nuvem (Com Firebase)
- Dados salvos no **Firebase Firestore**
- **Sincronização automática** entre dispositivos
- **Backup na nuvem** - dados seguros e acessíveis
- Funciona **online** - requer conexão para salvar

## 🌐 Compatibilidade

- ✅ **Desktop:** Windows, macOS, Linux
- ✅ **Mobile:** Android, iOS
- ✅ **Navegadores:** Chrome, Firefox, Edge, Safari
- ✅ **Offline:** Funciona sem internet (modo local)
- ✅ **Online:** Sincronização na nuvem (com Firebase)

## 🛠️ Tecnologias

- **HTML5** - Estrutura
- **CSS3** - Estilos responsivos
- **JavaScript ES6+** - Lógica e interatividade
- **Firebase Firestore** - Banco de dados na nuvem
- **Chart.js** - Gráficos
- **Signature Pad** - Assinaturas digitais
- **LocalStorage** - Persistência local

## 📊 Recursos Avançados

- **Dashboard Interativo** com estatísticas em tempo real
- **Sistema de Empréstimos** com cautelas digitais
- **Controle de Validade** de produtos
- **Relatórios de Logs** filtráveis por data e usuário
- **Previsões Inteligentes** baseadas em padrões de consumo
- **Interface Multi-idioma** (Português Brasil)
- **Sincronização Multi-dispositivo** (com Firebase)

## 🔒 Segurança

- Sistema de autenticação
- Controle de permissões por usuário
- Logs completos de todas as ações
- Dados criptografados (localStorage/Firebase)
- Regras de segurança configuráveis no Firebase

## 🆘 Suporte

- **Modo Local:** Funciona sem configuração adicional
- **Modo Firebase:** Configure apenas se precisar de sincronização na nuvem
- **GitHub Pages:** Hospedagem gratuita e ilimitada
- **Compatibilidade:** Testado em todos os navegadores modernos

---

**Desenvolvido para marcenarias que precisam de controle eficiente de estoque, tanto local quanto na nuvem.**
