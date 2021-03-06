# NAME

Business::AT::SSN

# SYNOPSIS

    use Business::AT::SSN;

# DESCRIPTION

Business::AT::SSN checks Austrian social security numbers (Sozialversicherungsnummer) 
for wellformed-ness according to 
https://www.sozialversicherung.at/portal27/portal/ecardportal/content/contentWindow?&contentid=10008.551806&action=b&cacheability=PAGE

if possible (not all SSNs contain a valid date) it also creates a DateTime Object with the 
date of birth

# METHODS

- my $obj = Business::AT::SSN->new(\[$ssn\])

    The new constructor optionally takes a ssn number

- $obj->ssn(\[$ssn\])

    if no argument is given, it returns the current ssn number.
    if an argument is provided, it will set the ssn number.

- $obj->is\_valid()

    Returns true if the ssn number is valid.

- $obj->date\_of\_birth

    Returns the date of birth as a DateTime object

- $array\_ref = $obj->error\_messages

    Returns a array ref of error messages after calling is\_valid

# AUTHOR

Mark Hofstetter <mark@hofstetter.at>

# COPYRIGHT

Copyright 2014- Mark Hofstetter

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO
