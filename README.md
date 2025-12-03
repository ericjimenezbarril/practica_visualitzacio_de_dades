# AgriClimate Analytics - Visualització de Dades Agrícoles i Climàtiques

## Descripció del Projecte

**Projecte acadèmic** de visualització de dades que integra múltiples fonts institucionals 
per analitzar la relació entre canvi climàtic, productivitat agrícola i desenvolupament 
econòmic a escala global durant el període 1961-2024.

### Objectius
- Integrar dades climàtiques, agrícoles i econòmiques de 6 fonts institucionals diferents
- Aplicar tècniques avançades de neteja i imputació intel·ligent de dades
- Generar datasets robustos per a visualitzacions sobre vulnerabilitat climàtica agrícola
- Incorporar perspectiva de gènere en l'anàlisi del sector agrícola


## Fonts de Dades

1. **FAOSTAT** (FAO): Emissions, ocupació, ús del sòl, fertilitzants, pesticides, producció
2. **IMF Climate Data**: Temperatura superficial global
3. **World Bank Climate Portal**: Series CRU TS 4.09 (temperatura i precipitació)
4. **World Bank Development Indicators**: PIB agrícola, regadiu, ocupació
5. **Datahub.io**: PIB per països
6. **Google Public Data**: Coordenades geogràfiques (latitud/longitud)

## Tècniques Destacades

### Imputació Intel·ligent Multi-Capa
- **Interpolació temporal** per país (variables econòmiques)
- **Regressió lineal** per tendències (sèries productives)
- **Imputació proporcional per commodity** (coherència agronòmica)
- **KNN Imputer** per dependències espacials (clima)
- **Normalització de proporcions** complementàries

### Neteja i Transformació
- Anàlisi de consistència interna (female + male = total)
- Eliminació de variables amb >80% valors nuls
- Conversió d'unitats i agregacions
- Enriquiment amb coordenades geogràfiques

## Datasets Finals

**agri_country_year_df_processed.csv** (Agregat per país-any)
- 10.653 registres × 31 variables
- Cobertura: 196 països, 1961-2024
- Variables: clima, emissions, superfície, fertilitzants, ocupació, PIB, demografia

**agri_production_and_prices_df_processed.csv** (Desagregat per cultiu)
- 617.291 registres × 7 variables
- +300 cultius diferents
- Variables: superfície collida, producció (kt), rendiment (kg/ha)

## Preguntes d'Investigació

1. Com ha evolucionat la relació entre temperatura global i producció agrícola?
2. Quines regions són més vulnerables al canvi climàtic agroalimentari?
3. Com ha evolucionat la intensitat de carboni de l'agricultura?
4. Relació entre fertilitzants, rendiments i emissions
5. Impacte del canvi climàtic en la participació de dones en agricultura

## Perspectiva de Gènere

Inclou desagregació per sexe en:
- Ocupació agrícola (female_share_of_employment_in_agriculture)
- Població (female_population_%)
- Permet analitzar desigualtats de gènere en contextos rurals

## Requisits Tècnics

conda env create -f environment_visualitzacio.yml
conda activate visualitzacioLlibreries principals: pandas, numpy, geopandas, scikit-learn, country_converter

## Documentació

- **Justificació de selecció de dades**: `justificacio_seleccio_dades.tex` (LaTeX)
- **Procés d'integració**: `output/data_integration.html`
- **Procés de neteja**: `output/data_cleaning.html`

## Autor

Eric Jiménez Barril  
Projecte Acadèmic de Visualització de Dades  
Desembre 2025

## Llicència

Projecte acadèmic amb finalitat educativa. Les dades originals pertanyen a les seves 
respectives fonts institucionals (FAO, World Bank, IMF).

---

**Nota**: Aquest és un projecte fictici amb finalitat exclusivament acadèmica. 
L'escenari empresarial "AgriClimate Analytics" serveix com a marc narratiu per 
justificar la selecció i tractament de dades.

