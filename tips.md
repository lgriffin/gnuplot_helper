# Navigating to your directory

On my OSX machine, it defaults to my /Users directory. So the first thing I do is
```
cd '/Users/path/to/my/working/dir'
```

I "lost" too many charts by forgetting to do this!

# Setting data file seperator

When working with CSV files, you need to set the seperator between your data otherwise you get an error such as:
```
warning: Skipping data file with no valid points
```

Setting it is simple as running:
```
set datafile separator ","
```

# Setting Variables

It's useful to have a couple of variables set, particularly colours for allowing you set the colours for certain elements of your graphs. Setting a variable is as simple as:
```
red = '#FF0000'
blue = '#0000FF'
```

Finding that niche colour you like is important. Factoring in poor projectors, or black/white requirements so I always find it useful to set it as a variable

# Setting Axis Labels

Graphs have an XLabel and a YLabel corresponding to the X-Axis and Y-Axis accordingly. Gnuplot also allows you set a 2nd Y-Axis label, called the Y2Label allowing you have multiple scales associated with a graph. Setting labels is as follows:

```
set ylabel 'This is the vertical Y-Axis Label on the left of your chart'
set xlabel 'This is the horizontal X-Axis Label on the bottom of your chart'
set y2label 'This adds a right hand Y2-Axis Label on the right of your chart'
```

# Manually setting ranges

Gnuplot will try and represent your data automatically to fit the scales of the graph. However at times it is useful to set the range manually. This works particularly well with percentages. Ranges can be negative and have a min and max in the format [min:max]. As such you can set one or both, leaving a blank option to show you are only range limiting one side.

```
set yrange [0:100]
set xrange [-10:10]
set zrange [:500]
set y2range [0:1000]
```
