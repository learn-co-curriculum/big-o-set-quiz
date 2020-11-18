# Day 5: Big O Set Quiz

In this quiz we'll ask you to calculate the time complexity for several of the MySet class methods. Remember that we used a Hash/Object as the underlying data structure for our class. If you don't know the time complexity for a method, you may need to Google.

1. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
constructor(iterable) {
  if (!(iterable === undefined || 
    Array.isArray(iterable) || 
    typeof iterable === 'string')) {
      throw new Error('MySet only accepts iterables or nothing on initialization!');
  }

  this.data = {};

  if (iterable) {
    for (const el of iterable) {
      this.data[el] = true;
    }
  }
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def initialize(iterable = nil)
  raise 'MySet only accepts iterables or nothing on initialization!' unless 
    iterable.nil? || iterable.kind_of?(Array) || iterable.kind_of?(String)

  @data = {}

  unless iterable.nil?
    items = iterable.kind_of?(String) ? iterable.split('') : iterable

    items.each { |el| @data[el] = true }
  end
end
</code>
</pre>

- O(n): Linear time
  - Correct! The worst case is if an Array or String is provided as an argument. In that case, we iterate over the input and add each item to <code>data</code>, which is a linear-time operation.
- O(1): Constant time
  - Not quite. This would be true if the Array or String were always the same length, but an Array or String of any length could be provided.
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.

2. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
add(item) {
  this.data[item] = true;
  return this;
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def add(item)
  @data[item] = true
  self
end
</code>
</pre>

- O(1): Constant time
  - Perfect! Accessing a value by key in a Hash/Object takes constant time, so does returning the instance.
- O(2): Constant time
  - Not quite. Remember that we have to simplify our notation, so constant time is always expressed as O(1), even if we perform many constant-time operations.
- O(n): Linear time
  - Not quite. You may wish to look up Big O for accessing values by key in a Hash.
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.

3. Mult choice

Calculate the time complexity for the following method:

<h3>JavaScript</h3>
<pre>
<code>
has(item) {
  return !!this.data[item];
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def has(item)
  !!@data[item]
end
</code>
</pre>

- O(1): Constant time
  - Yes! Accessing a value by key takes constant time. 
- O(n): Linear time
  - Not quite. What is Big O for accessing a value by key in a Hash or Object? 
- I don't know
  - With time and practice, it'll start to sink in. Keep studying and you'll get there.