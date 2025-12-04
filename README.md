#
🚀 Carteira Cidadã: O Futuro da Gestão de Documentos Digitais

Este repositório contém a documentação completa de Análise e Projeto de Software para o aplicativo Carteira Cidadã, uma solução desenvolvida para centralizar, organizar e proteger documentos digitais no Brasil.  

O projeto visa solucionar a fragmentação atual, onde o cidadão é obrigado a usar múltiplos aplicativos e sistemas para acessar informações essenciais. Essa dispersão causa desorganização, perda de tempo e falta de padronização na segurança. A Carteira Cidadã oferece uma experiência prática, unificada e mais segura.  

🎯 Objetivo do Sistema

O objetivo principal é reunir todos os documentos do usuário em uma plataforma única, permitindo acesso rápido, organização simples e segurança reforçada.  

O sistema utiliza tecnologias de verificação, autenticação e integridade para garantir confiabilidade e preservar a autenticidade das informações. Ele se integra a bases oficiais do governo para validar e importar dados com segurança.  

✨ Funcionalidades Chave (Requisitos Funcionais)

As funcionalidades do sistema foram priorizadas em alta para garantir a segurança e a usabilidade essenciais:

• Cadastro e Acesso: Permite o cadastro de contas Pessoa Física (PF) e Pessoa Jurídica (PJ). O login de PF pode ser feito via CPF/senha ou gov.br, e o de PJ via CNPJ/senha. O Logout é permitido a qualquer momento.

• Segurança na Conta: Solicita autenticação facial no primeiro acesso da conta PF e permite a reconfiguração da FaceID. O CPF ou CNPJ não podem ser alterados após o cadastro.  

• Gestão de Documentos: Permite upload de arquivos PDF e JPEG, e exige que todo documento seja anexado a uma pasta. É criada automaticamente a pasta 'Documentos Pessoais' ao cadastrar PF. O usuário pode criar pastas personalizadas e editar pastas existentes.  

• Validação e Integridade: Permite anexar documentos autenticados/registrados via código de verificação. Registra o HASH, titularidade e dados de segurança dos documentos e impede qualquer edição no arquivo original. O sistema valida se o documento pertence ao titular da conta.  

• Busca e Visualização: Permite a busca de documentos pelo nome e a visualização completa dos documentos anexados.  

🛡️ Requisitos Não Funcionais (Segurança e Qualidade)

A qualidade e a segurança do sistema são garantidas pelos seguintes requisitos:

• Segurança com HASH: O sistema deve garantir a integridade dos documentos utilizando HASH criptográfico.  

• Imutabilidade: O sistema deve impedir qualquer edição do arquivo original.  

• Comunicação Segura: As integrações com serviços governamentais devem ocorrer por conexões criptografadas.  

• Conformidade Legal: O sistema deve seguir a LGPD e padrões governamentais.  

• Criptografia de Dados: Todos os dados sensíveis devem ser armazenados de forma criptografada.  

• Alta Disponibilidade e Desempenho: O sistema deve suportar grande volume de usuários simultâneos e carregar documentos e realizar buscas de forma ágil, com um tempo de resposta de 2 a 3 segundos para operações comuns.  

• Compatibilidade: O sistema deve funcionar em dispositivos Android e iOS.  

📐 Arquitetura do Sistema (Diagrama de Implantação)
A arquitetura do sistema é distribuída e focada em segurança na comunicação:

1. Smartphone: Dispositivo do usuário (Android/iOS) que hospeda o aplicativo (artefatos app.apk e app.ipa) com módulos de faceID e upload.

2. Servidor de Aplicação (API REST): Responsável pela lógica de negócio, contendo o backend.jar com módulos de autenticação, HASH, validação de titularidade e o conector governamental externo.

3. Servidor de Banco de Dados: Armazena o schema.sql. A comunicação com o Servidor de Aplicação é feita via JDBC/TLS.

4. Servidor de Armazenamento: Armazena os arquivos de documentos (documents.pdf, images.jpeg) e se comunica via HTTPS.

5. APIs Governamentais Externas: Serviços externos que realizam validação de documentos, código de verificação e o login via gov.br.

📚 Documentação (Diagramas UML e Protótipos)

Este repositório contém os seguintes artefatos de documentação:

• Modelo de Caso de Uso: Diagrama e descrição textual dos principais casos de uso (Fazer Login, Adicionar Documento, Validar Documentos e Gerenciar Contas).  

• Diagrama de Classes: Define a estrutura de dados, incluindo classes como Usuário, Pessoa Física, Pessoa Jurídica, Pastas e Documentos.  

• Diagramas Dinâmicos:

• Diagrama de Atividade para o processo de Fazer Login.  

• Diagrama de Sequência para o processo de Anexo de Documento, detalhando a interação entre o Usuário, o App, o Servidor e os Sistemas Governamentais Externos.  

• Protótipos de Tela: Inclui o design das telas de Login (PF/PJ), Cadastro (PF), Telas Principais (Home) e as Telas de Operações (Autenticação Facial e Adicionar Documento).  

👥 Desenvolvedores

• Ronald Machado Guimarães
• Cassio Emanuel Santos
• José Lucas Guimarães
• Bilsa Ferreira
• João Pedro Silva Maciel
