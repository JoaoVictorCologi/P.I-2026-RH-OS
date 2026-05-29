# P.I-2026-RH-OS
# Aplicativo desenvolvido em Flutter com integração de IA para análise automatizada de currículos – Projeto Integrado 2026.

## Problema

Empresas de Recursos Humanos enfrentam dificuldades na triagem de currículos devido ao grande volume de candidatos.  
O processo manual é demorado, suscetível a erros e pode atrasar contratações estratégicas.

## Objetivo

Desenvolver um aplicativo móvel em Flutter com integração de Inteligência Artificial capaz de:

- Escanear currículos em PDF ou imagem
- Extrair automaticamente informações relevantes
- Classificar candidatos com base em critérios definidos
- Gerar resumo automático do perfil profissional

## Público-Alvo

- Empresas de Recursos Humanos
- Recrutadores
- Pequenas e médias empresas

## ODS Relacionado

ODS 8 – Trabalho Decente e Crescimento Econômico

## Estrutura do Repositório

P.I-2026-RH-OS/
│
├── android/
├── docs/
│   ├── RF.md
│   ├── RN.md
│   ├── RNF.md
│   ├── arquitetura.md
│   ├── visao-do-produto.md
│   ├── Testes/
│   │   ├── Documento A - Base Conceitual de Teste.docx
│   │   ├── Documento B - Processo de Teste.docx
│   │   ├── Documento C - Tecnicas e Casos de Teste.docx
│   │   ├── Documento D - Execucao e Resultados dos Testes.docx
│   │   └── Relatorio Tecnico Atividade Normas 25010 e 15288.docx
│   ├── caso-de-uso/
│   └── diagramas/
│       ├── classes/
│       ├── componentes/
│       ├── uc-01/ até uc-06/
│
├── lib/
│   ├── main.dart
│   ├── app.dart
│   ├── firebase_options.dart
│   ├── core/
│   │   ├── constantes/
│   │   ├── di/
│   │   ├── tema/
│   │   └── utils/
│   ├── data/
│   │   ├── banco/
│   │   ├── parsers/
│   │   │   └── ocr/
│   │   ├── repositorios/
│   │   └── servicos/
│   ├── domain/
│   │   ├── casos_de_uso/
│   │   │   ├── candidatos/
│   │   │   ├── candidaturas/
│   │   │   └── vagas/
│   │   ├── entidades/
│   │   └── repositorios/
│   └── presentation/
│       ├── admin/
│       ├── auth/
│       ├── curriculos/
│       ├── dashboard/
│       ├── entrevistas/
│       ├── home/
│       ├── mais/
│       ├── notificacoes/
│       ├── perfil/
│       ├── vagas/
│       └── widgets/
│
├── test/
│   ├── Curriculos/
│   ├── fixtures/
│   ├── entidades/
│   ├── integracao/
│   ├── servicos/
│   ├── extracao_real_test.dart
│   └── extrator_test.dart
│
├── firestore.rules
├── firestore.indexes.json
├── firebase.json
└── pubspec.yaml


# Guia Rápido — RH-OS

## Como usar o aplicativo

### 1) Pré-requisitos
- Flutter 3.x
- Dart 3.x
- Android SDK
- Emulador Android ou dispositivo físico

### 2) Instalar dependências
```bash
flutter pub get
```

### 3) Executar no Android
```bash
flutter devices
flutter run -d <device-id>
```

### 4) Executar com OCR Gemini (opcional)
```bash
flutter run -d <device-id> --dart-define=GEMINI_API_KEY=SUA_CHAVE
```

### 5) Login inicial (ambiente com seed habilitado)
- Admin: `admin@rhos.com` / `admin123`
- RH: `recrutador@rhos.com` / `rec123`

## Caminhos dos documentos de Qualidade e Teste de Software

### Documentação principal de testes
- `docs/Testes/Documento A - Base Conceitual de Teste.docx`
- `docs/Testes/Documento B - Processo de Teste.docx`
- `docs/Testes/Documento C - Tecnicas e Casos de Teste.docx`
- `docs/Testes/Documento D - Execucao e Resultados dos Testes.docx`

### Relatório de normas e qualidade
- `docs/Testes/Relatorio Tecnico Atividade Normas 25010 e 15288.docx`

### Requisitos e arquitetura (apoio de qualidade)
- `docs/RF.md`
- `docs/RN.md`
- `docs/RNF.md`
- `docs/arquitetura.md`

### Suíte de testes automatizados
- Pasta: `test/`
- Execução:
```bash
flutter test
```

