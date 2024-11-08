# My-modal-test-bf

`My-modal-test-bf` est un composant de modal pour React. Il permet d'afficher un message en overlay centré avec un bouton de fermeture.

## Prérequis

- **Node.js** : Version 16.x ou supérieure recommandée.

## Installation

Installez le package via npm :

```bash
npm install my-modal-test-bf
```

## Importation

Pour utiliser le composant, importez-le dans votre fichier :

```javascript
import { Modal } from 'my-modal-test-bf'
```

## Utilisation

Le composant `Modal` prend deux props principales :

- `message` (string) : Le message affiché dans le modal.
- `onClose` (function) : Une fonction callback appelée lors de la fermeture du modal.

### Exemple de base

```javascript
import React, { useState } from 'react'
import Modal from '<nom-du-package-modal>'

const App = () => {
  const [isModalOpen, setIsModalOpen] = useState(false)

  const handleOpenModal = () => {
    setIsModalOpen(true)
  }

  const handleCloseModal = () => {
    setIsModalOpen(false)
  }

  return (
    <div>
      <button onClick={handleOpenModal}>Open Modal</button>
      {isModalOpen && (
        <Modal
          message="This is a simple modal message."
          onClose={handleCloseModal}
        />
      )}
    </div>
  )
}

export default App
```

## Props

| Prop      | Type     | Description                           | Requis |
| --------- | -------- | ------------------------------------- | ------ |
| `message` | `string` | Message à afficher dans le modal      | Oui    |
| `onClose` | `func`   | Fonction appelée pour fermer le modal | Oui    |

### Détails des Props

- **`message`** : Texte affiché au centre du modal.
- **`onClose`** : Fonction exécutée lors du clic sur le bouton de fermeture ou sur le symbole "×".
