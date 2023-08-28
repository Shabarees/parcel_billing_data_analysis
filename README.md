# parcel_billing_data_analysis
Please update your directory for the following
# read excel file
xlxs =pd.ExcelFile("/Users/.........../invoices.xlsx")

# sheet all the sheet name matches
xlxs.sheet_names

# create a dataframe by reading first sheet
df=pd.read_excel("/Users/........../invoices.xlsx", xlxs.sheet_names[0])

# read all the sheets into dataframe
length=len(xlxs.sheet_names)
for x in xlxs.sheet_names[1:]:
    data = pd.read_excel("/Users/........../invoices.xlsx",x)
    frames=[df,data]
    df=pd.concat(frames)

result.to_csv("/Users/.........../result.csv")
df2.to_csv("/Users/........../database_invoice.csv")
