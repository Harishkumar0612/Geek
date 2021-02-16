# Geek
1.Pangram program 
public class Pangram {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here//
         Scanner s=new Scanner(System.in);
        String str="a quick brown fox jump over lazy dog`                                                                                                                      ";
    System.out.print(binary(str));
    }
   static String binary(String str){
       str=str.toLowerCase();
       String o="";char p=' ';
         Map<Character,Integer>m=new TreeMap<>();
         ArrayList<String>al=new ArrayList<>();
         char x[]={'a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z'};
         for(int i=0;i<x.length;i++){
             m.put(x[i],0);
         }
         for(int i=0;i<str.length();i++){
             if(m.containsKey(str.charAt(i))){
             m.put(str.charAt(i),m.get(str.charAt(i))+1);
             }
          }
            System.out.print(m);
         Set<Map.Entry<Character,Integer>>s=m.entrySet();
         for(Map.Entry<Character,Integer>e:s){        
             if(e.getValue()==0){
                 p=e.getKey();
                 String d=Character.toString(p);
                 al.add(d);
}
}
         StringBuilder sb=new StringBuilder();
         for(String y:al ){
             sb.append(y);
         }
         o=String.valueOf(sb);
         return o;
   }
}
