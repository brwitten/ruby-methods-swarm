## <img src="https://avatars2.githubusercontent.com/u/210414?v=4&s=200" height="20px"> Ruby Method: `Array.flatten!`

### **DataType: Array**

The **flatten!** command is awesome and I love that it has the bang on it.  It is an array method that reduces a multiple dimension array into a one dimension array.  It performs this action on the originating (`self`) array

![](https://media.giphy.com/media/12qYxZDaxx4zaU/giphy.gif)

Example:

Here is an array of hobbies that are loosely associated.  Some are random so aren't associated at all.

```ruby
  hobbies = [
    ['camping', 'hiking', 'kayaking'] ,
    [ 'guitar', 'bass', 'synth'] ,
    ['arduino', 'IoT'] ,
    'woodworking',
    'gardening'
  ]
  hobbies.flatten! => [
    "camping",
    "hiking",
    "kayaking",
    "guitar",
    "bass",
    "synth",
    "arduino",
    "IoT",
    "woodworking",
    "gardening"
  ]
```
Calling `flatten!` on the hobbies array turns this two-dimensional array to a single or 'flattened' array.

Here's a pretty far-out example of `flatten!` taken to an extreme:

```ruby
wacky_array = [ [1, 2, ["three", "four", ['f', 'i', 'v', 'e']]]]
wacky_array.flatten! => [1, 2, "three", "four", "f", "i", "v", "e"]
```
**Note**: If I all `flatten!` on a one-dimensional array it will return a `nil`

```ruby
primary_colors = ['red', 'yellow', 'blue']
primary_colors.flatten! => nil
```

Since this has a bang at the end it replaces the original array; this is known as being executed 'in place.'  The non-`in place` version will return a **new** array of the original array in a flattened form.
