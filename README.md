# resumo-do-lab-computacao-em-nuvem
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

## O que é computação em nuvem:
é a entrega de serviços de computação pela Internet. Os serviços de computação incluem infraestrutura de TI comum, como máquinas virtuais, armazenamento, banco de dados e rede. Os serviços de nuvem também expandem as ofertas tradificonais de TI para incluir itens como LoT (Internet das Coisas), ML (machine learning) e Ia (inteligência artificial).

Como a computação em nuvem usa a Internet para fornecer esses serviços, ela não precisa ficar restrita pela infraestrutura física da mesma forma que um datacenter tradicional. Isso significa que, se você precisar aumentar rapidamente sua infraestrutura de TI, não precisará esperar para construir um novo datacenter; você pode usar a nuvem para expandir rapidamente seu volume de TI.

##Descrever o modelo de responsabilidade compartilhada

Com o modelo de responsabilidade compartilhada, as responsabilidades são compartilhadas entre o provedor de nuvem e o consumidor. Segurança física, energia, resfriamento e conectividade de rede são responsabilidade do provedor de nuvem. O consumidor é responsável pelos dados e pelas informações armazenados na nuvem. O consumidor também é responsável pela segurança de acesso, o que significa que você só dá acesso àqueles que precisam.

Então, para algumas coisas, *a responsabilidade depende da situação*. Se você estiver usando um banco de dados SQL na nuvem, o provedor de nuvem será responsável pela manutenção do banco de dados real. No entanto, você ainda será responsável pelos dados que são ingeridos no banco de dados. Se você implantasse uma máquina virtual e instalasse um banco de dados SQL nela, seria responsável pelos patches e atualizações do banco de dados, além da manutenção dos dados e das informações armazenados no banco de dados.
Ao usar um provedor de nuvem, você sempre será responsável por:

- Informações e dados armazenados na nuvem
- Dispositivos que têm permissão para se conectar à nuvem (telefones celulares, computadores e assim por diante)
- Contas e identidades das pessoas, serviços e dispositivos em sua organização

***O provedor de nuvem é sempre responsável por:***

- Datacenter físico
- Rede física
- Hosts físicos

***Seu modelo de serviço determinará a responsabilidade por coisas como:***

- Sistemas operacionais
- Controles de rede
- Aplicativos
- Identidade e infraestrutura

- **Nuvem privada**: é, de certa forma, a evolução natural de um datacenter corporativo. Ela é uma nuvem (que fornece serviços de TI pela Internet) usada por uma única entidade. A nuvem privada fornece um controle muito maior para a empresa e o departamento de TI. No entanto, ela também tem mais custos e menos benefícios em relação a uma implantação de nuvem pública. Por fim, uma nuvem privada pode ser hospedada em seu datacenter local. Ela também pode ser hospedada em um datacenter dedicado externo, até mesmo por terceiros que tenham dedicado esse datacenter à sua empresa.
- **Nuvem pública**: é criada, controlada e mantida por um provedor de nuvem de terceiros. Com uma nuvem pública, qualquer pessoa que queira comprar serviços de nuvem pode acessar e usar os recursos. A disponibilidade pública geral é uma diferença fundamental entre nuvens públicas e privadas.
- **Nuvem híbrida**: é um ambiente de computação que usa nuvens públicas e privadas em um ambiente interconectado. pode ser usado para permitir que uma nuvem privada escale para atender a uma demanda maior temporária implantando recursos de nuvem pública. A nuvem híbrida pode ser usada para fornecer uma camada adicional de segurança. Por exemplo, os usuários podem escolher com flexibilidade quais serviços manter na nuvem pública e quais implantar na infraestrutura de nuvem privada.


# **Confiabilidade e previsibilidade na nuvem**

- **Confiabilidade:** Resiliência é a capacidade que um sistema tem de se recuperar de falhas e continuar funcionando. Ela também é um dos pilares do Microsoft Azure Well-Architected Framework.
    
    Devido ao design descentralizado, a nuvem naturalmente dá suporte a uma infraestrutura confiável e resiliente. Com um design descentralizado, a nuvem permite que você tenha recursos implantados em várias regiões do mundo. Com essa escala global, mesmo que ocorra um evento catastrófico em uma região, as outras regiões ainda estarão em funcionamento. 
    

- **Previsibilidade:**  Previsibilidade pode se concentrar na previsibilidade de desempenho ou na previsibilidade de custo. Tanto a previsibilidade de desempenho quanto a de custo são bastante influenciadas pelo Microsoft Azure Well-Architected Framework. Implante uma solução criada em torno dessa estrutura e você terá uma solução cujo custo e desempenho são previsíveis.

- **Desempenho:** Se concentra em prever os recursos necessários para oferecer uma experiência positiva aos clientes. O dimensionamento automático, o balanceamento de carga e a alta disponibilidade são apenas alguns dos conceitos de nuvem que dão suporte à previsibilidade de desempenho. Se de repente você precisar de mais recursos, o dimensionamento automático poderá implantar recursos adicionais para atender à demanda e depois reduzir a implantação quando a demanda cair. Ou se o tráfego estiver bem concentrado em uma área, o balanceamento de carga ajudará a redirecionar parte da sobrecarga para áreas menos sobrecarregadas.

- **Custo:** Se concentra em prever o custo dos gastos com a nuvem. Com a nuvem, você pode acompanhar o uso de recursos em tempo real, monitorar os recursos para garantir a maior eficiência de uso possível e aplicar a análise de dados para encontrar padrões e tendências que ajudam a planejar melhor as implantações de recursos. Operando na nuvem e usando a análise e as informações da nuvem, você pode prever custos futuros e ajustar os recursos conforme o necessário.


## Descrever a infraestrutura como serviço

O IaaS (infraestrutura como serviço) é a categoria mais flexível de serviços de nuvem, pois oferece o máximo de controle sobre os recursos de nuvem. Nesse modelo, o provedor de nuvem é responsável por manter o hardware, a conectividade de rede (com a Internet) e a segurança física.  Você é responsável por todo o resto: instalação, configuração e manutenção do sistema operacional; configuração de rede; configuração de banco de dados e armazenamento e assim por diante. Com o IaaS, basicamente o hardware é alugado em um datacenter de nuvem, mas cabe a você decidir o que fazer com ele.

- **Modelo de responsabilidade compartilhada**
    
    No IaaS, a maior parte da responsabilidade fica com você. O provedor de nuvem é responsável por manter a infraestrutura física e o acesso à Internet. Você é responsável por: instalação e configuração, aplicação de patch, atualizações e segurança.
    
- **Cenários**
    
    Alguns cenários comuns em que o IaaS faz sentido incluem:
    
    - Migração lift-and-shift(Elevação e deslocamento): Você está configurando recursos de nuvem semelhantes aos do datacenter local e apenas migra os elementos em execução local para execução na infraestrutura IaaS.
    - Teste e desenvolvimento: você estabeleceu configurações para ambientes de desenvolvimento e teste que precisa replicar rapidamente. Você pode inicializar ou desativar os diferentes ambientes rapidamente com uma estrutura de IaaS, mantendo o controle completo.

## Descrever a plataforma como serviço

O PaaS (Plataforma como serviço) é um meio termo entre alugar espaço em um datacenter (infraestrutura como serviço) e pagar uma solução completa e implantada (software como serviço). Nesse modelo, o provedor de nuvem mantém a infraestrutura física, a segurança física e a conexão com a Internet. Ele também mantém os sistemas operacionais, o middleware, as ferramentas de desenvolvimento e os serviços de business intelligence que compõem uma solução de nuvem. Você não precisa se preocupar com o licenciamento nem com a aplicação de patch em sistemas operacionais e bancos de dados.

O PaaS é adequado para fornecer um ambiente de desenvolvimento completo sem a preocupação de manter toda a infraestrutura de desenvolvimento.

- **Modelo de responsabilidade compartilhada**
    
    O PaaS divide a responsabilidade entre você e o provedor de nuvem. O provedor de nuvem é responsável por manter a infraestrutura física e o acesso à Internet, como no IaaS. No modelo de PaaS, o provedor de nuvem também mantém os sistemas operacionais, os bancos de dados e as ferramentas de desenvolvimento. Pense no PaaS como o uso de um computador conectado ao domínio: o departamento de TI mantém o dispositivo com atualizações, patches e renovações regulares.
    
    Dependendo da configuração, você ou o provedor de nuvem pode ser responsável pelas configurações de rede e a conectividade no ambiente de nuvem, a segurança da rede e do aplicativo e a infraestrutura de diretório.
    
- **Cenários:**
    
    Alguns cenários comuns em que o PaaS faz sentido incluem:
    
    - Estrutura de desenvolvimento: O PaaS fornece uma estrutura que os desenvolvedores podem usar como base para desenvolver ou personalizar aplicativos baseados em nuvem. Semelhante à forma como você cria uma macro do Excel, o PaaS permite aos desenvolvedores criar aplicativos usando componentes de software internos. São incluídos recursos de nuvem, como escalabilidade, alta disponibilidade e a funcionalidade de multilocatário, reduzindo a quantidade de codificação que os desenvolvedores precisam realizar.
    - Análise ou business intelligence: as ferramentas fornecidas como serviço com o PaaS permitem que as organizações analisem e minerem dados, encontrando insights e padrões e prevendo res  ultados para aprimorar a previsão, as decisões de design de produto, o retornos sobre investimentos e outras decisões de negócios.
    

## Descrever o software como serviço

O SaaS (software como serviço) é o modelo de serviço de nuvem mais completo do ponto de vista do produto. Nesse modelo, você está essencialmente alugando ou usando um aplicativo totalmente desenvolvido. Email, software financeiro, aplicativos de mensagens e software de conectividade são exemplos comuns de uma implementação de SaaS.

Embora o modelo de SaaS possa ser o menos flexível, ele também é o mais fácil de colocar em funcionamento. Ele requer a menor quantidade de conhecimento técnico ou experiência para o emprego total.

- **Modelo de responsabilidade compartilhada:**
    
    O SaaS é o modelo que coloca a maior responsabilidade sobre o provedor de nuvem e a menor responsabilidade com o usuário. Você é responsável pelos dados que coloca no sistema, pelos dispositivos que permite que se conectem ao sistema e pelos usuários que têm acesso. Quase todo o resto é responsabilidade do provedor de nuvem. O provedor de nuvem é responsável pela segurança física dos datacenters, pela energia, pela conectividade de rede e pelo desenvolvimento e aplicação de patch dos aplicativos.
    
- **Cenários:**
    
    Alguns cenários comuns de SaaS são:
    
    - Email e mensagens.
    - Aplicativos de produtividade empresarial.
    - Controle de finanças e despesas.
