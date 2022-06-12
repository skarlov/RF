## Vjezba 2 - Računalna forenzika

# File type:

Kod:
```
import magic

data1 = magic.from_file("file1")
data2 = magic.from_file("file2.txt")
data3 = magic.from_file("file3")

print(data1)
print(data2)
print(data3)
```
![1](https://user-images.githubusercontent.com/56872071/172830215-a3921ec3-dea6-489f-bc78-d8282fccec73.png)

# Hash:

Kod:
```
import hashlib
file1 = "test.txt"
data1 = open(file1, "r").read()
file2 = "test1.txt"
data2 = open(file2, "r").read()

file1_md5 = hashlib.md5(data1.encode('utf-8')).hexdigest()
file1_sha1 = hashlib.sha1(data1.encode('utf-8')).hexdigest()
file1_sha256 = hashlib.sha256(data1.encode('utf-8')).hexdigest()
file2_md5 = hashlib.md5(data2.encode('utf-8')).hexdigest()
file2_sha1 = hashlib.sha1(data2.encode('utf-8')).hexdigest()
file2_sha256 = hashlib.sha256(data2.encode('utf-8')).hexdigest()

print("test.txt md5: " + file1_md5)
print("test.txt sha1: " + file1_sha1)
print ("test.txt sha256: " + file1_sha256)
print("\n")
print("test1.txt md5: " + file2_md5)
print("test1.txt sha1: " + file2_sha1)
print ("test1.txt sha256: " + file2_sha256)
```
![image](https://user-images.githubusercontent.com/56872071/173234563-9e56aac7-7b19-4750-a261-6021c3f42bdd.png)

# Uspoređivanje Word dokumenta s različitim ekstenzijama:

Kod:
```
import hashlib
file1 = "test.docx"
data1 = open(file1, "r", encoding="latin-1").read()
file2 = "test.jpg"
data2 = open(file2, "r", encoding="latin-1").read()

file1_md5 = hashlib.md5(data1.encode('latin-1')).hexdigest()
file1_sha1 = hashlib.sha1(data1.encode('latin-1')).hexdigest()
file1_sha256 = hashlib.sha256(data1.encode('latin-1')).hexdigest()
file2_md5 = hashlib.md5(data2.encode('latin-1')).hexdigest()
file2_sha1 = hashlib.sha1(data2.encode('latin-1')).hexdigest()
file2_sha256 = hashlib.sha256(data2.encode('latin-1')).hexdigest()

print("test.docx md5: " + file1_md5)
print("test.docx sha1: " + file1_sha1)
print ("test.docx sha256: " + file1_sha256)
print("\n")
print("test.jpg md5: " + file2_md5)
print("test.jpg sha1: " + file2_sha1)
print ("test.jpg sha256: " + file2_sha256)
```
![image](https://user-images.githubusercontent.com/56872071/173234801-adc4c3f6-1e33-4ffe-a294-6814a5dca27d.png)

# File type u folderu Dokaz:

Kod:
```
import magic

data1 = magic.from_file("Dokaz/Secret_file_11.txt")
data2 = magic.from_file("Dokaz/Secret_file_12.pdf")
data3 = magic.from_file("Dokaz/Secret_file_22.png")
data4 = magic.from_file("Dokaz/Secret_file_48.docx")
data5 = magic.from_file("Dokaz/Secret_file_49.pdf")
data6 = magic.from_file("Dokaz/Secret_file_52.jpg")
data7 = magic.from_file("Dokaz/Secret_file_72.docx")
data8 = magic.from_file("Dokaz/Secret_file_92.jpg")


print("Secret_file_11.txt:\t" + data1)
print("Secret_file_12.pdf:\t" + data2)
print("Secret_file_22.png:\t" + data3)
print("Secret_file_48.docx:\t" + data4)
print("Secret_file_49.pdf:\t" + data5)
print("Secret_file_52.jpg:\t" + data6)
print("Secret_file_72.docx:\t" + data7)
print("Secret_file_92.jpg:\t" + data8)
```
![image](https://user-images.githubusercontent.com/56872071/172834528-b8d2c9dd-4351-43c5-bd1e-e06692f36ad2.png)
