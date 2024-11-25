# **dbt + Postgres**

1. **Setup dbt**:  
   - Configured dbt to work with a PostgreSQL database (our target warehouse).  

2. **Created Models**:  
   - Defined two models (`my_first_dbt_model` and `my_second_dbt_model`) that transform raw data into usable tables or views.  

3. **Ran the Models (`dbt run`)**:  
   - Executed SQL transformations defined in the models, creating:
     - A **table** (`my_first_dbt_model`): Data is materialized as a physical table in the database.
     - A **view** (`my_second_dbt_model`): Data is materialized as a SQL view (computed on demand).

4. **Validated Data with Tests (`dbt test`)**:  
   - Applied **data quality tests** (e.g., `not_null`, `unique`) to ensure the data meets specified requirements.


## **Key Concepts**

### **1. Models**
- Models in dbt are SQL files that define transformations for your data.
- They convert raw data into clean, structured datasets for analytics or reporting.
- Models can be materialized as tables or views depending on the configuration.

### **2. dbt Commands**
- **`dbt run`**: Executes all models and materializes the tables or views in the database.
- **`dbt test`**: Runs data quality tests defined in `schema.yml` to validate data.

### **3. Tests**
Tests ensure the accuracy and quality of the data:
- **Built-in tests** like `not_null` and `unique` validate the data’s integrity.

### **4. Materialization**
Defines how a model is stored in the database:
- **Table**: Fully computed and stored as a physical table.
- **View**: Stored as a SQL query; computed on demand.

### **5. DAG (Directed Acyclic Graph)**
- dbt creates a dependency graph between models, building a pipeline of transformations.


## **What Did We Achieve?**

1. **Data Transformation Workflow**:  
   - Raw data was transformed into structured datasets ready for analysis.

2. **Data Quality Validation**:  
   - Applied tests to ensure columns met quality standards (e.g., no null values, unique IDs).

3. **Automated Documentation**:  
   - dbt automatically generated documentation for the models and their dependencies.


## **Example Output**

### **Models**
- `my_first_dbt_model`: Created as a **table**.
- `my_second_dbt_model`: Created as a **view**.


## **Why Use dbt?**

- **SQL-Centric**: Simplifies transformations directly in the database.  
- **Modular**: Each model represents a single transformation step.  
- **Version Control**: Compatible with Git for collaborative workflows.  
- **Testing and Validation**: Ensures data quality at every stage.  
- **Documentation**: Auto-generated documentation for models and their dependencies.  

---


### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [chat](https://community.getdbt.com/) on Slack for live discussions and support
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices
