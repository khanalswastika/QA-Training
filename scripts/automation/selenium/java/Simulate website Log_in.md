## Code
```
import org.openqa.selenium.*;
import org.openqa.selenium.chrome.ChromeDriver;

public class First_Day {

	public static void main(String[] args) throws InterruptedException {
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://demoblaze.com");
		
		WebElement nav_login, uname, pwd, loginbutton;
		nav_login = driver.findElement(By.id("login2"));
		nav_login.click();
		Thread.sleep(5000);
		uname = driver.findElement(By.id("loginusername"));
		uname.sendKeys("testmorning");
		pwd = driver.findElement(By.id("loginpassword"));
		pwd.sendKeys("test123");
		loginbutton = driver.findElement(By.xpath("//*[@id=\"logInModal\"]/div/div/div[3]/button[2]"));
		loginbutton.click();
	}
}
```