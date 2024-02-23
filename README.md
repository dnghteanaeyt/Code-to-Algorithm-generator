# Code-to-Algorithm-generator
Code to Algorithm generator is a Compiler Design project which uses lex and yacc programming language for lexical analysis and parsing.
import java.util.*;
class Vowel_Star{
    public static void main(){
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter Your Word In UpperCase Only.");
        String word=sc.next();
        for(int i=0;i<word.length();i++){
            if(Character.isUpperCase(word.charAt(i)))
                continue;
            else{
                System.out.println("Your Word Is Not In All Capital Letters.");
                System.exit(0);
            }
        }
        word=word+" ";
        for(int i=0;i<word.length()-1;i++){
            switch(word.charAt(i)){
                case 'A':
                case 'E':
                case 'I':
                case 'O':
                case 'U':
                word=word.substring(0,i)+"*"+word.substring(i+1,word.length()-1)+" ";
            }
        }
        System.out.println("Your Word After Updation Is : "+word);
    }
}
