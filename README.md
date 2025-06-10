Desbloqueador de Compartilhamento de Impressora (Printer Share Fix)
Uma ferramenta simples de um clique para corrigir a vulnerabilidade de spooler de impressão do Windows (CVE-2021-1678) que impede o compartilhamento de impressoras USB em rede.

O Problema
Após as atualizações de segurança do Windows, foi introduzida uma nova configuração que, por padrão, aumenta o nível de autenticação para comunicação via RPC. Na prática, isso impede que computadores em uma rede local instalem impressoras USB compartilhadas, frequentemente exibindo o "erro 0x0000011b".

Esta ferramenta automatiza a correção necessária, tornando o processo rápido e acessível para qualquer usuário.

Como Usar 🛠️
O uso do programa é extremamente simples.

Baixe o arquivo Impressoras.exe da seção Releases https://github.com/CarlosAndradeP/desbloqueio-de-impressora-usb-na-rede./releases/.

Execute como Administrador: Clique com o botão direito no arquivo e selecione "Executar como administrador". Isso é essencial para que o programa tenha permissão para alterar o Registro do Windows.

Aplique a Correção: Clique no único botão da tela para aplicar a alteração no registro.

Reinicie o Computador: Uma reinicialização é necessária para que as alterações entrem em vigor.

Após reiniciar, sua impressora USB deverá estar acessível para instalação em outros computadores da rede.

Detalhes Técnicos ⚙️
O programa realiza uma única e específica alteração no Registro do Windows para desativar o novo requisito de autenticação.

Caminho do Registro:

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Print

Chave Adicionada:

Nome: RpcAuthnLevelPrivacyEnabled

Tipo: REG_DWORD (32 bits)

Valor: 0

Ao definir este valor como 0, o nível de privacidade de autenticação RPC é desativado para o serviço de impressão, restaurando a funcionalidade de compartilhamento anterior.

Para Desenvolvedores 👨‍💻
Este programa foi criado com Clickteam Fusion.

Para editar ou recompilar o projeto, você precisará do Clickteam Fusion.

O arquivo fonte do projeto é Impressoras.mfa.

O executável gerado é Impressoras.exe.

Aviso ⚠️
Este programa modifica o Registro do Windows. A edição incorreta do registro pode levar a problemas de instabilidade no sistema operacional. Use esta ferramenta por sua conta e risco. Embora a alteração seja específica e testada, o autor não se responsabiliza por quaisquer danos que possam ocorrer em seu sistema.
