### O que é um Container?

#### Por baixo dos panos

A tecnologia Docker usa o kernel do Linux e recursos do kernel, como Cgroups e namespaces,
para segregar processos de modo que eles possam ser executados de maneira independente. O
objetivo dos containers é criar essa independência: a habilidade de executar diversos 
processos e aplicativos separadamente para utilizar melhor a infraestrutura e, ao mesmo
tempo, manter a segurança que você teria em sistemas separados.