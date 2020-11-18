# Day 4: Big O Queue Quiz

In this quiz we'll ask you to calculate the time complexity for several of the Queue class methods. Remember that we used an Array as the underlying data structure for our class. If you don't know the time complexity for an Array method, you may need to Google.

1. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
dequeue() {
  return this.queue.shift();
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def dequeue
  @queue.shift
end
</code>
</pre>

- O(n): Linear time
  - Correct! We're guessing you Googled this one or had a little knowledge nugget already tucked away in your brain. Removing an element from the front of the queue takes linear time because the Array must be re-indexed after the 0th element is removed.
- O(1): Constant time
  - Not quite. We suggest Googling the time complexity of calling shift on an Array. As it turns out, it's not quite as simple as just removing the element. Other work also occurs.
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.

2. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
search(target) {
  return this.queue.indexOf(target);
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def search(target)
  @queue.index(target) || -1
end
</code>
</pre>

- O(n): Linear time
  - Correct! In the worst case, we'll have to traverse the whole queue, so the runtime is directly proportional to the number of items in the queue.
- O(1): Constant time
  - Not quite. What if the queue has many items and the target isn't in it? How will that affect the runtime?
- O(log n): Logarithmic time
  - Not quite. Keep in mind that for logarithmic time operations, the input gets divided as it's operated upon. Notice that the method iterates through the items in the queue one by one.
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.

3. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
size() {
  return this.queue.length;
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def size
  @queue.length
end
</code>
</pre>

- O(1): Constant time
  - Yes! Getting the size of the queue takes constant time because it calls <code>length</code> upon the underlying array. 
- O(n): Linear time
  - Not quite. What is Big O for getting the length of an Array or accessing an attribute on an object? 
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.