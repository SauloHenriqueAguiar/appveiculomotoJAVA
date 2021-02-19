# appveiculomotoJAVA

package com.mycompany.veicul;


public class Moto extends veiculo {

    private float fatorDesconto;
    
    
    
    public Moto(String modelo, String placa,float valorDiaria, float fatorDesconto) {
        super(modelo, placa,valorDiaria);
        this.fatorDesconto =  fatorDesconto;
    }

    @Override
    public float calcularAluguel(int qtdDias) {
        return super.getValorDiaria()*qtdDias - (super.getValorDiaria()*qtdDias*fatorDesconto/100.0f);
    }
    
}
