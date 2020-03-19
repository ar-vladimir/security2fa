# Two Factor Authentication for Sellers2 (Project Title)

Version 1.1 of the security two factor authentication

## Installation (A step by step series of examples that tell you how to get it running)
In the Application.cfc call TwoFactorAuthentication function with parameters

Use the sellers2 table to pull/save data
			

## Usage

```
<cffunction
        name="OnRequest"
        access="public"
        returntype="void"
        output="true"
        hint="Fires after pre page processing is complete.">
        
        <!--- Define arguments. --->
        <cfargument
            name="TargetPage"
            type="string"
            required="true"
            />
        
        <!--- other code here --->
        
        <!--- login code --->
 		
				<!--- 2fa challenge --->
				<cfinclude template="inc_twoFactorAuthentication.cfm">
        
        <!--- Include the requested page. --->
        <cfinclude template="#ARGUMENTS.TargetPage#" />

        <!--- Return out. --->
        <cfreturn />
        
</cffunction>        
```	


##Versioning
0.0.2 (major.minor.hotfix)
We use [SemVer](http://semver.org/) for versioning. For the versions available, see the tags on this repository.
- mxunit test intro
	~mxunit is preferred base on number of stars and fork vs testbox
- Code clean up from 0.0.1
- remove comments
- cookie.seller to cookie.selsellerid for better naming
- redirect after success 2fa challenge. use http referrer
 

##Testing
https://www.bennadel.com/blog/2394-writing-my-first-unit-tests-with-mxunit-and-coldfusion.htm
By isolating the tests within their own, light-weight application, we are able to load only the code that is being tested. As Robert Martin (Uncle Bob) would say, your application should be something that is "plugged-in" to your Domain Model.



## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
