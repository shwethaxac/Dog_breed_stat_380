library(data.table)
library(Rtsne)
library(ggplot2)
library(caret)
library(ClusterR)
library(dplyr)


# load in data 
perplexity90<-fread("~/Desktop/p90.csv")
perplexity60<-fread("~/Desktop/p60.csv")
perplexity30<-fread("~/Desktop/p30.csv")
sub<-fread("~/Desktop/xes.csv")

#write in data
fwrite(data,"~/Desktop/380_d/dogs/project/volume/data/raw/data.csv")
fwrite(sub,"~/Desktop/380_d/dogs/project/volume/data/raw/xes.csv")
fwrite(perplexity90,"~/Desktop/380_d/dogs/project/volume/data/interim/p90.csv")
fwrite(perplexity60,"~/Desktop/380_d/dogs/project/volume/data/interim/p60.csv")
fwrite(perplexity30,"~/Desktop/380_d/dogs/project/volume/data/interim/p30.csv")


breed_1_avg<-(perplexity90$breed_1 + perplexity60$breed_1 + perplexity30$breed_1)/3
breed_2_avg<-(perplexity90$breed_2 + perplexity60$breed_2 + perplexity30$breed_2)/3
breed_3_avg<-(perplexity90$breed_3 + perplexity60$breed_3 + perplexity30$breed_3)/3
breed_4_avg<-(perplexity90$breed_4 + perplexity60$breed_4 + perplexity30$breed_4)/3


sub$breed_1<-breed_1_avg
sub$breed_2<-breed_2_avg
sub$breed_3<-breed_3_avg
sub$breed_4<-breed_4_avg

fwrite(sub,"~/Desktop/sub_dogs.csv")
fwrite(sub,"~/Desktop/380_d/dogs/project/volume/data/processed/sub_dogs.csv")
