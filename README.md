# Crypto Alert – Testes E2E com Maestro

## 1. Sobre o projeto

Este repositório tem como objetivo desenvolver testes automatizados End-to-End (E2E) para o aplicativo Crypto Alert, utilizando a ferramenta Maestro.

Os testes buscam verificar funcionalidades principais do aplicativo, como visualização de criptomoedas, consulta de alertas, criação de alertas de preço e validação do formulário.

## 2. Tecnologias utilizadas

- React Native
- Expo
- TypeScript
- Maestro
- Android

## 3. Estrutura dos testes

Os fluxos automatizados estão organizados na pasta `.maestro`:

| Arquivo | Descrição |
|---|---|
| 01-lista-criptomoedas.yaml | Verifica a exibição das criptomoedas. |
| 02-alertas-vazio.yaml | Verifica o estado vazio da tela de alertas. |
| 03-criar-alerta.yaml | Verifica a criação de um alerta de preço. |
| 04-validacao-formulario.yaml | Verifica a validação do formulário vazio. |

## 4. Configuração do ambiente

### Pré-requisitos

- Node.js instalado.
- npm instalado.
- Android Studio com emulador configurado ou dispositivo Android.
- Maestro instalado e configurado no PATH.
- Depuração USB habilitada, caso utilize um celular físico.

### Instalação

Clone o repositório:

```bash
git clone https://github.com/Gisele002/crypto-alert-e2e-maestro.git
```

Entre na pasta:

```bash
cd crypto-alert-e2e-maestro
```

Instale as dependências:

```bash
npm install
```

## 5. Executando o aplicativo

Com um emulador Android aberto ou celular conectado, execute:

```bash
npx expo run:android
```

O comando realiza a compilação e instalação do aplicativo no dispositivo Android.

## 6. Executando os testes

Com o aplicativo instalado e aberto no dispositivo, execute todos os fluxos:

```bash
maestro test .maestro
```

Para executar um fluxo individual:

```bash
maestro test .maestro/01-lista-criptomoedas.yaml
```

Substitua o nome do arquivo para executar os demais fluxos.

## 7. Evidências dos testes

As evidências de execução serão organizadas na pasta `evidencias/`, contendo registros visuais dos fluxos automatizados.

**Status:** execução dos testes e coleta das evidências pendentes de validação no dispositivo Android.

## 8. Considerações finais

O projeto busca aplicar conceitos de testes automatizados E2E, utilizando o Maestro para verificar o comportamento das principais funcionalidades do aplicativo Crypto Alert.