- 👋 Hi, I’m @fasluevin
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
fasluevin/fasluevin is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


import java.sql.*; 
public class MySqlCon{ 
public static void main(String args[])
{ 
Try
{ 
Class.forName("com.mysql.jdbc.Driver"); 
Connection con=DriverManager.getConnection( 
"jdbc:mysql://localhost:3306/mydb","root",""); 
//here mydb is database name, root is username and password is nil
Statement stmt=con.createStatement(); 
ResultSet rs=stmt.executeQuery("select * from employee"); 
System.out.printf("\n%4s %15s %15s 
%15s","Roll","Name","Designation","Department");
System.out.println("\n_____________________________________________________");
while(rs.next()) 
{
System.out.printf("\n%3d %15s %15s 
%15s",rs.getInt(1),rs.getString(2),rs.getString(3),rs.getString(4)); 
}
System.out.println();
con.close();
}
catch(Exception e)
{ 
System.out.println(e);
