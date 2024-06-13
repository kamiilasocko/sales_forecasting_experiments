<div class="cell markdown">

# Forecasting and optimizing fuel sales using machine learning

</div>

<div class="cell markdown">

## All Experiments

</div>

<div class="cell markdown">

### Structure of sales data at various hierarchical levels

</div>

<div class="cell markdown">

![Data tanks](data/tanks.png) ![Data products](data/products.png) ![Data
sites](data/sites.png)

</div>

<div class="cell markdown">

### Local vs. global models

</div>

<div class="cell markdown">

**Average error for local and global models:**

![Data tanks](local/comparison/mae.png) ![Data
tanks](local/comparison/smape.png) ![Data
tanks](local/comparison/rmse.png)

**Model size**

![Data tanks](local/comparison/model_size.png)

**t-test**

![Data tanks](local/comparison/ttest.png)

**Training time**

![Data tanks](local/comparison/training_time/rmse.png) ![Data
tanks](local/comparison/training_time/smape.png)

</div>

<div class="cell markdown">

### Micro level: sales at the tank level for various models

</div>

<div class="cell markdown">

The results were examined on the validation and test sets. Charts from
the test set are shown:

</div>

<div class="cell markdown">

![Data tanks](global/tank/xgboost.png) ![Data
tanks](global/tank/deepar.png) ![Data tanks](global/tank/gru.png) ![Data
tanks](global/tank/lstm.png) ![Data tanks](global/tank/nhits.png) ![Data
tanks](global/tank/nbeats.png) ![Data tanks](global/tank/tft.png)

</div>

<div class="cell markdown">

### Forecasts for all models

</div>

<div class="cell markdown">

For test dataset:

</div>

<div class="cell markdown">

![Data tanks](global/tank/tank1pred.png) ![Data
tanks](global/tank/tank2pred.png) ![Data
tanks](global/tank/tank3pred.png) ![Data
tanks](global/tank/tank4pred.png) ![Data
tanks](global/tank/tank5pred.png)

</div>

<div class="cell markdown">

### Diebold-Mariano Test and critical difference diagram

</div>

<div class="cell markdown">

P-values ​​and DM test results are presented for 3 given metrics:

</div>

<div class="cell markdown">

**p-value**

![Data tanks](global/tank/dm_p_mae.png) ![Data
tanks](global/tank/dm_p_rmse.png) ![Data
tanks](global/tank/dm_p_smape.png)

**DM test results**

![Data tanks](global/tank/dm_test_mae.png) ![Data
tanks](global/tank/dm_test_rmse.png) ![Data
tanks](global/tank/dm_test_smape.png)

**CD results**

**MAE**

![Data tanks](global/tank/cd_p_mae.png)

**RMSE**

![Data tanks](global/tank/cd_p_rmse.png)

**sMAPE**

![Data tanks](global/tank/cd_p_smape.png)

**with Holm-Benferoni**

![Data tanks](global/tank/dm_p_smape_hb.png) ![Data
tanks](global/tank/cd_p_smape_hb.png)

</div>

<div class="cell markdown">

### Friedman and Wilcoxon test

</div>

<div class="cell markdown">

![Data tanks](global/tank/friedman.png) ![Data
tanks](global/tank/wil_test_mae.png)

</div>

<div class="cell markdown">

### Residuals

</div>

<div class="cell markdown">

![Data tanks](global/tank/residuals.png)

</div>

<div class="cell markdown">

### Metrics x Horizon length x Model

![Data tanks](global/tank/mae_horizon.png) ![Data
tanks](global/tank/rmse_horizon.png) ![Data
tanks](global/tank/smape_horizon.png)

</div>

<div class="cell markdown">

### Micro level: sales at the product level for various models

</div>

<div class="cell markdown">

The results were examined on the validation and test sets. Charts from
the test set are shown:

</div>

<div class="cell markdown">

![Data products](global/product/xgboost.png) ![Data
products](global/product/deepar.png) ![Data
products](global/product/gru.png) ![Data
products](global/product/lstm.png) ![Data
products](global/product/nhits.png) ![Data
products](global/product/nbeats.png) ![Data
products](global/product/tft.png)

</div>

<div class="cell markdown">

### Forecasts for all models

</div>

<div class="cell markdown">

For test dataset:

</div>

<div class="cell markdown">

![Data products](global/product/1pred.png) ![Data
products](global/product/2pred.png) ![Data
products](global/product/3pred.png)

</div>

<div class="cell markdown">

### Diebold-Mariano Test and critical difference diagram

</div>

<div class="cell markdown">

P-values ​​and DM test results are presented for 3 given metrics:

</div>

<div class="cell markdown">

**p-value**

![Data products](global/product/dm_p_mae.png) ![Data
products](global/product/dm_p_rmse.png) ![Data
products](global/product/dm_p_smape.png)

**DM test results**

![Data products](global/product/dm_test_mae.png) ![Data
products](global/product/dm_test_rmse.png) ![Data
products](global/product/dm_test_smape.png)

**CD results**

**MAE**

![Data products](global/product/cd_p_mae.png)

**RMSE**

![Data products](global/product/cd_p_rmse.png)

**sMAPE**

![Data products](global/product/cd_p_smape.png)

**with Holm-Benferoni**

![Data products](global/product/dm_p_smape_hb.png) ![Data
products](global/product/cd_p_smape_hb.png)

</div>

<div class="cell markdown">

### Friedman and Wilcoxon test

</div>

<div class="cell markdown">

![Data products](global/product/friedman.png)

</div>

<div class="cell markdown">

### Residuals

</div>

<div class="cell markdown">

![Data products](global/product/residuals.png)

</div>

<div class="cell markdown">

### Metrics x Horizon length x Model

![Data products](global/product/mae_horizon.png) ![Data
products](global/product/rmse_horizon.png) ![Data
products](global/product/smape_horizon.png)

</div>

<div class="cell markdown">

### Macro level: sales at the site level for various models

</div>

<div class="cell markdown">

The results were examined on the validation and test sets. Charts from
the test set are shown:

</div>

<div class="cell markdown">

![Data sites](global/site/xgboost.png) ![Data
sites](global/site/deepar.png) ![Data sites](global/site/gru.png) ![Data
sites](global/site/lstm.png) ![Data sites](global/site/nhits.png) ![Data
sites](global/site/nbeats.png) ![Data sites](global/site/tft.png)

</div>

<div class="cell markdown">

### Forecasts for all models

</div>

<div class="cell markdown">

For test dataset:

</div>

<div class="cell markdown">

![Data tanks](global/site/1pred.png) ![Data
tanks](global/site/2pred.png) ![Data tanks](global/site/3pred.png)

</div>

<div class="cell markdown">

### Diebold-Mariano Test and critical difference diagram

</div>

<div class="cell markdown">

P-values ​​and DM test results are presented for 3 given metrics:

</div>

<div class="cell markdown">

**p-value**

![Data sites](global/site/dm_p_mae.png) ![Data
sites](global/site/dm_p_rmse.png) ![Data
sites](global/site/dm_p_smape.png)

**DM test results**

![Data sites](global/site/dm_test_mae.png) ![Data
sites](global/site/dm_test_rmse.png) ![Data
sites](global/site/dm_test_smape.png)

**CD results**

**MAE**

![Data sites](global/site/cd_p_mae.png)

**RMSE**

![Data sites](global/site/cd_p_rmse.png)

**sMAPE**

![Data sites](global/site/cd_p_smape.png)

**with Holm-Benferoni**

![Data sites](global/site/dm_p_smape_hb.png) ![Data
sites](global/site/cd_p_smape_hb.png)

</div>

<div class="cell markdown">

### Friedman test

</div>

<div class="cell markdown">

![Data sites](global/site/friedman.png)

</div>

<div class="cell markdown">

### Residuals

</div>

<div class="cell markdown">

![Data sites](global/site/residuals.png)

</div>

<div class="cell markdown">

### Metrics x Horizon length x Model

![Data sites](global/site/mae_horizon.png) ![Data
sites](global/site/rmse_horizon.png) ![Data
sites](global/site/smape_horizon.png)

</div>

<div class="cell markdown">

### Hierarchical forecast reconciliations

</div>

<div class="cell markdown">

**Without hierarchical forecast reconciliation** ![HFR](hfr/before.png)

**With hierarchical forecast reconciliation** ![HFR](hfr/after.png)

</div>

<div class="cell markdown">

### Lag-Llama research

</div>

<div class="cell markdown">

Zero-shot predictions:

</div>

<div class="cell markdown">

![lagllama](lagllama/zeroshot.png)

</div>

<div class="cell markdown">

Fine-tuning training data:

</div>

<div class="cell markdown">

![lagllama](lagllama/train.png)

</div>

<div class="cell markdown">

Fine tuning test data:

</div>

<div class="cell markdown">

![lagllama](lagllama/test.png)

</div>

<div class="cell markdown">

### Average time prediction

</div>

<div class="cell markdown">

![all](avg_time_prediction.png)

</div>
