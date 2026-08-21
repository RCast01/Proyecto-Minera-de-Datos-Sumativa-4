# Proyecto-Minera-de-Datos-Sumativa-4
# cargar librerias
library(tidyverse)
library(cluster)
library(factoextra)

# 1. cargar datos y sacar nulos
df <- read.csv("data/weekly_route_operations.csv") %>% drop_na()

# filtramos solo las variables numericas que sirven para logistica
vars_num <- c("trade_volume_tonnes", "freight_cost_usd", "container_availability_index", 
              "port_congestion_index", "weather_disruption_score", "carbon_emissions_tonnes")
df_cluster <- df[, vars_num]

# 2. estandarizar datos (paso clave para que funcione bien kmeans)
df_scaled <- scale(df_cluster)

# 3. probar configuraciones k=3 y k=4
set.seed(42)

# probar con 3 clusters
k3 <- kmeans(df_scaled, centers = 3, nstart = 25)
sil3 <- silhouette(k3$cluster, dist(df_scaled))
cat("SSE K=3:", k3$tot.withinss, "\n")
cat("Silueta K=3:", summary(sil3)$avg.width, "\n")

# probar con 4 clusters
k4 <- kmeans(df_scaled, centers = 4, nstart = 25)
sil4 <- silhouette(k4$cluster, dist(df_scaled))
cat("SSE K=4:", k4$tot.withinss, "\n")
cat("Silueta K=4:", summary(sil4)$avg.width, "\n")

# 4. graficos para visualizar resultados
# grafico del codo
fviz_nbclust(df_scaled, kmeans, method = "wss") +
  labs(title = "Metodo del Codo")

# grafico de los clusters finales
fviz_cluster(k3, data = df_scaled, 
             geom = "point",
             main = "Clusters Finales (K=3)")
