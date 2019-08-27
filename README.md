# 2110-2114
정보 프로젝트

base = input('5-3순서대로 입력해주세요') <br>
fragment = input('5-3순서대로 입력해주세요') <br>
def enzyme(base,fragemnt) : <br>
    base_saver = [] <br>
    cnt = 0 <br>
    check = 0 <br>
    while len(base[0:-1] ) != 1 : <br>
        for i in range(len(base)-2) : <br>
            if base[i:i+len(fragment)] == fragment : <br>
                base1 = base[0:i+1] <br>
                print(base1) <br>
                check += 0 <br>
                break <br>
        if check == 0 : <br>
            break <br>
        base_saver.append(base1) <br>
        cnt +=1 <br>
        base = base[len(base1):len(base)] <br>
    if check != 0 : <br>
        print('RFLP의 갯수는' , cnt , '입니다') <br>
    else : <br>
        print('만들어진 절편은 존재하지 않습니다.') <br>
enzyme(base,fragment) <br>

class Base : <br>
    def __init__(self, k=[]) : <br>
        self.bases = k <br>
    def polymerase(self) : <br>
        a = self.bases[::-1] <br>
        b = [] <br>
        for i in range(len(a)) : <br>
            if a[i] == 'A' : <br>
                b.append('T') <br>
            elif a[i] == 'G' : <br>
                b.append('C') <br>
            elif a[i] == 'C' : <br>
                b.append('G') <br>
            elif a[i] == 'T' : <br>
                b.append('A') <br>
        for i in range(len(b)) : <br>
            print(b[i], end = '') <br>
        
    def lyase(self) : 
        return self.bases[0:-1] 
    def size(self) :
        return len(self.bases) 
    def restrict(self) : 
        fragment = input('5-3순서대로 입력해주세요')
        enzyme(self.bases,fragment)
    def Dna_checker(self) : 
        for i in range(len(self.bases)): 
            if self.bases[i] == 'A': 
                continue 
            elif self.bases[i] == 'G':
                continue <br>
            elif self.bases[i] == 'C': 
                continue 
            elif self.bases[i] == 'T':
                continue <br>
        else: 
            print('다음의 DNA는 존재하지 않습니다.')
            return False 
