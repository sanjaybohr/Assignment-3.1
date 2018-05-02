# Assignment-3.1
1.	How many vowels are there in the names of USA States?

              States<- rownames(USArrests)
              vowels<-c("a","e","i","o","u")
              num_vowels = vector(mode = "integer", length = 5)
              for (i in seq_along(vowels)) {
              num_aux = str_count(tolower(States), vowels[i])
              num_vowels[i] = sum(num_aux)
              }
              names(num_vowels) = vowels
              num_vowels

2. Visualize the vowels distribution.

           barplot(num_vowels, main = "Number of vowels in USA States names",
            border = NA, ylim = c(0, 80))
