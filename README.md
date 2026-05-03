# Statistics-in-R-with-the-S-P-500

data from: https://datahub.io/core/s-and-p-500-companies-financials

Basic commands for reference


# We need to first rename the dataset so its easier to work with
library(readr)

financials <- read_csv("constituents-financials.csv")

# Now we run the mean function. Mean is adding up all the amounts then dividing it by the base number. 
# (your dataset name$column) -> dataset$column
# na.rm = TRUE -> this means when there are empty columns(which in this dataset, there are) the command ignores those empty fields.
> mean(financials$`Price/Earnings`, na.rm = TRUE)
[1] 39.69787



> median(financials$Price, na.rm = TRUE)
[1] 122.2
