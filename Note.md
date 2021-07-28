1.Edittext首行缩进
方式一：使用LeadingMarginSpan.Standard
```java
    val textBuilder = SpannableStringBuilder()
    val spaceSpan = LeadingMarginSpan.Standard(indentSize, 0)
    textBuilder.setSpan(spaceSpan, 0, 0, Spanned.SPAN_INCLUSIVE_EXCLUSIVE)
    editText.setText(textBuilder)
    val hintBuilder = SpannableStringBuilder()
    hintBuilder.append(hint)
    hintBuilder.setSpan(spaceSpan, 0, 0, Spanned.SPAN_INCLUSIVE_EXCLUSIVE)
    editText.setHint(hintBuilder)
```