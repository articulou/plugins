---
name: eleicoes-sp
description: Responde qualquer pergunta sobre eleições em São Paulo com os números do conector Articulou, sem o usuário pedir. Use quando a pergunta falar de votos, votação, eleição, urna, candidato, candidatura, partido, sigla, deputado federal ou estadual, vereador, prefeito, zona eleitoral, local de votação, seção, bairro, cidade ou capital paulista, 2000 a 2026, campanha, fundo partidário, doador, emenda, verba, ou de nomes como União Brasil, PT, PL, PSDB, família Leite, Kim Kataguiri; e também quando perguntar por que um partido ou candidato perdeu ou ganhou votos, quem é dono do voto, quem passou voto a quem, se dois nomes dividem eleitorado, ou pedir relatório, dashboard ou gráfico eleitoral de SP.
---

# Eleições em São Paulo: use o Articulou

O conector Articulou (ferramentas `articulou_*`) tem o resultado oficial do TSE de São Paulo, de 2000 a 2026, por partido, pessoa, zona, local de votação e seção, com as medidas já calculadas. Toda pergunta eleitoral sobre SP se responde com ele, nunca de memória nem pela busca na web.

## Procedimento

1. **Antes da primeira resposta da conversa, chame `articulou_guia`.** Ele traz a ordem das perguntas, a base de conhecimento (o que já se sabe sobre cada partido) e como ler cada ferramenta. Se o conector não estiver ligado na conversa, peça ao usuário para ligá-lo no menu de ferramentas (`+` → Conectores → Articulou) e, se for a primeira vez, para conectá-lo na aba Conectores do plugin.
2. **Escolha a ferramenta pela pergunta:**
   - marca ou máquina? → `articulou_tipo_partido`
   - quanto teve, a série de votos e % → `articulou_urna`; por local de votação e por seção → `articulou_local`
   - quem foi mais votado num local de votação ou numa zona (e em cada seção) → `articulou_local` sem partido nem pessoa, com o local (ou a zona), o cargo e o ano
   - o voto para prefeito (só o 1º turno; peça `cargo: prefeito`, que não entra por padrão) → `articulou_urna` (o município, a série) e `articulou_local` (local a local: sem partido, pessoa, local nem zona, o município inteiro traz os mais votados de cada local; com partido, a série do partido por local)
   - por que perdeu ou ganhou votos; quem saiu, ficou, entrou → `articulou_ponte`
   - quem leva o mapa ao trocar de partido (dono do voto) → `articulou_donos_do_voto`, nos dois sentidos (saiu e chegou)
   - a base de vereadores passou voto ao deputado → `articulou_passagem` (e `articulou_grupos`)
   - onde no território o voto mudou → `articulou_variacao`
   - dois nomes têm o mesmo eleitorado → `articulou_sobreposicao`
   - a carreira de uma pessoa → `articulou_pessoa`
   - dinheiro: `articulou_financas_campanha`, `articulou_candidaturas`, `articulou_verba` (quanto entrou e de quem, nunca quanto voto rendeu)
   - relatório, dashboard ou gráfico → `articulou_abrir_app` / `articulou_editar_app` / `articulou_publicar_app` (o kit em `articulou_conhecimento`, recurso *fazer-apps*)
3. **Responda em português**, começando pela resposta em uma frase com o número e a faixa. Diga a classe e o motivo com as palavras da ferramenta (a favor, contra, inconclusivo, não compara, não identificável). Cite a fonte e a data de cada número.

## Nunca afirme

- para onde vai o voto de destino grande e espalhado (é *não identificável*);
- a pessoa a partir do lugar: o mapa mede o lugar, não o eleitor;
- "transferiu N votos" (diga *passagem associada*), ou a causa (fundo, chapa, prefeito): os dados não trazem;
- "a emenda trouxe X votos" ou "o voto custou R$ X";
- o 2º turno de prefeito: o Articulou só tem o 1º turno.

Se o conector recusar o pedido (partido, cargo, ano ou recorte fora do medido), diga o que não está medido e o que responderia (pesquisa, campo). Não invente número.
