# Articulou

Análise do voto em São Paulo a partir dos dados públicos do TSE, de 2000 a 2026, para analistas e dirigentes de partido.

## Use

Instale o plugin, conecte o Articulou na aba Conectores (entra com o e-mail convidado pela sua organização) e pergunte em
português: por que o partido perdeu votos, quem é dono do próprio voto, como o voto evoluiu por local de votação ou seção,
se a base de vereadores passou voto ao deputado. A skill `eleicoes-sp` faz o Claude chamar o Articulou sozinho em toda pergunta
eleitoral sobre SP, sem precisar nomeá-lo.

## Dados

O plugin manda ao servidor da sua organização (`<organização>.articulou.com`) só o que a pergunta pede: partido, pessoa, cargo,
ano, recorte. O servidor devolve números do TSE já calculados e guarda os relatórios que você publicar. Nada mais sai da conversa.
