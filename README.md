# Pipeline de Dados Serverless End-to-End (GCP & Python)

[![GCP](https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)](https://cloud.google.com/)
[![Python](https://img.shields.io/badge/PYTHON-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![BigQuery](https://img.shields.io/badge/BIGQUERY-669DF6?style=for-the-badge&logo=google-cloud&logoColor=white)](https://cloud.google.com/bigquery/)
[![Git](https://img.shields.io/badge/GIT-F05032?style=for-the-badge&logo=git&logoColor=white)](https://git-scm.com/)

</div>

---

## 📌 Visão Geral do Projeto

Este repositório contém um projeto completo de engenharia de dados e software desenvolvido para processamento em nuvem utilizando serviços do **Google Cloud Platform (GCP)**. O objetivo principal é estruturar um pipeline de dados robusto seguindo a **Arquitetura Medalhão** (Bronze ➔ Silver ➔ Gold) no Google Cloud Storage, aplicando boas práticas de desenvolvimento (*Clean Code*, *Clean Architecture*) e metodologias ágeis.

---

## 🏗️ Arquitetura do Projeto

O pipeline foi desenhado em camadas no ambiente GCP, garantindo rastreabilidade, limpeza rigorosa e alta performance nas consultas:

```text
[ API Pública / Origem ] ---> [ Google Cloud Storage (Camada Bronze / Raw) ]
                                         |
                                         v
[ Google Cloud Storage (Camada Gold) ] <--- [ Python / Cloud Functions (Camada Silver) ]
                                         |
                                         v
                      [ Consultas via Google BigQuery / SQL ]
