# COVID-19-TRACKER

  private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
 try
        {
          Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");
         Connection con=DriverManager.getConnection("jdbc:sqlserver://MANISHTHAKUR;databasename=Vaccine;IntegratedSecurity=true");
         con.commit();
         Statement st=con.createStatement();
         String sql="select s_id,s_name from login where s_id='"+t1.getText()+"'and s_name='"+p1.getText()+"'";
         
         ResultSet rs=st.executeQuery(sql);
         if(rs.next())
         {
             System.out.println("WELCOME YOU ARE VALID USER");
         }

            
           System.out.println("connection has been Established");
           
            
            
        }
        catch(Exception e)
        {
           System.out.println("not established");
        }
