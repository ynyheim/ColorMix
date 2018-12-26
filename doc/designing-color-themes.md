# Designing OrangeMix

Color themes are a highly subjective thing for developers. Luckily there are numerous color themes available for most development platforms.

Still, I have more than once glanced at the color theme used by my colleague and silently thought "How on earth can you stand looking at *that* color combination all day long"? I'm sure they do the same when looking at my screen.

I have tried and experimented with quite a few color themes in different development platforms. Most of them have either too much or too little contrast for my taste. The color mix is also often too radical with lots of different colors for almost every other language token.

> The ideal color theme would make good code *looking good*, and vice versa make bad code *looking bad*.

Ideal or not, a good color theme should

* be pleasurable for the eye and support the fact that developers spend hours at end reading code on screen
* be conservative in the number of different colors used
* have a *sensible* contrast and color balance (where "sensible" of course is highly subjective)
* emphasize important stuff in the code while at the same time tone down less important stuff (whatever "important" might mean in the given language context)
* configuration is code in theory, but it makes sense to treat source code a bit differently compared to (markup) text. Main reason is that configuration and data formats are often more "packed" with text (less indentation and white space). Too much contrast and colors will reduce readability in these files.)

Translating the above criteria into more general and concrete guidelines means:

* Using a dark mode theme
* Few colors; white and grey hues combined with different hues of orange, green hues for comments, blue hues for other artifacts in the source code
* Keywords in general are toned down. Important keywords or keywords indicating "dangerous" behavior should stand out
* Definition of new types/key language features should stand out
* Constants of any sort should stand out
* Generic type parameters should stand out (in languages supporting generics/template-based programming)
* Comments should be clearly different from code and stand out (I firmly believe good, intentional and relevant comments do have its place in code)
* Operators and language constructs easily skipped by the human eye (typically because they occur with no white space between them) should stand out
* All other code (including punctuation and operators) should be *neutral* (displayed in the default foreground color). The exception, of course, would be punctation or operators indicating "dangerous" or "non-normal" behavior.
* Source code could have higher brightness compared to text/configuration/data.