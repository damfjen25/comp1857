import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt


df = pd.read_csv('df_weather.csv')


df_hanoi = df[df['location.name'] == 'Hà Nội'].copy()


cols = [
    'day.avgtemp_c',       
    'day.avghumidity',     
    'day.maxwind_kph',     
    'day.totalprecip_mm',  
    'day.uv'               
]

corr_matrix = df_hanoi[cols].corr()

plt.figure(figsize=(10, 8))
sns.heatmap(corr_matrix, 
            annot=True,           
            cmap='coolwarm',      
            fmt=".2f",            
            linewidths=0.5,       
            square=True)          

plt.title('Correlation Matrix of Weather Variables (Hanoi)', fontsize=14)
plt.show()
