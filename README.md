# Observation
General Observations


To read yaml file (application) into pojo do following

@Configurationproperties
public class ConfigProp {

  public List<Rules> rules =new ArrayList<>();
  
  or
  
  public List<Map<String,String>> rules =new HashMap();
  
  or
  
  Map<String,String> map=new HashMap<>()  //for single objet not list of object
  
  public static class Rules {
    Stirng id;
    String name;
    
    //getter setter
  
  }
  
  } //end of class
  
  
  
  application.yml  (Example 1 array list of Map)
  
  
  -id :1
   name : tanmay
  -id: 2
   name: Mahesh
   
   application.yml (Example 2 Map)
   
   id:1
   name: tanmay
   
   
   
   ===============================================================================================================
   
   
   apart from application.yml other files can be map to pojo
   
   @Component
   @PropertySource("classpath:test-rule.yml")
   class Rules {
   
     Stirng name;
     String id;
   
   }
   
   test-rule.yml
   
   id : 1
   name : naman
   
   ===================================================================================================================
