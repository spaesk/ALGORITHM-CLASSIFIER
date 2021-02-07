# ALGORITHM-CLASSIFIER

SOURCE CODE TO XML : 
for %f in (C:\Users\spaes\Desktop\min\dp\*.txt) do srcml C:\Users\spaes\Desktop\min\dp\%~nf.txt --language C++ -o C:\Users\spaes\Desktop\min\XML\%~nf.xml

for %f in (C:\Users\spaes\Desktop\min\bs\*.txt) do srcml C:\Users\spaes\Desktop\min\bs\%~nf.txt --language C++ -o C:\Users\spaes\Desktop\min\bs_XML\%~nf.xml

for %f in (C:\Users\spaes\Desktop\min\gr\*.txt) do srcml C:\Users\spaes\Desktop\min\gr\%~nf.txt --language C++ -o C:\Users\spaes\Desktop\min\gr_XML\%~nf.xml


XML to TXT:
1. query1 : (count of variables)
for %f in (C:\Users\spaes\Desktop\min\XML\*.XML) do srcml --xpath count("//src:decl/src:name") C:\Users\spaes\Desktop\min\XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\bs_XML\*.XML) do srcml --xpath count("//src:decl/src:name") C:\Users\spaes\Desktop\min\bs_XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\gr_XML\*.XML) do srcml --xpath count("//src:decl/src:name") C:\Users\spaes\Desktop\min\gr_XML\%~nf.xml >> %~nf.txt


2. query2: (count of all operators)
for %f in (C:\Users\spaes\Desktop\min\XML\*.XML) do srcml --xpath count("//src:expr/src:operator") C:\Users\spaes\Desktop\min\XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\bs_XML\*.XML) do srcml --xpath count("//src:expr/src:operator") C:\Users\spaes\Desktop\min\bs_XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\gr_XML\*.XML) do srcml --xpath count("//src:expr/src:operator") C:\Users\spaes\Desktop\min\gr_XML\%~nf.xml >> %~nf.txt



3.Count of all constructs :
for %f in (C:\Users\spaes\Desktop\min\XML\*.XML) do srcml --xpath count("//src:for | //src:for/src:for | //src:for/src:for/src:for | //src:while | //src:while/src:while | //src:while/src:while/src:while | //src:if_stmt | //src:for/src:if_stmt | //src:for/src:for/src:if_stmt | //src:while/src:if_stmt | //src:while/src:while/src:if_stmt") C:\Users\spaes\Desktop\min\XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\bs_XML\*.XML) do srcml --xpath count("//src:for | //src:for/src:for | //src:for/src:for/src:for | //src:while | //src:while/src:while | //src:while/src:while/src:while | //src:if_stmt | //src:for/src:if_stmt | //src:for/src:for/src:if_stmt | //src:while/src:if_stmt | //src:while/src:while/src:if_stmt") C:\Users\spaes\Desktop\min\bs_XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\gr_XML\*.XML) do srcml --xpath count("//src:for | //src:for/src:for | //src:for/src:for/src:for | //src:while | //src:while/src:while | //src:while/src:while/src:while | //src:if_stmt | //src:for/src:if_stmt | //src:for/src:for/src:if_stmt | //src:while/src:if_stmt | //src:while/src:while/src:if_stmt") C:\Users\spaes\Desktop\min\gr_XML\%~nf.xml >> %~nf.txt

//srcml --xpath count("//src:for | //src:for/src:for | //src:for/src:for/src:for | //src:while | //src:while/src:while | //src:while/src:while/src:while | //src:if_stmt | //src:for/src:if_stmt | //src:for/src:for/src:if_stmt | //src:while/src:if_stmt | //src:while/src:while/src:if_stmt") C:\Users\spaes\Desktop\XML\5.xml

4.query 4 : Lines of Code:
NO USE

5. query 4 : (Count of all bitwise operators) :
for %f in (C:\Users\spaes\Desktop\min\XML\*.XML) do srcml --xpath count("//src:expr[src:operator='^'] | //src:expr[src:operator='^='] | //src:expr[src:operator='&'] | //src:expr[src:operator='&='] | //src:expr[src:operator='|'] | //src:expr[src:operator='|='] | //src:expr[src:operator='or'] | //src:expr[src:operator='or='] | //src:expr[src:operator='and'] | //src:expr[src:operator='and='] | //src:expr[src:operator='<<'] | //src:expr[src:operator='<<='] | //src:expr[src:operator='>>'] | //src:expr[src:operator='>>=']") C:\Users\spaes\Desktop\min\XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\bs_XML\*.XML) do srcml --xpath count("//src:expr[src:operator='^'] | //src:expr[src:operator='^='] | //src:expr[src:operator='&'] | //src:expr[src:operator='&='] | //src:expr[src:operator='|'] | //src:expr[src:operator='|='] | //src:expr[src:operator='or'] | //src:expr[src:operator='or='] | //src:expr[src:operator='and'] | //src:expr[src:operator='and='] | //src:expr[src:operator='<<'] | //src:expr[src:operator='<<='] | //src:expr[src:operator='>>'] | //src:expr[src:operator='>>=']") C:\Users\spaes\Desktop\min\bs_XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\gr_XML\*.XML) do srcml --xpath count("//src:expr[src:operator='^'] | //src:expr[src:operator='^='] | //src:expr[src:operator='&'] | //src:expr[src:operator='&='] | //src:expr[src:operator='|'] | //src:expr[src:operator='|='] | //src:expr[src:operator='or'] | //src:expr[src:operator='or='] | //src:expr[src:operator='and'] | //src:expr[src:operator='and='] | //src:expr[src:operator='<<'] | //src:expr[src:operator='<<='] | //src:expr[src:operator='>>'] | //src:expr[src:operator='>>=']") C:\Users\spaes\Desktop\min\gr_XML\%~nf.xml >> %~nf.txt

//srcml --xpath count("//src:expr[src:operator='^'] | //src:expr[src:operator='^='] | //src:expr[src:operator='&'] | //src:expr[src:operator='&='] | //src:expr[src:operator='|'] | //src:expr[src:operator='|='] | //src:expr[src:operator='or'] | //src:expr[src:operator='or='] | //src:expr[src:operator='and'] | //src:expr[src:operator='and='] | //src:expr[src:operator='<<'] | //src:expr[src:operator='<<='] | //src:expr[src:operator='>>'] | //src:expr[src:operator='>>=']") C:\Users\spaes\Desktop\XML\ex.xml

6. query 5 : (Count of declaration statements):
for %f in (C:\Users\spaes\Desktop\min\XML\*.XML) do srcml --xpath count("//src:decl_stmt") C:\Users\spaes\Desktop\min\XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\bs_XML\*.XML) do srcml --xpath count("//src:decl_stmt") C:\Users\spaes\Desktop\min\bs_XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\gr_XML\*.XML) do srcml --xpath count("//src:decl_stmt") C:\Users\spaes\Desktop\min\gr_XML\%~nf.xml >> %~nf.txt

//srcml --xpath count("//src:decl_stmt") C:\Users\spaes\Desktop\XML\5.xml

7. query 7 : (Count of functions(including main) ) :
for %f in (C:\Users\spaes\Desktop\min\XML\*.XML) do srcml --xpath count("//src:function") C:\Users\spaes\Desktop\min\XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\bs_XML\*.XML) do srcml --xpath count("//src:function") C:\Users\spaes\Desktop\min\bs_XML\%~nf.xml >> %~nf.txt
for %f in (C:\Users\spaes\Desktop\min\gr_XML\*.XML) do srcml --xpath count("//src:function") C:\Users\spaes\Desktop\min\gr_XML\%~nf.xml >> %~nf.txt

//srcml --xpath count("//src:function") C:\Users\spaes\Desktop\XML\5.xml




**Python script to convert feature extracted txt to csv to attached with the name code.py
