<h1 align="center">CPI - Snippets</h1>

<p align="center">🚀 Snippets para ser usado no SAP CPI, principalmente em Groovy Script<p>

---
</br></br>
<!-- TOC -->autoauto- [1. Groovy Script](#1-groovy-script)auto    - [1.1. Adicionar Attachment](#11-adicionar-attachment)auto    - [1.2. Texto 2](#12-texto-2)autoauto<!-- /TOC -->
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

## 1.2. Texto 2