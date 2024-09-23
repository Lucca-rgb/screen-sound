using System.Collections.Generic;
 
string mensagemDeBoasVindas = "Boas Vindas ao Screen Sound";
Dictionary<string, List<int>> bandasRegistradas = new Dictionary<string, List<int>>();
bandasRegistradas.Add("Linkin Park", new List<int> { 10, 8, 6});
bandasRegistradas.Add("The Beatles", new List<int> { 8, 8, 8 });
bandasRegistradas.Add("Black Sabbath", new List<int> { 8, 9, 10 });
void ExibirLogo()
{
    Console.WriteLine("Screen Sound");
    Console.WriteLine("******************************");
    Console.WriteLine(mensagemDeBoasVindas);
    Console.WriteLine("******************************");
}
 
void ExibirOpcoesDoMenu()
{
    ExibirLogo();
    Console.WriteLine("\nDigite 1 para registrar uma banda");
    Console.WriteLine("Digite 2 para listar bandas");
    Console.WriteLine("Digite 3 para avaliar uma banda");
    Console.WriteLine("Digite 4 para exibir média de avaliação de uma banda");
    Console.WriteLine("Digite -1 para sair");
 
    Console.Write("\nDigite a sua opção: ");
    string opcaoEscolhida = Console.ReadLine()!;
    int opcaoEscolhidaNumerica = int.Parse(opcaoEscolhida);
    switch (opcaoEscolhidaNumerica)
    {
        case 1: RegistrarBanda();
            break;
        case 2: mostrarBandasRegistradas();
            break;
        case 3: AvaliarUmaBanda();
            break;
        case 4: ExibirMedia();
            break;
        case -1:
            Console.WriteLine("Tchau, Tchau. Volte Sempre :) ");
            break;
        default: 
            Console.WriteLine("Opção Inválida! tente novamente.");
            Console.WriteLine("Recarregando menu de opções...\n");
            Thread.Sleep(3000);
            Console.Clear();
            ExibirOpcoesDoMenu();
            break;
    }
}
 
void RegistrarBanda()
{
    Console.Clear();
    ExibirTituloDaOpcao("Registro das Bandas");
    Console.Write("Digite o nome da Banda: ");
    string nomeDaBanda = Console.ReadLine()!;
    bandasRegistradas.Add(nomeDaBanda, new List<int>());
    Console.Write($"A banda {nomeDaBanda} foi registrada com sucesso.");
    Thread.Sleep(3000);
    Console.Clear();
    ExibirOpcoesDoMenu();
}
 
void mostrarBandasRegistradas()
{
    Console.Clear();
    ExibirTituloDaOpcao("Exibindo Bandas registradas");
    foreach (string banda in bandasRegistradas.Keys)
    {
        Console.WriteLine($"Banda: {banda}");
    }
    Console.WriteLine("Digite qualquer tecla para voltar ao menu: ");
    Console.ReadKey();
    Console.Clear();
    ExibirOpcoesDoMenu();
}
 
void ExibirTituloDaOpcao(string Titulo)
{
    int quantidadeDeLetras = Titulo.Length;
    string asteriscos = string.Empty.PadLeft(quantidadeDeLetras, '*');
    Console.WriteLine(asteriscos);
    Console.WriteLine(Titulo);
    Console.WriteLine(asteriscos + "\n");
}
 
void AvaliarUmaBanda()
{
    Console.Clear();
    ExibirTituloDaOpcao("Avaliando Bandas");
    Console.Write("Digite o nome da banda que deseja avaliar: ");
    string nomeDaBanda = Console.ReadLine()!;
    if (bandasRegistradas.ContainsKey(nomeDaBanda))
    {
        Console.Write($"Qual a nota que deseja aplicar para a banda {nomeDaBanda}? ");
        int nota = int.Parse(Console.ReadLine()!);
        bandasRegistradas[nomeDaBanda].Add(nota);
        Console.WriteLine($"\nA nota {nota} foi registradda com sucesso.");
        Thread.Sleep(1300);
        Console.Clear();
        ExibirOpcoesDoMenu();
    }
    else 
    {
        Console.WriteLine($"\nA banda {nomeDaBanda} não foi encontrada, tente registrar ela na próxima tela ;).");
        Console.Write("Carregando Tela de Registros de Banda...");
        Thread.Sleep(5000);
        ExibirOpUm();
    }
}
 
void ExibirMedia()
{
    Console.Clear();
    ExibirTituloDaOpcao("Media de avaliação das Bandas");
    Console.Write("Digite o nome da Banda que deseja visualizar: ");
    string nomeDaBanda = Console.ReadLine()!;
    if (bandasRegistradas.ContainsKey(nomeDaBanda))
    {
        List<int>notasDaBanda = bandasRegistradas[nomeDaBanda];
        Console.WriteLine($"\nA média da banda {nomeDaBanda} é { notasDaBanda.Average()}");
        Console.WriteLine("Digite qualquer tecla para voltar ao menu: ");
        Console.ReadKey();
        Console.Clear();
        ExibirOpcoesDoMenu();
    }
    else
    {
        Console.WriteLine($"\nA banda {nomeDaBanda} não foi encontrada, tente registrar ela na próxima tela ;).");
        Console.Write("Carregando Tela de Registros de Banda...");
        Thread.Sleep(5000);
        ExibirOpUm();
    }
}
 
void ExibirOpUm()
{
    Console.Clear();
    RegistrarBanda();
}
 
ExibirOpcoesDoMenu();
