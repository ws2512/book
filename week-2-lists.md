# 2. Lists

### 4.18

#### Array and List:

* Array: size fixed
* List: size flexible

The Golden Rule of Equals \(GRoE\): When you write `y = x`, you are telling the Java interpreter to copy the bits from x into y.

In Java, there are 8 primitive types: byte, short, int, long, float, double, boolean, char. Everything else, including arrays, is not a primitive type but rather a `reference type`.

**Reference Variable Declaration:**

When declaring a reference variable \(Dog, Planet, array, etc.\), Java allocates a box of 64 bits, no matter what type of object. The 64 bit box contains the address of the variable instead of the real data.

#### Finished Proj 0 \(NBody Simulation\):

![Simulation of a tiny universe](.gitbook/assets/proj0.jpeg)

#### Public vs Private:

different access control to members \(i.e. method or variable\)

**`public` ,** you're effectively committing to supporting that member's behavior exactly as it is now, forever.

**`private`,** only be accessed by code inside the same **`.java`** file, so you can hide details of certain pieces to other users.

#### Nested Classes:

Declaring a nested class as `static` means that methods inside the static class can not access any of the members of the enclosing class.

#### Caching:

Saving intermediate results so we don't need repeated retrieval or calculation, this saves a lot of time.

#### Invariants:

A typical example is dummy node in lists. Adding a dummy node would often save you the extra code for special cases, making the code more clean and simple. 

#### Destructive vs. Non-destructive Methods: <a id="implementing-destructive-vs-non-destructive-methods"></a>

By destructive, we mean that the original variable changes. Be careful about writing this kind funcs.

For non-destructive, the original variable doesn't get modified, instead, a fresh new copy is modified and returned.

```text
IntList origL = IntList.of(1, 2, 3)
dSquareList(origL);
// origL is now (1, 4, 9)

IntList origL = IntList.of(1, 2, 3)
IntList squaredList = squareListIterative(origL);
// origL is still (1, 2, 3)
// squaredList is (1, 4, 9)
```

### 4.25

#### **Generics:**

Allow you to create data structures that hold any reference type. We just need to put the desired type inside of angle brackets during declaration, and also use empty angle brackets during instantiation. For example:

```text
DLList<String> d2 = new DLList<>("hello");
d2.addLast("world");
```

* If you need to instantiate a generic over a primitive type, use `Integer`, `Double`, `Character`, `Boolean`, `Long`, `Short`, `Byte`, or `Float` instead of their primitive equivalents.

#### Arrays:

A sequence of N memory boxes \(N = length\) where all boxes are of the same type, and are numbered 0 through N - 1.

**creation:**

* `x = new int[3];`
* `y = new int[]{1, 2, 3, 4, 5};`
* `int[] z = {9, 10, 11, 12, 13};`

**copy:**

* `System.arraycopy(b, 0, x, 3, 2)` is the equivalent of `x[3:5] = b[0:2]` in Python.
* Java arrays only perform bounds checking at runtime.

**resizing:**

multiplicative instead of additive

