import pandas as pd

df=pd.read_csv(r"c:\Users\Mark\Desktop\DATA CLEANING .csv", encoding="latin1")
print(df)

# Remove duplicates
df = df.drop_duplicates()


# Handle missing descriptions
df["Description"] = df["Description"].fillna("Unknown")

# Convert date
df["InvoiceDate"] = pd.to_datetime(
    df["InvoiceDate"],
    dayfirst=True
)

# Customer ID as integer
df["Customer ID"] = df["Customer ID"].astype("Int64")

# Standardize text columns
df["Country"] = (
    df["Country"]
    .str.strip()
    .str.title()
)


df["Description"] = (
    df["Description"]
    .str.strip()
    .str.upper()
)

# Save cleaned file
df.to_csv(
    "Cleaned_Data.csv",
    index=False
)
