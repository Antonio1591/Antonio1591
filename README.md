- 👋 Hi, I’m @Antonio1591
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Antonio1591/Antonio1591 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
\using System;
using System.Globalization;
using System.Collections.Generic;


namespace exercecios
{
    internal class Program
    {
        static void Main(string[] args)
        {

            List<Agenda> agenda = new List<Agenda>();
            int Opcao;
            
            
            Console.WriteLine($"Digite a opção: 1- Adiciona Numero.  2- exibir números.   3-Finalizar. ");
            Opcao = int.Parse(Console.ReadLine());
            while (Opcao == Opcao)
            {
                
                if (Opcao == 1)
                {
                    int Para = 0;
                    int quantidade = 0;
                    Console.WriteLine($"Selecione a quantidade de regisgtro que deseja adicionar");
                    quantidade = int.Parse(Console.ReadLine());
                    while (true)
                    {                     
                        
                        Para++;                       
                        string Nome;
                        double numero;
                        Console.WriteLine("Digite o nome");
                        Nome = Console.ReadLine();
                        Console.WriteLine("Digite o numero");
                        numero = double.Parse(Console.ReadLine());
                        agenda.Add(new Agenda()
                        {

                            Nome = Nome,

                            Numero = numero,

                        });

                        if (Para == quantidade)
                        {
                            break;
                        }
                    }
                }
                else if (Opcao == 2)
                {
                    foreach(var Agenda in agenda )
                    {
                        Console.WriteLine(Agenda.Nome);
                        Console.WriteLine(Agenda.Numero);
                    }
                }

                else if (Opcao==3)
                {
                    break;
                }
               else
                {
                    Console.WriteLine("Digite uma opção valida");
                    
                }
                Console.WriteLine($"Digite a opção: 1- Adiciona Numero.  2- exibir números.   3-Finalizar. ");
                Opcao = int.Parse(Console.ReadLine());
            
            }

            Console.WriteLine($"Agenda Finalizada");
            Console.ReadLine();
        }

        public class Agenda

        {
            public String Nome;
            public double Numero;

        }

    }

}
