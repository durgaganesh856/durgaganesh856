package github;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

import io.github.bonigarcia.wdm.WebDriverManager;

public class Navigation_Methods {

	public static void main(String[] args) throws InterruptedException {


		WebDriverManager.chromedriver().setup();
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://www.google.com/?authuser=1");
		Thread.sleep(1000);
		driver.findElement(By.name("q")).sendKeys("Gap QA Technologies");
		driver.findElement(By.name("q")).submit();
		Thread.sleep(2000);
		driver.navigate().to("https://accounts.google.com/v3/signin/identifier?hl=en-gb&ifkv=ARZ0qKJgOlWE--4ytoBqfmYDfsltnbaUOx20p_GwY82zpwTfiDWFfqmREcVV4JS2owo_fiKIk4y0wg&flowName=GlifWebSignIn&flowEntry=ServiceLogin&dsh=S2031020269%3A1712988558973860&theme=mn&ddm=0");
		Thread.sleep(2000);
		driver.findElement(By.id("identifierId")).sendKeys("testingmarch2024@gmail.com");
		Thread.sleep(1000);
		driver.navigate().refresh();
		Thread.sleep(2000);
		driver.navigate().back();
		Thread.sleep(2000);
		driver.navigate().forward();
		Thread.sleep(2000);
		driver.close();

	}

}








