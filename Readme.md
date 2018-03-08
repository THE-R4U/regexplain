regexplain
================

<!-- Links -->

## WORK IN PROGRESS\!\!

regexplain is going to be an RStudio addin that helps you interactively
build up your regex. Inspired by [RegExr](https://regexr.com/) and
`stringr::str_view`.

## Done (ish)

You can use `view_regex()` for a `stringr::str_view()` replacement that
includes groups.

``` r
text <- c("breakfast=eggs;lunch=pizza",
          "breakfast=bacon;lunch=spaghetti", 
          "no food here")
pattern <- "((\\w+)=)(\\w+).+(ch=s?p)"

view_regex(text, pattern)
```

![Example `view_regex(text, pattern)`.](docs/view-regex.png)

## Planned (ish)

1.  An Rstudio addin gadget that allows you to interactively enter the
    regex and see the results. Like the above example, where the regex
    field is a text input.

2.  Import data from your environment, like a character vector, file, or
    data.frame column when opening the gadget.

3.  Help tab in the gadget, pulling from `?regex` but with some
    navigation.

4.  Tab to interactively explore output of varying regex-applying
    functions. In other words, see what `stringr::str_locate_all` or
    `stringr::str_match_all` or `grep` or `grepl` return when applying
    the regex to your text.
