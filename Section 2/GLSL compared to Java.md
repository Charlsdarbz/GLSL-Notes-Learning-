I jst compared anytimes he said something being simalar to JS to jst be Simlar or not to Java instead of JS

----------------------------------------------------------------------------------------------------------------------------

# GLSL
GLSL is Based on the C programming language
GLSL is strongly typed meaning we have to define the type of a variable for example

```GLSL
int num1 = 1;
float num2 = 33.3;
bool isFacing = true; // true or false
```

GLSL is strict about combining variables for example

```GLSL
int myVar = 12.0 * 3; // can't combined a float with an integer must convert the float into an int to allow it to work.

// this would work because we convert the float into a int.
int myVar = int(12.0) * 3; // 36!
```

GLSL is also strict about semi-colons (like java)
so the compiler will complain if you miss one out...

The syntax for If statements are exactly the same in GLSL as they are in Java.

```Java

// Java
if (condition) {
    // Executes if the condition is true
} else if (anotherCondition) {
    // Executes if the first condition is false and this one is true
} else {
    // Executes if all previous conditions are false
}

// Same shit

// GLSL
if (condition) {
    // Executes if the condition is true
} else if (anotherCondition) {
    // Executes if the first condition is false and this one is true
} else {
    // Executes if all previous conditions are false
}

```


A for loop

// Java
```Java

final int count = 10;
for (int i=0; i < count; i++) {
    // Do some random ah shi
} 

```

// GLSL
```GLSL
const int count = 10;
for (let i=0; i<count; i++) {
    // Also do some random ah shi
}
```



also GLSL is strict about variables that contain a single value
GLSL contains the **vec** class

# The vec class
<img width="228" height="228" alt="image" src="https://github.com/user-attachments/assets/3b4f472a-fadf-4d3d-9503-8e6998c01cc4" />



```GLSL
vec2 v = vec2(0.5);
// Now v.x = 0.5 and v.y = 0.5

//you can access them via v.x and v.y
// then you can use all the arithmatic operators on the variable
w = v * 2.0;

// you can also create a vec3 that contains 3 values
vec3 v = vec3(0.5);
// Now v.x = 0.5, v.y = 0.5 and v.z = 0.5


// you can also create a vec4 that contains 4 values
vec4 = w = vec4(1.0);
// Now w.x = 1.0, w.y = 1.0, w.z = 1.0 and w.w = 1.0

// if you want to use integers prefix the vec with an 'i'
ivec2 i1 = ivec2(725);
ivec3 i2 = ivec3(13);
ivec4 i3 = ivec4(54);

// simalar to if you want a vector with a boolean value then prefix it with a 'b'
bvec2 b1 = bvec2(true);
bvec3 b2 = bvec3(false);
bvec4 b3 = bvec4(true);


```

