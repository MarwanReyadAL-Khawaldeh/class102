# Color

## Introduction to Color
CSS supports a wide variety of colors. These include named colors, like blue, black, and LimeGreen, along with colors described by a numeric value. Using a numeric system allows us to take advantage of the whole spectrum of colors that browsers support.



## Foreground Color color
The color property allows you
to specify the color of text inside
an element.

**Colors in CSS can be described in three different ways:**

* Named colors : English words that describe colors, also called keyword colors.

* RGB : numeric values that describe a mix of red, green, and blue.

* HSL : numeric values that describe a mix of hue, saturation, and lightness.

![css](/img/css.PNG)

## Understanding Color
Every color on a computer screen is created by mixing amounts of red,
green, and blue. To find the color you want, you can use a color picker.

* **RGB Values**
Values for red, green, and blue
are expressed as numbers
between 0 and 255.

* **Hex Codes**
Hex values represent values
for red, green, and blue in
hexadecimal code.

* **Color Names**
Colors are represented by
predefined names. However,
they are very limited in number.

* **Hue**
Hue is near to the colloquial idea
of color. Technically speaking
however, a color can also have
saturation and brightness as
well as hue.

* **Saturation**
Saturation refers to the amount
of gray in a color. At maximum
saturation, there would be no
gray in the color. At minimum
saturation, the color would be
mostly gray.

* **Brightness**
Brightness (or "value") refers
to how much black is in a color.
At maximum brightness, there
would be no black in the color.
At minimum brightness, the
color would be very dark.

# Contrast
When picking foreground and background
colors, it is important to ensure that there is
enough contrast for the text to be legible.

* **Low Contrast**
1. Text is harder to read when
there is low contrast between
background and foreground
colors.

2. A lack of contrast is particularly
a problem for those with
visual impairments and color
blindness.

3. It also affects those with poor
monitors and sunlight on their
screens 

* **High Contrast**
Text is easier to read when
there is higher contrast between
background and foreground
colors.

* **Medium Contrast**
For long spans of text, reducing the contrast a little bit improves readability.

## Opacity and Alpha

To use opacity in the HSL color scheme, use hsla instead of hsl, and four values instead of three. For example:

```color: hsla(34, 100%, 50%, 0.1);```

The first three values work the same as hsl. The fourth value (which we have not seen before) is the alpha. This last value is sometimes called the opacity.

Alpha is a decimal number from zero to one. If alpha is zero, the color will be completely transparent. If alpha is one, the color will be opaque. The value for half transparent would be 0.5.



The RGB color scheme has a similar syntax for opacity, rgba. Again, the first three values work the same as rgb and the last value is the alpha. Here’s an example:

```color: rgba(234, 45, 98, 0.33);```

Alpha can only be used with HSL and RGB colors; we cannot add the alpha value to color: green color: #FFFFF.

There is, however, a named color keyword for zero opacity, transparent. It’s equivalent to rgba(0, 0, 0, 0). It’s used like any other color keyword:

```color: transparent;```

# HSL
One syntax that we can use to specify colors is called hexadecimal. Colors specified using this system are called hex colors. A hex color begins with a hash character (#) which is followed by three or six characters. The characters represent values for red, blue and green.

```DarkSeaGreen: #8FBC8F```

```Sienna:       #A0522D```

```SaddleBrown:  #8B4513```

```Brown:        #A52A2A```

```Black:        #000000 or #000```

```White:        #FFFFFF or #FFF```

```Aqua:         #00FFFF or #0FF```

You can include hex colors just as you would include named colors: 
```background-color: #9932cc;.```.

#  HSL & HSLA

* **hue**
This is expressed as an angle
(between 0 and 360 degrees).

* **saturation**
This is expressed as a
percentage.

* **lightness**
This is expressed as a
percentage with 0% being white,
50% being normal, and 100%
being black.

The hsla color property allows you to specify color properties using hue, saturation, and lightness , and adds a fourth value which represents transparency.

* **alpha**
This is expressed as a number between 0 and 1.0.
For example, 0.5 represents 50% transparency, and 0.75 represents 75% transparency.
