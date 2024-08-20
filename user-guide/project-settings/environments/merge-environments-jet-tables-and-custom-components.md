---
description: >-
  The Merge Environments feature in Jet Admin allows you to transfer and unify
  Jet Tables, custom components, and resources across different environments.
---

# Merge Environments: Jet Tables and Custom Components

#### Key Features

* **Transfer Jet Tables**: Move tables and data seamlessly between environments.
* **Resource Unification**: Align tables, columns, and other resources.

#### Steps to Merge Environments

1. **Go to Project Settings**:
   * Navigate to the project settings of your Jet Admin app.
2. **Find the Copy Environment Button**:
   * In the project settings, locate the "Copy Environment" button.
3. **Select Source and Target Environments**:
   * Choose the environment you want to copy from (`environment_from`) and the environment you want to copy to (`environment_to`).
4. **Press Copy**:
   * Press the "Copy" button to initiate the transfer and unification process.

{% @arcade/embed flowId="MrePW666AUNIUBR656DJ" url="https://app.arcade.software/share/MrePW666AUNIUBR656DJ" %}

#### Important Notes

* **Table Creation**: If there are no tables in the target environment (environment\_to) that exist in the source environment (environment\_from), the system will create the table in the target environment and transfer the data as well.
* **Column Handling**:
  * If a column exists in the source environment but not in the target environment, it will be created in the target environment with `nullable=true` and `default=null`.
  * If a column exists in the target environment but not in the source environment, it will be deleted from the target environment.
  * If a column exists in both environments but has a different data type, the system will attempt to change the column type in the target environment to match the source.
* **Data Incompatibility**:
  * If a data incompatibility error occurs, set the existing values to `null` in the target environment before proceeding.
  * If the default value for a column in the source environment is not null, ensure the column is also made nullable in the target environment.
* **Table Deletion**:
  * If a table exists in the target environment but not in the source environment, it will be deleted from the target environment.
