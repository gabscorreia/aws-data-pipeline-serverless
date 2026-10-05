# Pipeline de Dados Serverless End-to-End (AWS & Python)

[![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![Python](https://img.shields.io/badge/PYTHON-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Glue](https://img.shields.io/badge/AWS_GLUE-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/glue/)
[![Athena](https://img.shields.io/badge/AWS_ATHENA-3776AB?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/athena/)
[![Git](https://img.shields.io/badge/GIT-F05032?style=for-the-badge&logo=git&logoColor=white)](https://git-scm.com/)

</div>

---

## 📌 Visão Geral do Projeto

Este repositório contém um projeto completo de engenharia de dados e software desenvolvido para processamento em nuvem utilizando serviços da **AWS**. O objetivo principal é estruturar um pipeline de dados robusto seguindo a **Arquitetura Medalhão** (Bronze ➔ Silver ➔ Gold) no Amazon S3, aplicando boas práticas de desenvolvimento (*Clean Code*, *Clean Architecture*) e metodologias ágeis.

---

## 🏗️ Arquitetura do Projeto

O pipeline foi desenhado em camadas no ambiente AWS, garantindo rastreabilidade, limpeza rigorosa e alta performance nas consultas:

```text
[ API Pública / Origem ] ---> [ Amazon S3 (Camada Bronze / Raw) ]
                                         |
                                         v
[ Amazon S3 (Camada Gold / Analytics) ] <--- [ AWS Glue (Camada Silver / Processed) ]
                                         |
                                         v
                            [ Consultas via AWS Athena / SQL ]
