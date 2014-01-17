# bootstrap-datepicker fork description
This fork is a fork of a fork that enables week-selections using:
    
    .datepicker({ selectWeek: true });

And replaces the `format` input string with two functions that converts the date from and to a string, enabling your input field to contain non-standard values, such as **Week 3, 2014** for instance.

    format: {
        fromString: function(value) {
            return moment(value.replace('Week ',''), 'W, GGGG');
        },
        toString: function(date) {
            return 'Week ' + moment(date).format('W, GGGG');
        }
    }

## Example (using moment.js)

    $('#myInput').datepicker({ 
   		selectWeek: true,
	    format: {
	        fromString: function(value) {
	            return moment(value.replace('Week ',''), 'W, GGGG');
	        },
	        toString: function(date) {
	            return 'Week ' + moment(date).format('W, GGGG');
	        }
	    }
	});

## Forked readme:

## bootstrap-datepicker

This is a fork of Stefan Petre's [original code](http://www.eyecon.ro/bootstrap-datepicker/);
thanks go to him for getting this thing started!

Please note that this fork is not used on Stefan's page, nor is it maintained or contributed to by him.

Versions are incremented according to [semver](http://semver.org/).

* [Online Demo](http://eternicode.github.io/bootstrap-datepicker/)
* [Online Docs](http://bootstrap-datepicker.readthedocs.org/) (ReadTheDocs.com)
* [Google Group](https://groups.google.com/group/bootstrap-datepicker/)
* [Travis CI ![Build Status](https://travis-ci.org/eternicode/bootstrap-datepicker.png?branch=master)](https://travis-ci.org/eternicode/bootstrap-datepicker)
