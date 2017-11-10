## <img src="https://avatars2.githubusercontent.com/u/210414?v=4&s=200" height="20px"> Ruby Method: `String.squeeze!`

### **DataType: String**

The **squeeze!** command allows you to remove repeating characters from a string. You can remove specific repeating characters, ranges within the alphabet, or all repeating letters.

![alt text](https://media.giphy.com/media/I8zGepJNKOGL6/giphy.gif)


Here are some examples of strings being transformed by squeeze:

```ruby
  repeat_string = "Well, hello!"
  repeat_string.squeeze! => "Wel, helo!"

  repeat_again_string = "Aahhhhhhhh!"
  repeat_again_string.squeeze!("h") => "Aah!"

  repeat_again_again_string = "   What    is     new"
  repeat_again_again_string.squeeze!(" ") => "What is new"

```

Since this has a bang at the end it replaces the original array; this is known as being executed 'in place.'
