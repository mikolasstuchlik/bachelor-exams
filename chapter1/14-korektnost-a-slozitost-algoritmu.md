# 14. Korektnost a složitost algoritmu

* Parciální a totální korektnost, důkazy korektnosti.
* Asymptotická složitost, $$\mathcal{O}$$-notace.
* Zdůvodnění korektnosti a složitosti základních algoritmů \(např. řadicí algoritmy, binární vyhledávání\).

> IB002, IB102/IB107

### Parciální a totální korektnost, důkazy korektnosti.

* [Otázka _Důkazy programů_](http://statnice.dqd.cz/home:inf:ap5) na dqd.cz
* [Slajdy z IB002](https://is.muni.cz/el/1433/jaro2016/IB002/um/IB002_2016_slajdy.pdf) \(str 22\)

### Asymptotická složitost, O-notace.

* [Otázka _Složitost_](http://statnice.dqd.cz/home:inf:in14) na dqd.cz
* [Slajdy z IB002](https://is.muni.cz/el/1433/jaro2016/IB002/um/IB002_2016_slajdy.pdf) \(str 33\)

### Zdůvodnění korektnosti a složitosti základních algoritmů \(např. řadicí algoritmy, binární vyhledávání\).

* [Otázka _Důkazy programů_](http://statnice.dqd.cz/home:inf:ap5) na dqd.cz

Příklad `Insert Sort`:  
\([Slajdy z IB002](https://is.muni.cz/el/1433/jaro2016/IB002/um/IB002_2016_slajdy.pdf) \(str 28\)\)

```
for j=2 to A.length do
    key <- A[j]
    i <- j-1
    while i>0 and A[i]>key do
        A[i+1] <- A[i]
        i <- i-1
    od
    A[i+1] <- key
od
```

Binární vyhledávání:  
\(Zpracováno [zde](http://interactivepython.org/runestone/static/pythonds/SortSearch/TheBinarySearch.html)\)

```
def binarySearch(alist, item):
        first = 0
        last = len(alist)-1
        found = False

        while first<=last and not found:
            midpoint = (first + last)//2
            if alist[midpoint] == item:
                found = True
            else:
                if item < alist[midpoint]:
                    last = midpoint-1
                else:
                    first = midpoint+1

        return found
```



