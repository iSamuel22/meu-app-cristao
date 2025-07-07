# 📱 MeuAppCristao

Um aplicativo Flutter completo para auxiliar a vida devocional cristã, oferecendo ferramentas para gerenciar pedidos de oração, devocionais pessoais e acompanhar o progresso de leitura bíblica.

## 🌟 Funcionalidades

### 📿 **Pedidos de Oração**
- ✅ Adicionar, editar e excluir pedidos de oração
- ✅ Marcar pedidos como respondidos
- ✅ Visualização completa de textos longos
- ✅ Data de criação automática
- ✅ Exclusão em lote (todos os pedidos)

### 📖 **Devocionais**
- ✅ Criar devocionais personalizados com título e conteúdo
- ✅ Editar e excluir devocionais
- ✅ Visualização expandida para textos longos
- ✅ Histórico com data de criação
- ✅ Gerenciamento completo de conteúdo

### 📚 **Progresso de Leitura Bíblica**
- ✅ Acompanhar leitura por livro e capítulo
- ✅ Organização por Antigo e Novo Testamento
- ✅ Visualização de versículos por capítulo
- ✅ Marcar capítulos como lidos
- ✅ Barra de progresso por livro
- ✅ Indicadores visuais de progresso

## 🛠️ Tecnologias Utilizadas

### **Framework e Linguagem**
- **Flutter** 3.x
- **Dart** 3.x

### **Backend e Banco de Dados**
- **Firebase Firestore** - Banco de dados em tempo real
- **Firebase Core** - Configuração base

### **Packages**
- `cloud_firestore` - Integração com Firestore
- `firebase_core` - Configuração Firebase
- `intl` - Formatação de datas em português
- `http` - Requisições HTTP para API bíblica

## 🏗️ Arquitetura do Projeto

```
lib/
├── database/
│   ├── database.dart             # Classes de acesso ao Firestore
│   └── firebase_options.dart     # Configurações do Firebase
├── models/
│   └── models.dart               # Modelos de dados
├── services/
│   └── biblia_service.dart       # Serviço para API bíblica
├── doc/
│   └── especificacao.pdf         # Especificação do projeto - Professor Foly
│   └── info.txt                  # Algumas informações
│   └── uso_componentes.txt       # Documentação de componentes
├── main.dart                     # Arquivo principal
├── tela_oracao.dart              # Tela de pedidos de oração
├── tela_devocional.dart          # Tela de devocionais
└── tela_progresso_leitura.dart   # Tela de progresso bíblico
```

## 📋 Pré-requisitos

- **Flutter SDK** 3.0+
- **Dart SDK** 3.0+
- **Android Studio** ou **VS Code**
- **Projeto Firebase** configurado

## 🚀 Instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/seu-usuario/meuAppCristao.git
cd meuAppCristao
```

2. **Instale as dependências:**
```bash
flutter pub get
```

3. **Configure o Firebase:**
   - Crie um projeto no [Firebase Console](https://console.firebase.google.com/)
   - Adicione um app Android/iOS
   - Baixe o arquivo `google-services.json` (Android) ou `GoogleService-Info.plist` (iOS)
   - Coloque na pasta apropriada do projeto

4. **Execute o aplicativo:**
```bash
flutter run
```

## 🎨 Componentes Flutter Utilizados

### **📚 Componentes Básicos**
- `MaterialApp`, `Scaffold`, `AppBar`
- `Column`, `Row`, `Container`, `Padding`
- `ListView.builder`, `Card`, `ListTile`
- `TextField`, `TextFormField`, `ElevatedButton`
- `AlertDialog`, `SnackBar`

### **🆕 Componentes Avançados**
- `TabBar` + `TabBarView` - Navegação por abas
- `ExpansionTile` - Listas expansíveis
- `PopupMenuButton` - Menus contextuais
- `CircularProgressIndicator` - Indicadores de loading
- `GestureDetector` - Detecção de gestos
- `SingleChildScrollView` - Scroll em dialogs

## 📊 Estrutura de Dados

### **Pedido de Oração**
```dart
class PedidoOracao {
  String texto;
  bool respondido;
  Timestamp criadoEm;
}
```

### **Devocional**
```dart
class Devocional {
  String titulo;
  String conteudo;
  Timestamp criadoEm;
}
```

## 🔥 Funcionalidades do Firebase

### **Firestore Collections:**
- `pedidos_oracao` - Armazena pedidos de oração
- `devocionais` - Armazena devocionais pessoais
- `progresso_leitura` - Armazena progresso de leitura bíblica

### **Operações Implementadas:**
- ✅ **Create** - Adicionar novos registros
- ✅ **Read** - Listar e visualizar dados
- ✅ **Update** - Editar registros existentes
- ✅ **Delete** - Excluir registros individuais ou em lote

## 📱 Interface do Usuário

### **🎨 Tema Personalizado**
- Cor primária: `Colors.indigo`
- Fundo: `Colors.indigo.shade50`
- Botões com cantos arredondados
- Cards com sombra e bordas suaves

### **🔄 Navegação**
- `BottomNavigationBar` com 3 abas
- Transições suaves entre telas
- Dialogs modais para edição

### **📊 Indicadores Visuais**
- Progresso de leitura com `LinearProgressIndicator`
- Estados visuais (lido/não lido)
- Timestamps formatados em português

## 🌐 API Externa

### **Bíblia Online**
- **URL Base:** `https://www.abibliadigital.com.br/api`
- **Endpoints:**
  - `/books` - Lista de livros bíblicos
  - `/verses/{versao}/{livro}/{capitulo}` - Versículos por capítulo

## 🔧 Configuração do Ambiente

### **pubspec.yaml**
```yaml
dependencies:
  flutter:
    sdk: flutter

  cupertino_icons: ^1.0.8
  firebase_core: ^3.14.0
  cloud_firestore: ^5.6.9
  http: ^1.1.0
  shared_preferences: ^2.2.2
  intl: ^0.18.1


dev_dependencies:
  flutter_test:
    sdk: flutter

   flutter_lints: ^5.0.0
```

## 🚀 Build e Deploy

### **Build APK:**
```bash
flutter build apk --release
```

### **Build App Bundle:**
```bash
flutter build appbundle --release
```

## 📝 Funcionalidades Futuras

- [ ] Notificações push para lembretes
- [ ] Backup automático na nuvem
- [ ] Compartilhamento de devocionais
- [ ] Temas claro/escuro
- [ ] Sincronização offline
- [ ] Grupos de oração
- [ ] Planos de leitura bíblica

## 🤝 Contribuindo

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/NovaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/NovaFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👨‍💻 Autor

**Programadores**
- GitHub: [@iSamuel22](https://github.com/iSamuel22)
- Email: samueljubim47@gmail.com
- GitHub: [@LucasPaschoal](https://github.com/LucasPaschoal)
- Email: lucaspaschoal@gmail.com

## 🙏 Agradecimentos

- **Firebase** - Pela plataforma robusta
- **Flutter Team** - Pelo framework excepcional
- **A Bíblia Digital** - Pela API bíblica gratuita
- **Comunidade Flutter** - Pelo suporte e documentação

---

## 📸 Screenshots

### Tela de Pedidos de Oração
![Pedidos de Oração](screenshots/oracao.png)

### Tela de Devocionais
![Devocionais](screenshots/devocionais.png)

### Tela de Progresso Bíblico
![Progresso Bíblico](screenshots/progresso.png)

---

**Feito com ❤️ e Flutter para a glória de Deus**
