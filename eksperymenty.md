{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Forecasting and optimizing fuel sales using machine learning"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## All Experiments"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Structure of sales data at various hierarchical levels"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data tanks](data/tanks.png)\n",
    "![Data products](data/products.png)\n",
    "![Data sites](data/sites.png)\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Local vs. gloval models"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Average error for local and global models:** \n",
    "\n",
    "![Data tanks](local/comparison/mae.png)\n",
    "![Data tanks](local/comparison/smape.png)\n",
    "![Data tanks](local/comparison/rmse.png)\n",
    "\n",
    "**Model size**\n",
    "\n",
    "![Data tanks](local/comparison/model_size.png)\n",
    "\n",
    "**t-test**\n",
    "\n",
    "![Data tanks](local/comparison/ttest.png)\n",
    "\n",
    "**Training time**\n",
    "\n",
    "![Data tanks](local/comparison/training_time/rmse.png)\n",
    "![Data tanks](local/comparison/training_time/smape.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Micro level: sales at the tank level for various models"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The results were examined on the validation and test sets. Charts from the test set are shown:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data tanks](global/tank/xgboost.png)\n",
    "![Data tanks](global/tank/deepar.png)\n",
    "![Data tanks](global/tank/gru.png)\n",
    "![Data tanks](global/tank/lstm.png)\n",
    "![Data tanks](global/tank/nhits.png)\n",
    "![Data tanks](global/tank/nbeats.png)\n",
    "![Data tanks](global/tank/tft.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Forecasts for all models"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "For test dataset:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data tanks](global/tank/tank1pred.png)\n",
    "![Data tanks](global/tank/tank2pred.png)\n",
    "![Data tanks](global/tank/tank3pred.png)\n",
    "![Data tanks](global/tank/tank4pred.png)\n",
    "![Data tanks](global/tank/tank5pred.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Diebold-Mariano Test and critical difference diagram"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "P-values ​​and DM test results are presented for 3 given metrics:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**p-value**\n",
    "\n",
    "![Data tanks](global/tank/dm_p_mae.png)\n",
    "![Data tanks](global/tank/dm_p_rmse.png)\n",
    "![Data tanks](global/tank/dm_p_smape.png)\n",
    "\n",
    "**DM test results**\n",
    "\n",
    "![Data tanks](global/tank/dm_test_mae.png)\n",
    "![Data tanks](global/tank/dm_test_rmse.png)\n",
    "![Data tanks](global/tank/dm_test_smape.png)\n",
    "\n",
    "**CD results**\n",
    "\n",
    "**MAE**\n",
    "\n",
    "![Data tanks](global/tank/cd_p_mae.png)\n",
    "\n",
    "**RMSE**\n",
    "\n",
    "![Data tanks](global/tank/cd_p_rmse.png)\n",
    "\n",
    "**sMAPE**\n",
    "\n",
    "![Data tanks](global/tank/cd_p_smape.png)\n",
    "\n",
    "\n",
    "**with Holm-Benferoni**\n",
    "\n",
    "![Data tanks](global/tank/dm_p_smape_hb.png)\n",
    "![Data tanks](global/tank/cd_p_smape_hb.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Friedman and Wilcoxon test"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data tanks](global/tank/friedman.png)\n",
    "![Data tanks](global/tank/wil_test_mae.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Residuals"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data tanks](global/tank/residuals.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Metrics x Horizon length x Model\n",
    "![Data tanks](global/tank/mae_horizon.png)\n",
    "![Data tanks](global/tank/rmse_horizon.png)\n",
    "![Data tanks](global/tank/smape_horizon.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Micro level: sales at the product level for various models"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The results were examined on the validation and test sets. Charts from the test set are shown:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data products](global/product/xgboost.png)\n",
    "![Data products](global/product/deepar.png)\n",
    "![Data products](global/product/gru.png)\n",
    "![Data products](global/product/lstm.png)\n",
    "![Data products](global/product/nhits.png)\n",
    "![Data products](global/product/nbeats.png)\n",
    "![Data products](global/product/tft.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Forecasts for all models"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "For test dataset:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data products](global/product/1pred.png)\n",
    "![Data products](global/product/2pred.png)\n",
    "![Data products](global/product/3pred.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Diebold-Mariano Test and critical difference diagram"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "P-values ​​and DM test results are presented for 3 given metrics:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**p-value**\n",
    "\n",
    "![Data products](global/product/dm_p_mae.png)\n",
    "![Data products](global/product/dm_p_rmse.png)\n",
    "![Data products](global/product/dm_p_smape.png)\n",
    "\n",
    "**DM test results**\n",
    "\n",
    "![Data products](global/product/dm_test_mae.png)\n",
    "![Data products](global/product/dm_test_rmse.png)\n",
    "![Data products](global/product/dm_test_smape.png)\n",
    "\n",
    "**CD results**\n",
    "\n",
    "**MAE**\n",
    "\n",
    "![Data products](global/product/cd_p_mae.png)\n",
    "\n",
    "**RMSE**\n",
    "\n",
    "![Data products](global/product/cd_p_rmse.png)\n",
    "\n",
    "**sMAPE**\n",
    "\n",
    "![Data products](global/product/cd_p_smape.png)\n",
    "\n",
    "\n",
    "**with Holm-Benferoni**\n",
    "\n",
    "![Data products](global/product/dm_p_smape_hb.png)\n",
    "![Data products](global/product/cd_p_smape_hb.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Friedman and Wilcoxon test"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data products](global/product/friedman.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Residuals"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data products](global/product/residuals.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Metrics x Horizon length x Model\n",
    "![Data products](global/product/mae_horizon.png)\n",
    "![Data products](global/product/rmse_horizon.png)\n",
    "![Data products](global/product/smape_horizon.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Macro level: sales at the site level for various models"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The results were examined on the validation and test sets. Charts from the test set are shown:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data sites](global/site/xgboost.png)\n",
    "![Data sites](global/site/deepar.png)\n",
    "![Data sites](global/site/gru.png)\n",
    "![Data sites](global/site/lstm.png)\n",
    "![Data sites](global/site/nhits.png)\n",
    "![Data sites](global/site/nbeats.png)\n",
    "![Data sites](global/site/tft.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Forecasts for all models"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "For test dataset:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data tanks](global/site/1pred.png)\n",
    "![Data tanks](global/site/2pred.png)\n",
    "![Data tanks](global/site/3pred.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Diebold-Mariano Test and critical difference diagram"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "P-values ​​and DM test results are presented for 3 given metrics:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**p-value**\n",
    "\n",
    "![Data sites](global/site/dm_p_mae.png)\n",
    "![Data sites](global/site/dm_p_rmse.png)\n",
    "![Data sites](global/site/dm_p_smape.png)\n",
    "\n",
    "**DM test results**\n",
    "\n",
    "![Data sites](global/site/dm_test_mae.png)\n",
    "![Data sites](global/site/dm_test_rmse.png)\n",
    "![Data sites](global/site/dm_test_smape.png)\n",
    "\n",
    "**CD results**\n",
    "\n",
    "**MAE**\n",
    "\n",
    "![Data sites](global/site/cd_p_mae.png)\n",
    "\n",
    "**RMSE**\n",
    "\n",
    "![Data sites](global/site/cd_p_rmse.png)\n",
    "\n",
    "**sMAPE**\n",
    "\n",
    "![Data sites](global/site/cd_p_smape.png)\n",
    "\n",
    "\n",
    "**with Holm-Benferoni**\n",
    "\n",
    "![Data sites](global/site/dm_p_smape_hb.png)\n",
    "![Data sites](global/site/cd_p_smape_hb.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Friedman test"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data sites](global/site/friedman.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Residuals"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![Data sites](global/site/residuals.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Metrics x Horizon length x Model\n",
    "![Data sites](global/site/mae_horizon.png)\n",
    "![Data sites](global/site/rmse_horizon.png)\n",
    "![Data sites](global/site/smape_horizon.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Hierarchical forecast reconciliations"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Without hierarchical forecast reconciliation**\n",
    "![HFR](hfr/before.png)\n",
    "\n",
    "**With hierarchical forecast reconciliation**\n",
    "![HFR](hfr/after.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Lag-Llama research"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Zero-shot predictions:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![lagllama](lagllama/zeroshot.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Fine-tuning training data:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![lagllama](lagllama/train.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Fine tuning test data:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![lagllama](lagllama/test.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Average time prediction"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "![all](avg_time_prediction.png)"
   ]
  }
 ],
 "metadata": {
  "language_info": {
   "name": "python"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
