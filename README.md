### https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_build_custom_form_controls

There are some cases where the available `native HTML form controls` may seem like they are not enough. For example, if you need to perform advanced styling on some controls such as the <select> element or if you want to provide custom behaviors, you may consider building your own controls.

## A
In this article, we will discuss how to build a **custom control**. To that end, we will work with an example: rebuilding the <select> element. We will also discuss how, when, and whether building your own control makes sense, and what to consider when building a control is a requirement.

### B
Note: We'll focus on building the control, not on how to make the code generic and reusable; that would involve some non-trivial JavaScript code and DOM manipulation in an unknown context, and that is out of the scope of this article.