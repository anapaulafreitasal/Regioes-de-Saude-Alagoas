# 🗺️ Regiões de Saúde de Alagoas  
### Arquivos geográficos oficiais (SHP + GPKG) com as 10 Regiões de Saúde do estado

## 📦 Conteúdo do Repositório

Este repositório contém as divisões geográficas das **10 Regiões de Saúde de Alagoas**, geradas a partir da base municipal oficial e processadas no QGIS utilizando ferramentas de junção, padronização e dissolução espacial.

### 📁 **Arquivos incluídos**

#### 🟩 GeoPackage (recomendado)
- `AL_RegioesSaude.gpkg`  
  - Contém a camada consolidada das Regiões de Saúde (10 polígonos)
  - Formato moderno, mais robusto, único arquivo  
  - Projeção: **SIRGAS 2000 / EPSG:4674**

#### 🟦 Shapefile (opcional)
Inclui todos os componentes:
- `.shp` — Geometria  
- `.shx` — Índice espacial  
- `.dbf` — Atributos (REGIAO, CD_MUN)  
- `.prj` — Projeção  
- `.cpg` — Codificação UTF-8  

> ⚠️ Lembre-se: o shapefile precisa **estar sempre com todos esses arquivos juntos**.

## 🧭 Sobre o Projeto

Este repositório foi criado para facilitar o acesso a dados geográficos usados rotineiramente em:

- 📊 Vigilância em Saúde  
- 🦟 Análise espacial de arboviroses (Dengue, Chikungunya, Zika)  
- 🗺️ Mapeamento de hotspots (Gi*, Moran’s I, Kernel)  
- 🏥 Gestão e planejamento em saúde pública  
- 🧪 Estudos técnicos e relatórios

## 🛠️ Metodologia Utilizada

Os arquivos foram processados no **QGIS** seguindo os passos:

1. Importação da base municipal (AL_Municipios_2024)  
2. Junção da tabela contendo os códigos IBGE (CD_MUN) e suas respectivas Regiões  
3. Conferência manual de todas as associações  
4. Uso da ferramenta **Dissolver** para agrupar municípios pela coluna **REGIAO**  
5. Exportação final para **SHP** e **GPKG**  

## 🧩 Estrutura do GeoPackage

O arquivo `AL_RegioesSaude.gpkg` contém:

| Campo | Descrição |
|-------|-----------|
| **REGIAO** | Número da Região de Saúde (1 a 10) |
| **geometry** | Polígonos dissolvidos representando cada região |

## 🚀 Como usar no QGIS

1. Abra o QGIS  
2. Vá em **Camada → Adicionar camada vetorial**  
3. Selecione `AL_RegioesSaude.gpkg`  
4. Para visualizar por região:
   - Propriedades → Simbologia → Categorizado → Campo **REGIAO** → Classificar  
5. Sobreponha com bases de casos, hotspots ou outras análises

## 📸 Preview do Mapa  

<img width="949" height="521" alt="image" src="https://github.com/user-attachments/assets/49272fec-a4be-4400-8304-6423f4a2a4a9" />

## 📚 Fonte dos dados

- **Municípios de Alagoas:** IBGE / AL_Municipios_2024  
- **Classificação das Regiões de Saúde:** SESAU / Vigilância  

## 📝 Licença  
Este projeto está licenciado sob a **MIT License** — você pode usar, adaptar e distribuir livremente, com atribuição.

## 👩‍💻 Contato  
Criado por **Ana Paula Freitas**  
📧 Caso deseje contribuir ou sugerir melhorias, abra uma *issue* ou *pull request*.
