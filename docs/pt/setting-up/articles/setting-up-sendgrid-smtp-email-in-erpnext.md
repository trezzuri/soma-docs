# Configurando Email SMTP Sendgrid no ERPNext


SMTP, ou protocolo simples de transferência de e-mail, é uma maneira rápida e fácil de enviar e-mail de um servidor para outro. O SendGrid fornece um serviço SMTP que permite que você entregue seu e-mail por meio de nosso servidor, em vez de seu cliente ou servidor. O ERPNext vem integrado com um cliente de e-mail configurado para que você possa enviar e receber e-mails no ERPNext e anexar a documentos, se necessário.
**Integrando a API da Web do SendGrid**A API SMTP do SendGrid permite que os desenvolvedores especifiquem instruções de tratamento personalizadas para e-mail usando um cabeçalho X-SMTPAPI inserido na mensagem.
**Etapa 1:** você precisa criar uma chave de API para autenticar seu aplicativo. Neste caso, *ERPNext*. Saiba mais sobre a integração do SendGrid com SMTP [aqui](https://sendgrid.com/docs/API_Reference/SMTP_API/integrating_with_the_smtp_api.html)
![](/files/5Wqn0hV.png)
  
**Etapa 2:** Assim que sua *chave API* for criada, você precisa configurá-la em sua conta ERPNext > Criar uma **Nova** **Conta de e-mail**.
**Endereço de e-mail:** *Seu endereço de e-mail***ID de login do e-mail:** *Chave de API* [chave de API gerada na Etapa 1]**Senha:** *Sua senha***Serviço:** Selecione " *EnviarGrid*"
![](/files/Q9to7Iu.png)
  
  
Agora **salve** esta informação e você configurou com sucesso o SendGrid SMTP Email no ERPNext.
Poder para você!
  
-----**﻿**