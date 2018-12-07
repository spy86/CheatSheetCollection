First import the regexp package

    import regexp

### Matching

    match, _ := regexp.MatchString("[a-zA-Z0-9]+", input)

match will be true if the pattern matches. To return the first match as
string use

    matchstr := regexp.FindString("([a-zA-Z0-9]+)", input)

To return all matches:

    matches := regexp.FindAllString("([a-zA-Z0-9]+)", input)

### Matching Methods

There are different matching methods