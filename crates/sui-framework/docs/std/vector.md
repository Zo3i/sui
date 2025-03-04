---
title: Module `std::vector`
---

A variable-sized container that can hold any type. Indexing is 0-based, and
vectors are growable. This module has many native functions.


-  [Constants](#@Constants_0)
-  [Function `empty`](#std_vector_empty)
-  [Function `length`](#std_vector_length)
-  [Function `borrow`](#std_vector_borrow)
-  [Function `push_back`](#std_vector_push_back)
-  [Function `borrow_mut`](#std_vector_borrow_mut)
-  [Function `pop_back`](#std_vector_pop_back)
-  [Function `destroy_empty`](#std_vector_destroy_empty)
-  [Function `swap`](#std_vector_swap)
-  [Function `singleton`](#std_vector_singleton)
-  [Function `reverse`](#std_vector_reverse)
-  [Function `append`](#std_vector_append)
-  [Function `is_empty`](#std_vector_is_empty)
-  [Function `contains`](#std_vector_contains)
-  [Function `index_of`](#std_vector_index_of)
-  [Function `remove`](#std_vector_remove)
-  [Function `insert`](#std_vector_insert)
-  [Function `swap_remove`](#std_vector_swap_remove)
-  [Function `flatten`](#std_vector_flatten)


<pre><code></code></pre>



<a name="@Constants_0"></a>

## Constants


<a name="std_vector_EINDEX_OUT_OF_BOUNDS"></a>

The index into the vector is out of bounds


<pre><code><b>const</b> <a href="../std/vector.md#std_vector_EINDEX_OUT_OF_BOUNDS">EINDEX_OUT_OF_BOUNDS</a>: <a href="../std/u64.md#std_u64">u64</a> = 131072;
</code></pre>



<a name="std_vector_empty"></a>

## Function `empty`

Create an empty vector.


<pre><code><b>public</b> <b>fun</b> emptyElement(): <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../std/vector.md#std_vector_empty">empty</a>&lt;Element&gt;(): <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;;
</code></pre>



</details>

<a name="std_vector_length"></a>

## Function `length`

Return the length of the vector.


<pre><code><b>public</b> <b>fun</b> lengthElement(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;): <a href="../std/u64.md#std_u64">u64</a>
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../std/vector.md#std_vector_length">length</a>&lt;Element&gt;(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;): <a href="../std/u64.md#std_u64">u64</a>;
</code></pre>



</details>

<a name="std_vector_borrow"></a>

## Function `borrow`

Acquire an immutable reference to the <code>i</code>th element of the vector <code>v</code>.
Aborts if <code>i</code> is out of bounds.


<pre><code><b>public</b> <b>fun</b> borrowElement(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>): &Element
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../std/vector.md#std_vector_borrow">borrow</a>&lt;Element&gt;(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>): &Element;
</code></pre>



</details>

<a name="std_vector_push_back"></a>

## Function `push_back`

Add element <code>e</code> to the end of the vector <code>v</code>.


<pre><code><b>public</b> <b>fun</b> push_backElement(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, e: Element)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../std/vector.md#std_vector_push_back">push_back</a>&lt;Element&gt;(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, e: Element);
</code></pre>



</details>

<a name="std_vector_borrow_mut"></a>

## Function `borrow_mut`

Return a mutable reference to the <code>i</code>th element in the vector <code>v</code>.
Aborts if <code>i</code> is out of bounds.


<pre><code><b>public</b> <b>fun</b> borrow_mutElement(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>): &<b>mut</b> Element
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../std/vector.md#std_vector_borrow_mut">borrow_mut</a>&lt;Element&gt;(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>): &<b>mut</b> Element;
</code></pre>



</details>

<a name="std_vector_pop_back"></a>

## Function `pop_back`

Pop an element from the end of vector <code>v</code>.
Aborts if <code>v</code> is empty.


<pre><code><b>public</b> <b>fun</b> pop_backElement(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;): Element
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../std/vector.md#std_vector_pop_back">pop_back</a>&lt;Element&gt;(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;): Element;
</code></pre>



</details>

<a name="std_vector_destroy_empty"></a>

## Function `destroy_empty`

Destroy the vector <code>v</code>.
Aborts if <code>v</code> is not empty.


<pre><code><b>public</b> <b>fun</b> destroy_emptyElement(v: <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../std/vector.md#std_vector_destroy_empty">destroy_empty</a>&lt;Element&gt;(v: <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;);
</code></pre>



</details>

<a name="std_vector_swap"></a>

## Function `swap`

Swaps the elements at the <code>i</code>th and <code>j</code>th indices in the vector <code>v</code>.
Aborts if <code>i</code> or <code>j</code> is out of bounds.


<pre><code><b>public</b> <b>fun</b> swapElement(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>, j: <a href="../std/u64.md#std_u64">u64</a>)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../std/vector.md#std_vector_swap">swap</a>&lt;Element&gt;(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>, j: <a href="../std/u64.md#std_u64">u64</a>);
</code></pre>



</details>

<a name="std_vector_singleton"></a>

## Function `singleton`

Return an vector of size one containing element <code>e</code>.


<pre><code><b>public</b> <b>fun</b> singletonElement(e: Element): <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_singleton">singleton</a>&lt;Element&gt;(e: Element): <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt; {
    <b>let</b> <b>mut</b> v = <a href="../std/vector.md#std_vector_empty">empty</a>();
    v.<a href="../std/vector.md#std_vector_push_back">push_back</a>(e);
    v
}
</code></pre>



</details>

<a name="std_vector_reverse"></a>

## Function `reverse`

Reverses the order of the elements in the vector <code>v</code> in place.


<pre><code><b>public</b> <b>fun</b> reverseElement(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_reverse">reverse</a>&lt;Element&gt;(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;) {
    <b>let</b> len = v.<a href="../std/vector.md#std_vector_length">length</a>();
    <b>if</b> (len == 0) <b>return</b> ();
    <b>let</b> <b>mut</b> front_index = 0;
    <b>let</b> <b>mut</b> back_index = len - 1;
    <b>while</b> (front_index &lt; back_index) {
        v.<a href="../std/vector.md#std_vector_swap">swap</a>(front_index, back_index);
        front_index = front_index + 1;
        back_index = back_index - 1;
    }
}
</code></pre>



</details>

<a name="std_vector_append"></a>

## Function `append`

Pushes all of the elements of the <code>other</code> vector into the <code>lhs</code> vector.


<pre><code><b>public</b> <b>fun</b> appendElement(lhs: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, other: <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_append">append</a>&lt;Element&gt;(lhs: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, other: <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;) {
    other.<a href="../std/vector.md#std_vector_do">do</a>!(|e| lhs.<a href="../std/vector.md#std_vector_push_back">push_back</a>(e));
}
</code></pre>



</details>

<a name="std_vector_is_empty"></a>

## Function `is_empty`

Return <code><b>true</b></code> if the vector <code>v</code> has no elements and <code><b>false</b></code> otherwise.


<pre><code><b>public</b> <b>fun</b> is_emptyElement(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;): bool
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_is_empty">is_empty</a>&lt;Element&gt;(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;): bool {
    v.<a href="../std/vector.md#std_vector_length">length</a>() == 0
}
</code></pre>



</details>

<a name="std_vector_contains"></a>

## Function `contains`

Return true if <code>e</code> is in the vector <code>v</code>.
Otherwise, returns false.


<pre><code><b>public</b> <b>fun</b> containsElement(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, e: &Element): bool
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_contains">contains</a>&lt;Element&gt;(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, e: &Element): bool {
    <b>let</b> <b>mut</b> i = 0;
    <b>let</b> len = v.<a href="../std/vector.md#std_vector_length">length</a>();
    <b>while</b> (i &lt; len) {
        <b>if</b> (&v[i] == e) <b>return</b> <b>true</b>;
        i = i + 1;
    };
    <b>false</b>
}
</code></pre>



</details>

<a name="std_vector_index_of"></a>

## Function `index_of`

Return <code>(<b>true</b>, i)</code> if <code>e</code> is in the vector <code>v</code> at index <code>i</code>.
Otherwise, returns <code>(<b>false</b>, 0)</code>.


<pre><code><b>public</b> <b>fun</b> index_ofElement(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, e: &Element): (bool, <a href="../std/u64.md#std_u64">u64</a>)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_index_of">index_of</a>&lt;Element&gt;(v: &<a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, e: &Element): (bool, <a href="../std/u64.md#std_u64">u64</a>) {
    <b>let</b> <b>mut</b> i = 0;
    <b>let</b> len = v.<a href="../std/vector.md#std_vector_length">length</a>();
    <b>while</b> (i &lt; len) {
        <b>if</b> (&v[i] == e) <b>return</b> (<b>true</b>, i);
        i = i + 1;
    };
    (<b>false</b>, 0)
}
</code></pre>



</details>

<a name="std_vector_remove"></a>

## Function `remove`

Remove the <code>i</code>th element of the vector <code>v</code>, shifting all subsequent elements.
This is O(n) and preserves ordering of elements in the vector.
Aborts if <code>i</code> is out of bounds.


<pre><code><b>public</b> <b>fun</b> removeElement(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>): Element
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_remove">remove</a>&lt;Element&gt;(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, <b>mut</b> i: <a href="../std/u64.md#std_u64">u64</a>): Element {
    <b>let</b> <b>mut</b> len = v.<a href="../std/vector.md#std_vector_length">length</a>();
    // i out of bounds; <b>abort</b>
    <b>if</b> (i &gt;= len) <b>abort</b> <a href="../std/vector.md#std_vector_EINDEX_OUT_OF_BOUNDS">EINDEX_OUT_OF_BOUNDS</a>;
    len = len - 1;
    <b>while</b> (i &lt; len) v.<a href="../std/vector.md#std_vector_swap">swap</a>(i, {
        i = i + 1;
        i
    });
    v.<a href="../std/vector.md#std_vector_pop_back">pop_back</a>()
}
</code></pre>



</details>

<a name="std_vector_insert"></a>

## Function `insert`

Insert <code>e</code> at position <code>i</code> in the vector <code>v</code>.
If <code>i</code> is in bounds, this shifts the old <code>v[i]</code> and all subsequent elements to the right.
If <code>i == v.<a href="../std/vector.md#std_vector_length">length</a>()</code>, this adds <code>e</code> to the end of the vector.
This is O(n) and preserves ordering of elements in the vector.
Aborts if <code>i &gt; v.<a href="../std/vector.md#std_vector_length">length</a>()</code>


<pre><code><b>public</b> <b>fun</b> insertElement(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, e: Element, i: <a href="../std/u64.md#std_u64">u64</a>)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_insert">insert</a>&lt;Element&gt;(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, e: Element, <b>mut</b> i: <a href="../std/u64.md#std_u64">u64</a>) {
    <b>let</b> len = v.<a href="../std/vector.md#std_vector_length">length</a>();
    // i too big <b>abort</b>
    <b>if</b> (i &gt; len) <b>abort</b> <a href="../std/vector.md#std_vector_EINDEX_OUT_OF_BOUNDS">EINDEX_OUT_OF_BOUNDS</a>;
    v.<a href="../std/vector.md#std_vector_push_back">push_back</a>(e);
    <b>while</b> (i &lt; len) {
        v.<a href="../std/vector.md#std_vector_swap">swap</a>(i, len);
        i = i + 1
    }
}
</code></pre>



</details>

<a name="std_vector_swap_remove"></a>

## Function `swap_remove`

Swap the <code>i</code>th element of the vector <code>v</code> with the last element and then pop the vector.
This is O(1), but does not preserve ordering of elements in the vector.
Aborts if <code>i</code> is out of bounds.


<pre><code><b>public</b> <b>fun</b> swap_removeElement(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>): Element
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_swap_remove">swap_remove</a>&lt;Element&gt;(v: &<b>mut</b> <a href="../std/vector.md#std_vector">vector</a>&lt;Element&gt;, i: <a href="../std/u64.md#std_u64">u64</a>): Element {
    <b>assert</b>!(v.<a href="../std/vector.md#std_vector_length">length</a>() != 0, <a href="../std/vector.md#std_vector_EINDEX_OUT_OF_BOUNDS">EINDEX_OUT_OF_BOUNDS</a>);
    <b>let</b> last_idx = v.<a href="../std/vector.md#std_vector_length">length</a>() - 1;
    v.<a href="../std/vector.md#std_vector_swap">swap</a>(i, last_idx);
    v.<a href="../std/vector.md#std_vector_pop_back">pop_back</a>()
}
</code></pre>



</details>

<a name="std_vector_flatten"></a>

## Function `flatten`

Concatenate the vectors of <code>v</code> into a single vector, keeping the order of the elements.


<pre><code><b>public</b> <b>fun</b> flattenT(v: <a href="../std/vector.md#std_vector">vector</a>&lt;<a href="../std/vector.md#std_vector">vector</a>&lt;T&gt;&gt;): <a href="../std/vector.md#std_vector">vector</a>&lt;T&gt;
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../std/vector.md#std_vector_flatten">flatten</a>&lt;T&gt;(v: <a href="../std/vector.md#std_vector">vector</a>&lt;<a href="../std/vector.md#std_vector">vector</a>&lt;T&gt;&gt;): <a href="../std/vector.md#std_vector">vector</a>&lt;T&gt; {
    <b>let</b> <b>mut</b> r = <a href="../std/vector.md#std_vector">vector</a>[];
    v.<a href="../std/vector.md#std_vector_do">do</a>!(|u| r.<a href="../std/vector.md#std_vector_append">append</a>(u));
    r
}
</code></pre>



</details>
