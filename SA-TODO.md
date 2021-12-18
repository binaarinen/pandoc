# Further corrections for SA

1) To disallow the user to set options:
 - set writerExtensions to mempty before using it
    - extensions werden nicht gebraucht. 
    - waere gut wenn --citation und --bibliography funktionieren wuerden

2) write tests for blurb and aside

3) revisit `escAttr = T.replace "\"" "\\\""`
 - it's supposed to to the same as the 3 lines 150-152 in the Inline.hs file

4) check if blurb is an element of `classes' instead of only that value
 - same for aside

5) samuel -- if divs dont have a special content, just return the content

6) Markdown.hs 648
 - make one line again

7) Why are some attribues treated specially (Inline 152ff)
    - We do in order to add the quotes around it

8) use `indent instead of attrlistId
 - done: Inline 165-170    -> umbenennen

9) Inline 185-500
 - use case statement with ` _ | variant == Markua -> return $ "`" etc.

10) Inline 502-523
 - same as on InlineMath
