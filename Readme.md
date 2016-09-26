#GsonCleanConverter : custom gson converter ,how to use guide. 

its very easy just add to retrofit builder with parameters
for example - 

     Retrofit retrofit = new Retrofit.Builder()
            .baseUrl(BASE_URL)
            .client(client)
            .addConverterFactory(CustomConverterRegex.create("\\",""))
            .build();

This will remove all backward slashes in json api fetched.

1st Parameter is regex pattern and 2nd is replacestring.


    (CustomConverterRegex.create("A","b"))

Above will convert all capital A in json api to small b


## Installation 

its just import gsoncleaner.jar file from [https://github.com/geniushkg/GsonCleanConverter/tree/master/gsoncleaner/build/libs](https://github.com/geniushkg/GsonCleanConverter/tree/master/gsoncleaner/build/libs "Release link")


to android studio libs folder and add via dependencies in project structure dialog and now your ready to go.

**Note  : gradle retrofit , gson and gson-converter are required to work with this converter**