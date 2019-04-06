# IIS Server Helfull Codes

#### Isues:

1. All in one Backup plugin Migration ( Import 100% and pause for unlimited time)

=> Add web.config file
```xml
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
  <system.webServer>
    <security>
      <requestFiltering>
        <requestLimits maxAllowedContentLength="2147483648" />
      </requestFiltering>
    </security>
    <rewrite>
      <rules>
        <rule name="CanonicalHostNameRule2" stopProcessing="true">
          <match url="(.*)" />
            <conditions>
              <add input="{HTTP_HOST}" pattern="^www\.mitechnologies\.com\.au$" />
            </conditions>
            <action type="Redirect" url="http://mitechnologies.com.au/{R:1}" />
        </rule>
        <rule name="CanonicalHostNameRule1" stopProcessing="true">
          <match url="^(\w*/)?index\.php" />
            <conditions>
	      <add input="{HTTP_HOST}" pattern="mitechnologies\.com$" />
            </conditions>
            <action type="Redirect" url="http://mitechnologies.com.au/{R:1}" />
        </rule>
        <rule name="wordpress" patternSyntax="Wildcard">
	  <match url="*" />
	    <conditions>
	      <add input="{REQUEST_FILENAME}" matchType="IsFile" negate="true" />
	      <add input="{REQUEST_FILENAME}" matchType="IsDirectory" negate="true" />
	    </conditions>
	    <action type="Rewrite" url="index.php" />
	</rule>
      </rules>
    </rewrite>
  </system.webServer>
</configuration>

```

2. To add HTTPS in IIS Server it needs .pfx file

=> To create .pfx file, open GIT bash and code below:

```bash
openssl pkcs12 -export -out domain.name.pfx -inkey domain.name.key -in domain.name.crt
```