# Calculate Genetic Risk Score

data$grs <- rowSums(data[,snp])
data <- transform(data, sex = as.numeric(sex))
data <- transform(data, age = as.numeric(age))

#Standardized 

data$grs.std <- (data$grs-mean(data$grs))/sd(data$grs)

