# 2. Lists

### 4.18

#### Array and List:

* Array: size fixed
* List: size flexible

The Golden Rule of Equals \(GRoE\): When you write `y = x`, you are telling the Java interpreter to copy the bits from x into y.

In Java, there are 8 primitive types: byte, short, int, long, float, double, boolean, char. Everything else, including arrays, is not a primitive type but rather a `reference type`.

**Reference Variable Declaration:**

When declaring a reference variable \(Dog, Planet, array, etc.\), Java allocates a box of 64 bits, no matter what type of object. The 64 bit box contains the address of the variable instead of the real data.

