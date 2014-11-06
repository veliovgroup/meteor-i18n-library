##Internationalization and localization driver for Meteor (i18n)

----

####Usage:
Request by Folder.File.Object.Property
```
{{ i18n 'main.FooterText' }}
```


Request by Folder.File.Property with string placeholder replacement
```
{{ i18n 'validation.max.string' '300'  }}
```


Request by File.Property with placeholders replacements
```
{{ i18n 'main.HelloText'
    user.name=user.name /* With variable */
    user.middlename='Lee' /* With string */
    three='lastname' /* With wrong name of placeholder (by order) */  }}
```


Replace placeholders with an object
```
Template.home.helpers({
   user: {
       name: "Pavel",
       middlename: "Lee",
       lastname: "Thompson"
   }
});

{{ i18n 'main.FooterText' user=user }}
```