# Options

* toc
{:toc}

## `src`
TODO

Type
: `String` (URL)

Default
: `null`

HTML attribute
: `root-margin`

jQuery attribute
: `data-root-margin`

***

## `srcset`
TODO

Type
: `String` (valid `<img/>` srcset value)

Default
: `null`

HTML attribute
: `root-margin`

jQuery attribute
: `data-root-margin`

***

## `width`
The width of the requested image. This doesn't necessarily have to be the actual width of the image, since it is only used to calculate the aspect ratio of the placeholder.
However, if the provided `width` is lower than the width available to the parent `hy-img` component, `width` will be used to set the size of the placeholder directly (in px).

Type
: `Number` (in px)

Default
: `null`

HTML attribute
: `width`

jQuery attribute
: `data-width`

***

## `height`
The height of the requested image. This doesn't necessarily have to be the actual height of the image, since it is only used to calculate the aspect ratio of the placeholder.
However, if the provided `width` (no typo!) is lower than the width available to the parent `hy-img` component, `height` will be used to set the size of the placeholder directly (in px).

Type
: `Number` (in px)

Default
: `null`

HTML attribute
: `height`

jQuery attribute
: `data-height`

***

## `root`
Specifies which scrollable element will trigger loading the image.
When no value is provided, it will default to the document (same as intersection observer).

Passes on the value to the `root` option of the underlying `IntersectionObserver`.

Type
: `String` (CSS Selector)

Default
: `null`

HTML attribute
: `root`

jQuery attribute
: `data-root`

***

## `rootMargin`
Passes on the value to the `rootMargin` option of the underlying `IntersectionObserver`.

Type
: `String` (CSS Position String, e.g. `0px`, or `100px 150px 200px`)

Default
: `0px`

HTML attribute
: `root-margin`

jQuery attribute
: `data-root-margin`

***

## `alt`
An textual description of the image. Same as image alt text.
Will be passed on to the `alt` attribute of the underlying `img` tag.

***

## `decoding`
Will be passed on to the `decoding` attribute of the underlying `img` tag.

***

## `longdesc`
Will be passed on to the `longdesc` attribute of the underlying `img` tag.

<!-- ## `ismap`
## `usemap` -->

<!-- ## `replaceIds`
An array of HTML `id`s, that are children of this component,
that should be replaced by the HTML elements of the same `id` from another page.

If no ids are provided, hy-push-state will attempt to replace the entire content of the component ,
provided the component itself has an id.
If the component doesn't have an id,
hy-push-state will attempt to find the equivalent component in the new document based on it's tag name,
but it is highly recommended that you don't rely on this feature.

Type
: `Array` of `String` (where strings are HTML element `id`s, that are children of this component)

Default
: `[]`

jQuery attribute
: `data-replace-ids` (e.g.: `data-replace-ids="some-id,another-id"`)

HTML attribute
: `replace-ids` (e.g.: `replace-ids="some-id,another-id"`)

**Example**: Assume we have a web component `very-special` that has some state of its own,
so we don't want to replace it on a page transition.
However, we still want `a` tags inside `very-special` to trigger transitions,
so we give unique ids (per page) to the parts we want to replace, so that `very-special` remains untouched:

```html
<hy-push-state replace-ids="my-content,my-aside">
  <main id="my-content">
    Transition to <a href="/page">Another Page</a>
  </main>

  <very-special>
    This element should persist between transitions,
    but a <a href="/another-page">Link</a>
    in here should still trigger a page transition.

    <aside id="my-aside">
      The contents of this should be replaced dynamically as well.
    </aside>
  </very-special>
</hy-push-state>
```

***

## `linkSelector`
A CSS selector to find all links that can cause a page transition.

You can use this to add a blacklist CSS class, e.g. `a[href]:not(.blacklisted)`,
or a whitelist CSS class, e.g. `a[href].whitelisted`.

By default, all `a` tags with a `href` attribute are selected.
If your site follows a convention of starting internal links with `/`,
you can use `a[href^='/']` to only select links of this form.

Note that hy-push-state will still determine whether a given link points to an internal or external site,
so that this selector doesn't have to have 100% accuracy.

Type
: `String` (CSS Selector)

Default
: `'a[href]:not(.no-push-state)'`

jQuery attribute
: `data-link-selector`

HTML attribute
: `link-selector`

***

## `scrollRestoration`
TODO

Type
: `Boolean`

Default
: `false`

jQuery attribute
: `data-scroll-restoration`

HTML attribute
: `scroll-restoration`

***

## `duration`
The duration of a page transition. Use this to ensure that animations have sufficient time to finish
before the current content gets replaced with new content.

Note that hy-push-state gives you more fine-grained control over animation durations
via the [`hy-push-state-start`](events.md#hy-push-state-start) event's `waitUntil` method.

Type
: `Number` (ms)

Default
: `0`

jQuery attribute
: `data-duration`

HTML attribute
: `duration` -->
