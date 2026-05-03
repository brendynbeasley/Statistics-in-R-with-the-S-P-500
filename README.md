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


# Think of median as a true "middle" of the data set
> median(financials$Price, na.rm = TRUE)
[1] 122.2


# This is the mode function %>% as you can see its not clearly labeled the "mode" but now we introduce the count function as well as the
# sort function. The mode is the most frequently occurring number in the data set. We include sort = TRUE because it tells R to sort 
# the count results from most common to least common. 
> financials %>% count(Price, sort = TRUE)
# A tibble: 500 × 2
   Price     n
   <dbl> <int>
 1 NA        3
 2 63.5      2
 3  9.72     1
 4 10.1      1
 5 10.3      1
 6 10.4      1
 7 10.9      1
 8 11        1
 9 11.3      1
10 15.6      1
# ℹ 490 more rows
# ℹ Use `print(n = ...)` to see more rows

