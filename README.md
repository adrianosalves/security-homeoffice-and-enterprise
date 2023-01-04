# Security para HomeOffice e Pequenas Empresas

Com o avanço das tecnologias para proteção de vulnerabilidade e malwares é necessários que pessoas que trabalha em HomeOffice e dentro das Empresas precisam se adequar as novas tecnologias para minimizar e proteger contra ataques ciberneticos que ocorre a todos momento.

Vamos listas algumas novas tecnologias para a proteção e gerenciamento de computadores mostrando a camada de proteção necessária e suas vantagens:

Alem do Antivírus que protege os computadores contra malwares, com passar dos anos surgiu novas tecnologias que proteger contra novas tecnicas de exploração e vulnerabilidade em uma rede de computadores.

Segue abaixo algumas camadas de proteçao:

- Antívirus (Bloquea Malware conhecidos)
- Controle de Aplicativos (Permite Apenas Programas Confiavel a ser executados)
- WebSecurity (Permite o Bloqueios de Links Maliciosos)
- EDR (EndPoint Detecção e Resposta - Monitorar e coletar dados de atividade de pontos de extremidade que possam indicar uma ameaça.)
- MDR (Detecção e Resposta Gerenciada - combinam análises avançadas, inteligência de ameaças e experiência humana em investigação e resposta a incidentes implantados nos níveis de host e rede.)
- RMM (Gerenciamento e Monitoramento Remoto - Permite Suporte Remoto e Gerenciamento dos Computadores Remoto)

# Microsoft - Control de Aplicativo para Windows

fonte: https://learn.microsoft.com/pt-br/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control

Com milhares de novos arquivos mal-intencionados criados todos os dias, o uso dos métodos tradicionais, como soluções antivírus - detecção com base em assinaturas para combater malware, oferece uma defesa inadequada contra novos ataques.

Na maioria das organizações, as informações são o ativo mais valioso e garantir que apenas usuários aprovados tenham acesso a essas informações é imperativo. No entanto, quando um usuário executa um processo, esse processo tem o mesmo nível de acesso aos dados que o usuário tem. Dessa forma, as informações confidenciais podem ser facilmente excluídas ou transmitidas para fora da organização caso um usuário execute um software mal-intencionado consciente ou inconscientemente.

O controle de aplicativo pode ajudar a mitigar esses tipos de ameaças à segurança restringindo os aplicativos que os usuários podem executar e o código executado no System Core (kernel). As políticas de controle de aplicativo também podem bloquear scripts e MSIs não assinados e restringir Windows PowerShell a serem executadas no Modo de Linguagem Restrita.

O controle de aplicativo é uma linha de defesa crucial para proteger as empresas, dado o cenário de ameaças de hoje, e tem uma vantagem inerente sobre as soluções antivírus tradicionais. Especificamente, o controle de aplicativo se afasta de um modelo de confiança do aplicativo em que todos os aplicativos são considerados confiáveis para um em que os aplicativos devem ganhar confiança para serem executados. Muitas organizações, como a Australian Signals Directorate, entendem a importância do controle de aplicativos e frequentemente citam o controle de aplicativo como um dos meios mais eficazes para lidar com a ameaça de malware baseado em arquivo executável (.exe, .dll etc.).

## Windows Defender Controle de Aplicativo (WDAC)

Para ativar ou desativar o Controle de Aplicativo Inteligente entre os pontos de extremidade da sua organização, você pode definir o valor do registro DWORD *(VerifiedAndReputablePolicyState )* em **HKLM\SYSTEM\CurrentControlSet\Control\CI\Policy** um dos valores listados abaixo. Depois de alterar o valor do registro, você deve reiniciar o dispositivo ou executar **RefreshPolicy.exe** (https://www.microsoft.com/download/details.aspx?id=102925) para que a alteração entre em vigor.

```
Valor 	Descrição
0 	Desativado
1 	Impor
2 	Avaliação
```

https://webapp-wdac-wizard.azurewebsites.net/

## Microsoft Guia de Designe WAC

fonte: https://learn.microsoft.com/pt-br/windows/security/threat-protection/windows-defender-application-control/wdac-wizard-create-supplemental-policy?source=recommendations

**Criando uma nova política suplementar com o Assistente**

A partir Windows 10 versão 1903, Windows Defender WDAC (Controle de Aplicativo) dá suporte à criação de várias políticas ativas em um dispositivo. Uma ou mais políticas complementares permitem que os clientes expandam uma política de base do WDAC para aumentar o círculo de confiança da política. Uma política suplementar pode expandir apenas uma política base, mas vários suplementos podem expandir a mesma política base. Quando políticas suplementares estiverem sendo usadas, os aplicativos permitidos pela base ou por sua política/política suplementar poderão ser executados.

As informações de pré-requisito sobre o controle de aplicativo podem ser acessadas por meio do guia de design do WDAC. Esta página descreve as etapas para criar uma política de controle de aplicativo suplementar, configurar as opções de política e as regras do signatário e do arquivo.

![image](https://user-images.githubusercontent.com/33209944/210555952-b0d22951-025c-41ca-9001-68f40feaf9e4.png)


## Microsoft Guia Operacional:

fonte: https://learn.microsoft.com/pt-br/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control-operational-guide

**CITool.exe referência técnica**

A Ferramenta de CI facilita Windows Defender gerenciamento de políticas do WDAC (Controle de Aplicativo) para administradores de TI. A ferramenta CI pode ser usada para gerenciar Windows Defender políticas de Controle de Aplicativo e Tokens de CI. Este artigo descreve como usar a Ferramenta de CI para atualizar e gerenciar políticas. Atualmente, a Ferramenta de CI está incluída no Windows 11, versão 22H2.





