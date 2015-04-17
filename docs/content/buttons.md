---
layout: page
title: Buttons
---

Buttons are used to execute actions in forms, dialogs, and more. Use any of the available button classes to quickly create a styled button.

## Examples

Bootstrap includes six predefined button styles, each serving its own semantic purpose.

{% example html %}
<!-- Provides extra visual weight and identifies the primary action in a set of buttons -->
<button type="button" class="btn btn-primary">Primary</button>

<!-- Secondary, outline button -->
<button type="button" class="btn btn-secondary">Secondary</button>

<!-- Indicates a successful or positive action -->
<button type="button" class="btn btn-success">Success</button>

<!-- Indicates caution should be taken with this action -->
<button type="button" class="btn btn-warning">Warning</button>

<!-- Indicates a dangerous or potentially negative action -->
<button type="button" class="btn btn-danger">Danger</button>

<!-- Deemphasize a button by making it look like a link while maintaining button behavior -->
<button type="button" class="btn btn-link">Link</button>
{% endexample %}

{% callout warning %}
#### Conveying meaning to assistive technologies

Using color to add meaning to a button only provides a visual indication, which will not be conveyed to users of assistive technologies – such as screen readers. Ensure that information denoted by the color is either obvious from the content itself (the visible text of the button), or is included through alternative means, such as additional text hidden with the `.sr-only` class.
{% endcallout %}

## Button tags

Use the button classes on an `<a>`, `<button>`, or `<input>` element.

{% example html %}
<a class="btn btn-secondary" href="#" role="button">Link</a>
<button class="btn btn-secondary" type="submit">Button</button>
<input class="btn btn-secondary" type="button" value="Input">
<input class="btn btn-secondary" type="submit" value="Submit">
{% endexample %}

{% callout warning %}
#### Links acting as buttons

If the `<a>` elements are used to act as buttons – triggering in-page functionality, rather than navigating to another document or section within the current page – they should also be given an appropriate `role="button"`.
{% endcallout %}

{% callout warning %}
#### Cross-browser rendering

As a best practice, **we highly recommend using the `<button>` element whenever possible** to ensure matching cross-browser rendering.
{% endcallout %}

## Sizes

Fancy larger or smaller buttons? Add `.btn-lg`, `.btn-sm`, or `.btn-xs` for additional sizes.

{% example html %}
<button type="button" class="btn btn-primary btn-lg">Large button</button>
<button type="button" class="btn btn-secondary btn-lg">Large button</button>
{% endexample %}

{% example html %}
<button type="button" class="btn btn-primary btn-sm">Small button</button>
<button type="button" class="btn btn-secondary btn-sm">Small button</button>
{% endexample %}

{% example html %}
<button type="button" class="btn btn-primary btn-xs">Extra small button</button>
<button type="button" class="btn btn-secondary btn-xs">Extra small button</button>
{% endexample %}

Create block level buttons—those that span the full width of a parent—by adding `.btn-block`.

{% example html %}
<button type="button" class="btn btn-primary btn-lg btn-block">Block level button</button>
<button type="button" class="btn btn-secondary btn-lg btn-block">Block level button</button>
{% endexample %}

## Active state

Buttons will appear pressed (with a darker background, darker border, and inset shadow) when active. **There's no need to add a class to `<button>`s as they use a pseudo-class**. However, you can still force the same active appearance with `.active` (and include the <code>aria-pressed="true"</code> attribute) should you need to replicate the state programmatically.

{% example html %}
<a href="#" class="btn btn-primary btn-lg active" role="button">Primary link</a>
<a href="#" class="btn btn-secondary btn-lg active" role="button">Link</a>
{% endexample %}

## Disabled state

Make buttons look unclickable by adding the `disabled` boolean attribute to any `<button>` element.

{% example html %}
<button type="button" class="btn btn-lg btn-primary" disabled>Primary button</button>
<button type="button" class="btn btn-secondary btn-lg" disabled>Button</button>
{% endexample %}

As `<a>` elements don't support the `disabled` attribute, you must add the `.disabled` class to fake it.

{% example html %}
<a href="#" class="btn btn-primary btn-lg disabled" role="button">Primary link</a>
<a href="#" class="btn btn-secondary btn-lg disabled" role="button">Link</a>
{% endexample %}

{% callout warning %}
#### Cross-browser compatibility

If you add the `disabled` attribute to a `<button>`, Internet Explorer 9 and below will render text gray with a nasty text-shadow that we cannot fix.
{% endcallout %}

{% callout warning %}
#### Link functionality caveat

This class uses `pointer-events: none` to try to disable the link functionality of `<a>`s, but that CSS property is not yet standardized and isn't fully supported in Opera 18 and below, or in Internet Explorer 11\. In addition, even in browsers that do support `pointer-events: none`, keyboard navigation remains unaffected, meaning that sighted keyboard users and users of assistive technologies will still be able to activate these links. So to be safe, use custom JavaScript to disable such links.
{% endcallout %}

{% callout warning %}
#### Context-specific usage

While button classes can be used on `<a>` and `<button>` elements, only `<button>` elements are supported within our nav and navbar components.
{% endcallout %}