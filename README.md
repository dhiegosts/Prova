#Atividade avaliativa

void main(){
ContaBancaria c = new ContaBancaria (351, 280522, 'Dhiego', 10);
c.Deposito(4);
c.Transferencia(2);
c.Saque(1);


}

class ContaBancaria{
int ag;
int cont;
String nome;
double saldo;
  
  ContaBancaria(int ag, int cont, String nome, double saldo ){
  this.ag = ag;
  this.cont = cont;
  this.nome = nome;
  this.saldo = saldo;
  
}

void SaldoA() =>  print("Saldo Atual: ${this.saldo}");
 

void Saque(double dinheiro){
   if(saldo<dinheiro){
    print("Saldo insuficiente para saque!");
  }
    else{
      print("Saque concluido!");
      this.saldo = this.saldo - dinheiro;
      SaldoA();
    }
}

void Deposito(double dinheiro){
  this.saldo = this.saldo + dinheiro;
  print("Deposito efetuado!");
}

void Transferencia(double dinheiro){
 
    
  if(saldo<dinheiro){
    print("Saldo insuficiente!");
  }
    else{
      print("Transferencia concluida!");
      this.saldo = this.saldo - dinheiro;
      SaldoA();
    }
     
  }
}

