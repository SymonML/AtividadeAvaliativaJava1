# AtividadeAvaliativaJava1

public class Fatura {
    private String numero;
    private String descricao;
    private int quantidade;
    private double precoItem;

    public Fatura(String numero, String descricao, int quantidade, double precoItem) {
        this.numero = numero;
        this.descricao = descricao;
        this.quantidade = quantidade;
        this.precoItem = precoItem;
    }

    public String getNumero() {
        return this.numero;
    }

    public void setNumero(String numero) {
        this.numero = numero;
    }

    public String getDescricao() {
        return this.descricao;
    }

    public void setDescricao(String descricao) {
        this.descricao = descricao;
    }

    public int getQuantidade() {
        return this.quantidade;
    }

    public void setQuantidade(int quantidade) {
        this.quantidade = quantidade;
    }

    public double getPrecoItem() {
        return this.precoItem;
    }

    public void setPrecoItem(double precoItem) {
        this.precoItem = precoItem;
    }

    public double getTotalFatura() {
        double vlTotalFat = quantidade * precoItem;
        if (vlTotalFat < 0) {
            vlTotalFat = 0.0;
        }
        return vlTotalFat;
    }

    @Override
    public String toString() {
        return "Fatura Numero: " + numero + ", Descricao: " + descricao + ", Quantidade: " + quantidade + ", Preco Unitario: R$" + precoItem + ", Total: R$" + getTotalFatura();
    }

    public static void main(String[] args) {
        Fatura fatura1 = new Fatura("1111", "Celular", 1, 1500.50);
        Fatura fatura2 = new Fatura("2222", "Carregador", 1, 50.50);

        System.out.println("A fatura sai no valor de: " + fatura1);
        System.out.println("A fatura sai no valor de: " + fatura2);
    }
}
