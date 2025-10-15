Título do Projeto:
📱 Piscicultura App — Gerenciamento Inteligente de Tanques e Lotes

Descrição para a IA (Cursor):

Crie um aplicativo completo de Piscicultura usando React Native com Expo.
O app deve rodar localmente com o comando npx expo start e ter uma estrutura organizada conforme o modelo abaixo.
O objetivo é permitir que piscicultores gerenciem tanques, lotes, alimentação, qualidade da água, biometria dos peixes e relatórios de desempenho.
⚙️ Estrutura de pastas
piscicultura-app/
├── App.js
├── firebaseConfig.js
├── app.json
├── package.json
├── babel.config.js
└── src/
    ├── navigation/
    │   ├── AppNavigator.js
    │   └── AuthNavigator.js
    ├── screens/
    │   ├── Auth/
    │   │   ├── LoginScreen.js
    │   │   └── RegisterScreen.js
    │   ├── Dashboard/
    │   │   ├── DashboardScreen.js
    │   │   ├── AlertsScreen.js
    │   │   └── ReportsScreen.js
    │   ├── Tanks/
    │   │   ├── TanksScreen.js
    │   │   └── AddTankScreen.js
    │   ├── Lots/
    │   │   ├── LotsScreen.js
    │   │   ├── AddLotScreen.js
    │   │   └── LotDetailScreen.js
    │   ├── Records/
    │   │   ├── WaterQualityScreen.js
    │   │   ├── FeedingScreen.js
    │   │   └── BiometricsScreen.js
    │   └── Settings/
    │       ├── ProfileScreen.js
    │       └── SettingsScreen.js
    ├── components/
    │   ├── TankCard.js
    │   ├── LotCard.js
    │   ├── StatCard.js
    │   └── DataChart.js
    ├── utils/
    │   ├── formulas.js
    │   └── helpers.js
    └── styles/
        └── global.js
🧩 Requisitos Gerais

Framework: React Native com Expo.

Linguagem: JavaScript (sem TypeScript).

Design: Interface limpa, moderna e responsiva.

Navegação: Usar @react-navigation/native e @react-navigation/native-stack.

Armazenamento:

AsyncStorage para dados locais (usuário, tanques, lotes, registros).

Estrutura de firebaseConfig.js já pronta para integração futura (Firebase Authentication e Firestore).

Estilo:

Centralizar cores e fontes em src/styles/global.js.

Usar SafeAreaView, ScrollView e TouchableOpacity quando apropriado.

Ícones: @expo/vector-icons.

Gráficos: react-native-chart-kit.

🖥️ Funcionalidades Principais
🔐 Autenticação (/screens/Auth)

LoginScreen.js:
Formulário com email e senha.
Botão "Entrar" e link "Criar conta".

RegisterScreen.js:
Cadastro com nome, email e senha.
Dados salvos localmente com AsyncStorage.

📊 Dashboard (/screens/Dashboard)

DashboardScreen.js:
Mostra visão geral com:

Quantidade de tanques e lotes.

Últimas medições de temperatura, pH e oxigênio.

Cartões de estatísticas com ícones (StatCard.js).

AlertsScreen.js:
Lista de alertas automáticos (ex: temperatura fora do limite).

ReportsScreen.js:
Relatórios de crescimento e consumo.
Exibir gráficos com react-native-chart-kit e opção de exportar em CSV.

🐟 Tanques (/screens/Tanks)

TanksScreen.js:
Lista tanques cadastrados (usa TankCard.js).

AddTankScreen.js:
Formulário para adicionar novo tanque (nome, volume, espécie, temperatura ideal, pH ideal, oxigênio ideal).

🧬 Lotes (/screens/Lots)

LotsScreen.js:
Lista de lotes com nome do tanque, espécie e quantidade.

AddLotScreen.js:
Formulário para criar novo lote.

LotDetailScreen.js:
Exibe informações completas do lote e seu histórico (alimentação, biometria e qualidade da água).

📋 Registros (/screens/Records)

WaterQualityScreen.js:
Registrar pH, temperatura e oxigênio dissolvido.

FeedingScreen.js:
Registrar alimentação (quantidade, hora, tipo de ração).

BiometricsScreen.js:
Registrar peso médio, crescimento e taxa de mortalidade.

⚙️ Configurações (/screens/Settings)

ProfileScreen.js:
Permite editar nome, email, telefone e nome da fazenda.
Foto de perfil usando expo-image-picker.
Salvar alterações com AsyncStorage.

SettingsScreen.js:
Opções gerais: tema claro/escuro, reset de dados e sobre o app.

🧱 Componentes Reutilizáveis

TankCard.js → Card para exibir informações do tanque.

LotCard.js → Card com informações do lote.

StatCard.js → Card para estatísticas no dashboard.

DataChart.js → Componente para exibir gráficos reutilizáveis.

🧮 Utils

formulas.js → Funções para cálculos úteis (ex: conversão de volume, taxa de conversão alimentar).

helpers.js → Funções genéricas (validação de dados, formatação de datas).
🎨 Estilo Global

Arquivo: src/styles/global.js

Paleta de cores principal:
export default {
  colors: {
    primary: '#2E86AB',
    secondary: '#A2D5F2',
    background: '#F8F9FA',
    text: '#333',
    card: '#FFFFFF',
  },
  fonts: {
    regular: 'System',
    bold: 'System',
  },
};


npm install @react-navigation/native @react-navigation/native-stack
npm install @react-native-async-storage/async-storage
npm install react-native-chart-kit react-native-svg
npm install expo-image-picker expo-file-system
npm install @expo/vector-icons
