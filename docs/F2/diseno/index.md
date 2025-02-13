# Diseno

An example of a codeblock for Python:

```py
# Function to add two numbers
def add_two_numbers(a, b):
    return a + b

result = add_two_numbers(5, 3)
print('The sum is:', result)
```

```java title="hello.java" linenums="1"
// Initial class
public class Hello{
    public static void main(String [] args){
        System.out.println("hello world");
    }
}
```

```js title="code-examples.md" linenums="1" hl_lines="2-4"
// Function to concatenate two strings
function concatenateStrings(str1, str2) {
  return str1 + str2;
}

// Example usage
const result = concatenateStrings("Hello, ", "World!");
console.log("The concatenated string is:", result);
```


``` yaml
theme:
  features:
    - content.code.annotate # (1)
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be written in Markdown.