# 2110-2114
정보 프로젝트

dna = input('5-3 방향의 염기서열을 입력해주세요) <br>
fullprimer = input('5-3 방향의 염기서열을 입력해주세요') <br>
def enzyme(dna,fullprimer) : 
    dna_saver = []
    cnt = 0
    check = 0
    while len(dna[0:-1] ) != 1 :
        for i in range(len(dna)-1) :
            if dna[i:i+len(fullprimer)] == fullprimer :
                dna1 = dna[0:i+1]
                print(dna1)
                check += 1
                break
        else : 
            print(dna)
            cnt += 1
            break
        if check == 0 :
            break
        dna_saver.append(dna1)
        cnt +=1
        dna = dna[len(dna1):len(dna)]
    if check != 0 :
        print('RFLP의 갯수는' , cnt , '입니다')
    else :
        print('만들어진 절편은 존재하지 않습니다.')
enzyme(dna,fullprimer)

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
        
    def lyase(self) : <br>
        return self.bases[0:-1] <br>
    def size(self) : <br>
        return len(self.bases) <br>
    def restrict(self) : <br>
        fragment = input('5-3순서대로 입력해주세요') <br>
        enzyme(self.bases,fragment) <br>
    def Dna_checker(self) : <br>
        for i in range(len(self.bases)): <br>
            if self.bases[i] == 'A': <br>
                continue <br>
            elif self.bases[i] == 'G': <br>
                continue <br>
            elif self.bases[i] == 'C': <br>
                continue <br>
            elif self.bases[i] == 'T': <br>
                continue <br>
        else: <br>
            print('다음의 DNA는 존재하지 않습니다.') <br>
            return False <br>
