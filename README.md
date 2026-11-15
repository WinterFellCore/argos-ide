<p align="center">
  <img src="https://argos-ide.vercel.app/img/icon-180.png" width="96" alt="">
</p>

<h1 align="center">Argos IDE</h1>

<p align="center">
  Editor de código para Windows, em português, com um agente de IA que trabalha no seu projeto.
  <br>
  <a href="https://argos-ide.vercel.app"><b>Site</b></a> ·
  <a href="https://github.com/WinterFellCore/argos-ide/releases/latest"><b>Baixar</b></a> ·
  <a href="https://github.com/WinterFellCore/argos-ide/releases">Todas as versões</a>
</p>

<p align="center">
  <img src="https://argos-ide.vercel.app/og-image.png" width="720" alt="Tela do Argos IDE">
</p>

## O que ele faz

- **Agente de IA (Argos):** lê e edita arquivos, roda comandos, busca no projeto, testa páginas e compila. Pede permissão antes de comandos e de escrever fora do projeto, e cada mudança pode ser desfeita por arquivo.
- **Modelos locais ou na nuvem:** roda modelos no próprio PC (llama.cpp) ou usa provedores compatíveis com a API da OpenAI e o Gemini.
- **C# e C++ sem o Visual Studio aberto:** compila e executa projetos .NET, CMake e `.sln`/`.vcxproj`, com os erros no painel Problemas.
- **Inteligência de código:** autocompletar, ir para a definição e erros enquanto digita, com clangd (C/C++) e csharp-ls (C#).
- **Modelos de projeto:** C# console, WinForms e WPF, C++ console e janela com Dear ImGui + DirectX 11.
- **Para sites:** prévia ao vivo, prévia no celular pela rede local e publicação.
- **Editor completo:** abas, terminal com cores e links para erros, Git, painel Problemas, temas e respostas lidas em voz alta (voz neural que roda no PC).

## Instalar

Baixe o `Argos-Setup.exe` em [Releases](https://github.com/WinterFellCore/argos-ide/releases/latest). Precisa de Windows 10 ou 11, 64 bits.

O próprio Argos avisa quando sai uma versão nova. Cada download é conferido com uma assinatura Ed25519 e com o SHA-256 antes de instalar.

## Como é feito

| Parte | Tecnologia |
| --- | --- |
| Servidor da IDE (arquivos, terminal, compilação, LSP, atualizações) | Node.js, sem framework |
| Interface | HTML, CSS e JavaScript, com o editor Monaco |
| Agente de IA | Python |
| Janela e instalador | C# (WinForms + WebView2) |

As chaves de API ficam guardadas com a DPAPI do Windows. O servidor só aceita conexões do próprio PC e exige um token em cada pedido. A prévia no celular só abre quando você liga e pede um código.

## Sobre o projeto

Feito por [@WinterFellCore](https://github.com/WinterFellCore) em cerca de 30 dias, com ajuda de um agente de IA para escrever o código. As ideias, as decisões, os testes e as releases são meus.

O código-fonte ainda não é público; este repositório tem as versões para baixar.
