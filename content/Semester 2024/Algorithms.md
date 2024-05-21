##### N-queens problem
```
PlaceQueens(Q[1..n], r):
	if r=n+1:
		print(Q[1..n])
	else 
		for j<-1 to n:
			legal-> true
			for j<-1 to r-1:
				if (Q[i]=j or Q[j-r+i] or Q[j+r-i]):
					legal<-false
		if legal
			Q[r]<-j
			PlaceQueens(Q[1..n], r)
```

##### LISBigger
```
LISBigger(A[1..n], prev):
	if n=0:
		return 0
	else A[1]<=prev:
		return LISBigger(prev,A[2..n])
	else
		skip<-LISBigger(prev, A[2..n])
		take<-LISBigger(A[1], A[2..n]+1)
		return{ max,skip }
```

##### Karp-Rabin String Matching
```
n=length(T)
k=length(P)
for i<-0 to n-k do:
	textHash<-hashT.getHash(i, i+k-1)
	patternHash<-hashT.getHash(0,k-1)
	if patternHash=textHash
		valid<-True
		for j<-0 to k-1 do
			if T[i+j] is not equal to P[j]:
				valid<-false
				break
	if valid:
		answer<-answer+1
```

##### Naive String Matching
```
n=length(T)
k=length(P)
for i<-0 to n-k do
	valid<-true
	for j<-0 to k-1 do
		if T[i..j] is not equal to P[j]
			valid<-false
	if valid:
		answer<-answer + 1
```

##### Finite Automata
```
n=T.length
q=0 
for i=0 to n
	q=theta(q-T[i])
if q==m:
	print(i-m)
```

##### Subset Sum
```
if T=0
	return True
else if T<0 and x=phi
	return False
else
	x<-any element of x
	with<-subset(x\{x}, T-x)
	wout<-subset(x\{x}, T)
	return with V wout
	
```