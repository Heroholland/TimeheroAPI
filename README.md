# TimeheroAPI
 A new API for minecraft 1.8 and up that saves you time with timehero!
## What it does
TimeheroAPI allows you to speed up your code with easy to use and remember methods that can do what multiple lines of code would usually do in one line. It includes all of the essentials you need to quickly and easily get your plugin done as quickly as possible.
## Implementation
To implement this API simply download the .jar file above and insert it into the build path on your Java project. 
Now use this example class to implement the code:
```java
public class ExampleAPI extends JavaPlugin {
private Timehero t;
 public void onEnable() {
  System.out.println("Testing the TimeheroAPI");
 }
 public boolean onCommand(CommandSender sender, Command cmd, String label, String args[]) {
  Player player = (Player) sender;
  //IMPLEMENT TIMEHERO API
  t = new Timehero(player);
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
  t = new Timehero(player);
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
