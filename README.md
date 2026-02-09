# X-path
1. Basic XPath (Tag only)
 //input
 //button
 //a

🔹 2. XPath using attribute
 //input[@id='userId']
 //input[@name='email']
 //button[@type='submit']
 //a[@href='#']

🔹 3. XPath with multiple attributes
 //input[@id='userId' and @type='text']
 //button[@type='submit' and @name='login']

🔹 4. XPath using text()
 //button[text()='Login']
 //a[text()='Register']
 //label[text()='User Email']

🔹 5. XPath using contains()
 //input[contains(@placeholder,'email')]
 //button[contains(text(),'Submit')]
 //a[contains(@href,'facebook')]

🔹 6. XPath using starts-with()
 //input[starts-with(@id,'user')]
 //a[starts-with(text(),'Reg')]

🔹 7. XPath using normalize-space()
 //label[normalize-space()='User Email']
 //button[normalize-space()='Submit Form']

🔹 8. XPath with index
 (//input[@type='text'])[1]
 (//button)[2]
 (//a)[last()]

🔹 9. Parent / Child navigation
 //div/input
 //form//input
 //div[@class='container']/child::button

🔹 10. Following / Preceding
 //label[text()='User Email']/following::input[1]
 //input[@id='userId']/preceding::label[1]

🔹 11. Following-sibling / preceding-sibling
 //label[text()='User Email']/following-sibling::input
 //input[@id='userId']/preceding-sibling::label

🔹 12. Ancestor / Descendant
 //input[@id='userId']/ancestor::form
 //form/descendant::input

🔹 13. XPath for Buttons
 //button[text()='Login']
 //button[contains(text(),'Click')]
 //button[@type='reset']

🔹 14. XPath for Links
 //a[text()='Courses']
 //a[contains(text(),'Hub')]
 //a[@target='_blank']

🔹 15. XPath for Dropdown
 //select[@id='country']
 //select/option[text()='India']
 //select/option[contains(text(),'USA')]

🔹 16. XPath for Checkboxes / Radio buttons
 //input[@type='checkbox']
 //label[text()='Male']/preceding-sibling::input
 //input[@type='radio' and @value='female']

🔹 17. XPath for Images
 //img[@alt='SelectorsHub Logo']
 //img[contains(@src,'logo')]

🔹 18. XPath for Tables
 //table//tr
 //table//tr[3]/td[2]
 //table//th[text()='Name']

🔹 19. XPath for SVG Elements
 //*[name()='svg']
 //*[name()='svg']//*[name()='path']

🔹 20. XPath for Shadow DOM (use CSS selector only — XPath not supported)

❌ XPath cannot access shadow-root.

Use:

 element.shadowRoot.querySelector('input#name')

🔥 BONUS: Invalid XPath (for practice)

These are shown on the SelectorsHub practice page:

❌ Wrong

 //a[normalise-space()="Why testRigor?"]
 //input[@id='pass']div
 //input[@id='pass']/div/
 //label[ends-with(text(),'User Email')]


✔ Corrected

 //a[normalize-space()="Why testRigor?"]
 //input[@id='pass']/div
 //label[substring(text(), string-length(text())-9)='User Email']





<Project Sdk="Microsoft.NET.Sdk.Web">
 
  <PropertyGroup>
    <TargetFramework>net9.0</TargetFramework>
    <Nullable>enable</Nullable>
    <ImplicitUsings>enable</ImplicitUsings>
  </PropertyGroup>
 
  <ItemGroup>
    <PackageReference Include="Microsoft.AspNetCore.OpenApi" Version="9.0.12" />
    <PackageReference Include="Microsoft.AspNetCore.Authentication.JwtBearer" Version="9.0.10" />
    <PackageReference Include="Microsoft.AspNetCore.Identity.EntityFrameworkCore" Version="9.0.10" />
    <PackageReference Include="Microsoft.AspNetCore.OpenApi" Version="9.0.10" />
    <PackageReference Include="Microsoft.EntityFrameworkCore" Version="9.0.10" />
    <PackageReference Include="Microsoft.EntityFrameworkCore.Sqlite" Version="9.0.10" />
    <PackageReference Include="Microsoft.EntityFrameworkCore.SqlServer" Version="9.0.10" />
    <PackageReference Include="Microsoft.EntityFrameworkCore.Tools" Version="9.0.10">
     
 
      <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
      <PrivateAssets>all</PrivateAssets>
    </PackageReference>
    <PackageReference Include="Microsoft.VisualStudio.Web.CodeGeneration.Design" Version="9.0.0" />
      <PackageReference Include="Swashbuckle.AspNetCore" Version="9.0.6" />
    <PackageReference Include="System.IdentityModel.Tokens.Jwt" Version="8.14.0" />
  </ItemGroup>
 
</Project>
