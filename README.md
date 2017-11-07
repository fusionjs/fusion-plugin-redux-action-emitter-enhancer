# fusion-redux-action-emitter-enhancer

Redux store enhancer that emits actions via an injected event emitter.

---

### Example

```js
import reduxActionEnhancerFactory from 'fusion-redux-action-emitter-enhancer';
...

export default function start() {
  const app = new App(root);

  ...
  const UniversalEvents = app.plugin(UniversalEventsPlugin, {fetch});
  const enhancer = reduxActionEnhancerFactory(UniversalEvents);
  app.plugin(Redux, { reducer, enhancer });
  ...

  return app;
}
```

---

### API

The following events are emitted:

- `redux-action-emitter:action`

---
