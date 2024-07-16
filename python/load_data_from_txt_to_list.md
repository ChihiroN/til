テキストファイルからリスト型にデータをロードする

```
data_list=[]
with open(file_path,'r') as f: 
	data = f.read()    
	data_list = data.split("\n") 
	f.close() 
print(data_list) 
```