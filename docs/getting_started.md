# Introdução ao WeHostVoIP

WeHostVoIP ou WeVoIP como gostamos de nos chamar, é um PABX Multi-ISP, Multi-Tenant em nuvem criado especialmente para provedores de serviços de comunicação.

Seguindo este guia, você poderá iniciar uma operação de Cloud PBX em poucas horas. Existem várias etapas para se preparar para uma operação.

- [Introdução ao WeHostVoIP](#introdução-ao-wehostvoip)
  - [Conceitos WeHostVoIP](#conceitos-wehostvoip)
  - [Etapa 1 Criando um novo ISP](#etapa-1-criando-um-novo-isp)
  - [Etapa 2 Criando um plano de serviço](#etapa-2-criando-um-plano-de-serviço)
  - [Etapa 3 Criando um cliente](#etapa-3-criando-um-cliente)
  - [Etapa 4 Criando uma operadora](#etapa-4-criando-uma-operadora)
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

Console ISP - https://uc.wehostvoip.io
Console do tenant - https://uc.wehostvoip.io/tenants
Console de telefone - https://phone.wehostvoip.io

No console do ISP (https://uc.wehostvoip.io) você configura os planos mestres para o provedor de Cloud PBX. Você vai conectar operadoras, criar planos de serviço, ajustar regras de normalização para números e muitas tarefas que você terá que fazer apenas uma vez.

![wehostvoip-isp](https://user-images.githubusercontent.com/4958202/153396697-236b7908-6c70-4fe8-8357-c304e5be5841.png)

O console do tenant é realmente a interface do PBX, você criará um ou vários tenants por cliente. Não há limites para o número de tenants criados.

![wehostvoip-subscribers](https://user-images.githubusercontent.com/4958202/153419253-5f00900a-9c67-4615-994c-d8b091ced713.png)

Finalmente a interface do telefone é um WebRTC onde você pode fazer ou receber chamadas. O sistema também suporta quase qualquer telefone ou dispositivo SIP.

![imagem](https://user-images.githubusercontent.com/4958202/153306639-b3a04b17-c07e-49af-bb0d-7898f25b1499.png)

## Etapa 1 Criando um novo ISP

Para criar um novo ISP, você deve iniciar o processo de inscrição no portal uc.wehostvoip.io

![wehostvoip-signup-page](https://user-images.githubusercontent.com/4958202/153394573-98053c2c-de18-4f68-bb54-8a3854d751b8.png)

Depois de pressionar o cadastro, o sistema solicitará que você forneça um e-mail para confirmação

![wehostvoip-email-confirmation](https://user-images.githubusercontent.com/4958202/153394860-fc61c76d-fe05-475b-9d4f-898d3a478770.png)

Agora você tem que ir ao seu e-mail e clicar no link de confirmação do e-mail. Depois de pressionar o link, você verá o link de configuração do ISP.

![wehostvoip-1st-onbording](https://user-images.githubusercontent.com/4958202/153395980-67dcd005-d5c5-4acb-a1ff-256649f46613.png)

Forneça um nome completo e senha para o nome de usuário e pressione próximo

![wehostvoip-2nd-onboarding](https://user-images.githubusercontent.com/4958202/153396350-df093e03-9dbd-45a9-b795-f84bdf99c170.png)

Agora, existem parâmetros importantes aqui. O parâmetro mais importante é o namespace. Quando você começar a usar o wehostvoip, para fazer login no sistema, você precisará do seu próprio namespace. Escolha um namespace e anote o nome que você precisará no futuro. Também importante é a moeda. Preencha o restante das informações e pressione próximo.

![wehostvoip-3rd-onboarding](https://user-images.githubusercontent.com/4958202/153397395-95d4c7e1-645b-4c67-a409-0db6f95fd563.png)

Basta preencher seus dados de contato e pressionar próximo

![wehostvoip-4th-onboarding](https://user-images.githubusercontent.com/4958202/153398003-c74bfb17-f734-445d-ad53-459d3525d466.png)

Agora você pode personalizar seus logotipos e cores. Após fazer isso, pressione validar para verificar se você preencheu todos os dados necessários.

Depois de terminar, você poderá ver a interface do ISP

![isf-after-onboarding](https://user-images.githubusercontent.com/4958202/153399595-0cd0dd4a-94a8-4167-8aa7-e2ab0adcd66c.png)

## Etapa 2 Criando um plano de serviço

O plano de serviço é o coração do sistema. Você poderá alterar seus clientes usando um sistema pré-pago ou pós-pago. Você pode começar com algo tão simples quanto cobrar por mês e depois criar planos mais sofisticados para cobrar por trecho ou por prefixo. No início, vamos criar um plano simples para cobrar apenas uma taxa mensal.

Pressione, criar plano de serviço para começar a criar um plano.

Nomeie seu primeiro plano de serviço como Padrão.

![wehostvoip-service-plan-1](https://user-images.githubusercontent.com/4958202/153400844-7030dc71-5e6b-4dc4-ad17-34096eb36f41.png)

Para os próximos dois menus abaixo, marque a caixa "No Service Deck", "No Rate Deck"

![service-plan-2](https://user-images.githubusercontent.com/4958202/153401140-0272f11b-7129-42e2-917a-b4545615d1b3.png)

Em seguida, pressione Criar Plano de Serviço, não saia da página sem criar o plano de serviço.

## Etapa 3 Criando um cliente

Depois de criar um plano de serviço, agora você pode criar um cliente. Basta pressionar o menu do cliente no lado direito e pressionar criar para criar um novo cliente. Cliente é um de seus clientes que comprará um serviço de PBX. Antes de criar um tenant, você precisa criar um cliente.

![wehostvoip-customer-01](https://user-images.githubusercontent.com/4958202/153402853-53436e6e-0d48-4e10-a6c8-e13993d0be3b.png)

Há coisas importantes neste menu. O número máximo de assinantes e o número máximo de chamadas simultâneas. Você pode controlar quantas licenças cada usuário está usando de você. Você deve selecionar o plano de serviço e todos os outros campos são autoexplicativos.

## Etapa 4 Criando uma operadora

Agora é hora de especificar onde você encerrará suas chamadas. Para este início vamos encerrar as chamadas usando um gateway de teste chamado sipa.flagonc.com. Você pode testar as chamadas recebidas registrando um telefone no mesmo servidor. Vou fornecer instruções no ponto certo. Por enquanto vamos criar um gateway e uma operadora. Uma operadora pode ter mais de um gateway para redundância, mas o sistema não faz rota por prefixo. Esta é a função do softswitch ISP ou gateway que encerra as chamadas. Não queríamos ter redundância nessas funções.

Ao criar uma operadora, o primeiro passo é criar o gateway

![imagem](https://user-images.githubusercontent.com/4958202/153416460-90f10b2b-5adf-4121-afb3-324f10d3a225.png)

Realmente depende da operadora que termina suas chamadas. Você pode ter que retirar alguns números ou números de prefixo antes de entregar à sua operadora. A configuração do gateway permite que você faça isso. A autenticação deve ser por IP, não enviamos credenciais digest com base em nome de usuário e senha.

Após criar o gateway, associe-o à operadora e salve.

![imagem](https://user-images.githubusercontent.com/4958202/153416615-365c5086-f762-48a5-8de5-66a15547cbe9.png)

Veja, muito rápido, a operadora é criada

## Etapa 5 Criando um plano de discagem

Internamente, WeHostVoIP lida com todos os números no formato [E.164](https://en.wikipedia.org/wiki/E.164) com "+" na frente do número. Existem diferentes maneiras de discar em cada país. Às vezes, você precisa prefixar o número que deseja discar com 9 ou 0. No entanto, tudo deve ser normalizado para E164. Criamos alguns presets para o Brasil e os EUA. O dialplan tem três campos muito importantes. Se você deseja criar um plano de discagem, precisa entender [expressões regulares](https://en.wikipedia.org/wiki/Regular_expression). Existe a expressão de correspondência para corresponder ao número, a expressão subs para separar o número em partes usando parênteses e a expressão de substituição para reconstruir o número. Você pode usar duas variáveis ​​_CC (Código do País do Usuário) e _AC (Código de Área do Usuário)_. Se você estiver em um país diferente, entre em contato para que eu possa criar uma predefinição para simplificar seu país. Para começar, vou usar uma predefinição para US sem 9 como prefixo.

![wehostvoip-dialplan](https://user-images.githubusercontent.com/4958202/153420608-15c30d48-8547-4067-a6dc-68281a784796.png)

## Etapa 6 Adicionar números ao inventário

Esta etapa é opcional

Se você tem números ou intervalos DID para vender, você deve especificá-los em seu ISP. Seus usuários poderão alocar DIDs para seus próprios usuários.

![imagem](https://user-images.githubusercontent.com/4958202/153417573-58a74558-add1-4e62-8fc1-7b520cf6466b.png)

## Etapa 7 Criando domínios

Esta etapa é opcional

Você pode criar um domínio diretamente abaixo do seu namespace, como customer1.gettingstarted.com. Para isso você não precisa criar um domínio. No entanto, se seu cliente já usa o Google Apps ou o Azure AD com um domínio específico, você pode adicionar seus domínios aqui. Você precisa verificar a propriedade do domínio adicionando um TXT em um servidor de domínio.

![imagem](https://user-images.githubusercontent.com/4958202/153421332-cc46251c-d353-4ee6-8576-e02af0372a49.png)

## Etapa 8 Criando seu primeiro tenant

A maioria das configurações que você fez até agora são feitas apenas uma vez, exceto para clientes. Após esta configuração você já pode criar
um tenant para atender seus clientes.

Para criar um tenant é muito simples, você começa adicionando um domínio. Pode ser um subdomínio do seu namespace ou o domínio do cliente previamente criado e verificado. Vamos usar customer1 aqui como o domínio.

![imagem](https://user-images.githubusercontent.com/4958202/153424359-8802e406-cc17-4cbf-80a2-57f716180184.png)

Depois de especificar o domínio, você deve especificar os controladores de cliente, operadora, administradores, plano de discagem e de borda de sessão. É um formulário muito rápido. Cada ISP deve negociar seu próprio SBC para operações dependendo do tráfego esperado. Para fins de demonstração, você pode usar demo.wehostvoip.io na porta 61110. Este SBC limita a duração das chamadas em 30 segundos e as chamadas por segundo a 1 chamada a cada 30s. Basta testar e ver se o WeHostVoIP se encaixa no seu modelo de negócios.

## Etapa 9 Acessando seu tenant

Clique no botão de visualização no final da linha (próximo aos botões excluir e editar). Você chegará à interface do tenant como abaixo.

![wehostvoip-tenant-login](https://user-images.githubusercontent.com/4958202/153426130-c153085f-194c-4adb-8391-a01bf98be08d.png)

Assim que o login for concluído, você acessará a interface abaixo.

![imagem](https://user-images.githubusercontent.com/4958202/153426266-4b21a276-114a-404f-bfb6-1f55a32618d7.png)

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

![imagem](https://user-images.githubusercontent.com/4958202/153440169-18a7170a-763a-470e-b725-1dceda01489a.png)

**Não esqueça de adicionar uma senha para SIP e para o Softphone, anote a senha, você precisará da senha antes**

## Passo 11 Cadastrando Alice no WebPhone

Para cadastrar Alice no webphone, basta acessar a url https://phone.wehostvoip.io e adicionar o nome e a senha. Neste ponto, ainda não podemos fazer login com o Google ou o Azure. Para isso é necessário registrar e verificar um domínio. Você só poderá fazer login com o Google ou AzureAd se tiver um domínio sincronizado. Temos um capítulo especial para isso.

![imagem](https://user-images.githubusercontent.com/4958202/153724987-44d9ba93-87b1-44d6-b186-f5059bfdb3d2.png)

Depois de fazer o login, você verá um círculo verde no canto superior direito.

## Etapa 12 Registrando Bob no Softphone

Este é o cliente gratuito para WeHostVoIP. Se você preferir usar um telefone de comunicação unificada completo, entre em contato conosco para obter um plano de atualização, pois o telefone UC é cobrado separadamente. A marca de um novo telefone UC envolve várias etapas, incluindo o registro de um número DUNS e a publicação na Apple e na Google Store. Esses recursos não são abordados no Guia de Introdução.

Você só pode usar o softphone se estiver usando o Windows 7 ou posterior. Baixe o softphone em https://uc.wehostvoip.io/downloads/wevoip-3.20.7002.exe, extraia e execute o arquivo

Após a instalação, faça login usando o nome de usuário e a senha do **softphone**.

![imagem](https://user-images.githubusercontent.com/4958202/153725448-8a30f3bf-c243-46b4-8fd7-d2bd97c47749.png)

## Etapa 13 Faça uma chamada entre telefones

Basta chamar Alice e Bob por seus nomes. Você também pode usar seus apelidos alice (1000) e bob (1001). Disque 1000 de bob e 1001 de alice para testar a discagem.

## Etapa 14 Adicionar um país no grupo de segurança

Para evitar fraudes, os assinantes não têm permissão por padrão para fazer chamadas PSTN. Você terá que autorizar os países ou prefixos para permitir chamadas de saída. Nós tornamos esse processo muito fácil. Em nosso cas estamos adicionando EUA. Quando você seleciona EUA, ele seleciona todos os códigos de área da NANPA pertencentes aos EUA e não carrega destinos do Caribe frequentemente usados ​​para fraude.

![imagem](https://user-images.githubusercontent.com/4958202/153725725-aba5e01b-2a59-4c56-8357-9b3f7391933b.png)

## Etapa 15 Fazer uma chamada para um destino externo

Disque 22224444, você deve receber uma mensagem engraçada. Como estamos usando ogateway de teste sua chamada não está indo para o PSTN. Se você quiser que sua chamada vá para o PSTN, você deve adicionar sua própria operadora.

## Etapa 16 Testando as chamadas recebidas

Testar uma chamada recebida é um pouco mais difícil. Se você adicionou uma transportadora real e você tem um número real, o processo é muito fácil. No entanto, para os propósitos deste Guia de introdução, usaremos um softphone conectado ao gateway de teste para conectar-se ao nosso SBC demo.wehostvoip.io.
