# TimeheroAPI
 A new API for minecraft bukkit/spigot 1.8 that saves you time while creating plugins with timehero!
## What it does
TimeheroAPI allows you to speed up your code with easy to use and remember methods that can do what multiple lines of code would usually do in one line. It includes all of the essentials you need to quickly and easily get your plugin done as quickly as possible.
## Features
TimeheroAPI has many features. A large amount of the methods can be found in the Javadocs. Timehero also includes a Packet API and a MySQLI API. That means you can run and get from MySQL easily with the TimeheroAPI.
For the PacketAPI use the following code
`TimeheroPacket p = t.getPacketAPI();`
For theMySQLIAPI use the following code
`TimeheroMySQLI m = t.getMySQLI();`
## Javadocs
The javadocs for the TimeheroAPI can be found above in javadocs/index.html. The javadocs can help you greatly by showing you all of the methods.
## Implementation
To implement this API simply download the .jar file above and insert it into the build path on your Java project. 
Now use this example class to implement the code:
```java
public class ExampleAPI extends JavaPlugin {
private Timehero t;
 public void onEnable() {
 this.getServer().getPluginManager().registerEvents(t, this);
  System.out.println("Testing the TimeheroAPI");
 }
 public boolean onCommand(CommandSender sender, Command cmd, String label, String args[]) {
  Player player = (Player) sender;
  //IMPLEMENT TIMEHERO API
  t = new Timehero();
  t.setPlayer(player);
  //CREATE A TIMEHERO OBJECT.
  //TIMEHERO NEEDS THE PLAYER TO SAVE TIME FOR YOU BY REMEMBERING THE PLAYER FOR YOU.
 }
}
```
## Example Use
```java
public class ExampleAPI extends JavaPlugin {
private Timehero t;
 public void onEnable() {
  System.out.println("Testing the TimeheroAPI");
 }
 public boolean onCommand(CommandSender sender, Command cmd, String label, String args[]) {
  Player player = (Player) sender;
  //IMPLEMENT TIMEHERO API
  t = new Timehero();
  t.setPlayer(player);
  //TIMEHERO NEEDS THE PLAYER TO SAVE TIME FOR YOU BY REMEMBERING THE PLAYER FOR YOU.
  if (t.checkCommand(cmd, "timeherotest") {
  //ABOVE IS AN EXAMPLE OF TIMEHERO API SAVING TIME.
  t.playerMessage("&4&lEnabled the Timehero API successfully!");
  //TIMEHERO AUTO TRANSLATES THE & COLORCODE FOR YOU.
  t.spawnEntity(t.playerLocation(), EntityType.ZOMBIE);
  //TIMEHERO SAVES THE PLAYER AND LETS YOU GET THEIR LOCATION QUICKLY.
  //TIMEHERO ALSO LETS YOU SPAWN ENTITIES QUICKLY
  t.playerGodmode();
  //TIMEHERO ALLOWS YOU TO PUT THE PLAYER IN AND OUT OF GODMODE.
  }
 }
}
```
