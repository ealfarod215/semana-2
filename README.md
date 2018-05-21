# semana-2
work made in class
#main
package test;

import Ulacit.Password;

public class Test {


    public static void main(String[] args) {
        Password pass = new Password();
        Boolean isValid = pass.verify("Gato123#");
        System.out.println("el password "+ (isValid ? "si": "no"));

    }
    
}
##################
package Ulacit;

public class Password {
public Boolean verify (String password) {
    Boolean validlength = password.length() > 6;
    Boolean hasSingn = password.contains("#") || password.contains("&");
    Boolean hasnum = password.contains("0") || password.contains("1") || password.contains("2") || password.contains("3") || password.contains("4") || password.contains("5") || password.contains("6") || password.contains("7") || password.contains("8") || password.contains("9");
    return validlength && hasSingn && hasnum;
}
public int calllengnth (String password){
    if (password.length() > 15){
        System.out.println("+ que 15");
        
    }else{
        System.out.println("- que 15");
    }
    if (password.length() == 2)
        System.out.println("Es 2");
    return password.length();
    
}

public Boolean checkNumbers(String password){
    for (int i = 0; i < password.length(); i++){
       char currentChar = password.charAt(i);
       if (Character.isDigit(currentChar)) {
           System.out.println(currentChar);
       }
       
    }
    return false;
}
}
