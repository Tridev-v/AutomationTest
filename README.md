# AutomationTest
testing



package Management;

import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;
import org.testng.Reporter;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.BeforeMethod;

public class MMbaseclass extends Exeldata
{
	 protected WebDriver driver;

	 
    @BeforeMethod
    public void setupApplication() {
        Reporter.log("=====Browser Session Started=========", true);
        driver = new ChromeDriver();
//        driver.get("http://192.168.0.149:8086/login");
        // maximize window
        driver.manage().window().maximize();
        Reporter.log("=====Application  Started=========", true);
    }

    
    //CLICK ON TASK MANAGEMENT
    public void taskmanage() throws InterruptedException
    {
    	driver.findElement(By.xpath("(//span[@class='m-menu__link-text pl-5'])[2]")).click();
    	Thread.sleep(2000);
        Reporter.log("=====TASK MANAGEMENT CLICKED =========", true);

    }
    
    //CLICK ON COMM INVESTIGATION
    public void comminvest() throws InterruptedException
    {
    	driver.findElement(By.id("task-com-active")).click();
    	Thread.sleep(2000);
        Reporter.log("=====COMM INVESTIGATION CLICKED =========", true);

    }
    
    //CLICK ON UPDATES
    public void updates() throws InterruptedException
    {
    	driver.findElement(By.xpath("//td[@class='fs-6 sorting_1']")).click();
    	Thread.sleep(1000);
    }
    
    //ENTER FIELD VIDIT DATE
    public void fieldvisit(String date)
    {
    	JavascriptExecutor ja = (JavascriptExecutor)driver;
    	ja.executeScript("window.scrollBy(0,300)");
    	driver.findElement(By.id("visitedDate")).sendKeys(date);
    }
    
    //ENTER FIELD VISIT REMARKS
    public void remarks(String rem) throws InterruptedException
    {
    	driver.findElement(By.id("field-visit-remark")).sendKeys(rem);
    	Thread.sleep(1000);
    }
    
    //SELECT NEED METERIALS
    public void needmet(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("job-done-notdone"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
        
    
    //ERNTER JOB DONE REMARKS
    public void done(String rem) throws InterruptedException
    {
    	driver.findElement(By.id("jobDoneRemark-disabled")).sendKeys(rem);
    	Thread.sleep(1000);
    	driver.findElement(By.id("submit-invest-data")).click();
    	JavascriptExecutor ja = (JavascriptExecutor)driver;
    	ja.executeScript("window.scrollBy(0,-300)");
    }
    
    //CLICK ON MASTER
    public void master() throws InterruptedException
    {
    	driver.findElement(By.xpath("(//span[@class='m-menu__link-text pl-5'])[15]")).click();
    	Thread.sleep(1000);
    	  Reporter.log("=====MASTER CLICKED =========", true);
    }
    
    //CLICK ON MASTER ID
    public void masterid() throws InterruptedException
    {
    	driver.findElement(By.xpath("//span[text()='Master Id']")).click();
    	Thread.sleep(1000);
    	  Reporter.log("=====MASTER ID CLICKED =========", true);
    }
    
  //CLICK ON ADD ID
    public void addid() throws InterruptedException
    {
    	driver.findElement(By.xpath("//a[text()='Add Id']")).click();
    	Thread.sleep(1000);
    	  Reporter.log("=====ADD ID CLICKED =========", true);
    }
    
  //ENTER DEPARTMENT ID STARTING NUMBER
    public void depid(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("department-startNo")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER DEPARTMENT DISCRIPTION
    public void depdis(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("department-desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
  //CLICK ON ADD 
    public void add() throws InterruptedException
    {
    	driver.findElement(By.xpath("(//button[text()='Add'])[6]")).click();
    	Thread.sleep(1000);
  
    }
    
    
  //CLICK ON DEPARTMENT 
    public void department() throws InterruptedException
    {
    	driver.findElement(By.xpath("//span[text()='Department']")).click();
    	Thread.sleep(1000);
    }
    
    //SELECT DEPARTMENT NAME
    public void depname(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("departmentName"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //CLICK ON SUBMIT 
    public void submit() throws InterruptedException
    {
    	driver.findElement(By.xpath("//button[text()='Submit']")).click();
    	Thread.sleep(1000);
    }
    
    
    
    
//CLICK ON dEPARTMRNT ID
    public void departmentId() throws InterruptedException
    {
    	driver.findElement(By.xpath("//span[text()='Department Id']")).click();
    	Thread.sleep(1000);
    }
    
    
    //SELECT BUDGECT ID
    public void depname1(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("budget-deptName"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER START NUMBER
    public void bidgectIdNum(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("budget-deptId")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
   
    
    //ENTER DEPARTMENT DISCRIPTION
    public void bidgectDisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("budget-deptIdDesc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //CLICK ON ADD 
    public void add1() throws InterruptedException
    {
    	driver.findElement(By.xpath("(//button[text()='Add'])[1]")).click();
    	Thread.sleep(1000);
  
    }
    
    
    
    //SELECT OUT MATL  ISSUE ID
    public void matlissueid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("OutMatl"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER OUT MATL  ISSUE START NUMBER
    public void matlissueStartNo(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("OutMatl_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER OUT MATL  ISSU DISCRIPTION
    public void matlissueDisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("OutMatl_dec")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    //SELECT OUT SPR MTRL ISSUE ID
    public void sprmatlissueid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("OutSprMatl"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER OUT SPR MTRL ISSUE START NUMBER
    public void sprmatlissueStartNo(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("OutSprMatl_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER OUT SPR MTRL ISSU DISCRIPTION
    public void sprmatlissueDisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("OutSprMatl_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    //SELECT OUT TOOL MTRL ISSUE ID
    public void toolmatlissueid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("OutToolsMatl"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER OUT TOOL MTRL ISSUE START NUMBER
    public void toolmatlissueStartNo(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("OutToolsMatl_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER OUT TOOL MTRL ISSU DISCRIPTION
    public void toolmatlissueDisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("OutToolsMatl_Dec")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    //SELECT SEQUENCE ID
    public void sequenceif(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("Sequence"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER SEQUENCE START NUMBER
    public void sequencestartno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("Sequence_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER SEQUENCE DISCRIPTION
    public void sequencedisp(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("SequenceDesc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    

    
    //SELECT REJ DMG MATL RTN ID
    public void regdmgmtlid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("DmgMatl"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER REJ DMG MATL RTN START NUMBER
    public void regdmgmtlsno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("DmgMatl_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER REJ DMG MATL RTN DISCRIPTION
    public void regdmgmtldis(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("DmgMatl_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
   //////////////////////////////////////////////////////////////////////////// 
    
    //SELECT REJ DMG SPR RTN ID
    public void sprregdmgmtlid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("DmgSprRtn"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER REJ DMG SPR RTN START NUMBER
    public void sprregdmgmtlsno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("DmgSprRtn_No")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER REJ DMG SPR RTN DISCRIPTION
    public void sprregdmgmtldis(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("DmgSprRtn_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    //SELECT REJ DMG TOOL RTN ID
    public void toolregdmgmtlid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("DmgToolsRtn"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER REJ DMG SPR TOOL START NUMBER
    public void toolregdmgmtlsno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("DmgToolsRtn_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER REJ DMG SPR TOOL DISCRIPTION
    public void toolregdmgmtldis(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("DmgToolsRtn_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    
    
    
    //SELECT STOCK MATL RTN ID
    public void stockmtlid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("StockMatlRtn"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER STOCK MATL START NUMBER
    public void stockmtlidstarno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("StockMatlRtn_No")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER STOCK MATL DISCRIPTION
    public void stockmtldisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("StockMatlRtn_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    
    
    //SELECT STOCK SPARE MATL RTN ID
    public void stocsprkmtlid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("StockSparesRtn"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER STOCK SPARE MATL START NUMBER
    public void stocsprkmtlidstarno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("StockSparesRtn_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER STOCK SPARE MATL DISCRIPTION
    public void stocksprmtldisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("StockSparesRtn_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    
    
    
    //SELECT STOCK SPARE TOOL MATL RTN ID
    public void stocsprkmtltoolid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("StockToolsRtn"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER STOCK SPARE TOOL MATL START NUMBER
    public void stocsprkmtlidstartoolno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("StockToolsRtn_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER STOCK SPARE TOOL MATL DISCRIPTION
    public void stocksprmtltooldisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("StockToolsRtn_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    
    

    //SELECT INDENT ID
    public void indentid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("Indent"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER INDENT NUMBER
    public void indentidno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("Indent_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER INDENTL DISCRIPTION
    public void indentiddic(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("Indent_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    
    //SELECT WORK OEDER CNSL ID
    public void workcnslid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("WorkOrderCnsl"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER  WORK OEDER CNSL  NUMBER
    public void workcnslidno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("WorkOrderCnsl_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER  WORK OEDER CNSL  DISCRIPTION
    public void workcnsliddisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("WorkOrderCnsl_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    
    //SELECT WORK OEDER  ID
    public void workorderid(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("WorkOrderId"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //ENTER  WORK OEDER   NUMBER
    public void workorderidno(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("WorkOrderId_no")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER  WORK OEDER SL  DISCRIPTION
    public void workorderiddisc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("WorkOrderId_Desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
   
    
  //CLICK ON DIVISION SUB DIVISION
    public void divisionSubdivision() throws InterruptedException
    {
    	driver.findElement(By.xpath("//span[text()='Division Sub-Division']")).click();
    	Thread.sleep(1000);
  
    } 
    
    //ENTER DIVISION
    public void division(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("division")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
  //ENTER SUB DIVISION
    public void SUBdivision(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("subdivision")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
  //ENTER SUB DIVISION SERVICE STATION
    public void servicestation(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("serviceStation")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //CLICK SUBMIT //button[text()='Submit ']
    public void Submit() throws InterruptedException
    {
    	driver.findElement(By.xpath("//button[text()='Submit ']")).click();
    	Thread.sleep(1000);
  
    }
    
  //CLICK ON DIVISION LOCATION
    public void dicisioLocation() throws InterruptedException
    {
    	driver.findElement(By.xpath("//span[text()='Distribution Location'] ")).click();
    	Thread.sleep(1000);
  
    } 
    
    //SELECT DIVISION
    public void Division(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("master-division-list"));
    	Thread.sleep(1000);
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    	
  //SELECT sub DIVISION
    public void SubDivision(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("master-sub-division-list"));
    	Thread.sleep(1000);
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
  //ENTER DISRIBUTER LOCATION NAME
    public void DisLocName(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("distlocation")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    //CLICK ON DISTRIBUTION SHEDULE
    public void distibutionshedule() throws InterruptedException
    {
    	driver.findElement(By.xpath("//span[text()='Distribution Schedule']")).click();
    	Thread.sleep(1000);
    	
    }
    
    //SELECT DIVISION
    public void SheduleDivision(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("master-division-list"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    //SELECT SUB DIVISION
    public void SheduleSubDivision(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("master-sub-division-list"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    
  //SELECT DISTRIBUTION LOCATION
    public void DistribiutionLocation(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("master-distlocation-list"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    	
    }
    
    
    //ENTER CATEGORY DISCRIPTION
    public void DistributionShedule(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("distSchedule")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    
    
    
    
    
    
    
    
    
    
    
    
    //CLICK ON WORK PRIYORITY     Work Priority
    public void workpriyority() throws InterruptedException
    {
    	driver.findElement(By.xpath("//span[text()='Work Priority'] ")).click();
    	Thread.sleep(1000);
    	JavascriptExecutor ja = (JavascriptExecutor)driver;
    	ja.executeScript("window.scrollBy(0,300)");
  
    } 
    
    //SELECT WORK PRIYORITY
    public void workpriority(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("workPriority"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    }
    
    //CLICK ON SUBMIT
    public void sbmit()
    {
    	driver.findElement(By.xpath("//button[text()='Submit'] ")).click();
    }
    	
    
    //ENTER CATEGORY STARTING NUMBER
    public void catStarNum(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("category-startNo")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //ENTER CATEGORY DISCRIPTION
    public void catdisp(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("category-desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
    //CLICK ON ADD 
    public void add4() throws InterruptedException
    {
    	driver.findElement(By.xpath("(//button[text()='Add'])[4]")).click();
    	Thread.sleep(1000);
  
    }
    
    //CLICK ON ITEM CATEGORY
    public void itemcat() throws InterruptedException
    {
    	driver.findElement(By.xpath("//span[text()='Item Category']")).click();
    	Thread.sleep(1000);
    }
    
    //CANTER CATEGORY NAME
    public void catname(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("categoryName")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
    }
    
  //ENTER HSN STARTING NUMNBER
    public void hsncodeid(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("hsn-startNo")).sendKeys(depid);
    	JavascriptExecutor ja = (JavascriptExecutor)driver;
    	ja.executeScript("window.scrollBy(0,300)");
    	Thread.sleep(1000);
    	
    }
    
  //ENTER HSN discription
    
    public void hsncodediscp(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("hsn-desc")).sendKeys(depid);
    	Thread.sleep(1000);
    	
    }
    
    //CLICK ON ADD 
    public void add10() throws InterruptedException
    {
    	driver.findElement(By.xpath("(//button[text()='Add'])[10]")).click();
    	Thread.sleep(1000);
  
    }
    
    
    //CLICK ON HSN CODE
   public void hsncode() throws InterruptedException
   {
	   driver.findElement(By.xpath("//span[text()='HSN CODE']")).click();
   	Thread.sleep(1000);
	   
   }
    
   //SELECT WORK PRIYORITY
   public void hsncodecat(String meterials) throws InterruptedException
   {
   	WebElement ddown = driver.findElement(By.id("category"));
   	Select select = new Select(ddown);
   	Thread.sleep(1000);
   	select.selectByVisibleText(meterials);
   	Thread.sleep(1000);
   }
   
   //ENTER HSN CODE	
   public void Hsncode(String depid) throws InterruptedException
   {
   	driver.findElement(By.id("hsnCode")).sendKeys(depid);
   	Thread.sleep(1000);
   	
   } 
    
   
   //ENTER HSN STARTING NUMNBER
     public void itmStatingnum(String depid) throws InterruptedException
     {
     	driver.findElement(By.id("item-startNo")).sendKeys(depid);
     	JavascriptExecutor ja = (JavascriptExecutor)driver;
     	ja.executeScript("window.scrollBy(0,300)");
     	Thread.sleep(1000);
     	
     }
    
    
   //ENTER item discription  
     public void itemdisp(String depid) throws InterruptedException
     {
     	driver.findElement(By.id("item-desc")).sendKeys(depid);
     	Thread.sleep(1000);
     	
     }
    
     //CLICK ON ADD 
     public void add17() throws InterruptedException
     {
     	driver.findElement(By.xpath("(//button[text()='Add'])[17]")).click();
     	Thread.sleep(1000);
   
     }
    
     
     //CLICK ON ITEM
    public void item() throws InterruptedException
    {
 	   driver.findElement(By.xpath("//span[text()='Items']")).click();
    	Thread.sleep(1000);
 	   
    }
    
    //SELECT ITEM MASTER CATEGORY
    public void itemmastercat(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("item-master-category"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    }
    
  //SELECT ITEM MASTER STOCK TYPE
    public void stocktype(String meterials) throws InterruptedException
    {
    	WebElement ddown = driver.findElement(By.id("stockType"));
    	Select select = new Select(ddown);
    	Thread.sleep(1000);
    	select.selectByVisibleText(meterials);
    	Thread.sleep(1000);
    }
    
  //ENTER item NAME  
    public void itemname(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("itemName")).sendKeys(depid);
    	Thread.sleep(1000);
    	
    }
  //ENTER item discription  
    public void itemdispc(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("description")).sendKeys(depid);
    	Thread.sleep(1000);
    	
    }
    
    //CLICK ON BRAND NAME
    public void  brand() throws InterruptedException
    {
 	   driver.findElement(By.xpath("//span[text()='Brand']")).click();
    	Thread.sleep(1000);
 	   
    }
    
  //ENTER BRAND NAME  
    public void brandname(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("brandName")).sendKeys(depid);
    	Thread.sleep(1000);
    	
    }
    
  //ENTER BRAND DETAILS  
    public void branddet(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("brandDtls")).sendKeys(depid);
    	Thread.sleep(1000);
    	
    }
    
    //CLICK ON UNIT OF MESURE
    public void unitofmesure() throws InterruptedException
    {
 	   driver.findElement(By.xpath("//span[text()='Units Of measures']")).click();
    	Thread.sleep(1000);
 	   
    }
    
    //ENTER UNIT TYPE  
    public void unittype(String depid) throws InterruptedException
    {
    	driver.findElement(By.id("unitType")).sendKeys(depid);
    	Thread.sleep(1000);
    	
    }
    

    //ENTER UNIT DISCRIPTION
      public void unitdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("description")).sendKeys(depid);
      	Thread.sleep(1000);
      }
      	
    //ENTER Suplier STARTING NUMNBER
      public void SuplierSDtartNum(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("supplier-startNo")).sendKeys(depid);
      
      	Thread.sleep(1000);
      	
      }
    
    //ENTER supplier DISCRIPTION
      public void Suppdis(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("supplier-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      }
    
    //CLICK ON ADD 
      public void add15() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[15]")).click();
      	Thread.sleep(1000);
    
      }
    
    //CLICK ON SUPPLIER DETAILS
      public void supplierdetails() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Supplier Details']")).click();
      	Thread.sleep(1000);
    
      }
    
      //ENTER SUPPLIER REGNO
      public void regno(String depid) throws InterruptedException
      {
    	driver.findElement(By.id("reciptNo")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
      }
      
    //ENTER SUPPLIER NMAE
      public void name(String depid) throws InterruptedException
      {
    	driver.findElement(By.id("supplierName")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
      }
      
      //SELECT GST TYPE
      public void gst(String meterials) throws InterruptedException
      {
      	WebElement ddown = driver.findElement(By.id("gstType"));
      	Select select = new Select(ddown);
      	Thread.sleep(1000);
      	select.selectByVisibleText(meterials);
      	Thread.sleep(1000);
      }
      
      
      //ENTER CONTACT NNUMBER
      public void contactno(String depid) throws InterruptedException
      {
    	driver.findElement(By.id("contactNo")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
      }
      
      //ENTER ADDRESS
      public void address(String depid) throws InterruptedException
      {
    	driver.findElement(By.id("supplierAdd")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
      }
      
      //ENTER gstno
      public void gstno(String depid) throws InterruptedException
      {
    	driver.findElement(By.id("gstIn")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
      }
    //ENTER contact no
      public void phno(String depid) throws InterruptedException
      {
    	driver.findElement(By.id("phoneNo")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
      }
      
    //ENTER mail
      public void mail(String depid) throws InterruptedException
      {
    	driver.findElement(By.id("emailId")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
      }
      
      
      //SELECT state
      public void State(String meterials) throws InterruptedException
      {
      	WebElement ddown = driver.findElement(By.id("rstates"));
      	Select select = new Select(ddown);
      	Thread.sleep(1000);
      	select.selectByVisibleText(meterials);
      	Thread.sleep(1000);
      }
    //SELECT city
      public void city(String meterials) throws InterruptedException
      {
      	WebElement ddown = driver.findElement(By.id("rcities"));
      	Select select = new Select(ddown);
      	Thread.sleep(1000);
      	select.selectByVisibleText(meterials);
      	Thread.sleep(1000);
      }
    //ENTER pincode
      public void pincode(String depid) throws InterruptedException
      {
    	driver.findElement(By.id("pincode")).sendKeys(depid);
    	Thread.sleep(1000);
    	  
      }
      
      
      
      
      
      
      
      
      
      //ENTER ASSER ID
      public void Assertnum(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("assert-startNo")).sendKeys(depid);
      
      	Thread.sleep(1000);
      	
      } 
      
      
      
      //ENTER ASSER DIceription
      public void Assertdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("assert-desc")).sendKeys(depid);
      
      	Thread.sleep(1000);
      	
      } 
      
      
      //CLICK ON ADD 
      public void add0() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[1]")).click();
      	Thread.sleep(1000);
    
      }
     
      
      
      
    
      //ENTER BRANCH id
      public void brach(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("branch-startNo")).sendKeys(depid);
      
      	Thread.sleep(1000);
		
      	
      } 
    
      //ENTER branch DIceription
      public void branchdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("branch-desc")).sendKeys(depid);
      
      	Thread.sleep(1000);
      	
      } 
      
      //CLICK ON ADD 
      public void add2() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[2]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      
      
      
      
      
      
      //ENTER Borewell id
      public void Borewellid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("borewell-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER Borwell DIceription
      public void borewelldisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("borewell-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add3() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[3]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      
      
      
      
      
    //ENTER company id
      public void compid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("company-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER company DIceription
      public void compdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("company-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add5() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[5]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      
      //ENTER device id
      public void devid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("device-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER company DIceription
      public void devdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("device-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add7() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[7]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      
      
      //ENTER dma id
      public void dmaid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("dma-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER dma DIceription
      public void dmadisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("dma-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add8() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[8]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      

      //ENTER employee id
      public void empid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("employee-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER employee DIceription
      public void empdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("employee-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add9() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[9]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      

      //ENTER HAndpump id
      public void HAndpumpid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("handpump-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER HAndpump DIceription
      public void HAndpumpdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("hand pump-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add11() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[11]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      

      //ENTER pipe id
      public void pipeid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pipe-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER pipe DIceription
      public void pipedisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pipe-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add12() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[12]")).click();
      	Thread.sleep(1000);
    
      }
      
      
     
      //ENTER inward id
      public void inwardid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("in-matl-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER inward DIceription
      public void inwarddisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("in-matl-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add13() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[13]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      //ENTER spare id
      public void spareid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("spare-matl-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER spare DIceription
      public void sparedisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("spare-matl-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add14() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[14]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      
      
      //ENTER tool id
      public void toolid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("tool-equi-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER tool DIceription
      public void toolsidp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("tool-equi-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add16() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[16]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      //ENTER leakage id
      public void leakageid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("leakage-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER leakage DIceription
      public void leakagedisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("leakage-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add18() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[18]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      
      
      //ENTER meter id
      public void meterid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("meter-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER meter DIceription
      public void meterdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("meter-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add19() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[19]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      

      //ENTER pump id
      public void pumpid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pump-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER pump DIceription
      public void pumpdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pump-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add20() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[20]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      

      //ENTER stock id
      public void stockid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("stock-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER stock DIceription
      public void stockdisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("stock-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add21() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[21]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      //ENTER vehicle id
      public void vehicleid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("vehicle-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER vehicle DIceription
      public void vehicledisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("vehicle-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add22() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[22]")).click();
      	Thread.sleep(1000);
    
      }
      
      

      //ENTER ward id
      public void wardid(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("ward-startNo")).sendKeys(depid);
      	Thread.sleep(1000);
		
      } 
    
      //ENTER ward DIceription
      public void warddisp(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("ward-desc")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }   
      //CLICK ON ADD 
      public void add23() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//button[text()='Add'])[23]")).click();
      	Thread.sleep(1000);
    
      }
      
      
      //CLICK DMS MASTER 
      public void dmsmaster() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='DMA Mster']")).click();
      	Thread.sleep(1000);
    
      }
      
      //ENTER DMA NO
      public void dmano(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("dmaNumber")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER DMA NAME
      public void dmaname(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("dmaName")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      //CLICK LEAKAGE TYPE
      public void leakage() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Leakage Type']")).click();
      	Thread.sleep(1000);
    
      }
      
      //ENTER LEAKAGE TYPE
      public void leakagetype(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("leakageType")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      //CLICK MAINTANANCE 
      public void maintanance() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Maintance Type']")).click();
      	Thread.sleep(1000);
    
      }
      
      //ENTER MAINTANACE TYPE
      public void maintanancetype(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("maintenTypeStatus")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      //CLICK MAINTANANCE ACTIVITY 
      public void maintananceActivity() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Maintenance Activities']")).click();
      	Thread.sleep(1000);
    
      }
      
      //ENTER MAINTANACE Activity TYPE
      public void maintananceActivitytype(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("maintenActivity")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
    //CLICK MAINTANANCE FREQUENCY 
      public void maintanancefreq() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Maintance Frequency']")).click();
      	Thread.sleep(1000);
    
      }
      
      //ENTER MAINTANACE Activity TYPE
      public void maintananceActivitywork(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("maintanWork")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER MAINTANACE Activity TYPE
      public void maintanancefrequency(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("maintanFrequency")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //CLICK MAINTANANCE PERFORMANCE 
      public void maintananceperformance() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Maintance Performance']")).click();
      	Thread.sleep(1000);
    
      } 
      
      //ENTER MAINTANACE PERFORMANCE TYPE
      public void maintananceperformancetype(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("maintenPerformType")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
    //CLICK MEETERTYPE
      public void meetertype() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Meter Type']")).click();
      	Thread.sleep(1000);
    
      }
      
    //ENTER MEETER TYPES
      public void Metertypes(String depid) throws InterruptedException
      {
      	WebElement ele = driver.findElement(By.xpath("//input[@placeholder='Enter Meter Type']"));
      	ele.clear();
      	ele.sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      
      
      
    //CLICK MEETER MANUFACTOR
      public void meetermanufactor() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Meter Manufacture']")).click();
      	Thread.sleep(1000);
    
      }
      
      
      //ENTER MEETER MANUFACTOR NAME
      public void manufactorname(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("meterManufacture")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER MEETER DIGIT 
      public void meterdigit(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("digit")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER RECEIVED DATE  
      public void receiveddate(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("receivedDate")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER MODEL NO  
      public void meetermodel(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("meterSlNo")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER WARRANTY  
      public void meeterwarrenty(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("warranty")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER WARRANTY  
      public void meetercondition(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("condition")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      
      //CLICK PIPEMANUFACTOR
      public void pipemanufactor() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Pipe Manufacture']")).click();
      	Thread.sleep(1000);
    
      } 
      
      //ENTER PIPE TYPE
      public void pipetype(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pipeType")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER PIPE MAKE
      public void pipemake(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pipeMake")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER PIPE WARRANTY
      public void pipewarranty(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pipeWarranty")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER PIPE SIZE
      public void pipesize(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("size")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER PIPE PURCHASE DATE
      public void purchasedate(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("purchaseDate")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER PIPE POWER
      public void power(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pipePower")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      //ENTER PIPE MANUFACTOR CONTACT
      public void manufactorcontact(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("contactNo")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
    //ENTER PIPE MANUFACTOR NAME
      public void manufactroname(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("manufactureName")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
    //ENTER PIPE MANUFACTOR NAME
      public void manufactoraddress(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("manufactAddress")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      //CLICK PUMP MANUFACTOR
      public void pumpmanufactor() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Pump Manufacture']")).click();
      	Thread.sleep(1000);
    
      }  
      
      //ENTER PUMP TYPE
      public void pumptype(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pumpType")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      //ENTER PUMP WARRANTY
      public void pumpwarranty(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("warranty")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER PUMP PRUCHASE DATE
      public void Ppurchasedate(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("purchageDate")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER PUMP MAKE
      public void pumpmake(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pumpMake")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      //ENTER PUMP POWER
      public void pumppower(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("pumpPower")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
    //ENTER PUMP MANUFACTOR CONTACT
      public void mancomntact(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("contactNo")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER PUMP MANUFACTOR NAME
      public void manname(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("manufactName")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER PUMP MANUFACTOR ADDRESS
      public void manaddress(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("manufactAddress")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }

      
      //SEAFTY PRECATIONS
      public void seaftyprecation() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Safety Precautions']")).click();
      	Thread.sleep(1000);
    
      }  
     
      //ENTER SEAFTY PRECATIONS
      public void seaftuyprect(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("saftyPrecausSts")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
     

      
      //SURVICE AREA
      public void servicearea() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Service Area']")).click();
      	Thread.sleep(1000);
    
      }  
     
      //SERVICE ARA DETAILS
      public void sirviceareadetails(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("serviceArea")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      //TEAM CODE
      public void teamcode() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Team Code']")).click();
      	Thread.sleep(1000);
    
      } 
    //ENTER TEAM CODE NAME
      public void teamcodename(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("teamCode")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER SIGHT ENGINEETR NAME
      public void signtengname(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("siteEnginner")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      
      //ENTER SIGHT SUPERVISER NAME
      public void supervisername(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("siteSuperwiser")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      // CLICK ON VEHICLE MASTER DETAILS  Vehicle masters Details
      public void vehiclemaste() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Vehicle masters Details']")).click();
      	Thread.sleep(1000);
    
      } 
    //ENTER VEHICLE NUMBER
      public void vehicleno(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("vehicleNo")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER VEHICLE TYPR
      public void vehicletype(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("vehicleType")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
       
      //ENTER VEHICLE RC NO
      public void rcno(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("rcNumber")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER VEHICLE MODEL
      public void vehiclemodel(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("vehiclemodel")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER VEHICLE PURCHASE DATE
      public void pdate(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("purchaseDate")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER VEHICLE INSURANCE NO
      public void insno(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("insurancNo")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER VEHICLE INSURANCE TYPE
      public void instype(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("insurancType")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER VEHICLE DRIVER NAME
      public void drivername(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("driverName")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
    //ENTER VEHICLE DRIVER MOB NO
      public void drivermobno(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("driverMob")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      //ENTER VEHICLE DRIVER IMEI
      public void driverimei(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("imeiNumber")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER VEHICLE DRIVER SIM NO
      public void SIMNO(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("simNumber")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      //ENTER VEHICLE DRIVER ADDRESS
      public void driveradds(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("driverAddr")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
      
      
      // WARD MASTER
      public void wardmaster() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Ward Master']")).click();
      	Thread.sleep(1000);
    
      }  
      
      //ENTER WARD NUMBER
      public void wardno(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("wardNumber")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      } 
      
    //ENTER WARD NAME
      public void wardname(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("wardName")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      // WATER SOURCE
      public void watersource() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Water Source']")).click();
      	Thread.sleep(1000);
    
      }  
      
    //ENTER WATER SOURCE
      public void Entwardname(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("waterSource")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      // WORKSTAUS
      public void workstatus() throws InterruptedException
      {
      	driver.findElement(By.xpath("//span[text()='Work Status']")).click();
      	Thread.sleep(1000);
    
      }  
       
      
      //ENTER WORK STATUS
      public void WntWorkstatus(String depid) throws InterruptedException
      {
      	driver.findElement(By.id("workStatus")).sendKeys(depid);
      	Thread.sleep(1000);
      	
      }
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      //CLICK ON ASSERT MANAGEMENT 
      public void AssertManagement() throws InterruptedException
      {
      	driver.findElement(By.xpath("(//a[@class='m-menu__link m-menu__toggle'])[3]")).click();
      	Thread.sleep(1000);
    
      }
      //CLICK ASSERT ENTRY
      public void AssertEntry() throws InterruptedException
      {
      	driver.findElement(By.id("asset-entry-active")).click();
      	Thread.sleep(1000);
      	
      } 
      
    //SELECT MEETER TYPE
      public void metertype(String meterials) throws InterruptedException
      {
      	WebElement ddown = driver.findElement(By.id("meterType"));
      	Select select = new Select(ddown);
      	Thread.sleep(1000);
      	select.selectByVisibleText(meterials);
      	Thread.sleep(1000);
      }
      
      //VEHICLE PHOTO
      public void filesss(String a) throws InterruptedException
      {
      String propath =System.getProperty("user.dir");
      WebElement conno =  driver.findElement(By.xpath("//input[@name='file']"));
       conno.sendKeys(propath+a);
  	  }
      
      
      
      
      
      
      
      
      
      
      
    
    
    
    
    
    @AfterMethod
    public void closeApplication() throws InterruptedException {
        Thread.sleep(2000);
        if (driver != null) {
            driver.quit();
        }
        Reporter.log("=====Browser Session End=========", true);
    }
}
