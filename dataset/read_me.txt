Because we only get part of the electronic documents, 
some of them are paper documents, and we manually input the data set, so there are some errors, 
which can be modified as follows.

Python code£º
ABR data set£º
df.loc[df['In/Out_Patient'] == 'in', 'In/Out_Patient'] = 1
df.loc[df['In/Out_Patient'] == 'out', 'In/Out_Patient'] = 0
df.loc[df['In/Out_Patient'] == ' out', 'In/Out_Patient'] = 0
df.loc[df['In/Out_Patient'] == 'out ', 'In/Out_Patient'] = 0

df.loc[df['Abnormal'] >= '1 ', 'Abnormal'] = 1