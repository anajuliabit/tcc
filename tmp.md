In the abstract, open source blockchain networks such as Ethereum and Bitcoin are
kits that allow you to pop up an economic system in software, complete with account management and a 
native unit of exchange to pass between accounts. Kind of like the game Monopoly. People call these native 
units of exchange coins, tokens, or cryptocurrencies, but they’re no different from tokens in any other
system: they’re a form of money (or scrip) that is usable only within that system. Blockchains work 
something like mesh networks or local area networks (LANs); they are merely connected to other “peer”
computers running the same software. When you want to make one of these peer-to-peer (P2P) networks 
accessible through a web browser, you need to use special software libraries such as Web3.js to connect an
application’s front end (the GUI you see in a browser), via JavaScript APIs, to its back end (the blockchain).
In Ethereum, you can take this concept one step further by easily writing financial contracts with other 
users inside the system. As you’ll see, these financial contracts are called smart contracts.
The key component is this idea of a Turing-complete blockchain. ... As a data structure, it
works kind of the same way that Bitcoin works, except the difference in Ethereum is,
it has this built-in programming language.
—Vitalik Buterin, inventor of Ethereum3

In Ethereum, smart contracts are written in the programming language Solidity, which you’ll learn about in Chapter 4. Turing completeness was an advantage that many developers quickly latched onto, but more important is Ethereum’s ability to save state. In computing, a simple definition of a stateful system is one that can detect changes to information and remember them over time.
1Ethereum Blog, “Visions, Part 1: The Value of Blockchain Technology,” https://blog. Ethereum.org/2015/04/13/visions-part-1-the-value-of-blockchain-technology/, 2015. 2American Banker, “Blockchain Won’t Make Banks Any Nimbler,” www.americanbanker.com/ bankthink/blockchain-wont-make-banks-any-nimbler-1079190-1.html, 2016.
3YouTube, “Technologies That Will Decentralize the World,” www.youtube.com/watch?v= er-k3ehpFaM&feature=share, 2016.
 2
Chapter 1 ■ Bridging the BloCkChain knowledge gap
Imagine a computer with no hard drive; you couldn’t do much with it. It would be like a calculator, the contents of its memory fleeting. The ability to engineer interactions between users in the future, and under certain conditions, is a powerful addition to a blockchain. It allows developers to introduce control flow into cryptocurrency transaction programming. This is the biggest distinction between Ethereum and Bitcoin, but not the only one, as you’ll see.
■ Note Control flow refers to the order in which computing instructions are executed or evaluated. examples are conditional statements (if this, then that) and loops (which run repeatedly until certain conditions are met).
In Bitcoin, all transactions happen as soon as possible. Because of Bitcoin’s lack of statefulness, it has to execute transactions all in one go. The blockchain as envisioned by Bitcoin’s creator(s) was a distributed transaction ledger that kept a running tally of everyone’s bitcoin balances in the network. (A stylistic note for close readers: Bitcoin the network is written in the uppercase, and bitcoin the token in lowercase.) In Ethereum, a similar system is made extensible in a standardized way.
Secondarily, this common scripting language makes it more straightforward for blockchains that share the Ethereum protocol to share data with one another, enabling groups that use separate blockchains to share information and value with each other.

\begin{resumo}
  (provisório) À medida que a tecnologia blockchain continua a ganhar adoção, percebe-se um crescimento na demanda por funcionalidades que viabilizem sua aplicação em situações reais. No âmbito deste artigo técnico, nos inspiramos na recente publicação da Visa como premissa para a exploração da implementação de pagamentos
  programáveis automatizados em carteiras de auto custódia. Adentramos na esfera do conceito de Abstração de
  Contas e propomos uma execução codificada em Solidity com o propósito de habilitar pagamentos recorrentes
  originados diretamente de carteiras sob controle do usuário. Por meio desta sondagem, nosso intuito   primordial é fornecer perspectivas elucidativas e orientações pragmáticas relativas à implementação de
  pagamentos automáticos no contexto das finanças descentralizadas.
\end{resumo}

\subsection{Análise publicação da Visa}
Em sua recente contribuição para a expansão do campo de pagamentos automáticos programáveis em
carteiras auto-custodiadas via blockchain, a Visa apresentou revelações significativas numa
publicação técnica intitulada "Autopayments via Account Abstraction". As próximas linhas fornecem
uma síntese das conclusões primárias e propostas emergentes desta publicação.

Na sua abordagem, a Visa introduz um mecanismo inovador que simplifica a possibilidade do usuário
de executar autopagamentos, prescindindo do uso da chave privada associada à sua identidade. O
intuito subjacente é viabilizar autopagamentos para comerciantes sem a necessidade de expor a chave
privada do usuário a qualquer servidor de terceiros. Como alternativa, um contrato inteligente é
capacitado para processar um autopagamento em nome do usuário para o comerciante destinatário, sem
a exigência da chave privada do usuário.

O modelo concebido pela Visa concede ao contrato inteligente a autoridade de conduzir pagamentos
automáticos aos comerciantes associados ao usuário, estando sempre condicionado à aprovação deste
último. Esta aprovação pode ser obtida através do fornecimento de dados que o contrato inteligente
está autorizado a utilizar para realizar os autopagamentos em representação do usuário. Em
essência, o usuário pode pré-autorizar a transação, habilitando o contrato inteligente a processar
o pagamento em seu nome quando uma solicitação é encaminhada pelo comerciante. A Visa sugere ainda
que o usuário possa compilar uma lista de permissões, onde poderá pré-autorizar transações com
pagadores predeterminados, como comerciantes, outros usuários, entre outros.

Na monografia técnica mencionada, a Visa recorreu a AA para investigar a implementação de contratos
inteligentes que viabilizem pagamentos programáveis automáticos. Propuseram uma inovadora solução
para uma aplicação real de pagamentos automáticos, demonstrando como estruturar um contrato
inteligente para uma carteira autogerida capaz de retirar fundos automaticamente, sem necessitar da
participação ativa do usuário em cada instante para instruir e realizar pagamentos numa blockchain.

\section{Desenvolvimento}\label{sec:desenvolvimento}
\subsection{Abordagem da solução}

Demonstração de como os pagamentos automáticos podem ser implementados usando contratos
inteligentes de pagamento automático pré-aprovados escritos em Solidity.

\subsection{Implementação técnica}

Explicação dos passos técnicos necessários para configurar contas delegáveis em carteiras
auto-custodiadas. Visão sobre o fluxo de transação e interação entre o contrato inteligente de
pagamento automático e as carteiras controladas pelo usuário.

\subsection{Vantagens e Potenciais Aplicações}:
Discussão dos benefícios e vantagens oferecidos pela solução proposta para pagamentos automáticos.
Exploração de casos de uso potenciais além de pagamentos recorrentes, como serviços de recuperação de conta de terceiros e gestão de ativos.

\section{Conclusão}\label{sec:conclusao}
\comment{text}{Nem tente escrever conclusão ainda. Uma porque isso é só pra TCC II}
\remove{Reflexão sobre a importância dos pagamentos programáveis e o potencial para inovações futuras no
  espaço blockchain. Pesquisa Futura e Considerações Identificação de possíveis áreas para futuras
  pesquisas e desenvolvimento na automatização de pagamentos em carteiras de auto-gestão. Discussão
  sobre possíveis desafios e considerações a serem tratados na implementação de pagamentos
  automáticos em escala.}

