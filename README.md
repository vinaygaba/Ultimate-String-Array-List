Ultimate String-Array List
================

![Feature Image](/images/StringArrayList.png)

As an Android developer, I absolutely hate it when I have to worry about getting data for common use cases which involve things like list of countries, list of states or even letting the users enter their birth year. We see this in most android apps, especially the ones which have a form that a user needs to fill. Even if I do find the data , it is hardly in a format that I can use easily in my app. Honestly, this is :poop:!

So I decided to do this :poop: work for you :smile:! This repo will be a comprehensive list of common use cases like these with data in a format which is extremely easy to use in an Android app.

**We have enough things to worry about as an Android developer and collecting data for common use cases shouldn't be one of them!**

Current List of String-Arrays
-----------------------------

The repository has the following list of string-array. Please note that this is continuously being updated so do check frequently. You can also send in your requests via the issue tracker. I am hoping that you take some inspiration from the categories I am adding and make contributions to this repo to make it more useful.

Name|Description
----|-----------
[App Categories.xml](/App%20Categories.xml)| List of app categories present on the Google Play Store
[Canada Province Codes.xml](/Country%20Lists/Canada/Canada%20Province%20Codes.xml)| List of codes of provinces in Canada
[Canada Provinces.xml](/Country%20Lists/Canada/Canada%20Provinces.xml)| List of provinces in Canada
[China Province Codes.xml](/Country%20Lists/China/China%20Province%20Codes.xml)| List of codes of provinces in China
[China Provinces.xml](/Country%20Lists/China/China%20Provinces.xml)| List of provinces in China
[Countries.xml](/Countries.xml)| List of all countries in the world
[Country with telephonice codes.xml](/Country%20with%20telephonice%20codes.xml)| List of countries with their telephone codes.
[Credit Card Networks.xml](/Credit%20Card%20Networks.xml)| List of credit card networks
[Cuisine.xml](/Cuisine.xml)| List of the different types of cuisines that people eat
[Days of Month.xml](/Days%20of%20Month.xml)| List of days possible in a month
[EPL Clubs.xml](/EPL%20Clubs.xml)| List of EPL Clubs(Season 14-15)
[Gender.xml](/Gender.xml)| List of the possible gender options
[Genre.xml](/Genre.xml)| List of the different genres of music
[India Banks.xml](/Country%20Lists/India/India%20Banks.xml)| List of all the banks running in India
[India Top Cities.xml](/Country%20Lists/India/India%20Top%20Cities.xml)| List of top cities in India
[India State Codes.xml](/Country%20Lists/India/India%20State%20Codes.xml)| List of codes of States in India
[India States.xml](/Country%20Lists/India/India%20States.xml)| List of States in India
[Months.xml](/Months.xml)| List of all the possible months of a year
[Moods.xml](/Moods.xml)| List of the different moods of people
[Mumbai Localities.xml](/Country%20Lists/India/Mumbai%20Localities.xml)| List of the localities of Mumbai
[Olympic Countries.xml](/Olympic%20Countries.xml)| List of countries participating in the 2016 Olympics
[Olympic Sports.xml](/Olympic%20Sports.xml)| List of the different sports being played in 2016 Olympics
[Seasons.xml](/Seasons.xml)| List of the possible season of a year
[Sex.xml](/Sex.xml)| List of different sex categories (You have a disgusting mind :smile:)
[US State Codes.xml](/US%20State%20Codes.xml)| List of codes of States in the US
[US States.xml](/US%20States.xml)| List of States in the US
[Weather.xml](/Weather.xml)| List of different weather conditions
[Years.xml](/Years.xml)| List of years from 1900 to 2050

Why String-Arrays?
------------------

String-Arrays are extremely flexible to use and it is very easy to use them in any data structure that we might like. Don't believe me? Fine let me prove it to you!

Copy the string array you want to use and place it in the `res/values/some_file_name.xml` file. It would look something like this:

```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string-array name="months">
        <item>January</item>
        .
        .
        .
    </string-array>
</resources>
```

Now to access this programmatically, we can do this:

```java
//Get it in an array of strings
String[] months = getResources().getStringArray(R.array.months);

//Convert it into a list
List<String> monthsList = new ArrayList<String>();
    list = Arrays.asList(months);
```

You can also combine these string arrays for use in your apps. Let's say I want a key-value pair with the state codes as the key and the state names as the value. To implement this, I can do the following:

```java
String[] us_state_codes = getResources().getStringArray(R.array.us_state_codes);


String[] us_state = getResources().getStringArray(R.array.us_states);

final Map<String, String> m = new HashMap<String, String>();

for(int i=0;i<us_state_codes.length();i++){
  m.put(us_state_codes[i],us_states[i]);
}

```

As you can see, this is a really flexible way to access data and can be used in various scenarios.

**Note: This is extremely basic stuff but I wanted to show these examples for people who have not worked with string-arrays before.**

Contributing
-----------------

Please use the issue tracker to report any discrepancies in the data or any string-arrays you would like to see.

For contributions to this repo, fell free to send a pull request.

Credits
-----------------

Author: Vinay Gaba (vinaygaba@gmail.com)

<a href="https://plus.google.com/+Vinaygaba">
  <img alt="Follow me on Google+"
       src="https://github.com/gabrielemariotti/cardslib/raw/master/demo/images/g+64.png" />
</a>
<a href="https://twitter.com/vinaygaba">
  <img alt="Follow me on Twitter"
       src="https://github.com/gabrielemariotti/cardslib/raw/master/demo/images/twitter64.png" />
</a>
<a href="https://www.linkedin.com/in/vinaygaba">
  <img alt="Follow me on LinkedIn"
       src="https://github.com/gabrielemariotti/cardslib/raw/master/demo/images/linkedin.png" />
</a>

License
-------

  Copyright 2015 Vinay Gaba

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
