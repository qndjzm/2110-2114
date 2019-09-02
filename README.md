#염기 서열 인식 및 효소 절편 제작
base = input('5-3순서대로 입력해주세요') #염기 서열 입력
fragment = input('5-3순서대로 입력해주세요') 
def enzyme(base,fragment) : 
    base_saver = [] 
    cnt = 0 
    check = 0 
    while len(base[0:-1] ) != 1 : 
        for i in range(len(base)-2) : 
            if base[i:i+len(fragment)] == fragment : 
                base1 = base[0:i+1] 
                print(base1) 
                check += 0 
                break 
        else :#모든 효소 절편이 절단되도록 설정
            print(base)
            cnt += 1
            break
        if check == 0 : 
            break 
        base_saver.append(base1) 
        cnt +=1 
        base = base[len(base1):len(base)] 
    if check != 0 : 
        print('RFLP의 갯수는' , cnt , '입니다') #효소 절편 개수 제시
    else : 
        print('만들어진 절편은 존재하지 않습니다.') 
enzyme(base,fragment) 

class Base : 
    def init(self, k=[]) : 
        self.bases = k 
    def polymerase(self) : 
        a = self.bases[::-1] 
        b = [] 
        for i in range(len(a)) : 
            if a[i] == 'A' : 
                b.append('T') 
            elif a[i] == 'G' : 
                b.append('C') 
            elif a[i] == 'C' : 
                b.append('G') 
            elif a[i] == 'T' : 
                b.append('A') 
        for i in range(len(b)) : 
            print(b[i], end = '') 

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
        print('다음의 DNA는 존재하지 않습니다.')#해당 염기 이외의 문자는 인식하지 않음
        return False 
