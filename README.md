Readme - Instalação e Execução do .NET 7.0

Esse repositório contém as instruções para instalar e executar o .NET 7.0 no Ubuntu.
Instalação

Para instalar o .NET SDK 7.0, siga os passos a seguir:

    Abra o terminal do Ubuntu.
    Execute o comando sudo apt-get update para atualizar a lista de pacotes disponíveis.
    Execute o comando sudo apt-get install -y dotnet-sdk-7.0 para instalar o .NET SDK 7.0.

Após a instalação, você pode verificar se a instalação foi bem sucedida, digitando o comando dotnet --version no terminal. Se tudo estiver correto, a versão do SDK será exibida.
Criação e Execução de uma API
Criação de diretórios

Primeiramente, crie dois diretórios utilizando o terminal do Ubuntu:

mkdir teste-api
mkdir nova-api

Criação da API

Em seguida, crie uma nova API utilizando o comando dotnet new webapi:

dotnet new webapi

Esse comando irá gerar uma nova API padrão do .NET.
Execução da API

Para executar a API, navegue até o diretório da API e execute o comando dotnet run:

cd minha-api
dotnet run

Esse comando inicia o servidor local da API e mostra o seguinte output:
asciidoc

Welcome to .NET 7.0!
---------------------
SDK Version: 7.0.107

----------------
Installed an ASP.NET Core HTTPS development certificate.
To trust the certificate run 'dotnet dev-certs https --trust' (Windows and macOS only).
Learn about HTTPS: https://aka.ms/dotnet-https
----------------
Write your first app: https://aka.ms/dotnet-hello-world
Find out what's new: https://aka.ms/dotnet-whats-new
Explore documentation: https://aka.ms/dotnet-docs
Report issues and find source on GitHub: https://github.com/dotnet/core
Use 'dotnet --help' to see available commands or visit: https://aka.ms/dotnet-cli
--------------------------------------------------------------------------------------
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: https://localhost:5223
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: http://localhost:5222
info: Microsoft.Hosting.Lifetime[0]
      Application started. Press Ctrl+C to shut down.

Acesso à API

A API criada pode ser acessada em http://localhost:5222 ou https://localhost:5223.

Caso seja necessário, também é possível confiar no certificado local gerado pelo ASP.NET Core, rodando o comando:

dotnet dev-certs https --trust

Lembre-se de que a porta padrão para uma aplicação ASP.NET Core é a porta 5000, então você pode alterar a porta na sua aplicação para a porta 5000 se desejar. Para fazer isso, você pode alterar a linha app.UseUrls(urls: new[] { "https://localhost:5223", "http://localhost:5222" }); no arquivo Program.cs para app.UseUrls(urls: new[] { "https://localhost:5001", "http://localhost:5000" }); e, em seguida, executar o comando dotnet run novamente.
Conclusão

Esse repositório serve como um guia básico para instalar e executar o .NET 7.0 no Ubuntu, além de criar e executar uma API simples utilizando o framework. Para mais informações, é possível consultar a documentação oficial da Microsoft sobre a instalação do .NET no Linux e a criação de APIs com o ASP.NET Core.
