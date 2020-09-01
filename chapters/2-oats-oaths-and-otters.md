# 2\. Oats, Oaths, and Otters

<img width="100%" src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F4.bp.blogspot.com%2F-0dhHe1ee4w8%2FUQYQSSINUnI%2FAAAAAAAACdg%2FqNiP5VMo_2c%2Fs1600%2Fotters_b.jpg&f=1&nofb=1" />

<section class="qa" id="1">
  <section class="q">
  <p>
  Remember <code>is_atom(A)</code>?
  </p>
  </section>
  <section class="a">
  <p>
    Yes.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that <code>is_atom(A)</code> is a function?
  </p>
  </section>
  <section class="a">
  <p>
  Almost true,</p><p><code>is_atom/1</code> is a function, but <code>is_atom(A)</code>
  is a <i>function call</i>.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    What is that number after the function name?
  </p>
  </section>
  <section class="a">
  <p> The function's <i>arity</i>, </p>
  <p>
    it is the number of arguments the function has. It can be zero or bigger,
    as functions can have zero or more arguments.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is <code>is_atom</code> a function then?
  </p>
  </section>
  <section class="a">
  <p>
    No,</p><p>it is just an atom.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Can any atom become a function?
  </p>
  <code>
    books(A)
  </code>
  </section>
  <section class="a">
  <p>Yes,</p>
  <p>except the atom itself does not become a function, it just <i>names</i> one.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Can any term name a function?
  </p>
  <code>
  [book_1](A)
  </code>
  </section>
  <section class="a">
  <p>No,</p>
  <p>only terms that are actually atoms.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is a valid function call?
  </p>
  <pre><code>
  A = is_atom
  A(a)
  </code></pre>
  </section>
  <section class="a">
  <p> Yes,</p>
  <p>because if we replace the name <code>A</code> with its value, we have an atom in its place.
  </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is this the definition of <code>is_empty/1</code> ?
  </p>
  <pre><code>
    is_empty([]) -> true;
    is_empty(__) -> false.
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p>
  <p>we define named functions with the following pattern: </p>
  <pre><code>
    name(Arguments) -> Term.
  </code></pre>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Why is <code>is_empty/1</code> defined twice then?
  </p>
  </section>
  <section class="a">
  <p>It only looks like that,</p>
  <p><code>is_empty/1</code> is a single function, defined in two <i>clauses</i>.</p>
  <p>Each clause looks like a new function definition, except that they are separated with a semicolon instead. Like this: </p>
  <pre><code>
    name(Arguments) -> Term0;
    name(Arguments) -> Term1;
    name(Arguments) -> Term2.
  </code></pre>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
    How will I know which one will be used?
  </p>
  </section>
  <section class="a">
  <p> The first one that pattern matches, </p>
  <p> starting from the top one. </p>
  </section>
</section>

<section class="law">
  <h2> The Law of Function Definition </h2>
  <p> A function can be defined in many function clauses, following this pattern: </p>
  <pre><code>
    name(Arguments) -> Term;
    name(Arguments) -> Term;
    name(Arguments) -> Term.
  </code></pre>
  <p>
    Where <code>name</code> is an atom, <code>Arguments</code> is a binding
    pattern match, and <code>Term</code> is a term that may include names bound in <code>Arguments</code>.
  </p>
</section>

<section class="qa">
  <section class="q">
  <p>
  So <code>is_empty([1])</code> is <code>false</code> because it does not match
  the first clause, but matches the second clause?
  </p>
  <pre><code>
    is_empty([]) -> true;
    is_empty(__) -> false.
  </code></pre>
  </section>
  <section class="a">
  <p>Correct,</p>
  <p> we say a function <i>returns</i> a term when it matches the corresponding clause.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
   How is the pattern matching in function clauses different from the one in name binding?
  </p>
  </section>
  <section class="a">
  <p>It is the same,</p>
  <p>if a function clause pattern matches, it binds names.</p>
  <br />
  <p>This means that all the names bound in the pattern match can be used in the clause body</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Is this the definition of <code>tail/1</code> ?
  </p>
  <pre><code>
    tail([_|Tail]) -> Tail.
  </code></pre>
  </section>
  <section class="a">
    <p>Yes,</p>
    <p> This function returns the tail of a list. </p>
    <br />
    <p> Note how this function has only one clause. We can not call it with anything other than a non-empty list. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Would this be an extended definition of <code>tail/1</code> ?
  </p>
  <pre><code>
    tail([_|Tail]) -> Tail;
    tail(________) -> [].
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p><p>it will return an empty list (<code>[]</code>) for all the inputs that are not lists with elements.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is it true that this is <code>[sun, moon]</code>?
  </p>
  <pre><code>
    tail([earth, sun, moon])
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  How can I know what will this return?</p>
  <code>tail([earth, sun, moon])</code>
  </section>
  <section class="a">
  <p>You can <i>reduce</i> the function manually,</p>
  <p> it just takes a few steps.</p>
  <br />
  <p>First we look at what you wrote: </p>
  <code> tail([earth, sun, moon]) </code>
  <p>Then we look for the pattern in the first clause </p>
  <code> tail([_ | Tail]) </code>
  <p> and we try to bind the pattern to your argument </p>
  <code>[_ | Tail] = [earth | [sun, moon]]</code>
  <p> Eureka! it is a match, so now <code>Tail</code> is bound to <code>[sun, moon]</code>.</p>
  <br />
  <p>Finally, we replace the function call with the right side of the clause: </p>
  <code> Tail </code>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is this the definition of <code>head/1</code> ?
  </p>
  <pre><code>
    head([Head|_]) -> Head.
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p>
  <p>this function returns the first element of a list.</p>
  <br />
  <p> Note again how this function has only one clause, like the first definition of <code>tail/1</code>.</p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
  Is this the definition of <code>pair/1</code> ?
  </p>
  <pre><code>
    pair(A) -> {A, A}.
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p>
  <p>this function will make a pair out of a single term.</p>
  <br />
  <p> Note again how this function has only one clause, but this clause matches <i> any term </i>. </p>
  </section>
</section>

<section class="law">
  <h2> The Law of Function Reduction </h2>
  <p> A function can be reduced by checking if the inputs match any of the pattern matches in the function's clauses, one by one, from top to bottom.</p>
  <br />
  <p> If there are any matches, the input will be matched against the clauses' pattern, and the function call will return the term on the right. </p>
  <br />
  <p> Example: </p>
  <pre><code>
    double([A]) -> [A, A];
    double({A}) -> {A, A};
    double(___) -> [].
    <br />
    double([cake]) = [cake, cake].
    double({cookie}) = {cookie, cookie}.
    double(chips) = [].
  </pre></code>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is this the definition of <code>first/1</code> ?
  </p>
  <pre><code>
    first({First, _}) -> First.
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p>
  <p>this function will take the first element from a pair.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
  Is this the definition of <code>second/1</code> ?
  </p>
  <pre><code>
    second({_, Second}) -> Second.
  </code></pre>
  </section>
  <section class="a">
  <p>Yes,</p>
  <p>this function will take the second element from a pair.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    What can be I put on the right side of a clause, where your example said <code>Term</code>?
  </p>
  <pre><code>
    name(Arguments) -> Term.
  </code></pre>
  </section>
  <section class="a">
  <p>Any term,</p>
  <p>including atoms, lists, tuples, or other function calls.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    Wait, do all function calls return terms?
  </p>
  </section>
  <section class="a">
  <p> Yes,</p>
  <p>if a function call matches one of the function clauses, it will return a term. </p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
    Is it true that this returns <code>cookie</code>?
  </p>
  <pre><code>
    List = [cake, cookie, chips]
    Tail = tail(List)
    head(Tail)
  </code></pre>
  </section>
  <section class="a">
  <p> Yes,</p>
  <p>it can also be written as <code>head(tail(List))</code>.</p>
  </section>
</section>

<section class="interlude">
  <p> If you believe all this, we can take a pause. </p>
  <div>
    <h2> This space would be for doodling </h2>
    <p> (but browser support is not there yet) <p>
  </div>
</section>
