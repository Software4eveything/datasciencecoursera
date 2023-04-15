import pandas as pd
file_name ='https://docs.google.com/spreadsheets/d/e/2PACX-1vSX7IQrG6UNyBk-08erUambZd5aBtzWjSbLPf_mWFag_91TBbi_YFlalhqNByIP7Y0HRg81F2Ov8Va5/pub?output=csv'
df=pd.read_csv(file_name)
df.head()
new_df= df.copy
new_df.sort_values(by=['Hov2'], ascending=False)
new_df.drop_duplicates(subset=['id', 'id_2'], keep='first', inplace=True)
new_df.sort_values(by=['id', 'id_2'], ascending=[True, True], inplace=True)
new_df.to_csv('task_1.csv', index=False)
    
