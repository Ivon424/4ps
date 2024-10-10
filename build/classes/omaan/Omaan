
package omaan;

import Omaan.config;
import java.util.Scanner;


public class Omaan {
    
    public static void main(String[] args) {
      
        
        Scanner sc = new Scanner (System.in);
        String response;
        do{
        System.out.println("1. ADD");
        System.out.println("2. VIEW");
        System.out.println("3. UPDATE");
        System.out.println("4. DELETE");
        System.out.println("5. EXIT");
        
        System.out.print("Enter Action: ");
        int action =  sc.nextInt();
       Omaan Omaan = new Omaan(); 
        switch(action){
            case 1:
            Omaan.add4ps();
            break;
            case 2:
             Omaan.view4ps();
            break;
            case 3:Omaan.view4ps();
                   Omaan.update4ps();
                   break;
              case 4:
             Omaan.view4ps();
             Omaan.delete4ps();
             Omaan.view4ps();
              break;
        }
            System.out.println("Do you want to continue? (yes/no): ");
            response = sc.next();  
            
        }while(response.equalsIgnoreCase("yes"));
        System.out.println("Thank you!"); 
    }



    public void add4ps(){
        Scanner sc = new Scanner(System.in);
        config conf = new config();
        
        System.out.print(" Beneficiary ID: ");
        String bID = sc.next();
        System.out.print("Full Name: ");
        String funame =sc.next();
        System.out.print("Age: ");
        String age = sc.next();
        System.out.print("Gender:");
        String gender = sc.next();
        System.out.print("Address: ");
        String address = sc.next();
        System.out.print("Family Members: ");
        String fam  = sc.next();
      
       
        String sql = "INSERT INTO tbl_4ps (b_id,full_name,Age,Gender,Address,fam_m) VALUES (?,?,?,? ,?,?)";
       
        conf.addRecord(sql, bID ,funame ,age,gender,address,fam);


    }
    
    private void view4ps() {
      
      
        String qry = "SELECT * FROM tbl_4ps"; 
        String[] hdrs = {"bID","funame", "age ","gender", " address","fam"};
        String[] clmns = {"b_id","full_name","Age","Gender","Address","fam_m"};
                

     config conf = new config();
     conf.viewRecords(qry,hdrs,clmns);
     
    }
    
    private void update4ps(){
    
        Scanner sc= new Scanner(System.in);
        System.out.print("Enter the ID to Update: ");
        int id = sc.nextInt();
        
        System.out.print("Enter new Full Name: ");
        String nfuname = sc.next();
        System.out.print("Enter new Age  : ");
        String nage = sc.next();
        System.out.print("Enter new Gender : ");
        String ngender = sc.next();
        System.out.print("Enter new Address: ");
        String naddress = sc.next();
        System.out.print("Enter new  Family Members : ");
        String nfam = sc.next();
        
        String qry = "UPDATE tbl_4ps SET full_name = ?,Age = ?, Gender = ?,address =?, fam_m =? WHERE b_id = ?";
        
        config conf = new config();
        conf.updateRecord(qry, nfuname,nage,ngender,naddress,nfam, id);
    }
    
 private void delete4ps(){
        
        Scanner sc= new Scanner(System.in);
        System.out.print("Enter the ID to Delete: ");
        int id = sc.nextInt();
        
        String qry = "DELETE FROM tbl_4ps WHERE b_id = ?";
        
        config conf = new config();
        conf.deleteRecord(qry, id);
        
 }
 
}
    

