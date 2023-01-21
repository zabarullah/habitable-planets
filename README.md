# Habitable-planets
Exploring habitable planets from a CVS file

This code is using the fs and csv-parse modules from Node.js to parse a CSV file called kepler_data.csv. 
It defines a function called isHabitablePlanet that checks if a planet has a certain set of characteristics (koi_disposition is CONFIRMED, koi_insol is 
between 0.36 and 1.11, and koi_prad is less than 1.6).

The code then reads the CSV file and uses the pipe() method to pipe the file data through the parse() method from the csv-parse module, 
which is set to ignore lines starting with '#' and to use the first row as column names.

The code then sets up event listeners for the data, error, and end events. For the data event, it calls the isHabitablePlanet function on each data (planet) 
returned by the parse method and if it is a habitable planet, it push it to an array called habitablePlanets. If an error occurs, the error message will 
be logged to the console. Once the stream is finished, the code logs the name of all the habitable planets found and the number of habitable planets found 
to the console.
