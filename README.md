# AWS-cloudformation
# 🚀 Implementando Infraestrutura Automatizada com AWS CloudFormation

## 📌 Descrição do Desafio

O objetivo foi **implementar uma infraestrutura automatizada utilizando AWS CloudFormation**, explorando os conceitos de **Infraestrutura como Código (IaC)** e documentando os aprendizados adquiridos durante o laboratório prático.

---

## 🎯 Objetivos de Aprendizagem
- Aplicar na prática os conceitos de **infraestrutura como código**.  
- Documentar o processo técnico de forma clara e estruturada.  
- Utilizar o **GitHub** como ferramenta para versionamento e compartilhamento de documentação técnica.  

---

## 📝 Anotações de Estudo

### 🔹 Desenvolvimento e Ferramentas
- A AWS oferece ferramentas para desenvolvedores como **AWS SDKs** e **AWS CLI**, que permitem interação com os serviços diretamente pelo terminal.  
- O **AWS CloudFormation** é a solução para **automatizar a criação e configuração de recursos** por meio de modelos declarativos.  
- O **AWS CodeDeploy** auxilia na **implantação automatizada de aplicações**, reduzindo erros manuais.

---

### 🔹 O que é o AWS CloudFormation
- Serviço de orquestração de recursos que permite criar e gerenciar infraestrutura AWS por meio de **templates**.  
- Esses modelos descrevem recursos como instâncias **EC2**, bancos **RDS**, redes, permissões e balanceadores de carga.  
- Elimina a necessidade de configuração manual, permitindo focar no desenvolvimento e gestão das aplicações.  

---

### 🔹 Benefícios do AWS CloudFormation
1. **Automação**  
   - Facilita a criação e o gerenciamento de recursos.  
   - Garante implantações rápidas, confiáveis e repetitivas.  

2. **Consistência e Padronização**  
   - Permite criar **modelos padrão** que podem ser reutilizados.  
   - Evita erros humanos e assegura ambientes idênticos.  

3. **Economia de Custos**  
   - Reduz tempo e gastos com reutilização de modelos existentes.  
   - Acelera a implementação de novas infraestruturas.  

4. **Segurança**  
   - Configura recursos de acordo com regras e políticas de segurança.  
   - Ajuda a proteger a infraestrutura contra ameaças.  

---

### 🔹 Formatos de Modelos
- Suporte para **JSON** e **YAML**.  
- Estrutura típica de um template inclui:  
  - **Parameters**: valores de entrada.  
  - **Mappings**: mapas de variáveis.  
  - **Conditions**: condições lógicas.  
  - **Resources**: os recursos da AWS.  
  - **Outputs**: valores de saída.  


---
## 🔹 Diferença entre CloudFormation e Terraform
- **AWS CloudFormation**:  
  - Ferramenta exclusiva da AWS.  
  - Totalmente integrada ao ecossistema da AWS.  
  - Ideal quando a infraestrutura será 100% dentro da AWS.  

- **Terraform**:  
  - Suporta múltiplos provedores de nuvem (AWS, Azure, GCP etc).  
  - Permite gerenciar ambientes **multi-cloud**.  
  - Mais flexível em cenários híbridos.

---
## 📚 Insights e Aprendizados
- Entendi na prática como a **infraestrutura como código (IaC)** facilita o provisionamento de ambientes.  
- O **CloudFormation** permite criar e replicar ambientes inteiros em poucos minutos, com consistência e sem erros manuais.  
- Usar **templates JSON/YAML** ajuda a manter a padronização, versionamento e reuso da infraestrutura.  
- Notei que o **Terraform** é uma alternativa importante em projetos multi-cloud, mas dentro da AWS o **CloudFormation** se mostra mais prático pela integração nativa.  
- Esse desafio me mostrou a importância de **documentar os processos**, pois o README se torna um registro útil de aprendizado e referência futura.  
---

### 🔹 Exemplo de Template
```json
{
  "Parameters": {
    "DBName": {
      "Default": "MyDatabase",
      "Description": "Nome do banco MySQL",
      "Type": "String",
      "MinLength": "1",
      "MaxLength": "64",
      "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*"
    }
  }
}
