import java.util.*;
import java.util.Scanner;
class questaoum{
  public static void main (String [] args){
    
    // number of companions present to determine the number of times run
    System.out.println("Name character");
    Scanner input = new Scanner(System.in);
    String quant = input.nextLine();
    listListing(Integer.parseInt(quant)); 
  }
  //input names fellas
  public static void listListing(int quant){
    List <Character> grupo = new ArrayList<Character>();
    Scanner inputt = new Scanner(System.in);
    int endLin = 1;
    for (int g = 0; g < quant; g++ ){
      System.out.println("Name Character:");
      String fellas = "";
      fellas = inputt.nextLine();
      grupo.add(fellas.charAt(fellas.length() -endLin));    
    }
    contCouting(grupo);
  }
  //breeds comparison list
  public static void contCouting(List <Character> listRaces){
   
    int elfs = 0;
    int humans = 0;
    int dwarfs = 0;
    int wizards = 0;
    int hobbiteca = 0; 
    /*fuck hobbits
    i can't stand it anymore
    */
    for (int p = 0; p < listRaces.size(); p++){
      Character race = listRaces.get(p);
      if (race == 'X'){
        hobbiteca+=1;
      }else if (race == 'M'){
        wizards+=1;
      }else if ( race == 'E'){
        elfs+=1;
      }else if (race == 'A'){
        dwarfs+=1;
      }else if (race == 'H'){
        humans += 1;
      }     
    }
    System.out.println(hobbiteca + " Hobbit(s)");
    System.out.println(humans + " Humano(s)");
    System.out.println(elfs + " Elfo(s)");
    System.out.println(dwarfs + " Anao(s)");
    System.out.println(wizards + " Mago(s)");    
  } 
}

