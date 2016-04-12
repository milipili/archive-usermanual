Range
=====
Range is a set of consecutive value, limited by 2 extremity values.

Its notations are:

* **[:** (include) and **]:** (exclude) for the begin extremity,
followed by a numeric value as the begin value.
* **:]** (include) and **:[** (exclude) for the end extremity, 
followed by a numeric value as the end value.
* **..** (interval) is situated between the begin and the end value.


```
// The following code displays 0 1 2 3 4
foreach v in [: 0..4 :] do
    console << v;

// The following code displays 0 1 2 3 
foreach v in [: 0..4 :[ do
    console << v;

// The following code displays  1 2 3 4
foreach v in ]: 0..4 :] do
    console << v;

// The following code displays  1 2 3 
foreach v in ]: 0..4 :[ do
    console << v;

```
