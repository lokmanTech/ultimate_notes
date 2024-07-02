### <a id=python>PYTHON</a>

|Table of contents|
|:----------------|
|[Python](python.md)|
|[Graph Visualization Techniques](python.md#vt)|
|[Backslash Character](python.md#backslash)|
|[Map Visualization Techniques](python.md#map)|

### What is python?

Python is a popular language. It was created by Guido van Rossum, and released in 1991.

It is used for:
- Web development (server-side)
- software development
- mathematics
- system scripting

What can Python do?
- Used on server to create web applications.
- Used alongside software to create workflows
- connect to database systems. It can also read modify files
- used to handle big data and perform complex mathematics
- used for rapid prototyping or for production-ready software development

Why python?
- works on different platforms (Windows, Mac, Linux, Raspberry Pi, etc.)
- has a simple syntax similar to the English Language
- Has syntax that allows developers to write programs with fewer lines than some other programming languages
- runs on an interpreter system, meaning that code can be executed as soon as it is written. This means that prototyping can be very quick
- can be treated in a procedural way, an object oriented way or a functional way.

Good to know
- The most recent major version of python is python 3, which we shall be using in this. However, python 2 although not being update with anything other that security updates is still quite popular.

Pyhon Syntax compared to other programming languages
- was designed for readability, and has some similarities to the English with influence from mathematics
- uses new lines to complete a command, as opposed to other programming languages which often use semicolons or parentheses.
- relies on indentationm using whitespaces, to define scope; such as the scope of loops, funcstion and classes. Other programming languages ofthen use curly-bracket for this purpose.
















### 1.0 Familiarity with Functions, Reserved Keywords & Symbols

Familiarize yourself with functions, reserved keywords, and symbols to enhance your understanding of any programming code. In class, there is often a chapter-by-chapter syllabus, but different people have different learning methods.

For me, learning chapter by chapter sometimes makes me feel stuck, especially during programming tests. But, learning the common functions, keywords and symbols, does escalate my learning process.

Here are some common functions, keywords, and symbols:

#### Functions:
1. `print()`: Outputs a message to the console.
2. `input()`: Takes user input from the console.
3. `len()`: Returns the length of an object (e.g., string, list).
4. `range()`: Generates a sequence of numbers.
5. `type()`: Returns the type of an object.
6. `int()`: Converts a value to an integer.
7. `float()`: Converts a value to a floating-point number.
8. `str()`: Converts a value to a string.
9. `list()`: Creates a list.
10. `tuple()`: Creates a tuple.
11. `dict()`: Creates a dictionary.
12. `set()`: Creates a set.
13. `abs()`: Returns the absolute value of a number.
14. `sum()`: Returns the sum of elements in an iterable.
15. `max()`: Returns the maximum value in an iterable.
16. `min()`: Returns the minimum value in an iterable.
17. `sorted()`: Returns a sorted list of the specified iterable object.
18. `enumerate()`: Returns an enumerate object.
19. `zip()`: Returns an iterator that aggregates elements from multiple iterables.
20. `map()`: Applies a function to all items in an input list.

#### Reserved Keywords:
1. `False`: Represents the false value of the Boolean type.
2. `None`: Represents the absence of a value.
3. `True`: Represents the true value of the Boolean type.
4. `and`: A logical operator for boolean AND.
5. `as`: Used to create an alias while importing a module.
6. `assert`: Used for debugging purposes, tests if a condition is true.
7. `break`: Terminates the nearest enclosing loop.
8. `class`: Used to define a new class.
9. `continue`: Skips the rest of the code inside a loop for the current iteration only.
10. `def`: Used to define a new function.
11. `del`: Deletes objects.
12. `elif`: Used in conditional statements, same as else if.
13. `else`: Used in conditional statements.
14. `except`: Used with exceptions, what to do when an exception occurs.
15. `finally`: Used with exceptions, a block of code that will be executed no matter if there is an exception or not.
16. `for`: Used to create a for loop.
17. `from`: Used to import specific parts of a module.
18. `global`: Declares a global variable.
19. `if`: Used to make a conditional statement.
20. `import`: Used to import a module.
21. `in`: Used to check if a value is present in a list, tuple, etc.
22. `is`: Used to test if two variables refer to the same object.
23. `lambda`: Used to create an anonymous function.
24. `nonlocal`: Declares a non-local variable.
25. `not`: A logical operator for boolean NOT.
26. `or`: A logical operator for boolean OR.
27. `pass`: A null statement, a statement that will do nothing.
28. `raise`: Raises an exception.
29. `return`: Exits a function and returns a value.
30. `try`: Used to make a try...except statement.
31. `while`: Used to create a while loop.
32. `with`: Used to simplify exception handling.
33. `yield`: Ends a function and returns a generator.

#### Symbols:
1. `+`: Addition operator.
2. `-`: Subtraction operator/negation operator.
3. `*`: Multiplication operator.
4. `/`: Division operator.
5. `%`: Modulus operator.
6. `**`: Exponentiation operator.
7. `//`: Floor division operator.
8. `=`: Assignment operator.
9. `==`: Equality comparison operator.
10. `!=`: Not equal comparison operator.
11. `<`: Less than comparison operator.
12. `>`: Greater than comparison operator.
13. `<=`: Less than or equal to comparison operator.
14. `>=`: Greater than or equal to comparison operator.
15. `+=`: Increment assignment operator.
16. `-=`: Decrement assignment operator.
17. `*=`: Multiplication assignment operator.
18. `/=`: Division assignment operator.
19. `//=`: Floor division assignment operator.
20. `%=`: Modulus assignment operator.
21. `**=`: Exponentiation assignment operator.
22. `&`: Bitwise AND operator.
23. `|`: Bitwise OR operator.
24. `^`: Bitwise XOR operator.
25. `~`: Bitwise NOT operator.
26. `<<`: Bitwise left shift operator.
27. `>>`: Bitwise right shift operator.
28. `and`: Logical AND operator.
29. `or`: Logical OR operator.
30. `not`: Logical NOT operator.
31. `is`: Identity operator.
32. `in`: Membership operator.
33. `not in`: Negated membership operator.
34. `:`: Colon used in defining blocks and dictionaries.
35. `,`: Comma used to separate items in lists, tuples, and function arguments.
36. `.`: Dot used to access methods and attributes of objects.
37. `()`: Parentheses used in function calls and to define tuples.
38. `[]`: Square brackets used to define lists and to index/slice sequences.
39. `{}`: Curly braces used to define dictionaries and sets.
40. `#`: Hash symbol used to indicate comments.
41. `"""`: Triple quotes used for multi-line strings.

This list covers a broad range of functions, reserved keywords, and symbols that you'll encounter while programming in Python. There you go, happy learning, for practices you can visit any AI website for more on the definition, and test it at [one compiler](https://onecompiler.com/python) website to test the code.

## <a id="vt"></a> 8 Elegant Alternatives to Traditionals Plots

**1 Size-encoded heatmaps**

Color in heatmaps shows trends, but size clarifies exact values. Bigger size means bigger value (positive or negative).

<p align="center"><img src="img/Colour+SizeEncodedHeatmap.png"></p>

**2 Waterfall Charts**

Line/bar charts hide small changes. Waterfall charts show how values rise and fall perfectly for visualizing small, incremental changes.

<p align="center"><img src="img/WaterfallCharts.png"></p>

**3 Bump Chart**

Bar charts overwhelm with many ranks. Bump charts shine for visualizing category ranking changes over time.

<p align="center"><img src="img/BumpChart.png"></p>

**4 Raincloud Plots**

Box plots & histograms can be misleading. Raincloud plots combine 3 views (stats, overview, distribution) for clarity.

<p align="center"><img src="img/RaincloudPlots.png"></p>

**5 Hexbin Plots**

Many data points? Ditch scatter plots for hexbins! These colorful hexagons show data density, making trends clearer.

<p align="center"><img src="img/HexbinPlots.png"></p>

**6 Density Plots**

Another choice is a density plot, which illustrates the distribution of points in a two-dimensional space.

<p align="center"><img src="img/DensityPlots.png"></p>

**7 Bubble Charts**

Bar charts? Overwhelmed with categories?  Try bubble plots!  Imagine scatter plots with categories on one axis and size showing a separate value.

<p align="center"><img src="img/BubbleCharts.png"></p>

**8 Dot Plots**

Alternatively, dot plots work better for visualizing change over time.

<p align="center"><img src="img/DotPlots.png"></p>


### <a id=backslash>Backslash Character</a>

If we try to put a single quote character inside a single-quoted string, python gets confused:

```python
'Pluto's a planet!'
```
result: invalid syntax

we can fix this by "escaping" the single quote with a backslash.

```python
'Pluto\'s a planet!'
```
result: "Pluto's a planet!"

The table below summarizes some important uses of the backslash character.

|What you type..|What you get|example|print(example)|
|:-------------:|:----------:|:-----:|:------------:|
| \' | ' | 'What\'s up?' | What's up? |
| \" | " | "That's \"cool\"" | That's "cool" |
| \\ | \ | "Look, a mountain: /\\" | Look, a mountain: /\ |
| \n |  | "1\n2 3" | <p>1</p><p>2 3</p> |


the last sequence, `\n` represents the *newline character*. It causes Python to start a new line.


### <a id=map>Map Data Visualization</a>

To begin with I got this source of information from `Medium` website posted by `Aleksei Rozanov` on Feb 10, 2024, Title: [6 python libraries to make beautiful maps](https://medium.com/@alexroz/6-python-libraries-to-make-beautiful-maps-9fb9edb28b27)

**1. CARTOPY**

<p align="center"><img src="img/cartopy-01.png"></p>

Cartopy is a highly regarded library ideal for creating static maps with scalar or polygon data. It includes numerous built-in layers for land, water, and administrative borders. With its user-friendly commands, Cartopy makes map plotting straightforward and intuitive.

To install the package, you can use regular expression with *pip*:

```python
!pip install cartopy
```

Now, let's laod the data

```python
import numpy as np
import matplotlib.pyplota s plt

lats = np.load('lats.npy')
lons = np.load('lons.npy')
data = np.load('data.npy')
```

After this we can plot the data right away

```python
proj = ccrs.PlateCarree() #let's set the map's projection

fig, ax = plt.subplots(subplot_kw=dict(projection=proj), figsize=(10, 20))#now we need to create a figure with the pre-set projection and a size

ax.set_extent([-160, -105, 40 ,70], crs=ccrs.PlateCarree())#let's limit the coordinates to have only the region of MODIS product

plt.contourf(lons, lats, data,
             transform=ccrs.PlateCarree(), cmap = 'summer') #let's add a countor of the data using matplotlib
'''Adding nice cartopy features'''
ax.add_feature(cfeature.BORDERS, edgecolor='black', linewidth=1) 
ax.add_feature(cfeature.LAKES,  alpha=0.5)
ax.add_feature(cfeature.LAND)
ax.add_feature(cfeature.COASTLINE, edgecolor='black', linewidth=1)
ax.add_feature(cartopy.feature.RIVERS, edgecolor='blue', linewidth=0.5)
states_provinces = cfeature.NaturalEarthFeature(
            category='cultural',  name='admin_1_states_provinces',
            scale='10m', facecolor='none')
ax.add_feature(states_provinces, edgecolor='black', zorder=10, linestyle = '-', linewidth=0.5)


ax.gridlines(draw_labels=True)#formating the grid

lon, lat = -122.8414, 55.1119 
ax.plot(lon,lat,  'bo', markersize=6, color = 'red', transform=ccrs.Geodetic())#adding some random marker to the map
```

<p align="center"><img src="img/cartopy-02.png"></p>

As evident from the results, Cartopy offers a wealth of customization options for your maps, allowing you to manually adjust colors, line widths, density, and other layer parameters. Furthermore, the code is intuitive and easy to understand.

Another significant advantage of Cartopy is its extensive range of projections, enabling you to visualize a wide variety of data effectively.

InterruptedGoode Homolosine

<p align="center"><img src="img/cartopy-03.png"></p>

```python
import matplotlib.pyplot as plt
import cartopy.crs as ccrs

plt.figure(figsize=(6.92280629527, 3))
ax = plt.axes(projection=ccrs.InterruptedGoodeHomolosine())
ax.coastlines(resolution='110m')
ax.gridlines()
```

NorthPolarStereo

<p align="center"><img src="img/cartopy-04.png"></p>

```pyhton
import matplotlib.pyplot as plt
import cartopy.crs as ccrs

plt.figure(figsize=(3, 3))
ax = plt.axes(projection=ccrs.NorthPolarStereo())
ax.coastlines(resolution='110m')
ax.gridlines()
```

There are more Cartopy Map Visualization you can make, you can visit this website to gain more insights about Cartopy Visualization at [Cartopy Projection List](https://scitools.org.uk/cartopy/docs/v0.15/crs/projections.html)


