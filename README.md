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

Para ativar ou desativar o Controle de Aplicativo Inteligente entre os pontos de extremidade da sua organização, você pode definir o valor do registro DWORD *(VerifiedAndReputablePolicyState )* em **HKLM\SYSTEM\CurrentControlSet\Control\CI\Policy** um dos valores listados abaixo. Depois de alterar o valor do registro, você deve reiniciar o dispositivo ou executar **RefreshPolicy.exe** para que a alteração entre em vigor.

```
Valor 	Descrição
0 	Desativado
1 	Impor
2 	Avaliação
```






