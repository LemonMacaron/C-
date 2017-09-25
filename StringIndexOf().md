https://msdn.microsoft.com/ko-kr/library/k8b1470s(v=vs.110).aspx
https://msdn.microsoft.com/ko-kr/library/dn906223(v=vs.110).aspx

    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("The original string is:{0}{1}{0}",
                              Environment.NewLine, strTarget);
            // {0} = Environment.NewLine , 현재 환경에 대한 새로운 줄을 만듬.
            // {1} = strTarget , 위에서 설정한 The {0} jumped over the {1}.

            Console.Write("Enter an adjective (or group of adjectives) " +
                          "to describe the {0}: ==> ", animal1);
            string adj1 = Console.ReadLine();

            Console.Write("Enter an adjective (or group of adjectives) " +
                          "to describe the {0}: ==> ", animal2);
            string adj2 = Console.ReadLine();

            adj1 = adj1.Trim() + " ";
            adj2 = adj2.Trim() + " ";
            //adj1과 adj2 공백 제거

            strTarget = strTarget.Insert(strTarget.IndexOf(animal1), adj1);
            strTarget = strTarget.Insert(strTarget.IndexOf(animal2), adj2);

            Console.WriteLine("{0}The final string is:{0}{1}",
                              Environment.NewLine, strTarget);

            Console.ReadLine(); //console 창 유지를 위해 일부러 추가한 부분

            // Output from the example might appear as follows:
            //       The original string is:
            //       The fox jumped over the dog.
            //       
            //       Enter an adjective (or group of adjectives) to describe the fox: ==> bold
            //       Enter an adjective (or group of adjectives) to describe the dog: ==> lazy
            //       
            //       The final string is:
            //       The bold fox jumped over the lazy dog.
        }
