# criar usuario-login-antes-atualizar-imagem-produto.
Criar um usuário e fazer login antes de atualizar a imagem de um produto.

// Processo Seletivo de QA
//Realize os cenários a seguir no site Advantage Online Shopping:

// Será necessário criar um usuário e fazer login antes de atualizar a imagem de um produto.

const assert = require('assert')
describe('Default Suite', function() {
  this.timeout(30000)
  let driver
  let vars
  beforeEach(async function() {
    driver = await new Builder().forBrowser('chrome').build()
    vars = {}
  })
  afterEach(async function() {
    await driver.quit();
  })
  it('LOGIN', async function() {
    // Test name: LOGIN
    // Step # | name | target | value | comment
    // 1 | open | https://advantageonlineshopping.com/#/ |  | 
    await driver.get("https://advantageonlineshopping.com/#/")
    // 2 | setWindowSize | 1004x708 |  | 
    await driver.manage().window().setRect({ width: 1004, height: 708 })
    // 3 | click | id=menuUser |  | 
    await driver.findElement(By.id("menuUser")).click()
    // 4 | click | linkText=CREATE NEW ACCOUNT |  | 
    await driver.findElement(By.linkText("CREATE NEW ACCOUNT")).click()
    // 5 | click | css=.spliter:nth-child(2) > .ng-isolate-scope:nth-child(1) label:nth-child(4) |  | 
    await driver.findElement(By.css(".spliter:nth-child(2) > .ng-isolate-scope:nth-child(1) label:nth-child(4)")).click()
    // 6 | type | name=usernameRegisterPage | Claudinei | 
    await driver.findElement(By.name("usernameRegisterPage")).sendKeys("Claudinei")
    // 7 | click | css=div:nth-child(1) > .spliter:nth-child(2) > .ng-isolate-scope:nth-child(2) > .inputContainer |  | 
    await driver.findElement(By.css("div:nth-child(1) > .spliter:nth-child(2) > .ng-isolate-scope:nth-child(2) > .inputContainer")).click()
    // 8 | click | css=.spliter:nth-child(2) > .ng-isolate-scope:nth-child(2) label:nth-child(4) |  | 
    await driver.findElement(By.css(".spliter:nth-child(2) > .ng-isolate-scope:nth-child(2) label:nth-child(4)")).click()
    // 9 | type | name=emailRegisterPage | claudineitadeu@hotmail.com | 
    await driver.findElement(By.name("emailRegisterPage")).sendKeys("claudineitadeu@hotmail.com")
    // 10 | type | name=first_nameRegisterPage | Claudinei | 
    await driver.findElement(By.name("first_nameRegisterPage")).sendKeys("Claudinei")
    // 11 | type | name=last_nameRegisterPage | Tadeu Barbosa | 
    await driver.findElement(By.name("last_nameRegisterPage")).sendKeys("Tadeu Barbosa")
    // 12 | type | name=phone_numberRegisterPage | 11949180468 | 
    await driver.findElement(By.name("phone_numberRegisterPage")).sendKeys("11949180468")
    // 13 | select | name=countryListboxRegisterPage | label=Brazil | 
    {
      const dropdown = await driver.findElement(By.name("countryListboxRegisterPage"))
      await dropdown.findElement(By.xpath("//option[. = 'Brazil']")).click()
    }
    // 14 | type | name=cityRegisterPage | São Paulo | 
    await driver.findElement(By.name("cityRegisterPage")).sendKeys("São Paulo")
    // 15 | type | name=addressRegisterPage | Rua Vitório Azzalin | 
    await driver.findElement(By.name("addressRegisterPage")).sendKeys("Rua Vitório Azzalin")
    // 16 | type | name=state_/_province_/_regionRegisterPage | SP | 
    await driver.findElement(By.name("state_/_province_/_regionRegisterPage")).sendKeys("SP")
    // 17 | type | name=postal_codeRegisterPage | 03961-090 | 
    await driver.findElement(By.name("postal_codeRegisterPage")).sendKeys("03961-090")
    // 18 | click | css=.spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) label:nth-child(4) |  | 
    await driver.findElement(By.css(".spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) label:nth-child(4)")).click()
    // 19 | type | name=passwordRegisterPage | Mane@1965 | 
    await driver.findElement(By.name("passwordRegisterPage")).sendKeys("Mane@1965")
    // 20 | click | css=.spliter:nth-child(3) > .ng-isolate-scope:nth-child(2) label:nth-child(4) |  | 
    await driver.findElement(By.css(".spliter:nth-child(3) > .ng-isolate-scope:nth-child(2) label:nth-child(4)")).click()
    // 21 | type | name=confirm_passwordRegisterPage | Mane#1965 | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys("Mane#1965")
    // 22 | click | name=i_agree |  | 
    await driver.findElement(By.name("i_agree")).click()
    // 23 | click | id=registerCover |  | 
    await driver.findElement(By.id("registerCover")).click()
    // 24 | mouseDownAt | css=.spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) .star | 3.640625,7 | 
    {
      const element = await driver.findElement(By.css(".spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) .star"))
      await driver.actions({ bridge: true }).moveToElement(element).clickAndHold().perform()
    }
    // 25 | mouseMoveAt | css=.spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) .star | 3.640625,7 | 
    {
      const element = await driver.findElement(By.css(".spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) .star"))
      await driver.actions({ bridge: true }).moveToElement(element).perform()
    }
    // 26 | mouseUpAt | css=.spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) .star | 3.640625,7 | 
    {
      const element = await driver.findElement(By.css(".spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) .star"))
      await driver.actions({ bridge: true }).moveToElement(element).release().perform()
    }
    // 27 | click | css=div:nth-child(1) > .spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) > .inputContainer |  | 
    await driver.findElement(By.css("div:nth-child(1) > .spliter:nth-child(3) > .ng-isolate-scope:nth-child(1) > .inputContainer")).click()
    // 28 | mouseDownAt | name=passwordRegisterPage | 45.640625,16 | 
    {
      const element = await driver.findElement(By.name("passwordRegisterPage"))
      await driver.actions({ bridge: true }).moveToElement(element).clickAndHold().perform()
    }
    // 29 | mouseMoveAt | name=passwordRegisterPage | 45.640625,16 | 
    {
      const element = await driver.findElement(By.name("passwordRegisterPage"))
      await driver.actions({ bridge: true }).moveToElement(element).perform()
    }
    // 30 | mouseUpAt | name=passwordRegisterPage | 45.640625,16 | 
    {
      const element = await driver.findElement(By.name("passwordRegisterPage"))
      await driver.actions({ bridge: true }).moveToElement(element).release().perform()
    }
    // 31 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 32 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 33 | type | name=passwordRegisterPage | Mane@1980 | 
    await driver.findElement(By.name("passwordRegisterPage")).sendKeys("Mane@1980")
    // 34 | click | name=confirm_passwordRegisterPage |  | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).click()
    // 35 | click | css=div:nth-child(1) > .spliter:nth-child(3) |  | 
    await driver.findElement(By.css("div:nth-child(1) > .spliter:nth-child(3)")).click()
    // 36 | type | name=confirm_passwordRegisterPage | mANE@1980 | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys("mANE@1980")
    // 37 | click | linkText=- Same as Password |  | 
    await driver.findElement(By.linkText("- Same as Password")).click()
    // 38 | click | id=registerCover |  | 
    await driver.findElement(By.id("registerCover")).click()
    // 39 | type | name=passwordRegisterPage | cLAUDINEI#1965 | 
    await driver.findElement(By.name("passwordRegisterPage")).sendKeys("cLAUDINEI#1965")
    // 40 | click | css=div:nth-child(1) > .spliter:nth-child(3) |  | 
    await driver.findElement(By.css("div:nth-child(1) > .spliter:nth-child(3)")).click()
    // 41 | type | name=confirm_passwordRegisterPage | c | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys("c")
    // 42 | sendKeys | name=confirm_passwordRegisterPage | ${KEY_ENTER} | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys(Key.ENTER)
    // 43 | type | name=confirm_passwordRegisterPage | cLAUDINEI@1965 | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys("cLAUDINEI@1965")
    // 44 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 45 | click | name=confirm_passwordRegisterPage |  | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).click()
    // 46 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 47 | type | name=passwordRegisterPage | 1234567890 | 
    await driver.findElement(By.name("passwordRegisterPage")).sendKeys("1234567890")
    // 48 | click | name=confirm_passwordRegisterPage |  | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).click()
    // 49 | type | name=confirm_passwordRegisterPage | 1234567890 | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys("1234567890")
    // 50 | click | css=div:nth-child(1) > .spliter:nth-child(3) > .ng-isolate-scope:nth-child(2) > .inputContainer |  | 
    await driver.findElement(By.css("div:nth-child(1) > .spliter:nth-child(3) > .ng-isolate-scope:nth-child(2) > .inputContainer")).click()
    // 51 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 52 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 53 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 54 | type | name=passwordRegisterPage | cLAUDINEI1234567890 | 
    await driver.findElement(By.name("passwordRegisterPage")).sendKeys("cLAUDINEI1234567890")
    // 55 | click | name=confirm_passwordRegisterPage |  | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).click()
    // 56 | click | name=confirm_passwordRegisterPage |  | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).click()
    // 57 | click | css=div:nth-child(1) > .spliter:nth-child(3) |  | 
    await driver.findElement(By.css("div:nth-child(1) > .spliter:nth-child(3)")).click()
    // 58 | click | name=confirm_passwordRegisterPage |  | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).click()
    // 59 | type | name=confirm_passwordRegisterPage | cLAUDINEI1234567890 | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys("cLAUDINEI1234567890")
    // 60 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 61 | type | name=passwordRegisterPage | cLAUDINEI12345678 | 
    await driver.findElement(By.name("passwordRegisterPage")).sendKeys("cLAUDINEI12345678")
    // 62 | click | css=div:nth-child(1) > .spliter:nth-child(3) > .ng-isolate-scope:nth-child(2) > .inputContainer |  | 
    await driver.findElement(By.css("div:nth-child(1) > .spliter:nth-child(3) > .ng-isolate-scope:nth-child(2) > .inputContainer")).click()
    // 63 | type | name=confirm_passwordRegisterPage | cLAUDINEI12345678 | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys("cLAUDINEI12345678")
    // 64 | click | name=passwordRegisterPage |  | 
    await driver.findElement(By.name("passwordRegisterPage")).click()
    // 65 | type | name=passwordRegisterPage | mANE@1980 | 
    await driver.findElement(By.name("passwordRegisterPage")).sendKeys("mANE@1980")
    // 66 | click | css=div:nth-child(1) > .spliter:nth-child(3) > .ng-isolate-scope:nth-child(2) > .inputContainer |  | 
    await driver.findElement(By.css("div:nth-child(1) > .spliter:nth-child(3) > .ng-isolate-scope:nth-child(2) > .inputContainer")).click()
    // 67 | type | name=confirm_passwordRegisterPage | mANE@1980 | 
    await driver.findElement(By.name("confirm_passwordRegisterPage")).sendKeys("mANE@1980")
    // 68 | click | id=register_btn |  | 
    await driver.findElement(By.id("register_btn")).click()
  })
})

