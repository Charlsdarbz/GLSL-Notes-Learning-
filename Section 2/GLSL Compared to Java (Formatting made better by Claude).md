# GLSL

GLSL is based on the **C programming language**.

GLSL is **strongly typed**, meaning we have to define the type of a variable. For example:

```GLSL
int num1 = 1;
float num2 = 33.3;
bool isFacing = true; // true or false
```

GLSL is strict about combining different variable types. For example:

```GLSL
int myVar = 12.0 * 3; // Can't combine a float with an integer.

// This works because we convert the float into an int.
int myVar = int(12.0) * 3; // 36!
```

GLSL is also strict about **semicolons**, similar to Java, so the compiler will complain if you miss one.

---

## If Statements

The syntax for `if` statements is the same in GLSL as it is in Java.

```GLSL
if (condition) {
    // Executes if the condition is true
} else if (anotherCondition) {
    // Executes if the first condition is false and this one is true
} else {
    // Executes if all previous conditions are false
}
```

---

## For Loops

A `for` loop in GLSL is very similar to Java:

```GLSL
const int count = 10;

for (int i = 0; i < count; i++) {
    // Do some random ah shit
}
```

---

## Functions

Functions in GLSL are similar to methods in Java.

```Java
// Java
boolean inRect(Vec2 point, Vec4 rect) {
    boolean result = false;
    // Do some random ah calculations
    return result;
}
```

In GLSL, the syntax is very similar:

```GLSL
// GLSL
bool inRect(vec2 point, vec4 rect) {
    bool result = false;
    // Calculate some random ah shit
    return result;
}
```

The main difference here is that GLSL uses types such as `bool`, `vec2`, and `vec4`, while Java uses types such as `boolean` and classes like `Vec2` and `Vec4`.

---

## Function Overloading

GLSL supports **function overloading**, similar to Java.

A function can have the same name as another function as long as its **parameters are different**.

For example:

```GLSL
float calculate(float value) {
    return value * 2.0;
}

vec2 calculate(vec2 value) {
    return value * 2.0;
}
```

These are treated as different functions because they have different parameter types.

**Important:** You cannot overload a function in GLSL based only on its return type. The parameters must be different.

---

# The `vec` Types

GLSL contains built-in vector types called **`vec` types**.





These are useful because they allow you to store multiple values inside a single variable.

### `vec2`

A `vec2` contains **2 floating-point values**:

```GLSL
vec2 v = vec2(0.5);

// v.x = 0.5
// v.y = 0.5
```

You can access the individual values using `.x` and `.y`:

```GLSL
v.x
v.y
```

You can also perform arithmetic directly on the vector:

```GLSL
vec2 w = v * 2.0;
```

This multiplies **both values** by `2.0`.

---

### `vec3`

A `vec3` contains **3 floating-point values**:

```GLSL
vec3 v = vec3(0.5);

// v.x = 0.5
// v.y = 0.5
// v.z = 0.5
```

You can access the values using:

```GLSL
v.x
v.y
v.z
```

---

### `vec4`

A `vec4` contains **4 floating-point values**:

```GLSL
vec4 w = vec4(1.0);

// w.x = 1.0
// w.y = 1.0
// w.z = 1.0
// w.w = 1.0
```

The four components are:

```text
x
y
z
w
```

---

# Integer Vectors

If you want a vector containing **integers**, prefix the `vec` type with `i`.

```GLSL
ivec2 i1 = ivec2(725);
ivec3 i2 = ivec3(13);
ivec4 i3 = ivec4(54);
```

These are the integer versions of:

```text
vec2  → ivec2
vec3  → ivec3
vec4  → ivec4
```

---

# Boolean Vectors

If you want a vector containing **boolean values**, prefix the `vec` type with `b`.

```GLSL
bvec2 b1 = bvec2(true);
bvec3 b2 = bvec3(false);
bvec4 b3 = bvec4(true);
```

These are the boolean versions of:

```text
vec2  → bvec2
vec3  → bvec3
vec4  → bvec4
```

So overall:

| Type | Values |
|---|---|
| `vec2` | 2 floats |
| `vec3` | 3 floats |
| `vec4` | 4 floats |
| `ivec2` | 2 integers |
| `ivec3` | 3 integers |
| `ivec4` | 4 integers |
| `bvec2` | 2 booleans |
| `bvec3` | 3 booleans |
| `bvec4` | 4 booleans |
