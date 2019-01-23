# A song of Ice and Fire
The wildlings are primitive beings, mostly armed with primitive weapons made of stone, bone, or wood. Compared to other people with more specialized tools better suited for combat, put the two together and only one will win.

It can be very tempting to pass data around as primitives rather than create a whole new object. Quite often people will use primitives to represent different kinds of objects, strings for email addresses, integers or decimals for currency.

Some of the downsides to this approach is that it robs some of the context away, if you have the number 1000 on its own, what does that number represent? A time, currency, temperature?

Primitives can contain any kind of value, what if you have a method that requires a valid email address? Do you validate it each time that method is called, what if you've got more than one method where it is required?

By grouping this kind of logic you can create code that is more understandable, better organized, reusable and easier to navigate.  

The .NET framework has quite a few built in types for some situations, `DateTime`/`DateTimeOffset` for dates, `Uri` for urls etc.

## Requirements
1. Create a new type designed to hold temperature
2. This new type must support fahrenheit, celsius and kelvin
3. When printed it should display the name and the scale being used
4. Should be able to convert from one scale to another (celsius > fahrenheit etc.)
5. Should support comparison operators (==, !=, <, >, <=, >=), is 30&deg; greater than or smaller than 76F?
6. Should support arithmatic operators (+, -, *, /), 3 x 300K = ?, 30&deg; * 300K = ? etc.
7. Should be sortable by temperature when inserted into a sorted list, coldest to warmest, eg. (30&deg;, 76F, 300K would be sorted as 300K, 76F, 30&deg;)
8. I want to create a unique collection of temperatures
9. Support conversion from string to temperature using `TypeConverter`

## Things to learn
    - structs
    - enums
    - object.ToString
    - methods
    - properties
    - operator overloading
    - object.GetHashCode
    - HashSet
    - TypeConverter
    - immutabiity

## References
https://refactoring.guru/smells/primitive-obsession