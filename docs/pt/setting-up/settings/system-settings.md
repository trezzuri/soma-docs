# Configurações do sistema


**Configuração do sistema contém configurações para a configuração da conta em todo o sistema.**


Você pode localizar o SOMA para usar fuso horário, data, número ou formato de moeda específicos e também definir a expiração da sessão global por meio das Configurações do sistema.


Para abrir as Configurações do sistema, acesse:



> 
> Página inicial > Configurações > Configurações do sistema
> 
> 
> 


![Configurações do sistema](/private/files/system-settings.png)


## 1. Seções nas configurações do sistema


### 1.1 Geral


* **País**: Você pode definir o país padrão aqui, ele será obtido ao criar novos endereços. Se sua empresa tiver várias filiais em diferentes países, escolha o local da sede.
* **Fuso horário**: define a hora automaticamente com base no fuso horário.
* **Idioma**: Define o idioma global para a conta SOMA. Em seguida, o idioma será alterado em todos os menus, transações, mestres, etc.
* **Desativar compartilhamento de documentos**: desativa o acesso de compartilhamento para todos os usuários do sistema (exceto Administrador) para garantir que o acesso seja concedido apenas por meio de permissões. Os usuários só poderão ver com quem o documento é compartilhado e não compartilhar o documento em si. Além disso, atribuir um documento a um usuário será **bloqueado** se o responsável não tiver acesso ao documento.


### 1.2 Formato de data e número


* **Formato da data**: Formato no qual as datas serão exibidas. Por exemplo, dd.mm.aaaa ou mm/dd/aaaa. Isso depende de como as datas são formatadas em sua região.
* **Formato da hora**: Formato no qual a hora será exibida. Você pode optar por mostrar (`HH:mm:ss`) ou ocultar os segundos definindo a opção como (`HH:mm`) .
* **Formato numérico**: Formato no qual os números serão formatados. Por exemplo, 1.000 ou 1.000,00.
* **Float Precision**: O número de zeros exibidos após o ponto decimal para quantidades, etc. O intervalo é de 2 a 9. O padrão é 3.
* **Precisão da moeda**: número de zeros exibidos após o ponto decimal para valores de moeda. Se deixado em branco, será baseado no **Formato numérico**.
* **Primeiro dia da semana**: pode ser usado para configurar o dia de início da semana. Isso afeta os filtros dinâmicos da semana usados ​​nas exibições de lista e relatório, layout de seleção de data e exibição de calendário.
* **Método de arredondamento**: especifica o método de arredondamento a ser usado em todos os lugares. O método de arredondamento padrão é o Banker's Rounding, que arredonda 0,5 para o número par mais próximo. "Arredondamento Comercial" que arredonda 0,5 para o próximo número longe de zero, por exemplo 1,5 torna-se 2,0 e -1,5 torna-se -2,0 quando arredondado.


### 1.3 Backups


No SOMA você pode fazer backup do banco de dados, bem como de seus arquivos. Os backups de banco de dados são criados automaticamente, enquanto os backups de arquivos precisam ser baixados explicitamente.


Este campo mostra o número de backups após os quais os mais antigos serão excluídos. Por padrão, 3 backups são salvos em 24 horas. Novos backups são criados automaticamente a cada poucas horas e o backup mais recente substituirá o mais antigo. Para fazer backup dos arquivos, clique no botão Baixar backup de arquivos no formulário Baixar backups.


Manter backups regulares do seu sistema é uma boa prática em caso de algum contratempo e você deseja reverter ou apenas para seus registros.


### 1.4 Permissões


Usando permissões, você pode limitar o acesso do usuário aos tipos de documento. A limitação pode ser baseada em campos como Empresa, Território, Filial, etc. Para saber mais sobre Permissões de Usuário, [clique aqui](/docs/pt/setting-up/users-and-permissions/user -permissions).


Se a caixa de seleção Aplicar permissões estritas do usuário estiver marcada e a permissão do usuário for definida para um DocType para um usuário, todos os documentos em que o valor do link estiver **em branco** não serão exibidos para esse usuário .


Isso é feito de:



> 
> Página inicial > Usuários e permissões > Permissões > Permissões do usuário
> 
> 
> 


Por exemplo: Se você definir Permissões de usuário para território e definir o valor como Índia. Se a caixa de seleção estiver desmarcada, todas as transações (pedidos de venda, cotações) com a Índia e **em branco** serão mostradas aos usuários.


Se a caixa de seleção Apply Strict User Permissions estiver marcada, os documentos, onde Territory está em branco, não serão mostrados aos usuários.


### 1.5 Segurança


* **Expiração da sessão**: Número de horas ociosas após as quais você será desconectado de uma sessão. Isso ajuda em uma melhor segurança. Por exemplo, se não houver atividade por 6 horas, sua conta será desconectada.
* **Session Expiry Mobile**: expiração da sessão quando conectado a partir de um telefone celular.
* **Expiração da chave de compartilhamento do documento (em dias)**: número de dias após o qual o "link da Web do documento" enviado por e-mail expirará.
* **Permitir apenas uma sessão por usuário**: se você deseja usar um único conjunto de credenciais para vários usuários, marque esta caixa de seleção. O número de sessões simultâneas pode ser alterado em User master. As sessões de celular não são contadas aqui.
* **Permitir login usando número de celular**: Ao marcar a caixa de seleção 'Permitir login usando número de celular', você pode fazer login no SOMA usando um número de celular válido definido em sua conta de usuário.
* **Permitir login usando o nome de usuário**: permite o login do usuário por meio do nome de usuário definido em [Usuário mestre](/docs/pt/setting-up/users- and-permissions/adding-users).
* **Mostrar erro completo e permitir relatórios de problemas ao desenvolvedor**: isso exibirá todo o erro na tela e permitirá relatar problemas. Se você tiver conhecimento técnico nessa área, poderá ter uma ideia melhor do erro lendo toda a mensagem.
* **Remover tags EXIF ​​de imagens carregadas**: os metadados armazenados em arquivos de imagem no formato de arquivo EXIF ​​podem ser explorados para obter informações confidenciais do usuário. Esta opção permite que os usuários removam esses dados das imagens antes de fazer o upload.
* **Permitir links de visualização da Web mais antigos (inseguros)**: a configuração que permite links da Web sem expiração.
Observação: links da Web mais antigos (gerados na versão 13) são considerados inseguros, pois não expiram. Recomenda-se manter esta configuração desmarcada.


### 1.6 Senha


* **Forçar usuário a redefinir a senha**: Número de dias após os quais uma redefinição de senha é obrigatória. 0 significa sem limite.
* **Habilitar política de senha**: habilita um verificador de força de senha para que os usuários tenham que usar senhas fortes para seu login.
* **Pontuação mínima da senha**: pontuação para o verificador de força da senha


	+ 2 é médio
	+ 3 é forte
	+ 4 é muito forteA complexidade é baseada no número de caracteres, letras maiúsculas, caracteres especiais, etc.
* **Duração de Expiração do Link de Redefinição de Senha**: Esta configuração é usada para definir a duração após a qual o link rassword de redefinição recém-criado expira. A expiração padrão para o link de redefinição de senha é de 20 minutos. Defini-lo como "0 segundos" desativa a funcionalidade "Redefinir a expiração do link da senha".
* **Limite de geração de link de redefinição de senha**: usando esta configuração, o limite para o número de solicitações de redefinição de senha por hora pode ser definido. O limite padrão é 3. Defini-lo como 0 permitirá solicitações ilimitadas de geração de link de redefinição de senha.


### 1.7 Segurança de força bruta


* **Permitir tentativas de login consecutivas**: logins consecutivos após os quais você será bloqueado da conta por um período específico. Isso ajuda se um intruso tentar fazer login na sua conta.
* **Permitir login após falha**: segundos após os quais uma tentativa de login será permitida após tentativas consecutivas malsucedidas.


### 1.8 Autenticação de dois fatores


As configurações para autenticação de dois fatores podem ser definidas aqui.


Ao marcar 'Ativar Autenticação de Dois Fatores', as duas opções a seguir serão exibidas.


* **Ignorar a autenticação de dois fatores para usuários que fazem login a partir de um endereço IP restrito**: os usuários que fazem login a partir de endereços IP restritos não serão solicitados a fazer a autenticação de dois fatores. Você pode restringir os IPs do usuário mestre no campo Restringir IP.
* **Ignorar verificação de endereço IP restrito se Autenticação de dois fatores ativada**: Se marcada, todos os usuários podem fazer login com Autenticação de dois fatores, independentemente de seu IP ser restrito ou não.

< /li>
* **Método de autenticação de dois fatores**: selecione o método de autenticação a ser usado - aplicativo OTP, SMS ou e-mail.
* **Tempo de expiração da página de imagem do código QR**: tempo de expiração da imagem do QRCode se "Aplicativo OTP" for selecionado no método.
* Nome do emissor OTP da senha única.


![Two Factor Auth](/files/twofactor-settings.png)


### 1.9 E-mail


* **Endereço do rodapé do e-mail**: nome da organização, endereço e outros detalhes podem ser adicionados aqui. Isso será definido como padrão em todos os e-mails enviados.
* **Desativar rodapé de e-mail padrão**: se marcado, o rodapé de e-mail padrão será desativado para e-mails enviados.
* **Ocultar rodapé em relatórios de e-mail automático**: se marcado, os rodapés serão ocultados em [Relatórios de e-mail automático](/docs/pt/setting-up/email/auto- email-reports).
* **Enviar link de visualização da Web do documento no e-mail**: o SOMA possui uma visualização do portal disponível onde partes como Clientes e Fornecedores podem se inscrever e visualizar seu histórico de pedidos. Ao enviar uma transação por e-mail para sua parte, você também pode enviar um link da web para visualizar o mesmo documento no portal de sua conta SOMA. Esta opção habilitará esta funcionalidade.


![Email Footer](/files/email-footer.png)


### 1.10 Bate-papo


* **Ativar bate-papo**: esta opção ativará o bate-papo no aplicativo, que pode ser usado para se comunicar com outros funcionários.


### 1.10 Atualizações do sistema


* **Desativar notificação de atualização do sistema**: esta opção desativa todas as notificações de atualização de versão acionadas pelo aplicativo.


### 2. Tópicos Relacionados


1. [Configuração da empresa](/docs/pt/setting-up/company-setup)
2. [Padrões globais](/docs/pt/setting-up/settings/global-defaults)
3. [Mostrar ou ocultar módulos](/docs/pt/setting-up/settings/show-hide-modules)
