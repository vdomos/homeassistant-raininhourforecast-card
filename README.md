# rainInHourForecast card

Cette carte affiche la prévision de pluie dans l'heure en s'appuyant sur l'entité **sensor.<VILLE>_next_rain** de l'intégration **meteo-france**

![RainInHour1](Meteo-France_RainInHour_Card_1.png)

## Installation

### Copie du fichier

Installe `raininhourforecast card` en copiant le fichier  `meteofrance/meteofrance-raininhourforecast.js` du dépot dans `<config directory>/www/meteofrance/meteofrance-raininhourforecast.js` de l'instance Home Assistant.

**Example:**

```bash
cd <config directory>/www
mkdir meteofrance
cd meteofrance
wget https://github.com/vdomos/homeassistant-raininhourforecast-card/raw/master/raininhourforecast.js
```

### Configuration de la ressource

Faire le lien de la ressource js dans votre configuration `configuration.yaml`.

```yaml
lovelace:
  mode: yaml
  resources:
    - url: /local/meteofrance/meteofrance-raininhourforecast.js
      type: module
```

### Ajout de la "custom-card" 

Ajouter la nouvelle "card" dans la GUI home-assistant en ajoutant une carte manuelle sur une vue et en la renseignant avec la **custom-card** et 
l'entité **meteo-france**:


**Example:**

```yaml
type: 'custom:meteofrance-raininhourforecast'
entity: sensor.nancy_next_rain
```

![RainInHour1](Meteo-France_RainInHour_Card_1.png)


