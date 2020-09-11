### The Little Erlanger

---

<br />

# 2\. Oats, Oaths, and Otters

<img width="100%" src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F4.bp.blogspot.com%2F-0dhHe1ee4w8%2FUQYQSSINUnI%2FAAAAAAAACdg%2FqNiP5VMo_2c%2Fs1600%2Fotters_b.jpg&f=1&nofb=1" />

<section class="qa">
  <section class="q">
  <p>
    True or false: <code>list_of_atoms(L)</code>
  </p>
  <p> where </p>
  <pre><code>
    L = [the, cake, is, a, lie]
  </code></pre>
  </section>
  <section class="a">
  <p> True,</p>
  <p>because every term in the list <code>L</code> is an atom.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    True or false: <code>list_of_atoms(L)</code>
  </p>
  <p> where </p>
  <pre><code>
    L = [{the, cake}, is, a, lie]
  </code></pre>
  </section>
  <section class="a">
  <p> False,</p>
  <p>because the head of the list (<code>{the, cake}</code>) is a tuple.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    True or false: <code>list_of_atoms(L)</code>
  </p>
  <p> where </p>
  <pre><code>
    L = [the, cake, is, a, [lie]]
  </code></pre>
  </section>
  <section class="a">
  <p> False,</p>
  <p>because one of the elements of the list (<code>[lie]</code>) is a list.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    True or false: <code>list_of_atoms(L)</code>
  </p>
  <p> where </p>
  <pre><code>
    L = []
  </code></pre>
  </section>
  <section class="a">
  <p>True,</p>
  <p>because this list has no elements that are not atoms.</p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
  How does <code>list_of_atoms(L)</code> work?
  </p>
  </section>
  <section class="a">
    <p>You were not expected to be able to figure this out yet, because we are missing a few ideas. </p>
    <br />
  <p>Let's look at them, shall we?</p>
  </section>
</section>

<section class="interlude">
  <div>
    <h2> Take a deep breath </h2>
  </div>
</section>

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
  <p>we define named functions with the following recipe: </p>
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
  <br />
  <p>Each clause looks like a new function definition, except that they are separated with a semicolon instead. Like this: </p>
  <pre><code>
    name(Pattern1) -> Term1;
    name(Pattern2) -> Term2;
    name(Pattern3) -> Term3.
  </code></pre>
  <p>The term to the right of the arrow we call <i>function body</i>, or just <i>body</i>.</p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
  <p>
    How will I know which one will be used?
  </p>
  </section>
  <section class="a">
  <p> The first one that pattern matches successfully, starting from the top one. </p>
  </section>
</section>

<section class="law">
  <h2> The Law of Function Definition </h2>
  <p> A function can be defined in many function clauses, following this recipe: </p>
  <pre><code>
    name(Pattern1) -> Term1;
    name(Pattern2) -> Term2;
    name(Pattern3) -> Term3.
  </code></pre>
  <p>
    Where <code>name</code> is an atom, <code>Pattern</code> is a binding
    pattern match, and <code>Term</code> is a term that may include names bound
    in <code>Arguments</code>.
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
  <p>This means that all the names bound in the pattern match can be used in the clause body.</p>
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
  <p>Yes,</p><p>it will return an empty list (<code>[]</code>) for all the arguments that are not lists with elements.</p>
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
  <p>Yes.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p>
    How can I determine the answer for this function call
  </p>
  <code>tail([earth, sun, moon])</code>
  </section>
  <section class="a">
    <p>
      You were not expected to know this one either. The answer is determined by answering all the questions that <code>tail/1</code> asks.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What is the first question asked by <code>tail/1</code>? </p>
  </section>
  <section class="a">
    <p>
      The pattern in the first clause, <code>[_|Tail]</code>, asks if the
      argument is a list that can be split into a head and a tail. It also says
      that if the argument can be split, the tail should be bound to the name
      <code>Tail</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What is the next question? </p>
  </section>
  <section class="a">
    <p> If the first clause did not match, the next question is the next clause. </p>
    <br />
    <p>
      For the original <code>tail/1</code> there are no more. For your extended
      <code>tail/1</code>, the next question is the special name
      <code>_</code>, which ignores its arguments.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What happens after we answer the first question by matching the first clause? </p>
  </section>
  <section class="a">
    <p>
      The first thing that happens is that our arguments are now bound to the
      names in the pattern match. In this case, the name <code>Tail</code> is
      now bound to <code>[sun, moon]</code>.
    </p>
    <br />
    <p>
      Then the function call is replaced with the clause body, so
      <code>tail([earth, sun, moon])</code> becomes <code>Tail</code>, which
      really is <code>[sun, moon]</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What is the next question? </p>
  </section>
  <section class="a">
    <p>
      There's no more questions. That was the end of this function call.
    </p>
  </section>
</section>

<section class="qa before-law">
  <section class="q">
    <p> Can I do this for any function? </p>
  </section>
  <section class="a">
    <p> Yes, </p>
    <p> this will work for all functions in this journey. </p>
  </section>
</section>

<section class="law">
  <h2> The Law of Function Reduction </h2>
  <p>
    A function can be reduced by checking if the arguments match any of the
    pattern matches in the function's clauses, one by one, from top to bottom.
  </p>
  <br />
  <p>
    If there are any matches, the argument will be bound against the pattern, and
    the function call will return the clause body.
  </p>
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

<section class="qa">
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
    What can I put as the body a clause, where your example said <code>Term</code>?
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
  <p>if a function call matches one of the function clauses, it will return a term.</p>
  </section>
</section>

<section class="qa">
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

<section class="qa">
  <section class="q">
  <p> I found the definition of <code>list_of_atoms/1</code>! </p>
  <pre><code>
    list_of_atoms([]) -> true;
    list_of_atoms([Head|Tail]) ->
    &nbsp;&nbsp;continue(is_atom(Head), Tail).
    <br />
    continue(true, Tail) -> list_of_atoms(Tail);
    continue(false, _) -> false.
  </code></pre>
  <p>
  What is the value of <code>list_of_atoms(L)</code>
  </p>
  <p> where </p>
  <pre><code>
    L = [bacon, and, eggs]
  </code></pre>
  </section>
  <section class="a">
  <p> true,</p>
  <p>because <code>L</code> is a list of atoms.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> How do we determine the answer <code>true</code> <br /> for the function call <code>list_of_atoms(L)</code>? </p>
  </section>
  <section class="a">
    <p> We can reduce it, like we did with <code>tail/1</code>.</p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What is the first question asked by <code>list_of_atoms/1</code>? </p>
  </section>
  <section class="a">
    <p>
      The pattern in the first clause, <code>[]</code>, asks if the
      argument is an empty list. If it is, the function returns <code>true</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What is the next question? </p>
  </section>
  <section class="a">
    <p>
      The second pattern, <code>[Head|Tail]</code>, asks if the
      argument is an non-empty list. If it is, the matching binds
      <code>Head</code> to <code>bacon</code> and <code>Tail</code> to <code>[and, eggs]</code>.
    </p>
    <br />
    <p>
      If it does, we replace <code>list_of_atoms(L)</code> with the clause
      body: <code>continue(is_atom(bacon), [and, eggs])</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What is the next question? </p>
  </section>
  <section class="a">
    <p>
    There are no more questions from <code>list_of_atoms/1</code>. If the first
    clause matched, the function returned true. If the second clause matched,
    the function will call <code>is_atom/1</code>, and <code>continue/2</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> So we repeat the same process now for <code>continue/2</code>? </p>
  </section>
  <section class="a">
    <p> Correct. </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What is the first question asked by <code>continue/2</code>? </p>
  </section>
  <section class="a">
    <p>
      There are two patterns in the first clause, <code>true</code> and
      <code>Tail</code>, so there are two first questions.
    </p>
    <br />
    <p>
      The left one asks if the argument is the atom <code>true</code>, but does
      no binding. The rigth one does not ask what the argument is, but it binds it
      to <code>Tail</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> What is the next question? </p>
  </section>
  <section class="a">
    <p>
      There are two patterns in the second clause, <code>false</code> and
      <code>_</code>, so there are two second questions.
    </p>
    <br />
    <p>
      The left one asks if the argument is the atom <code>false</code>, but
      does no binding. The rigth one does not ask what the argument is, and it
      ignores it.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> How do I know which clause will match? </p>
  </section>
  <section class="a">
    <p>
      That depends on whether <code>is_atom(bacon)</code> is <code>true</code>
      or <code>false</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> It is <code>true</code>. Should I replace the function call <br />with the clause body? </p>
  </section>
  <section class="a">
    <p>
      Yes, go ahead.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> Is it true that <code>list_of_atoms([bacon, and, eggs])</code> <br /> 
      is the same as <code>list_of_atoms([and, eggs])</code> ?
    </p>
  </section>
  <section class="a">
    <p>
      Yes it is true,
    </p>
    <p>
      Because the matching clause binds the tail to <code>Tail</code> and passes
      it on to <code>continue/2</code>, which calls
      <code>list_of_atoms(Tail)</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> Is it true that <code>list_of_atoms([and, eggs])</code> <br /> 
      is the same as <code>list_of_atoms([eggs])</code> ?
    </p>
  </section>
  <section class="a">
    <p>
      Yes it is true, for the same reason.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> Is it true that <code>list_of_atoms([eggs])</code> <br /> 
      is the same as <code>list_of_atoms([])</code> ?
    </p>
  </section>
  <section class="a">
    <p>
      Yes it is true,
    </p>
    <p>
      Remember that all lists with elements have an empty list at the end. So the
      tail of <code>[eggs]</code> is <code>[]</code>.
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
    <p> So then <code>list_of_atoms([bacon, and, eggs])</code> <br /> 
    is the same as <code>list_of_atoms([])</code>, <br />
      which is the same as <code>true</code>.
    </p>
  </section>
  <section class="a">
    <p>
      Correct!
    </p>
  </section>
</section>

<section class="qa">
  <section class="q">
  <p> This is the function <code>member/2</code>: </p>
  <pre><code>
    member(____, []) -> false;
    member(Term, [Term|_]) -> true;
    member(Term, [_|Tail]) -> member(Atom, Tail).
  </code></pre>
  <p>
  What is the value of <code>member(A, L)</code>
  </p>
  <p> where </p>
  <pre><code>
    A = queso
    L = [pan, queso, vino]
  </code></pre>
  </section>
  <section class="a">
  <p> true,</p>
  <p>because the atom <code>queso</code> is one of the terms in the list <code>L</code>.</p>
  </section>
</section>


<section class="qa before-law">
<h1> This is very much a work in progress still, come back later!</h1>
</section>

<section class="interlude">
  <p> If you believe all this, we can take a pause. </p>
  <div>
    <h2> This space would be for doodling </h2>
    <p> (but browser support is not there yet) <p>
  </div>
</section>

---
<br />
<p style="text-align: center;">
  <a href="/"> Back to the Index </a>
</p>
