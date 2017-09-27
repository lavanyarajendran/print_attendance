# print_attendance
import java.io.*;
class StudentRecords
{
static BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

 public void addRecords() throws IOException
 {
 // Create or Modify a file for Database
 PrintWriter pw = new PrintWriter(new BufferedWriter(new
 FileWriter("studentRecords.txt",true)));
 String name, Class, fname, mname, address, dob;
 int age;
 long telephoneNo;
 String s;
 boolean addMore = false;
 // Read Data
 do
 {
  System.out.print("\nEnter name: ");
  name = br.readLine();

  System.out.print("Father's Name: ");
  fname = br.readLine();

  System.out.print("Mother's Name: ");
  mname = br.readLine();

  System.out.print("Address: ");
  address = br.readLine();

  System.out.print("Class: ");
  Class = br.readLine();

  System.out.print("Date of Birth (dd/mm/yy) : ");
  dob = br.readLine();

  System.out.print("Age: ");
  age = Integer.parseInt(br.readLine());

  System.out.print("Telephone No.: ");
  telephoneNo = Long.parseLong(br.readLine());
  // Print to File
  pw.println(name);
  pw.println(fname);
  pw.println(mname);
  pw.println(address);
  pw.println(Class);
  pw.println(dob);
  pw.println(age);
  pw.println(telephoneNo);
  
  System.out.print("\nRecords added successfully !\n\nDo you want to add more records ? (y/n) : ");
  s = br.readLine();
  if(s.equalsIgnoreCase("y"))
  {
   addMore = true;
   System.out.println();
  }
  else
   addMore = false;
 }
 while(addMore);
 pw.close();
 showMenu();
 }
