Ruby Recap
==========

This weekend challenge involved revisiting the basics of Ruby ahead of our introduction to the Ruby On Rails framework. There are 41 questions in the `lib/questions.rb` file, and an accompanying `spec/questions_spec.rb` file that tests the implementation of the answers provided.  To run a single example, change `it` to `fit` within the spec file and then run `$ rspec questions_spec.rb --tag focus` in the command line.  My submissions are in the `lib/questions.rb` file.

###2 Examples

```ruby

# return true if the date is a uk bank holiday for 2014
# the list of bank holidays is here:
# https://www.gov.uk/bank-holidays
def is_a_2014_bank_holiday?(date)
  bank_hols = ["25/08", "25/12", "26/12", "26/05", "05/05", "21/04", "18/04", "01/01"]
  bank_hols.include?(date.strftime("%d/%m"))
end


# capitalize the first letter in each word of a string, 
#  except 'a', 'and' and 'the'
# *unless* they come at the start of the start of the string, e.g.
# 'the lion the witch and the wardrobe' becomes
# 'The Lion the Witch and the Wardrobe'
def titleize_a_string(string)
  array = string.split(/\W+/).map {|x| ["and", "a", "the"].include?(x) ? x : x.capitalize}
  string = array.join(" ")
  string[0] = string[0].capitalize
  string
end

```