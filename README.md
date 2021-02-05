<h1 align="center">CPI - Snippets</h1>

<p align="center">🚀 Snippets para ser usado no SAP CPI, principalmente em Groovy Script<p>

</br></br>
Tabela de conteúdos
=================
<!-- TOC -->
* [1. Groovy Script](#1-groovy-script)
    * [1.1. Adicionar Attachment](#11-adicionar-attachment)
    * [1.2. Ler um Property](#12-ler-um-property)
<!-- /TOC -->
</br></br>
---

# 1. Groovy Script

## 1.1. Adicionar Attachment
Script para 
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