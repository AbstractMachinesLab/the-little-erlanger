### The Little Erlanger

---

<br />

# 1\. Stuff

<img width="100%" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.pinimg.com%2Foriginals%2Fbb%2F93%2Fae%2Fbb93aed890104c1c7ad30ff29aa778a6.jpg&f=1&nofb=1" />

<section class="qa" id="1">
  <section class="q">
  <p>
    Is it true that this is an atom?
  </p>
  <code>
    atom
  </code>
  </section>
  <section class="a">
  <p>
    Yes,</p><p> because <code>atom</code> is a string of characters beginning
    with the letter <code>a</code>.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is an atom?
  </p>
  <code>
    book
  </code>
  </section>
  <section class="a">
  <p>
    Yes,</p><p> because <code>book</code> is a string of characters beginning
    with a letter.
  </p>
  </section>
</section>


<section class="qa">
  <section class="q">
  <p>
  Is it true that this is an atom?
  </p>
  <code>
    1234
  </code>
  </section>
  <section class="a">
  <p>
  No,</p><p>because <code>1234</code> is not a string of
  characters beginning with a letter. 
  </p>
  </section>
</section>


<section class="qa">
  <section class="q">
  <p>
  Is it true that this is an atom?
  </p>
  <code>
    u
  </code>
  </section>
  <section class="a">
  <p>
  Yes,</p><p>because <code>u</code> is a string of one character, which is a
  letter.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is an atom?
  </p>
  <code>
    cray_1
  </code>
  </section>
  <section class="a">
  <p>
    Yes,</p><p>because <code>cray_1</code> is a string of characters beginning
    with a letter.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is a list?
  </p>
  <code>
    [book]
  </code>
  </section>
  <section class="a">
  <p>
    Yes,</p><p>because <code>[book]</code> is an atom enclosed by brackets.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a list?
  </p>
  <code>
  [atom, book, cray_1]
  </code>
  </section>
  <section class="a">
  <p>
  Yes,</p><p>because it is many atoms enclosed by brackets, separated with
  commas.
  </p>
  </section>
</section>


<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a list?
  </p>
  <code>
  [atom, book] cray_1
  </code>
  </section>
  <section class="a">
  <p>
  No,</p><p>because these are actually two Terms not enclosed by brackets. The
  first one is a list with two atoms, and the second one is just an atom.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a list?
  </p>
  <code>
  [[atom, book], cray_1]
  </code>
  </section>
  <section class="a">
  <p>
  Yes,</p><p>because these two Terms are now enclosed by brackets and separated
  by comas.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a Term?
  </p>
  <code>
  xyz
  </code>
  </section>
  <section class="a">
  <p>
  Yes,</p><p>because all atoms are Terms.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a Term?
  </p>
  <code>
  [x, y, z]
  </code>
  </section>
  <section class="a">
  <p>
  Yes,</p><p>because it is a list of atoms.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a Term?
  </p>
  <code>
  [[x, y], z]
  </code>
  </section>
  <section class="a">
  <p>Yes,</p><p>because all lists are Terms. Even lists of lists.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a list?
  </p>
  <code>
  [how, are, you, doing, so, far]
  </code>
  </section>
  <section class="a">
  <p>Yes,</p><p>because it is a collection of Terms enclosed by brackets, and 
  separated by comas.
  </p>
  </section>
</section>


<section class="qa">
  <section class="q">
  <p>
  How many terms are in the list
  </p>
  <code>
  [how, are, you, doing, so, far]
  </code>
  <p>
  and what are they?
  </p>
  </section>
  <section class="a">
  <p> Six, </p>
  <p>
  <code>how</code>,
  <code>are</code>,
  <code>you</code>,
  <code>doing</code>,
  <code>so</code>,
  and <code>far</code>.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a list?
  </p>
  <code>
  []
  </code>
  </section>
  <section class="a">
  <p>Yes,</p><p>because it contains zero Terms wrapped in brackets and
  separated by comas. We call this Term the <i>empty list</i>.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is the <i>cons</i> of the atom <code>a</code> and the list <code>[b, c]</code>?
  </p>
  </section>
  <section class="a">
  <p><code>[a, b, c]</code>, </p><p>because <i>cons</i> adds a term to the front of a list.</p>
  <br />
  <p>The action <i>to cons</i> is to grow a list by adding an element at the
  front. This is written as <code>[ a | [b, c] ]</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>[ a | [b, c] ]</code>?
  </p>
  </section>
  <section class="a">
    <p><code>[a, b, c]</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is an atom?
  </p>
  <code>
  []
  </code>
  </section>
  <section class="a">
  <p>No,</p><p>because <code>[]</code> is just a list.</p>
  </section>
</section>


<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a list?
  </p>
  <code>
  [[], [], []]
  </code>
  </section>
  <section class="a">
  <p>Yes,</p><p>because the empty list is a term, and we make lists by wrapping
  terms in brackets, separated by comas. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is a list?
  </p>
  <code>
    {atom}
  </code>
  </section>
  <section class="a">
  <p>
    No,</p><p>because <code>{atom}</code> is an atom enclosed by braces.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is a tuple?
  </p>
  <code>
    {atom}
  </code>
  </section>
  <section class="a">
  <p>
    Yes,</p><p>because <code>{atom}</code> is an atom enclosed by braces.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is a tuple?
  </p>
  <code>
    {ok, error}
  </code>
  </section>
  <section class="a">
  <p>
    Yes,</p><p>because <code>{ok, error}</code> is a pair of atoms wrapped in braces and separated by commas.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is a tuple?
  </p>
  <code>
    {[atom]}
  </code>
  </section>
  <section class="a">
  <p>
    Yes,</p><p>because <code>{[atom]}</code> is a list enclosed by braces.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is a tuple?
  </p>
  <code>
    {}
  </code>
  </section>
  <section class="a">
  <p>
    Yes,</p><p>because it contains zero Terms wrapped in braces and separated by
    commas. We call this Term the <i>empty tuple</i> or <i>unit</i>.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is it true that this is a tuple?
  </p>
  <code>
    {first, second, {third, {fourth}}}
  </code>
  </section>
  <section class="a">
  <p>Yes,</p>
  <p>because we make Tuples by wrapping Terms in braces and separating them with comas.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is the <i>cons</i> of the atom <code>a</code> and the tuple <code>{b, c}</code>?
  </p>
  </section>
  <section class="a">
  <p>Nothing, </p><p>because tuples can not be grown like lists do and have a fixed size when they are first created.</p>
  </section>
</section>


<section class="qa">
  <section class="q">
  <p>
  Is <code>is_atom(a)</code> true or false?
  </p>
  </section>
  <section class="a">
  <p>True,</p><p>because <code>a</code> is an atom.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is <code>is_atom([a])</code> true or false?
  </p>
  </section>
  <section class="a">
  <p>False,</p><p>because <code>[a]</code> is not an atom.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is <code>is_atom({a})</code> true or false?
  </p>
  </section>
  <section class="a">
  <p>False,</p><p>because <code>{a}</code> is not an atom.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  When is <code>is_atom(A)</code> true?
  </p>
  </section>
  <section class="a">
  <p>When <code>A</code> is bound to an atom.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is <code>A</code> not an atom?
  </p>
  </section>
  <section class="a">
  <p>Correct,</p><p>because <code>A</code> begins with an upper case
  <code>A</code>, it is not an atom, but it is a <i>name</i>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is <code>Book</code> a name?
  </p>
  </section>
  <section class="a">
  <p>Yes,</p><p>because <code>Book</code> begins with an upper case letter.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is <code>Cray1</code> a name?
  </p>
  </section>
  <section class="a">
  <p>Yes,</p><p>because <code>Cray1</code> begins with an upper case letter.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is <code>[A]</code> a name?
  </p>
  </section>
  <section class="a">
  <p>No,</p><p>but it is a list with a name in it.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  When are <code>A</code> and <code>a</code> the same?
  </p>
  </section>
  <section class="a">
  <p>When <code>A</code> is <i>bound</i> to <code>a</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is <code>A</code> bound to <code>a</code> here?
  </p>
  <code>
    A = a
  </code>
  </section>
  <section class="a">
  <p>Yes,</p><p>because names are bound with <code>=</code> to the term on the
  right the first time they appear.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Are these two the same now?
  </p>
  <pre><code>
    A = a
    a = A
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p><p>because <code>A</code> is a name that was bound to <code>a</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is <code>A</code> bound to <code>book</code> here?
  </p>
  <code>
    A = book 
  </code>
  </section>
  <section class="a">
  <p>Yes,</p><p>because names are bound with <code>=</code> to the term on the right, and <code>book</code> is an atom, and all atoms are terms.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What can I bind names to?
  </p>
  </section>
  <section class="a">
  <p>Any term.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Are all of these terms?
  </p>
  <pre><code>
    guacamole
    [coriander, avocado, salt, lime]
    {ok, this_is_delicious}
  </code></pre>
  </section>
  <section class="a">
    <p>Yes,</p><p>all lists, all atoms, and all tuples are <i>terms</i>.</p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
  Can I bind a name to multiple terms like below?
  </p>
  <pre><code>
    A = a
    A = b
  </code></pre>
  </section>
  <section class="a">
  <p>No,</p><p>once a name is bound, it is bound forever.</p>
  </section>
</section>

<section class="law">
  <h2> The Law of Bind </h2>
  <p> A Name can be bound to a Term with <code>=</code> one and only once. </p>
</section>


<section class="qa">
  <section class="q">
  <p>
  Is <code>A</code> then just another name for <code>a</code>?
  </p>
  </section>
  <section class="a">
  <p>Yes,</p><p>we say <code>A</code> has <i>value</i> <code>a</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is this the same as saying <code>a = b</code>?
  </p>
  <pre><code>
    A = a
    A = b
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p><p>because <code>=</code> checks if the term on the left and the
  term of the right have the same values.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>B</code> bound to here?
  </p>
  <pre><code>
    A = a
    B = A
  </code></pre>
  </section>
  <section class="a">
  <p><code>a</code>,</p><p>because binding a name to another name is the same
  as binding a name to the second name's value.<p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Can I bind <code>Stuff</code> to this list?
  </p>
  <code>
    Stuff = [book, toy, computer]
  </code>
  </section>
  <section class="a">
  <p>Yes, </p><p>because lists are Terms.<p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  True or false: I can build lists with names.
  </p>
  </section>
  <section class="a">
  <p>True, </p><p>because lists are composed of terms and names are terms.<p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Stuff</code> bound to here?
  </p>
  <code>
    Stuff = [Book, Toy]
  </code>
  <p>
   when
   </p>
  <pre><code>
    Book = the_little_erlanger
    Toy = r2d2
  </code></pre>
  </section>
  <section class="a">
  <p><code>[the_little_erlanger, r2d2]</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  So this is the same as above? 
  </p>
  <pre><code>
    [the_little_erlanger, r2d2] = [Book, Toy]
  </code></pre>
  <p>
   when
   </p>
  <pre><code>
    Book = the_little_erlanger
    Toy = r2d2
  </code></pre>
  </section>
  <section class="a">
  <p>Yes, </p><p> because binding makes sure both sides are the same. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Head</code> bound to here?
  </p>
  <pre><code>
    Book = the_little_erlanger
    [Head] = [Book]
  </code></pre>
  </section>
  <section class="a">
  <p><code>the_little_erlanger</code>, </p><p> because binding makes sure both sides are the same. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What are <code>Head</code> and <code>Second</code> bound to here?
  </p>
  <pre><code>
    Books = [ the_little_erlanger
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; , the_little_schemer ]
    [First, Second] = Books
  </code></pre>
  </section>
  <section class="a">
  <p><code>the_little_erlanger</code> and <code>the_little_schemer</code>,</p><p> because binding makes sure both sides are the same. </p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
  So I can use <code>=</code> to give names to terms inside of terms?
  </p>
  </section>
  <section class="a">
  <p>Correct,</p><p> because binding makes sure both sides are the same, you
  can use new names on the left side to bind them to their corresponding right
  hand-side parts. </p><br/><p>We call this <i>pattern matching</i>.</p>
  </section>
</section>

<section class="law">
  <h2> The Law of Pattern Matching </h2>
  <p>
    Names can be bound to Terms inside other Terms with <code>=</code> if
    the left side has the same shape as the right side.
  </p>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Head</code> bound to here?
  </p>
  <code>
    [Head] = [1]
  </code>
  </section>
  <section class="a">
  <p><code>1</code>. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Head</code> bound to here?
  </p>
  <code>
    [Head] = [[1]]
  </code>
  </section>
  <section class="a">
  <p><code>[1]</code>. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Head</code> bound to here?
  </p>
  <code>
    [Head] = [[1, hotdog]]
  </code>
  </section>
  <section class="a">
  <p><code>[1, hotdog]</code>. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Head</code> bound to here?
  </p>
  <code>
    [Head] = [[[1, hotdog], corn]]
  </code>
  </section>
  <section class="a">
  <p><code>[[1, hotdog], corn]</code>. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Head</code> bound to here?
  </p>
  <code>
    [[Head, corn]] = [[[1, hotdog], corn]]
  </code>
  </section>
  <section class="a">
  <p><code>[1, hotdog]</code>. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>One</code> bound to here?
  </p>
  <code>
    {One} = {1}
  </code>
  </section>
  <section class="a">
  <p><code>1</code>. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Tag</code> bound to here?
  </p>
  <code>
    {Tag, Numbers} = {ok, [1, 2]}
  </code>
  </section>
  <section class="a">
  <p><code>ok</code>. </p>
  <p><code>Numbers</code> is bound to <code>[1, 2]</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Order</code> bound to here?
  </p>
  <code>
    [{Order, Name}] = [{last, mustard}]
  </code>
  </section>
  <section class="a">
  <p><code>last</code>. </p>
  <p><code>Name</code> is bound to <code>mustard</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Could I bind <code>Order</code> to <code>last</code> if <code>Name</code> does not match <code>mustard</code>?
  </p>
  <code>
    [{Order, pepper}] = [{last, mustard}]
  </code>
  </section>
  <section class="a">
  <p>No, </p>
  <p> because pattern matching makes sure both sides are the same, this will not work since <code>pepper</code> and <code>mustard</code> are not the same term.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Head</code> bound to here?
  </p>
  <code>
    [Head] = []
  </code>
  </section>
  <section class="a">
  <p>Nothing, </p><p>because <code>=</code> can't match the left and the right sides.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Head</code> bound to here?
  </p>
  <code>
    [Head] = [1, 2, 3]
  </code>
  </section>
  <section class="a">
  <p>Nothing, </p><p>because <code>=</code> can't match the left and the right sides.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  True or false: I have to bind everything on the left with everything on the right.
  </p>
  </section>
  <section class="a">
  <p>True, </p><p>because <code>=</code> must match the left and the right sides.</p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
  Do I need to always come up with new names to bind terms to? 
  </p>
  </section>
  <section class="a">
  <p>Not quite, </p><p>the special name <code>_</code> (underscore) can be used to ignore terms.</p>
  </section>
</section>

<section class="law">
  <h2> The Law of _ </h2>
  <p>
  The name <code>_</code> (underscore) can be used to ignore a term in a binding. It can be used multiple times (<code>_____</code>), and in multiple places.
  </p>
</section>

<section class="qa">
  <section class="q">
  <p>
  Okay! What is <code>Head</code> bound to here?
  </p>
  <code>
    [Head, _, _] = [1, 2, 3]
  </code>
  </section>
  <section class="a">
  <p>1, </p><p>because <code>_</code> will ignore the other two list items.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Can I use <code>_</code> on the right hand side like this?
  </p>
  <code>
    Head = _
  </code>
  </section>
  <section class="a">
  <p>No, </p><p>because the special name <code>_</code> is only used to ignore bindings in a pattern match.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  What is <code>Tail</code> bound to here?
  </p>
  <code>
    [Head | Tail] = [1, 2, 3]
  </code>
  </section>
  <section class="a">
  <p><code>[2, 3]</code>, </p><p>because <i>cons</i> can be used to split a list into the first element, and the rest.</p>
  <br />
  <p>These are the head and tail of a list.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  True or false:
  </p>
  <pre><code>
    [Head | Tail] = [[1, 2] | 3]
    Head = 1
    Tail = [2, 3]
  </code></pre>
  </section>
  <section class="a">
  <p>True, </p><p>because <code>[[1, 2] | 3]</code> is the same as <code>[1, 2, 3]</code>.</p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
  True or false:
  </p>
  <pre><code>
    [Head | Tail] = [1]
    Head = 1
    Tail = []
  </code></pre>
  </section>
  <section class="a">
  <p>True, </p>
  <p>because all lists with elements, have an empty tail.</p>
  <br />
  <p>
    This means that <code>[1 | []] = []</code>.
  </p>
  </section>
</section>

<section class="interlude">
  <h2> Now go get some knäckebröd with mustard. </h2>
  <div>
    <p> This space reserved for </p>
    <h3>mustardy bread crumbles. </h3>
  </div>
</section>

---
<br />
<p style="text-align: center;">
  <a href="/"> Back to the Index </a>
  &mdash;
  <a href="/chapters/2-oats-oaths-and-otters.html"> Go to Chapter 2 </a>
</p>
