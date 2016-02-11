---
layout: post
title: THW - pandas
categories: meeting
---

* In ipython you can use `_` to process the last thing you processed,
not a great thing to use.
* Can pass `pandas` objects to `numpy`

##### General

* Last value for slices are not excluded, unlike `numpy`
* `mfs.loc[x,y]`: returns x through y, including y
* `mfs.iloc[x,y]`: integer location,  _does_ exclude y
* Uses filetype `hdf5` to hold data (hdf-store), can store multiple
  dataframe within the same file, retrieved with `keys` 


##### Dataframes

* _Note:_ you can read excel files via a dataframe
* Can call a column by name `df['column_name']`
* You can't call `df['row_num']` to get a row, you have to use
  `df.loc[row_num]`
* `df.ix` allows you to use mixed labels or integer locations, if you
  have a label that is an integer, it will always default to the label
  that is the integer, not the integer location.
* Generally don't want to use `df[column][row]` there are many other
  options (`ix`)
* Can change the indexing of a dataframe `df.index = []` this will
  change the index to whatever labels that you want
* Tools for fixing datasets, `df.fillna[x]` will fill any NaN's with
  the value `x`. Need to include `df.fillna[x, inplace=True]` to
  actually overwrite the objects.
* Most functions return a new object, the `inplace=True` flag
  overwrites the old object.
* `groupby('column')` make dataframes out of data that have the same
  value in 'column'. Can group by two different things. If you do
  that, you'd have to call the row with a touple `x.loc[(x,y),z]`
* `foo.xs` returns a cross section of your data for a given index, at
  a level. Syntax `fullhistogram.xs(x, level=1)` level indicates the
  level of index, if you only have one there is one, if you have
  multiple indexs, you can pick.
* 
