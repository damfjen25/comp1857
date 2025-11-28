import pandas as pd
import matplotlib.pyplot as plt


csv_file_name = "chart.csv"


try:

    df_temp = pd.read_csv(csv_file_name, sep=';', decimal=',')


    print("Successfully read 'chart.csv'! Data (first 5 rows):")
    print(df_temp.head())


    print("\nData Types:")
    print(df_temp.info())


    print("\n...Plotting chart...")

    plt.figure(figsize=(14, 7))


    plt.plot(df_temp['Category'], df_temp['Average Minimum Surface Air Temperature (°C)'],
             label='Average Minimum Temp', color='blue', marker='o')

    plt.plot(df_temp['Category'], df_temp['Average Mean Surface Air Temperature (°C)'],
             label='Average Mean Temp', color='green', marker='o')

    plt.plot(df_temp['Category'], df_temp['Average Maximum Surface Air Temperature (°C)'],
             label='Average Maximum Temp', color='red', marker='o')


    plt.title('Average Monthly Surface Air Temperature in Vietnam', fontsize=16)
    plt.xlabel('Month', fontsize=12)
    plt.ylabel('Temperature (°C)', fontsize=12)

    plt.legend(bbox_to_anchor=(1.05, 1), loc='upper left')
    plt.grid(True, linestyle='--', alpha=0.6)


    plt.tight_layout()


    plt.show()

except FileNotFoundError:
    print(f"ERROR: File not found '{csv_file_name}'!")
    print("Please make sure you have uploaded the file to Colab.")
except Exception as e:
    print(f"An error occurred: {e}")
