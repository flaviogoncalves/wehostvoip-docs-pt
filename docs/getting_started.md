# Introdução ao WeHostVoIP

WeHostVoIP ou WeVoIP como gostamos de nos chamar, é um PABX Multi-ISP, Multi-Tenant em nuvem criado especialmente para provedores de serviços de comunicação.

Seguindo este guia, você poderá iniciar uma operação de Cloud PBX em poucas horas. Existem várias etapas para se preparar para uma operação.

- [Introdução ao WeHostVoIP](#introdução-ao-wehostvoip)
  - [Conceitos WeHostVoIP](#conceitos-wehostvoip)
  - [Etapa 1 Criando um novo ISP](#etapa-1-criando-um-novo-isp)
  - [Etapa 2 Criando uma operadora](#etapa-2-adicionando-uma-operadora)
  - [Etapa 3 Criando um plano de serviço](#etapa-3-criando-um-plano-de-serviço)
  - [Etapa 4 Criando um cliente](#etapa-4-criando-um-cliente)
  - [Etapa 5 Criando um plano de discagem](#etapa-5-criando-um-plano-de-discagem)
  - [Etapa 6 Adicionar números ao inventário](#etapa-6-adicionar-números-ao-inventário)
  - [Etapa 7 Criando domínios](#etapa-7-criando-domínios)
  - [Etapa 8 Criando seu primeiro tenant](#etapa-8-criando-seu-primeiro-tenant)
  - [Etapa 9 Acessando seu tenant](#etapa-9-acessando-seu-tenant)
  - [Etapa 10 Criando assinantes](#etapa-10-criando-assinantes)
  - [Passo 11 Cadastrando Alice no WebPhone](#passo-11-cadastrando-alice-no-webphone)
  - [Etapa 12 Registrando Bob no Softphone](#etapa-12-registrando-bob-no-softphone)
  - [Etapa 13 Faça uma chamada entre telefones](#etapa-13-faça-uma-chamada-entre-telefones)
  - [Etapa 14 Adicionar um país no grupo de segurança](#etapa-14-adicionar-um-país-no-grupo-de-segurança)
  - [Etapa 15 Fazer uma chamada para um destino externo](#etapa-15-fazer-uma-chamada-para-um-destino-externo)
  - [Etapa 16 Testando as chamadas recebidas](#etapa-16-testando-as-chamadas-recebidas)


## Conceitos WeHostVoIP

Existem três consoles diferentes para WeVoIP.

Console ISP - https://isp.wehostvoip.io \
Console do tenant - https://console.wehostvoip.io \
Console de telefone - https://phone.wehostvoip.io

No console do ISP (https://isp.wehostvoip.io) você configura os planos mestres para o provedor de Cloud PBX. Você vai conectar operadoras, criar planos de serviço, ajustar regras de normalização para números e muitas tarefas que você terá que fazer apenas uma vez.

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/e5707f3e-e2f6-4583-9897-5c722cbaf81f){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

O console do tenant é realmente a interface do PBX, você criará um ou vários tenants por cliente. Não há limites para o número de tenants criados.

![wehostvoip-subscribers](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/b968a34b-8a32-4ca1-bda7-9974c6fc2ffd){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

Finalmente a interface do telefone é um WebRTC onde você pode fazer ou receber chamadas. O sistema também suporta quase qualquer telefone ou dispositivo SIP.

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/d43509c0-dd56-4162-b7a0-e112fa468e5f){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

## Etapa 1 Criando um novo ISP

Para criar um novo ISP, você deve iniciar o processo de inscrição no portal [isp.wehostvoip.io](https://isp.wehostvoip.io)

![image](https://user-images.githubusercontent.com/4958202/225346057-b9e16205-acaf-437b-a137-d54ed41cbcaa.png){ width="50%" style="display: block;margin-left: auto;margin-right: auto;"}

Depois de pressionar o cadastro, o sistema solicitará que você forneça um e-mail para confirmação

![wehostvoip-email-confirmation](https://user-images.githubusercontent.com/4958202/153394860-fc61c76d-fe05-475b-9d4f-898d3a478770.png){ width="50%" style="display: block;margin-left: auto;margin-right: auto;"}

Agora você tem que ir ao seu e-mail e clicar no link de confirmação do e-mail. Depois de pressionar o link, você verá o link de configuração do ISP.

![image](https://user-images.githubusercontent.com/4958202/225346430-34c9e499-5ecf-41ff-8d64-9e3e1441a540.png){ width="50%" style="display: block;margin-left: auto;margin-right: auto;"}

Forneça um nome completo e senha para o nome de usuário e pressione próximo

![image](https://user-images.githubusercontent.com/4958202/225346612-222882e7-c803-421e-9940-63aa3c1d6f91.png){ width="50%" style="display: block;margin-left: auto;margin-right: auto;"}

Agora, existem parâmetros importantes aqui. O parâmetro mais importante é o namespace. Quando você começar a usar o wehostvoip, para fazer login no sistema, você precisará do seu próprio namespace. Escolha um namespace e anote o nome que você precisará no futuro. Também importante é a moeda. Preencha o restante das informações e pressione próximo.

![image](https://user-images.githubusercontent.com/4958202/225346784-c093b3df-5872-4cb4-bbb2-f3b8eca72a85.png){ width="50%" style="display: block;margin-left: auto;margin-right: auto;"}

Agora você pode personalizar seus logotipos e cores. \
Para acessar novamente esta configuração, clicar no menu de opções no canto superior direito, Configurações, Tema.

![image](https://user-images.githubusercontent.com/4958202/225347049-1820c862-72c8-4fd6-9784-c755d364ed7b.png){ width="50%" style="display: block;margin-left: auto;margin-right: auto;"}

Depois de terminar, você deve escolher um plano, os valores dos planos estão em dólares, contate-nos se você desejar um plano em reais. 

![image](https://user-images.githubusercontent.com/4958202/225347424-1d5fab24-5fbd-4cc7-b4dd-70e3226dbcb1.png){ width="50%" style="display: block;margin-left: auto;margin-right: auto;"}

No final do processo você verá a tela de configuração do ISP

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/e5707f3e-e2f6-4583-9897-5c722cbaf81f){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

Vídeo, o vídeo do processo de onboarding pode ser visto em:

[![Watch the video](https://github.com/flaviogoncalves/wehostvoip-docs-pt/assets/104862214/431ab479-82bc-42d0-bc67-20a543433080)](https://youtu.be/8hhOX1ilF9o)

## Etapa 2 Adicionando uma operadora

Agora é hora de especificar onde você terminará suas chamadas. Para este início vamos terminar as chamadas usando um gateway de teste chamado sipa.flagonc.com. Você pode testar as chamadas recebidas registrando um telefone no mesmo servidor. Vou fornecer instruções no ponto certo. Por enquanto vamos criar um gateway e uma operadora. Uma operadora pode ter mais de um gateway para redundância, mas o sistema não faz rota por prefixo. Esta é a função do softswitch ISP ou gateway que encerra as chamadas. Não queríamos ter redundância nessas funções.

Ao criar uma operadora, o primeiro passo é criar o gateway e em seguida adicionar a operadora. Uma operadora pode ter mais de um gateway para no caso de falha do primeiro o segundo ser acionado. 

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/31849e1b-12e0-43a9-b7ef-b90cd9ca7d26){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

**Nome:** Ao criar um gateway a primeira coisa que você adiciona é o nome, por exemplo, primário \
**Endereço:** Em seguida adiciona o endereço e a porta do gateway, por exemplo: sipa.flagonc.com:5600 \
**Display:** Display é a parte em texto do identificador de chamada, também chamado de FROM diaplay \
**Strip de Saída:** Remover N dígitos do número e.164 ou original antes de enviar para o gateway \
**Prefixo de Saída:** Adicionar esta string do lado esquerdo do número antes de enviar para o gateway, ocorre após o strip \
**Strip de Entrada:** Remover N dígitos do número que está chegando na porta de entrada do SBC \
**Prefixo de Entrada:** Adicionar esta string do lado esquero do número entrante antes de entrar no SBC, ocorre após o strip \
**Dominio de Origem:** Também chamado de *From domain*, muitas vezes necessário para a autenticação, normalmente o endereço do gateway \
**Usuário de Origem:** Também chamado de *From user*, é o caller ID e é frequentemente usado para validar a chamada, ver com sua operadora \
**Aplicar sobre:** Usada apenas para o número de saída. Aplicar as regras sobre o número e164 interno ou sobre o número originalmente discado \
**Atributos:** Atributos opcionais, reservado para o suporte técnico \
**Adicionar PAI:** - Adicionar o P-Asserted-Identtity. Isto pode ser necessário em algumas operadoras

Ao terminar de preencher salve o gateway e salve a operadora. Se precisar de dois gateways crie os dois antes de salvar. 

![image](https://github.com/flaviogoncalves/wehostvoip-docs-pt/assets/104862214/d3f9002f-a53a-4caf-8282-4505d1c9af29){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}


## Etapa 3 Criando um plano de serviço

O plano de serviço é o coração do sistema. Você poderá alterar seus clientes usando um sistema pré-pago ou pós-pago. Você pode começar com algo tão simples quanto cobrar por mês e depois criar planos mais sofisticados para cobrar por trecho ou por prefixo. No início, vamos criar um plano simples para cobrar apenas uma taxa mensal.

Pressione, criar plano de serviço para começar a criar um plano.

Nomeie seu primeiro plano de serviço como Padrão.

![wehostvoip-service-plan-1](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/4b9cae38-9f23-4b79-9662-cc22e3721f86){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}


Selecione a Operadora e Plano de discagem. \
Para os próximos dois menus abaixo, marque a caixa "No Service Deck", "No Rate Deck"


![service-plan-2](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/18fc8b74-d05a-4bd9-aa84-170fe3d673ad){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}



Em seguida, pressione Criar Plano de Serviço, não saia da página sem criar o plano de serviço.

## Etapa 4 Criando um cliente

Depois de criar um plano de serviço, agora você pode criar um cliente. Basta pressionar o menu do cliente no lado direito e pressionar criar para criar um novo cliente. Cliente é um de seus clientes que comprará um serviço de PBX. Antes de criar um tenant, você precisa criar um cliente.

![wehostvoip-customer-01](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/7606475d-ae82-4184-803b-c5a476160a22){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/abf42801-a9ff-42df-8cf4-8b6fe97a868f){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

## Etapa 5 Criando um plano de discagem

Internamente, WeHostVoIP lida com todos os números no formato [E.164](https://en.wikipedia.org/wiki/E.164) com "+" na frente do número. Existem diferentes maneiras de discar em cada país. Às vezes, você precisa prefixar o número que deseja discar com 9 ou 0. No entanto, tudo deve ser normalizado para E164. Criamos alguns presets para o Brasil e os EUA. O dialplan tem três campos muito importantes. Se você deseja criar um plano de discagem, precisa entender [expressões regulares](https://en.wikipedia.org/wiki/Regular_expression). Existe a expressão de correspondência para corresponder ao número, a expressão subs para separar o número em partes usando parênteses e a expressão de substituição para reconstruir o número. Você pode usar duas variáveis ​​_CC (Código do País do Usuário) e _AC (Código de Área do Usuário)_. Se você estiver em um país diferente, entre em contato para que eu possa criar uma predefinição para simplificar seu país. Para começar, vou usar uma predefinição para US sem 9 como prefixo.

![wehostvoip-dialplan](https://user-images.githubusercontent.com/4958202/153420608-15c30d48-8547-4067-a6dc-68281a784796.png){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

## Etapa 6 Adicionar números ao inventário

Esta etapa é opcional

Se você tem números ou intervalos DID para vender, você deve especificá-los em seu ISP. Seus usuários poderão alocar DIDs para seus próprios usuários.

![imagem](https://user-images.githubusercontent.com/4958202/153417573-58a74558-add1-4e62-8fc1-7b520cf6466b.png){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

## Etapa 7 Criando domínios

Esta etapa é opcional

Você pode criar um domínio diretamente abaixo do seu namespace, como customer1.gettingstarted.com. Para isso você não precisa criar um domínio. No entanto, se seu cliente já usa o Google Apps ou o Azure AD com um domínio específico, você pode adicionar seus domínios aqui. Você precisa verificar a propriedade do domínio adicionando um TXT em um servidor de domínio.

![imagem](https://user-images.githubusercontent.com/4958202/153421332-cc46251c-d353-4ee6-8576-e02af0372a49.png){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

## Etapa 8 Criando seu primeiro tenant

A maioria das configurações que você fez até agora são feitas apenas uma vez, exceto para clientes. Após esta configuração você já pode criar
um tenant para atender seus clientes.

Para criar um tenant é muito simples, você começa adicionando um domínio. Pode ser um subdomínio do seu namespace ou o domínio do cliente previamente criado e verificado. Vamos usar customer1 aqui como o domínio.

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/f30bf22e-12d5-4bb5-8f15-c64d3d3e50a3){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

Depois de especificar o domínio, você deve especificar os controladores de cliente, operadora, administradores, plano de discagem e de borda de sessão. É um formulário muito rápido. O SBC compartilhado para o Brasil é sbc-br.wehostvoip.io:60110. Se você necessitar de um SBC não compartilhado entre em contato. Consulte sobre os planos gratuitos. 

## Etapa 9 Acessando seu tenant

Clique no botão de visualização no final da linha (próximo aos botões excluir e editar).

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/10087d6e-622c-48dc-8ab3-ad3446035db9){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

Você chegará à interface do tenant como abaixo.

![wehostvoip-tenant-login](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/df35a28b-051f-45c7-98ca-5f9e6579c2f7){ width="50%" style="display: block;margin-left: auto;margin-right: auto;"}

Assim que o login for concluído, você acessará a interface abaixo.

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/3c786c78-bc59-4812-813d-308af788fd42){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}


## Etapa 10 Criando assinantes

Agora, na tabela de assinantes, vamos criar dois usuários, Alice e Bob. Há muitos campos para adicionar em um assinante. Vamos passar por eles

* Nome de usuário - "Nome de usuário de autenticação"
* E-mail - "E-mail para fins de comunicação. Não é usado na autenticação"
* Senha - "Senha SIP para telefones"
* Alias ​​- "Alias ​​do usuário SIP, muitas vezes usamos o alias como extensão"
* VoiceMail to Email - "Após falhar uma chamada, o chamador poderá deixar uma mensagem de voz no e-mail do assinante"
* Código de área - "Código de área do usuário"
* ID do chamador - "Substituir o identificador de chamadas do usuário com este identificador de chamadas"
* Intervalo de datas - "Grupo de regras de tempo definindo o horário comercial"
* Plano Visual - "Usado apenas para receber chamadas"
* Grupo de segurança - "Grupo de segurança autorizando prefixos de países"
* Idioma - "Usado para geração de texto para fala"
* Grupo de Chamadas - "Grupo Numérico para Origem da Chamada Capturada"
* Grupo de Atendimento - "Grupo Numérico para Atender uma Chamada"
* Senha do softphone - "Senha para o softphone e webphone"
* Encaminhar, Encaminhar ocupado e Encaminhar sem resposta - "Configurações de encaminhamento de chamadas"
* Máximo de chamadas simultâneas - "Quantidade máxima de chamadas simultâneas"
* Tempo limite de discagem - "Quanto esperar para o usuário atender uma chamada"

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/4cdf6ecc-c0ec-46c8-91ee-c271354b03bb){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}
![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/fe437b4c-3c0a-4fe3-a76e-34618be64f14){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

**Não esqueça de adicionar uma senha para SIP e para o Softphone, anote a senha, você precisará da senha antes**

## Passo 11 Cadastrando Alice no WebPhone

Para cadastrar Alice no webphone, basta acessar a url https://phone.wehostvoip.io e adicionar o nome e a senha. Neste ponto, ainda não podemos fazer login com o Google ou o Azure. Para isso é necessário registrar e verificar um domínio. Você só poderá fazer login com o Google ou AzureAd se tiver um domínio sincronizado. Temos um capítulo especial para isso.

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/eb58b0c0-52fd-4467-9e46-31008c3957b5){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}

Depois de fazer o login, você verá um círculo verde no canto superior direito.

## Etapa 12 Registrando Bob no Softphone

Este é o cliente gratuito para WeHostVoIP. Se você preferir usar um telefone de comunicação unificada completo, entre em contato conosco para obter um plano de atualização, pois o telefone UC é cobrado separadamente. A marca de um novo telefone UC envolve várias etapas, incluindo o registro de um número DUNS e a publicação na Apple e na Google Store. Esses recursos não são abordados no Guia de Introdução.

Você só pode usar o softphone se estiver usando o Windows 7 ou posterior. Baixe o softphone em https://isp.wehostvoip.io/downloads/wevoip-3.20.7002.exe, extraia e execute o arquivo

Após a instalação, faça login usando o nome de usuário e a senha do **softphone**.

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/9d01901c-a650-48f7-9d41-beede9144bb8){ width="40%" style="display: block;margin-left: auto;margin-right: auto;"}

![imagem](https://user-images.githubusercontent.com/4958202/153725448-8a30f3bf-c243-46b4-8fd7-d2bd97c47749.png){ width="40%" style="display: block;margin-left: auto;margin-right: auto;"}

[Utilizando outro Softphone/Telefone](configure-softphones-ip_phones.md)

## Etapa 13 Faça uma chamada entre telefones

Basta chamar Alice e Bob por seus nomes. Você também pode usar seus apelidos alice (1000) e bob (1001). Disque 1000 de bob e 1001 de alice para testar a discagem.

## Etapa 14 Adicionar um país no grupo de segurança

Para evitar fraudes, os assinantes não têm permissão por padrão para fazer chamadas PSTN. Você terá que autorizar os países ou prefixos para permitir chamadas de saída. Nós tornamos esse processo muito fácil. Em nosso caso estamos adicionando EUA. Quando você seleciona EUA, ele seleciona todos os códigos de área da NANPA pertencentes aos EUA e não carrega destinos do Caribe frequentemente usados ​​para fraude.

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/9d6c33b4-f11f-42c5-b1e3-e7dbe4fdd8df){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}


![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/dd257eb8-1862-47c7-ab51-c402de853564){ width="80%" style="display: block;margin-left: auto;margin-right: auto;"}

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/89a2e946-a539-477d-9966-fcfbc36ae479){ width="80%" style="display: block;margin-left: auto;margin-right: auto;"}

Após adicionar os códigos/países clicar em salvar.

![image](https://github.com/pauloantonio-git/wehostvoip-docs-pt/assets/104862214/0c60c9c1-c211-4de9-9700-10f49c8637f9){ width="100%" style="display: block;margin-left: auto;margin-right: auto;"}


## Etapa 15 Fazer uma chamada para um destino externo

Disque 22224444, você deve receber uma mensagem engraçada. Como estamos usando o gateway de teste sua chamada não está indo para o PSTN. Se você quiser que sua chamada vá para o PSTN, você deve adicionar sua própria operadora.

## Etapa 16 Testando as chamadas recebidas

Testar uma chamada recebida é um pouco mais difícil. Se você adicionou uma transportadora real e você tem um número real, o processo é muito fácil. No entanto, para os propósitos deste Guia de introdução, usaremos um softphone conectado ao gateway de teste para conectar-se ao nosso SBC sbc-br.wehostvoip.io
