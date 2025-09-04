# 🏦 Beta Bank - Predicción de Deserción de Clientes
Beta Bank enfrenta un problema: cada mes pierde clientes de forma constante.  
Dado que **retener clientes existentes es más rentable que adquirir nuevos**, el objetivo de este proyecto es **predecir si un cliente dejará el banco próximamente**.  

Se cuenta con información histórica del comportamiento de los clientes y de la finalización de contratos con el banco.  

📊 **Objetivos principales:**
- Construir un modelo de machine learning que logre el **máximo valor F1 posible**.  
- Alcanzar al menos un **F1 ≥ 0.59** en el conjunto de prueba.  
- Medir también la métrica **AUC-ROC** y compararla con el F1.  
--- 

**Características disponibles:**
- `RowNumber`: índice de fila.  
- `CustomerId`: identificador único de cliente.  
- `Surname`: apellido del cliente.  
- `CreditScore`: puntuación de crédito.  
- `Geography`: país de residencia.  
- `Gender`: género.  
- `Age`: edad.  
- `Tenure`: antigüedad en años del cliente en el banco.  
- `Balance`: saldo de la cuenta.  
- `NumOfProducts`: número de productos contratados.  
- `HasCrCard`: si el cliente tiene tarjeta de crédito (1 = sí, 0 = no).  
- `IsActiveMember`: si el cliente es activo (1 = sí, 0 = no).  
- `EstimatedSalary`: salario estimado.  

**Variable objetivo:**
- `Exited`: indica si el cliente dejó el banco (1 = sí, 0 = no).  

---

## ⚙️ Flujo de trabajo
1. **Carga y exploración de datos**
   - Revisión de tipos de datos, valores nulos y duplicados.  
   - Análisis exploratorio de variables numéricas y categóricas.  

2. **Preparación de datos**
   - Codificación de variables categóricas.  
   - Escalado de características numéricas con `StandardScaler`.  
   - División en entrenamiento, validación y prueba.  

3. **Modelado**
   - Modelos entrenados:
     - Regresión Logística.  
     - Árboles de Decisión.  
     - Random Forest (con ajuste de hiperparámetros vía GridSearchCV).  

4. **Evaluación**
   - Métricas principales: **F1-score y AUC-ROC**.  
   - Análisis de la matriz de confusión.  
   - Selección del modelo con mejor balance entre rendimiento y generalización.  

5. **Conclusiones**
   - Se desarrolló un modelo capaz de predecir la probabilidad de cancelación de clientes.  
   - El modelo final supera el umbral mínimo de **F1 = 0.59** en el conjunto de prueba.  
   - AUC-ROC permitió validar la calidad de la clasificación más allá del F1.  

---

## 📊 Tecnologías utilizadas
- **Python 3**  
- **Pandas / NumPy** → manipulación y análisis de datos  
- **Matplotlib / Seaborn** → visualización  
- **Scikit-learn** → modelado, evaluación y preprocesamiento  

---

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tuusuario/Beta-Bank.git
   cd Beta-Bank
