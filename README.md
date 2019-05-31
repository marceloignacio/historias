**DETALHES DA IMPLEMENTAÇÃO**

- ***Para ajustar a questão visual, será criada uma barra de notificações, na parte superior do Omni, onde teremos os seguintes comportamentos:***
	-- Na barra, deverá existir um ícone de notificações onde serão exibidas as notificações do sistema, entre elas, que o Omni está Offline;
	-- Esse mesmo ícone, desaparecerá quando o sistema retomar a conectividade com o banco cartão;
	-- O sistema deverá verificar o status de conectividade com o banco Cartão, caso o retorno seja falso, sobre a barra existente, deverá ser exibida uma segunda barra, na cor vermelha, que seja possível fechamento, em sobreposição, alertando o usuário de que o Omni está em modo Offline;
	-- Essa verificação deverá ser executada duas vezes, com intervalo de tempo menor, sempre quando o primeiro teste retornar como falso (*Online=false*), evitando um falso negativo, só então o sistema entrará em "modo Offline";
	-- Deverá ser exibida mensagem ao operador de que o Omni está Offline, informando quais recursos ele terá nessa condição e também quais ações deverá adotar a fim de contornar essa situação. Quando o usuário fechar essa barra de alerta, deverá permencer no ícone "Offline" enquanto o sistema estiver sem conectividade, permitindo que o usuário tenha acesso sempre que desejar;
	-- Essa verificação de status, deverá ser executada a cada X (definir junto com o tempo do job de verificação de status de filial) tempo, onde permanecendo a condição de Offline, o sistema deverá exibir o alerta novamnete sobre a barra do sistema Omni e também a barra com informação dos recursos disponiveis nessa condição;
	-- Quando o sistema entrar em modo Offline, o sistema deverá ajustar o parâmetro *tefHabilitado=false*, para que o TEF passe a operar em modo Offline (TEF desabilitado). Isso obrigará o uso do POS, mas alterará o comportamento do Omni em relação ao TEF;
