# Assignment-9
Visualization in R
# Load the data
> motorcycles <- read.table(header=TRUE, text="
+ rownames time value
+ 1 1946 60
+ 2 1947 72
+ 3 1948 74
+ 4 1949 82
+ 5 1950 95
+ 6 1951 106
+ 7 1952 115
+ 8 1953 118
+ 9 1954 130
+ 10 1955 146
+ 11 1956 162
+ 12 1957 169
+ 13 1958 173
+ 14 1959 176
+ 15 1960 173
+ 16 1961 170
+ 17 1962 163
+ 18 1963 156
+ 19 1964 150
+ 20 1965 140
+ 21 1966 129
+ 22 1967 113
+ 23 1968 98
+ 24 1969 84
+ 25 1970 72
+ 26 1971 66
+ 27 1972 60
+ 28 1973 60
+ 29 1974 64
+ 30 1975 68
+ 31 1976 72
+ 32 1977 80
+ 33 1978 92
+ 34 1979 98
+ 35 1980 103
+ 36 1981 114
+ 37 1982 122
+ 38 1983 125
+ 39 1984 127
+ 40 1985 128
+ 41 1986 127
+ 42 1987 131
+ 43 1988 135
+ 44 1989 145
+ 45 1990 162
+ 46 1991 191
+ 47 1992 250
+ 48 1993 290")
> 
> # Basic line plot
> plot(motorcycles$time, motorcycles$value, type = "l", 
+      xlab = "Year", ylab = "Stock (in thousands)",
+      main = "Motorcycles in the Netherlands over Time")
> 
> # Install and load the lattice package if not already installed
> # install.packages("lattice")
> library(lattice)
> 
> # Lattice plot
> xyplot(value ~ time, data = motorcycles, type = "l", col = "green",
+        xlab = "Year", ylab = "Stock (in thousands)",
+        main = "Motorcycles in the Netherlands over Time")
> 
> # Install and load the ggplot2 package if not already installed
> # install.packages("ggplot2")
> library(ggplot2)
> 
> # ggplot2 plot
> ggplot(motorcycles, aes(x = time, y = value)) +
+     geom_line(color = "blue") +
+     labs(x = "Year", y = "Stock (in thousands)",
+          title = "Motorcycles in the Netherlands over Time")
