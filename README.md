# mera
```
chan	toBuffer=[4] of {int};
chan	toRec=[4] of {int};
chan	setToggle=[4] of {int};
int state=1;
int length=0;
active proctype sender(){

int data=-1;
(state==1)
do
:: toBuffer!data
od
}

active proctype toggle(){
int flag
setToggle?flag
if
:: (flag==1) -> state=1;
:: (flag==0) -> state=0
fi
}

active proctype buffer(){
int data;
toBuffer?data;
toRec!data;

length=length+1;
printf("LEN IS =%d",length);
int msg=0;
if
:: (length>4) -> setToggle!msg
fi
}

active proctype receiver(){
int data;
int msg=1;

toRec?data;
(data==-1)
length=length-1;
if





ATOMIC OLA THA EKTELESTOUN SE ENA BHMA-TAUTOXRONA
stou dijkstra to slide,oloi oi ypoloipoi users einai blocked
end label-states kaneis ok eina livelock(mia while)
accept label den maresei to tade livelock
progress label ...
temp claims:
* never claim = oti eipe
trace assert =kati san never claim

**ERGASIA**
Session protocol used in Application layer
latex gia to SIP (bibtex) ena mikro summary.
se promela to ideal case tou spin(3procs)
se periptwseis lathwn,px kai oi 2 busy
se me skip(thelei to datalink kai ema pragma akoma,selective repeat??)
se asserts

sto git
to state==1 prepei na einai mesa sto do od gia to checkarei panta
kai to len to  koitane kai ta 2 procs TAUTOXRONA

::(length<4) -> setToggle!msg
fi
}
```
