# ASPNETMVC


# ASP.NET MVC 

ASP.NET is a free web framework for building websites and web applications on .NET Framework using HTML, CSS, and JavaScript. 
ASP.NET MVC 5 is a web framework based on Model-View-Controller (MVC) architecture. 
Developers can build dynamic web applications using ASP.NET MVC framework that enables a clean separation of concerns, fast development, and TDD friendly

<img src='https://www.tutorialspoint.com/asp.net_mvc/images/building_mvc_application.jpg'/>

<img src='https://www.tutorialspoint.com/asp.net_mvc/images/mvc_architectural_pattern.jpg/>

The Model − A set of classes that describes the data you are working with as well as the business logic.

The View − Defines how the application’s UI will be displayed. It is a pure HTML, which decides how the UI is going to look like.

The Controller − A set of classes that handles communication from the user, overall application flow, and application-specific logic.


<img src='https://www.tutorialspoint.com/asp.net_mvc/images/route_handler.jpg/>

```
using System;
using System.Collections.Generic;
using System.Linq;

using System.Web;
using System.Web.Mvc;
using System.Web.Routing;

namespace MVCFirstApp {
   public class MvcApplication : System.Web.HttpApplication {
      protected void Application_Start(){
         AreaRegistration.RegisterAllAreas();
         RouteConfig.RegisterRoutes(RouteTable.Routes);
      }
   }
}

using System;
using System.Collections.Generic;
using System.Linq;

using System.Web;
using System.Web.Mvc;
using System.Web.Routing;

namespace MVCFirstApp {
   public class RouteConfig {
      public static void RegisterRoutes(RouteCollection routes){
         routes.IgnoreRoute("{resource}.axd/{*pathInfo}");
         routes.MapRoute(
            name: "Default",
            url: "{controller}/{action}/{id}",
            defaults: new{ controller = "Home", action = "Index", id = UrlParameter.Optional});
      }
   }
}
```

# Types of Action
Actions basically return different types of action results. The ActionResult class is the base for all action results. Following is the list of different kind of action results and its behavior.

Sr.No.	Name and Behavior
1	
ContentResult

Returns a string

2	
FileContentResult

Returns file content

3	
FilePathResult

Returns file content

4	
FileStreamResult

Returns file content

5	
EmptyResult

Returns nothing

6	
JavaScriptResult

Returns script for execution

7	
JsonResult

Returns JSON formatted data

8	
RedirectToResult

Redirects to the specified URL

9	
HttpUnauthorizedResult

Returns 403 HTTP Status code

10	
RedirectToRouteResult

Redirects to different action/different controller action

11	
ViewResult

Received as a response for view engine

12	
PartialViewResult

Received as a response for view engine


# Types of Filters
The ASP.NET MVC framework supports four different types of filters −

Authorization Filters − Implements the IAuthorizationFilter attribute.

Action Filters − Implements the IActionFilter attribute.

Result Filters − Implements the IResultFilter attribute.

Exception Filters − Implements the IExceptionFilter attribute.

# ASPNET MVC 1
  MVC architecture with webform engine
  Routing
  HTML Helpers
  Ajax Helpers
  Auto binding

# ASPNET MVC 2
  Area
  Asynchronous controller
  Html helper methods with lambda expression
  DataAnnotations attributes
  Client side validation
  Custom template
  Scaffolding
# ASPNET MVC 3
  Project Templates
    New Intranet Project Templates [no accountcontroller and windows auth added]
    Extensible scafolding with MVC scaffolding
    HTML5 support for new project
    Ability to create new unit test project
    Extensible new project dialog by selection of view engines
    
   View
    Razor view engine
    support for multiple view engine [cshtml-razor engine - html]
    Partial page rendering &caching
    Enable client side validation by default
    new overloads for HMTL.LabelFor()
  Controller
    Global action filters
    viewbag
    granular support for request validation
    stateless controller support
    new action results RedirectPermanent,HttpsStatusCodeResult, HttpNotFoundResult
# ASPNET MVC 4
  Framework:
    Add controllers in any custom folders
    Task support for async controllers
    bundling and minification
    Login from FB google using oath and openId dotnetopenauth
    App-Start folder for various configs
      RouteConfig.cs
      FilterConfig.cs
      WebApiConfig.cs
      BundleConfig.cs
      AuthConfig.cs
    DisplayMode

  Template
    WebApi
    Mobile
    Empty
    
# ASPNET MVC 5

    Attribute based routing
    Filter overrides  =>  allows you to clear or replace the certain filter types created in higher scope
      OverrideActionFilters to avoid action,auth,exception filters
    Asp.NET Identity support
    
# ASPNET MVC 6
    Support for Bootstrap
    Nuget package support
    Roslyn real time compiler
    routes.MapMVCAttributeRoutes();
