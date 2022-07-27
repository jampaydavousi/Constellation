# Constellation
Material for Constellation

Please Note:

The jupyter notebook used to process the training datasets and testing datasets is: dengue_final_copy.ipynb
The output of this notebook above is submitted to DrivenData Labs and posted in this repository.

The jupyter notebook that includes several data mining the rational and analysis, and testing is: dengue_jam_final

Introduction

The following provides a summary of the steps taken and the observations that led to creation of two different machine models for predicting the dengue outbreaks in San Juan and Iquitos.

In addition but separate from the analysis provided by the authors of this exercise and those illustrate in the benchmark ipynb notebook, a different approach was taken to discover if there are patterns among changing weather conditions and increase/decrease in dengue cases.

The feature and target datasets were merged and then split into San Juan and Iquitos.

Then the null values were filled using average values int eh respective columns.

Next, we looked at the change in total dengue cases and weather parameters across 52 weeks for all years, at both San Juan and Iquitos.

For San Juan, after analysis, new features were created based on rolling averages of the weather parameters that contribute to the changes in the total cases of dengue.
Then, we derived NEW weather FEATURES that provide historical context for rising, falling, or unchanged trends; FOR EACH actual observation of the primary parameters. The range from rolling average from a week prior to several weeks prior to the current observation. This ensures that both the changes in increase and decrease are properly sampled, as the rate of increase are slower and longer, and the rate of decrease is sharper and quicker.

For Iquitos, Similar analysis was conducted for the Iquitos. The changes among all the features (weather parameters) and target (total cases of Dengue) are closer in time, and do not show the lags observed above.
