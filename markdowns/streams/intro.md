# Streams
Kids, today we're going to learn about streams. 

The code below doesn't use them.
It transforms a list of names into a list of the same names but capitalized. 
See how much effort you have to put in to understand what the function actually does (well, imagining I didn't just tell you).
That's thanks to all the boilerplate and non-declarative code. 
There's a garbage list with an annoying name that actually changes meaning since it's mutable,
an ugly old for-loop, you have return your garbage list at the end and **EVERYTHING IS AWFUL**.

However there's a silver lining. You can easily make this code beautiful using Streams and its map operator.
Operators mostly take [lambda functions](https://image.slidesharecdn.com/javafp-forpdf-130313133408-phpapp01/95/fp-in-java-project-lambda-and-beyond-5-638.jpg?cb=1363255367) or function references. 
Check [this page](https://docs.oracle.com/javase/8/docs/api/java/util/stream/package-summary.html) for docs. 
To start a Stream from an array of values, use the static Stream.[of](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html#of-T...-) method. 
Don't forget to [.collect()](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html#collect-java.util.stream.Collector-) 
the results at the end to collect all the elements in a collection again. Why not return the stream itself?
Good question, attentive reader. You certainly can. Whether it's a good idea [depends on the context](https://stackoverflow.com/questions/24676877/should-i-return-a-collection-or-a-stream). 

@[Rewrite this garbage using Streams and make sure the test still runs!]({
    "stubs": ["src/main/java/streams/UpperCase.java", "src/test/java/streams/UpperCaseTest.java"], 
    "command": "streams.UpperCaseTest#test"
})