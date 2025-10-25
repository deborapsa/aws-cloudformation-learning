# AWS CloudFormation: Fundamentos, Criação de Stacks e Deploy de Firewall

Este repositório é uma documentação prática para aprendizado de **AWS CloudFormation**, incluindo a criação de stacks genéricas e stacks de firewall.

---

## 📌 O que é AWS CloudFormation?

AWS CloudFormation é um serviço da AWS que permite **provisionar e gerenciar recursos de forma automatizada** utilizando templates em formato YAML ou JSON.  
Com ele, você pode criar e atualizar recursos como EC2, VPCs, Security Groups e muito mais, de forma repetível e segura.

---

## 🛠 Criando Stacks no AWS CloudFormation

### Passos básicos:
1. Acesse o console do CloudFormation.
2. Clique em **Create Stack > With new resources (standard)**.
3. Faça upload do template YAML desejado (ex.: `basic_stack.yaml`).
4. Preencha as informações solicitadas (Nome da stack, parâmetros, tags).
5. Clique em **Create stack**.
6. Acompanhe o progresso na aba **Events** até a stack estar `CREATE_COMPLETE`.

**Exemplo de template básico (`templates/basic_stack.yaml`):**
```yaml
AWSTemplateFormatVersion: "2010-09-09"
Description: "Stack básica de teste"
Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: my-sample-bucket-12345
