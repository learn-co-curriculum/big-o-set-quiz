# Day 2: Big O Stack Quiz

In this quiz we'll ask you to calculate the time complexity for several of the Stack class methods. Remember that we used an Array as the underlying data structure for our class. If you don't know the time complexity for an Array method, you may need to Google.

1. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
peek() {
  return this.stack[this.size() - 1];
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def peek
  @stack.last
end
</code>
</pre>

- O(1): Constant time
  - Correct! Peeking at the last item takes constant time. An Array is the underlying data structure, and accessing an element by its index is always done in constant time. For the JS example, getting the size is also constant, so Big O is the same.
- O(n): Linear time
  - Not quite. Keep in mind that for linear time operations, the amount of time depends on the size of the input. In this case, it would then depend on the size of the stack. However, we used an Array as the underlying data structure. What's Big O for accessing an Array element by index?
- O(log n): Logarithmic time
  - Not quite. Keep in mind that for logarithmic time operations, the input gets divided as it's operated upon. In this case, it would then depend on the size of the stack. However, we used an Array as the underlying data structure. What's Big O for accessing an Array element by index?
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.

2. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
search(target) {
  for (let i = -1; i >= -this.size(); --i) {
    if (this.stack[this.size() + i] === target) {
      return Math.abs(i) - 1;
    }
  }

  return -1;
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def search(target)
  @stack.each_with_index do |item, idx|
    return size - idx - 1 if item == target
  end

  -1
end
</code>
</pre>

- O(n): Linear time
  - Correct! In the worst case, we'll have to traverse the whole stack, so the runtime is directly proportional to the number of items in the stack.
- O(1): Constant time
  - Not quite. What if the stack has many items and the target isn't in the stack? How will that affect the runtime?
- O(log n): Logarithmic time
  - Not quite. Keep in mind that for logarithmic time operations, the input gets divided as it's operated upon. Notice that the method iterates through the items in the stack.
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.

3. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
isFull() {
  return this.size() === this.limit;
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def isFull?
  size === @limit
end
</code>
</pre>

- O(1): Constant time
  - Yes! Getting the size of the stack takes constant time because it calls <code>length</code> upon the underlying array. Getting the <code>limit</code> and comparing it to the size also takes constant time.
- O(n): Linear time
  - Not quite. What is Big O for getting the length of an Array or accessing an attribute on an object? What is Big O for comparison operations, such as checking for equality?
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.