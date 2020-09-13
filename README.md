# repo_hi 
# repo_hi 
 using System;
using System.Collections;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Sample1Hashtable
{
    class Program
    {
        static void Main(string[] args)
        {
            

                //Declaración de Hashtable
                Hashtable miTabla = new Hashtable();

                //Adicionamos elementos 
                miTabla.Add("Pan", 56.5);
                miTabla.Add("Arroz", 40);
                miTabla.Add("Fideo", 50);
                miTabla.Add("Atún", 25);

                //Mostrar los elementos 
                foreach (DictionaryEntry elemento in miTabla)
                {
                    Console.WriteLine("({0}, {1})", elemento.Key, elemento.Value);
                }
                //Intentamos colocar un elemento con llave repetida
                //miTabla.Add("Pan", 22);


                //Cantidad de elementos 
                Console.WriteLine(miTabla.Count);
                Console.WriteLine("---");


                //Obtener un elemento dada su respectiva llave 
                Console.WriteLine(miTabla["Pan"]);
                Console.WriteLine(miTabla[25]);
                Console.WriteLine("---");


            //Colocar elemento en una llave
            miTabla["Queso"] = 75; //Esto adiciona(asigna)
            miTabla["Pan"] = 67;//Esto también adiciona (asigna)


           // Mostramos, vemos
            foreach (DictionaryEntry elementos in miTabla)
            {
                Console.WriteLine("({0}, {1}", elementos.Key, elementos.Value);
            }
            Console.WriteLine("---");


            //Verificamos si hay un elemento, dando como parámetro una llave
            Console.WriteLine(miTabla.Contains("Pan")); //Regresará el valor de true o false 
            Console.WriteLine(miTabla.Contains(335));
            Console.WriteLine("---");


            //Eliminamos un elemento (llave)
            miTabla.Remove("Fideo");
            //Podemos probar que resulta del intento de remover una llave que no existe


            //Vemos (o mostramos) como queda
            foreach (DictionaryEntry elementos in miTabla)
            {
                Console.WriteLine("({0}, {1})", elementos.Key, elementos.Value);
            }
            Console.WriteLine("---");


            foreach (string llave in miTabla.Keys)
            {
                Console.WriteLine(llave);
            }
            Console.WriteLine("--");


            foreach (int valor in miTabla.Values)
            {
                Console.WriteLine(valor);
            }



        }

        }
    }

    

