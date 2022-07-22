### https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_build_custom_form_controls

There are some cases where the available `native HTML form controls` may seem like they are not enough. For example, if you need to perform advanced styling on some controls such as the <select> element or if you want to provide custom behaviors, you may consider building your own controls.

In this article, we will discuss how to build a **custom control**. To that end, we will work with an example: rebuilding the <select> element. We will also discuss how, when, and whether building your own control makes sense, and what to consider when building a control is a requirement.

### B
Note: We'll focus on building the control, not on how to make the code generic and reusable; that would involve some non-trivial JavaScript code and DOM manipulation in an unknown context, and that is out of the scope of this article.

### Design, structure, and semantics

Before building a custom control, you should start by figuring out exactly what you want. This will save you some precious time. In particular, it's important to clearly define all the **states of your control**. To do this, it's good to start with an existing control whose states and behavior are well known, so that you can __mimic__ those as much as possible.


In terms of behavior, we are recreating a native HTML element. Therefore it should have the same behaviors and semantics as the **native HTML element**. We require our control __to be usable with a mouse as well as with a keyboard, and comprehensible to a screen reader__, just like any native control. Let's start by defining how the control reaches each state:

The control is in its normal state when:

    the page loads.
    the control was active and the user clicks anywhere outside it.
    the control was active and the user moves the focus to another control using the keyboard (e.g. the Tab key).
