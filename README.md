Download Link: https://assignmentchef.com/product/solved-cs112-problem-set-13
<br>
<strong>Problem Set 13</strong>

<strong>Sorting</strong>

<ol>

 <li>Trace the mergesort algorithm on the following list:</li>

</ol>

3, 26, 67, 25, 9, -6, 43, 82, 10, 54




Show the resulting recursion tree, with the to-be-sorted original and sub-lists at each node, and the number comparions for each merge. (Assume that if there is an odd number of entries in an array, the left part has one more entry than the right after the split.)

<ol start="2">

 <li>Mergesort works well on linked lists since it doesn’t need any extra space. Given the following linked list node class:</li>

</ol>

public class LLNode&lt;T extends Comparable&lt;T&gt;&gt;  {        public T info;        public LLNode&lt;T&gt; next;

…

}

complete the following method to “split” the linked list in half:

// splits the given list in half such that the return value is

// a reference to the first node of the second half. Also, the      // “next” field of the last node in the first half is set to null.     static &lt;T extends Comparable&lt;T&gt; LLNode&lt;T&gt; split(LLNode&lt;T&gt; list) {

// COMPLETE THIS METHOD

<table>

 <tbody>

  <tr>

   <td width="81"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

}

<ol start="3">

 <li>In Problem Set 3, #6, you saw how to merge two sorted linked lists of integers, into a single sorted list without duplicates. Here is the header of a modified version of that method, that merges lists of Comparable objects (not just ints), while preserving duplicates, if any. Complete this method using recursion. Your method should recycle the nodes in the original lists (no new nodes should be created).</li>

</ol>

// merge the lists l1 and l2 into a single linked list, whose

// first node is referenced by the return value – no additional

// linked list nodes are used

static &lt;T extends Comparable&lt;T&gt;&gt; LLNode&lt;T&gt; merge(LLNode&lt;T&gt; l1, LLNode&lt;T&gt; l2) {

// COMPLETE METHOD USING RECURSION, NO NEW NODES TO BE CREATED     }

Using this merge solution, and the solution to the split in the previous problem, complete the mergesort implementation:

// Sorts the input linked list using mergesort, and returns the front of

// the sorted linked list. DOES NOT CREATE ANY ADDITIONAL NODES.

public static &lt;T extends Comparable&lt;T&gt;

LLNode&lt;T&gt; mergesort(LLNode&lt;T&gt; list) {

// COMPLETE THIS METHOD

}

<ol start="4">

 <li>Trace the quicksort algorithm on the following array:</li>

</ol>




3, 26, 67, 25, 9, -6, 43, 82, 10, 54

Use the median of the first, middle, and last entries as the pivot to split a subarray. (If a subarray has fewer than 3 entries, use the first as the pivot.) Show the quicksort tree and the number of comparisons at each split.

<ol start="5">

 <li>A <em>stable</em> sorting algorithm is one which preserves the order of duplicate elements when sorted. For instance, suppose the following pairs of values are sorted on the <strong>first</strong> value in the pair:</li>

</ol>

(3,sun)  (2,mars)  (4,moon)  (3,venus)

then the output of a stable sorting algorithm would be:

(2,mars)  (3,sun)  (3,venus)  (4,moon)

Notice that (3,sun) comes before (3,venus), preserving the order of the input for elements that have the same sortable value of 3, hence <em>stable</em>.

However, if the output is this:

(2,mars)  (3,venus)  (3,sun)  (4,moon)

then the sorting algorithm is not stable since it does not preserve the input order of (3,sun) before (3,venus).

For each of insertion sort, mergesort, and quicksort, tell whether the algorithm is stable or not.

<ol start="6">

 <li>Given the following input array:</li>

</ol>




3, 26, 67, 25, 9, -6, 43, 82, 10, 54

<ol>

 <li>Trace the linear time build-heap algorithm on this array, to build a max-heap. How many comparisons did it take to build the heap?</li>

 <li>Starting with this max-heap, show how the array is then sorted by repeatedly moving the maximum entry to the end and applying sift-down to restore the (remaining) heap. How many comparisons did it take to sort the heap?</li>

</ol>