# Validador de Tags Canonicas e Consolidacao de URLs

[![Validador Tag Canonica](https://img.shields.io/badge/TAVARDT-Canonical-5b3cf5.svg)](https://tools.tavardt.com/br/validador-tag-canonica/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditoria de links canonicos, deteccao de tags duplicadas, verificacao de URLs absolutas e eficiencia de rastreamento.

Desenvolvido e mantido pela divisao de engenharia de indexacao e auditoria tecnica de busca da **TAVARDT**.

***

## Vetores de Risco e Impacto Operacional na Consolidacao de URLs

Configuracoes incorretas de tags canonicas geram canibalizacao organica e dispersao de autoridade em plataformas digitais. Parametros de rastreamento de marketing, navegacao facetada e divergencias de protocolo confundem os rastreadores do Googlebot.

Quando as diretivas canonicas entram em conflito ou apontam para destinos quebrados, os buscadores ignoram a consolidacao e indexam URLs redundantes. A auditoria continua assegura a correta unificacao de sinais e a preservacao do orcamento de rastreamento.

***

## Capacidades Centrais de Auditoria Tecnica

* **Extracao de Diretiva em Dupla Fonte**: Leitura de declaracoes canonicas tanto em tags HTML head quanto em cabecalhos de resposta HTTP Link.
* **Prevencao de Multiplas Tags Conflitantes**: Deteccao de definicoes canonicas redundantes ou contraditorias em um mesmo documento, com penalidade de 35 pontos.
* **Validacao de URL Absoluta e HTTPS**: Verificacao de caminhos absolutos completos e desqualificacao de URLs relativas ou sob protocolo inseguro HTTP.
* **Checagem Ativa de Resposta do Destino**: Validacao em tempo real do status HTTP do destino canonico, acusando erros 4xx ou 5xx que quebram o fluxo.
* **Analise de Autorreferencia e Consolidacao**: Verificacao de tags autorreferenciais para saneamento de parametros temporarios e IDs de rastreio.
* **Indice de Saude de Consolidacao**: Metrica quantitativa de 0 a 100 classificando o documento em COMPLIANT, WARNING ou CRITICAL.

***

## Instalacao e Execucao

Requer Python 3.8 ou superior sem dependencias externas adicionais.

```bash
git clone https://github.com/TAVARDT-Brasil/canonical-tag-validator-br.git
cd canonical-tag-validator-br
python canonical_validator.py https://empresa.com.br
```

Para gerar a saida em formato estruturado JSON em esteiras de integracao continua:

```bash
python canonical_validator.py https://empresa.com.br -j
```

***

## Perguntas Frequentes (FAQ Tecnico)

### 1. O que acontece quando multiplas tags canonicas conflitantes sao declaradas?
Os buscadores ignoram todas as declaracoes canonicas quando identificam instrucoes contraditorias na mesma URL. Isso forca os rastreadores a selecionar arbitrariamente uma versao, dispersando a forca de indexacao.

### 2. Por que a URL canonica deve ser estritamente absoluta e sob HTTPS?
Caminhos relativos causam falhas graves de interpretacao quando o documento e acessado por diferentes subdominios ou rotas virtuais. Declarar versoes sob HTTP inseguro gera inconsistencias de protocolo e redirecionamentos desnecessarios.

### 3. Qual o risco operacional de apontar a tag canonica para uma URL com erro 4xx ou 5xx?
Apontar a diretiva para um destino que retorna erro HTTP quebra integralmente o processo de consolidacao de sinais. O Google desconsidera a indicacao e passa a indexar versoes alternativas com parametros dinamicos.

### 4. A ferramenta valida diretivas canonicas emitidas no cabecalho HTTP Link?
Sim, o algoritmo inspeciona tanto elementos declarados no head do HTML quanto o cabecalho HTTP Link da resposta. Essa funcionalidade permite auditar a consolidacao canonica de documentos nao-HTML, como arquivos PDF.

### 5. Como as tags autorreferenciais atuam no saneamento de parametros de marketing?
Uma tag canonica autorreferencial limpa orienta os buscadores a descartarem parametros de campanha como utm e IDs de sessao. Isso garante a consolidacao de todas as metricas de busca na versao padrao da pagina.

***

## Consultoria em SEO Tecnico e Consolidacao de Indexacao

Para arquitetura avancada de indexacao e conformidade com diretrizes do W3C e Google Search Essentials, consulte a equipe da **TAVARDT**.

***

## Links Uteis

* **Portal Corporativo:** https://ag.tavardt.com/br/
* **Suite de Diagnosticos:** https://tools.tavardt.com/br/
* **Contato Tecnico:** https://ag.tavardt.com/br/contato/

***

### Licenca
Distribuido sob a Licenca MIT. Consulte o arquivo LICENSE para termos completos.

***

© 2026 TAVARDT. Todos os direitos reservados.
