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
::(length<4) -> setToggle!msg
fi
}
```
