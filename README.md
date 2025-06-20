## Serviços AWS dentro da farmácia

### 1. Amazon DynamoDB — Controle e gestão de estoque em tempo real  
Na farmácia, cada produto é cadastrado numa tabela no DynamoDB, com informações como nome, quantidade em estoque, validade e preço.  
- Quando uma venda acontece, o sistema atualiza o estoque automaticamente na tabela.  
- Isso evita falta ou excesso de produtos, pois o estoque é sempre atualizado e consultável rapidamente, mesmo que a farmácia cresça ou abra novas unidades.

### 2. Amazon S3 — Armazenamento seguro e acessível para documentos e imagens  
Toda documentação, como notas fiscais eletrônicas, receitas médicas escaneadas e fotos de produtos, é armazenada no S3.  
- A farmácia pode acessar esses documentos de qualquer lugar, sem depender de servidores físicos.  
- O S3 garante segurança, backup automático e alta disponibilidade.

### 3. AWS Lambda — Automação de processos sem necessidade de servidores  
Sempre que uma venda é registrada, uma função Lambda é acionada automaticamente para:  
- Atualizar o estoque no DynamoDB;  
- Enviar notificações para o gestor quando algum produto estiver com estoque baixo;  
- Gerar relatórios periódicos para análise de vendas e reposição.  

Isso tudo acontece sem a farmácia precisar gerenciar servidores, economizando tempo e dinheiro.

### 4. Amazon API Gateway — Canal de comunicação para apps e sistemas  
A farmácia pode criar APIs seguras para:  
- Aplicativos móveis para clientes consultarem produtos, promoções e fazerem pedidos;  
- Sistemas internos acessarem informações de estoque e vendas;  
- Parceiros integrarem suas soluções com a farmácia.  

O API Gateway gerencia o tráfego, segurança e escalabilidade dessas APIs, garantindo que o sistema funcione bem mesmo em horários de pico.

---

## Resumo prático do uso:

| Serviço           | Uso na farmácia                                          | Benefício principal                  |
|-------------------|---------------------------------------------------------|------------------------------------|
| DynamoDB          | Gerenciar dados de estoque e vendas em tempo real       | Velocidade e escalabilidade         |
| S3                | Armazenar documentos, imagens e backups                  | Segurança e acessibilidade          |
| Lambda            | Automatizar atualizações, notificações e relatórios      | Redução de custos e automação       |
| API Gateway       | Expor dados para apps, sites e parceiros                  | Comunicação segura e escalável      |
