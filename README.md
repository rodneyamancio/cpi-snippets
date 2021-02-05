<h1 align="center">CPI - Snippets</h1>

<p align="center">🚀 Snippets para ser usado no SAP CPI, principalmente em Groovy Script<p>

</br></br>
Tabela de conteúdos
=================
<!-- TOC -->autoauto- [1. Groovy Script](#1-groovy-script)auto    - [1.1. Adicionar Attachment](#11-adicionar-attachment)auto    - [1.2. Ler um Property](#12-ler-um-property)autoauto<!-- /TOC -->
</br></br>
---

# 1. Groovy Script

## 1.1. Adicionar Attachment
Script para Adicionar um attachment na execução do iFlow, muito útil para saber o que está acontecendo com o seu fluxo ao longo da execução.
Exemplos:
* Pode-se usar para gravar uma mensagem de erro caso ocorra
* gravar um payload antes de chamar um sistema externo, muito útil em análise de erros
* gravar o payload de entrada caso seu iFlow seja consumido por um sistema externo
* etc...
```groovy
def messageLog = messageLogFactory.getMessageLog(message);
def sTextoLog = 'Texto que vai para o LOG, podendo ser um JSON ou XML por exemplo'

messageLog.addAttachmentAsString("NomeAttachment", sTextoLog, "text/plain");
```

## 1.2. Ler um Property
Caso você tenha setado um Property em um content modifier, você pode ler ele a partir de um script groovy usando o código abaixo.

>> 🙋 Se você estiver trabalhando com tipos diferentes como Int, não esqueça de usar um toInteger()

```groovy
    def map = message.getProperties()
    int sProperty = map.get("PropertyQueQuerLer").toString()
```