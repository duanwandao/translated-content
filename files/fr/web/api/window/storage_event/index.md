---
title: 'Window: storage event'
slug: Web/API/Window/storage_event
tags:
  - API
  - Evènement
  - Reference
  - Stockage
  - Stockage Web
  - Window
translation_of: Web/API/Window/storage_event
---
{{APIRef}}

L'événement **`storage`** de l'interface {{domxref("Window")}} se déclenche lorsqu'une de stockage (`localStorage`) a été modifiée dans le contexte d'un autre document.

<table class="properties">
  <thead></thead>
  <tbody>
    <tr>
      <th>Bulles</th>
      <td>Non</td>
    </tr>
    <tr>
      <th>Annulable</th>
      <td>Non</td>
    </tr>
    <tr>
      <th>Interface</th>
      <td>{{domxref("StorageEvent")}}</td>
    </tr>
    <tr>
      <th>Propriété de gestionnaire d'événements</th>
      <td>
        {{domxref("WindowEventHandlers.onstorage", "onstorage")}}
      </td>
    </tr>
  </tbody>
</table>

## Exemples

Consignez l'élément `sampleList` sur la console lorsque l'événement `storage` se déclenche :

```js
window.addEventListener('storage', () => {
  // Lorsque le stockage local change, vider la liste sur
  // la console.
  console.log(JSON.parse(window.localStorage.getItem('sampleList')));
});
```

La même action peut être réalisée ) l'aide de la propriété du gestionnaire d'événements [`onstorage`](/en-US/docs/Web/API/WindowEventHandlers/onstorage) :

```js
window.onstorage = () => {
  // Lorsque le stockage local change, vider la liste dans
  // la console.
  console.log(JSON.parse(window.localStorage.getItem('sampleList')));
};
```

## Spécifications

| Spécification                                                                                | Statut                           |
| -------------------------------------------------------------------------------------------- | -------------------------------- |
| {{SpecName('HTML WHATWG', 'indices.html#event-storage', 'storage')}} | {{Spec2('HTML WHATWG')}} |

## Compatibilité des navigateurs

{{Compat("api.Window.storage_event")}}

## Voir également

- [Web Storage API](/en-US/docs/Web/API/Web_Storage_API)
- [Using the Web Storage API](/en-US/docs/Web/API/Web_Storage_API/Using_the_Web_Storage_API)
