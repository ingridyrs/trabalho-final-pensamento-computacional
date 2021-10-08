## trabalho-final-pensamento-computacional
Repositório para o trabalho final da disciplina de "Transparência, reprodutibilidade e uso ético de dados", contendo o trabalho da disciplina de "Pensamento Computacional"

O intuito desse repositório é documentar para a disciplina de Transparência, Reprodutibilidade e Uso Ético de Dados o trabalho de Pensamento COmputacional

O trabalho de da disciplina de Pensamento Computacional consiste em criar um programa que executa um processo de ETL - Extract, Transform, Load um HTML

## Obras de som em Domínio Público 
O site escolhido para o trabalho foi o Domínio Público ( http://www.dominiopublico.gov.br/pesquisa/PesquisaObraForm.jsp ) , uma biblioteca digital que reúne obras de livre acesso.
O programa aqui documentado visa visitar, extrair, limpar e exportar dados de todas as obras em domínio público no tipo de mídia "Som" no idioma "Português".

# O processo

## Análise do site:

O primeiro passo foi alterar o resultado da pesquisa por "Som" em "Português" para reunir o número total de obras (686) para que o trabalho fosse mais fácil. Por isso, a url foi alterada manualmente para que a página exibisse os 1.000 primeiros resultados da busca, que retornou 686 resultados.

Para extrair o html da página, foi usada a biblioteca urllib.request Depois, verificou-se charset=iso-8859-1 .

## Verificação de padrões da página
Buscou-se identificar padrões que discernissem os links comund + partes únicas das obras das demais informações da página

## Separação de código da obra + nome da obra
Cada obra de som do site www.dominiopublico.gov.br/pesquisa/ResultadoPesquisaObraForm.do?first=1000&skip=0&ds_titulo=&co_autor=&no_autor=&co_categoria=&pagina=1&select_action=Submit&co_midia=3&co_obra=&co_idioma=1&colunaOrdenar=null&ordem=null possui um número identificador + nome. Com split, separam-se essas informações.

## Armazanamento das variáveis
O código da obra é um número, por isso foi possível transfomá-lo em int (inteiro). Número int + nome da obra foram armazenados em lista e transformados em dicionário.

## Importação do arquivo em csv
Ao importar arquivo csv, nomear colunas e definir modo escrita. 

# Resultado
O arquivo deve conter 688 linhas e duas colunas contendo o nome da obra e o link para download do arquivo.
