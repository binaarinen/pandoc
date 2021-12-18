# Further corrections for SA

1) To disallow the user to set options:
 - done
 - set writerExtensions to mempty before using it
    - extensions werden nicht gebraucht. 
    - waere gut wenn --citation und --bibliography funktionieren wuerden

2) write tests for blurb and aside
 - TODO write tests

3) Tried: revisit `escAttr = T.replace "\"" "\\\""`
 - TODO
 - it's supposed to to the same as the 3 lines 150-152 in the Inline.hs file
   tried:     -- escAttr          = mconcat . map escAttrChar . T.unpack
              -- escAttrChar '"'  = literal "\""
              -- escAttrChar c    = literal $ T.singleton c
              escAttr = T.replace "\"" "\\\""

              and

              escAttr          = mconcat . map escAttrChar . T.unpack
              -- escAttrChar '"'  = literal "\""
              -- escAttrChar c    = literal $ T.singleton c
              escAttr = T.replace "\"" "\\\""

              => both results in compile error because of mismatched types
              => keine Ahnung, könnte man sicher hinbiegen, läuft ja momentan


4) done and tested: check if blurb is an element of `classes' instead of only that value
 - done and tested: same for aside

5) done and tested: if divs dont have a special content, just return the content
 - done

6) Markdown.hs 648 - make one line again
 - done

7) Why are some attribues treated specially (Inline 152ff)
    - We do in order to add the quotes around it

8) use `indent instead of attrlistId
 - done  Inline 165-170    -> umbenennen

9) Inline 185-500
 - use case statement with ` _ | variant == Markua -> return $ "`" etc.
 - TODO

10) Inline 502-523
 - same as on InlineMath
 - TODO
