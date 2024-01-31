# Routen & Endpunkte 

## Authentifizierung 

Die Authentifizierung findet mittels mittels Basic Auth (http://username:password@domain/) statt. 

`domain` steht dabei für die Domain unter der Sie auf GeoSpot! zugreifen. Für die SaaS lautet die Domain <https://www.geospot.de/>.

Sie können Ihren Account auch einer Konfigurationsdatei für einen schnelleren und sicheren Login hinterlegen.

## 1 Abfrage welche Werte zur Verfügung stehen

<https://www.geospot.de/api/available_values.json>

Bsp. Rückgabe:
Firmenzähler(fz_values) nur Daten optional

```json
{
  "values": {
    "ew": "Einwohner",
    "ew_0014": "Einwohner 0 bis 14 Jahre",
    "hh": "Anzahl Haushalte",
    "ew_zz": "Zuzüge insgesamt",
    "p25ew": "Einwohner insgesamt - Prognose 2025",
    "p30ew": "Einwohner insgesamt - Prognose 2030",
    "bap_gesamt": "Büroarbeitsplätze insgesamt",
    "cfiw_abs": "Affinität für Fitness/Wellness absolut",
    "lohas_abs": "Lifestyles of Health and Sustainability absolut",
    "sysgastro": "Systemgastronomie",
    "kk_ew": "Kaufkraft pro Einwohner",
    "tech_prueforga": "Technische Prüforganisationen" 
  }
  "fz_values": {
    "fz_1903": "Firmenzähler: Entsorgung und Recycling",
    "fz_k_1903": "Firmenzähler (kleine Betriebe): Entsorgung und Recycling",
    "fz_m_1903": "Firmenzähler (mittlere Betriebe): Entsorgung und Recycling",
    "fz_g_1903": "Firmenzähler (große Betriebe): Entsorgung und Recycling"
  }
}
```


Mit Zusatzinformationen Bundeswerten, Mittelwert, Scores

<https://www.geospot.de/api/available_values.json?extended=true>

```json
{
  "values": {
    "ew": {
      "name": "Einwohner",
      "country_value": 83155031,
      "country_mean": 189,
      "scores": {
        "1": {
          "min": 0,
          "max": 0
        },
        "2": {
          "min": 0,
          "max": 1
        },
        "3": {
          "min": 1,
          "max": 41
        },
        "4": {
          "min": 41,
          "max": 47
        },
        "5": {
          "min": 47,
          "max": 145
        },
        "6": {
          "min": 145,
          "max": 281
        },
        "7": {
          "min": 281,
          "max": 701
        },
        "8": {
          "min": 701,
          "max": 1208
        },
        "9": {
          "min": 1208,
          "max": 3294
        },
        "10": {
          "min": 3294,
          "max": 20000
        }
      }
    },
    "hh": {
      "name": "Anzahl Haushalte",
      "country_value": 41043789,
      "country_mean": 93,
      "scores": {
        "1": {
          "min": 0,
          "max": 0
        },
        "2": {
          "min": 0,
          "max": 1
        },
        "3": {
          "min": 1,
          "max": 19
        },
        "4": {
          "min": 19,
          "max": 21
        },
        "5": {
          "min": 21,
          "max": 66
        },
        "6": {
          "min": 66,
          "max": 128
        },
        "7": {
          "min": 128,
          "max": 331
        },
        "8": {
          "min": 331,
          "max": 606
        },
        "9": {
          "min": 606,
          "max": 1883
        },
        "10": {
          "min": 1883,
          "max": 1500000
        }
      }
    },
    "erw_tae": {
      "name": "Erwerbstätige gesamt",
      "country_value": 43018195,
      "country_mean": 98,
      "scores": {
        "1": {
          "min": 0,
          "max": 0
        },
        "2": {
          "min": 0,
          "max": 1
        },
        "3": {
          "min": 1,
          "max": 26
        },
        "4": {
          "min": 26,
          "max": 29
        },
        "5": {
          "min": 29,
          "max": 85
        },
        "6": {
          "min": 85,
          "max": 158
        },
        "7": {
          "min": 158,
          "max": 374
        },
        "8": {
          "min": 374,
          "max": 627
        },
        "9": {
          "min": 627,
          "max": 1649
        },
        "10": {
          "min": 1649,
          "max": 8000
        }
      }
    },
    "kfzbestand_gesamt": {
      "name": "Anzahl KFZ",
      "country_value": 58964379,
      "country_mean": 134,
      "scores": {
        "1": {
          "min": 0,
          "max": 1
        },
        "2": {
          "min": 1,
          "max": 10
        },
        "3": {
          "min": 10,
          "max": 20
        },
        "4": {
          "min": 20,
          "max": 50
        },
        "5": {
          "min": 50,
          "max": 100
        },
        "6": {
          "min": 100,
          "max": 200
        },
        "7": {
          "min": 200,
          "max": 500
        },
        "8": {
          "min": 500,
          "max": 750
        },
        "9": {
          "min": 750,
          "max": 1000
        },
        "10": {
          "min": 1000,
          "max": 10000
        }
      }
    }
  }
  "fz_values": {
    "fz_1903": {
      "name": "Firmenzähler: Entsorgung und Recycling",
      "country_value": 6890,
      "country_mean": 1
    },
    "fz_k_1903": {
      "name": "Firmenzähler (kleine Betriebe): Entsorgung und Recycling",
      "country_value": 4800,
      "country_mean": 1
    },
    "fz_m_1903": {
      "name": "Firmenzähler (mittlere Betriebe): Entsorgung und Recycling",
      "country_value": 1911,
      "country_mean": 1
    },
    "fz_g_1903": {
      "name": "Firmenzähler (große Betriebe): Entsorgung und Recycling",
      "country_value": 179,
      "country_mean": 1
    }
  }
}
```

## 2 Abfrage welche Punkt-Layer zur Verfügung stehen

<https://www.geospot.de/api/available_layers.json>

- System Layers, diese Daten kommen von gbconsite
- Own Layers, diese Daten kommen vom Kunden

Bsp. Rückgabe:

```json
{
    "system_layers": {
        "129": {
            "name": "FSP",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        },
        "128": {
            "name": "GTÜ",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        },
        "135": {
            "name": "Kfz-Handel",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        },
        "130": {
            "name": "KÜS",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        },
        "132": {
            "name": "TÜV NORD",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        },
        "127": {
            "name": "TÜV Rheinland",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        },
        "133": {
            "name": "TÜV SÜD",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        },
        "131": {
            "name": "TÜV Thüringen",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        },
        "134": {
            "name": "Unterhaltungselektronik-Fachmarkt",
            "properties": ["Name", "Adresse", "Entfernung (Meter)"]
        }
    },
    "own_layers": {
        "11": {
            "name": "PLZ Zentroide",
            "properties": ["name", "description", "Entfernung (Meter)"]
        },
        "10": {
            "name": "Schüco-Partner",
            "properties": ["ID", "Art", "Ort", "PLZ", "Typ", "Name", "Status", "Adresse", "Entfernung (Meter)"]
        }
    }
}
```

## 3 Abfrage zum Standort

<https://www.geospot.de/api/whitespot_location.json?lat=48.27679550566659&lon=11.574096679687498&radius=3000>

Als Bild:
<https://www.geospot.de/api/whitespot_location.png?lat=48.27679550566659&lon=11.574096679687498&radius=3000>

| **Parameter**       | **Beschreibung**                                                                                                                 | **Werte**                   |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| **radius**          | **Required** Radius                                                                                                                  |  integer                    |
| **minuten**         | **Required** Für Fahrzeitgebiet statt Radius                                                                                         |  integer                    |
| **lat**             | **Required** Latitude                                                                                                                | float                       |
| **lon**             | **Required** Longitude                                                                                                               | float                       |
| **postalCode**      | **Required alt. 1** Postleitzahl                                                                                                     | string                      |
| **city**            | **Required alt. 1** Ort                                                                                                              | string                      |
| **street**          | **Required alt. 1** Straße (kann auch die Hausnummer beinhalten)                                                                     | string                      |
| **houseNumber**     | **Optional alt. 1** Hausnummer                                                                                                       | string                      |
| **country**         | **Optional alt. 1** Land                                                                                                             | string                      |
| **address**         | **Required alt. 2** (kann mit alt. 1 kombiniert werden) kompletter Adressstring                                                        | string                      |
| **countryCode**     | **Optional alt. 1/2** Land ISO 3166-1 alpha-3 (DEU)                                                                                  | string                      |
| **grid200**         | **Optional** Die Werte (nicht Scores oder Bild) werden in einem 200x200 Meter Raster ermittelt statt 600x600. (sinnvoll bei kleinem Radius bzw. wenig Minuten. |  true  oder false (default) |
| **value_filter**    | **Optional** Filtern der ausgegebenen Daten-Variablen ("values"). Verfügbare Daten-Variablen sind abfragbar mit [available_values.json](#1-abfrage-welche-werte-zur-verfügung-stehen). Dringend empfohlen bei großem Umfang von Daten-Variablen. Beschleunigt Abfrage.   | Komma Liste                 |
| **all_layers**      | **Optional** Alle System Layers                                                                                                      | true oder false (default)   |
| **layer_ids**       | **Optional** System Layers mit Ids                                                                                                   | Komma Liste                 |
| **layer_names**     | **Optional** System Layers mit Namen                                                                                                 | Komma Liste                 |
| **all_own_layers**  | **Optional** Alle Eigenen Layers                                                                                                              | true oder false (default)   |
| **own_layer_ids**   | **Optional** Eigene Layers mit Ids                                                                                                   | Komma Liste                 |
| **own_layer_names** | **Optional** Eigene Layers mit Namen                                                                                                 | Komma Liste                 |
| **include_image**   | **Optional** Bild wird als Base64 String zurückgegeben(nur bei json)                                                                 | true  oder false (default)  |

Wenn keine Koordinaten vorhanden sind, dann die Alternative 1 und 2 verwenden.
Alternative 1: Es muss mindestens 1 Wert angegeben sein.


| **Parameter für Bild** | **Beschreibung (bei format png oder Paramter include_image)**                                                                   | **Werte**                   |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| **include_cells**   | **Optional** Zellen werden angezeigt                                                                                                 |  true  oder false (default) |
| **transparent**     | **Optional** Transparentz für die Zellen                                                                                             |  float 0.0 -1.0             |
| **filter**         | **Optional** Damit wird gesteuert, welche Scores in welchem Wertebereich verwendet werden. Bsp. filter[ew]=5,10 oder filter[ew]=5,10,true- Parameter include_cells wird automatisch auf true gesetzt |  min,max(,reverse)          |

<https://www.geospot.de/api/whitespot_location.png?lat=48.27679550566659&lon=11.574096679687498&radius=3000&filter[ew]=6,10&transparent=0.5>


Bsp. Rückgabe:
Firmenzähler(fz_data) nur Daten optional

```json
{
    "data": {
        "ew": {
            "name": "Einwohner",
            "value": 37332,
            "score": 5.7
        },
        "ew_0014": {
            "name": "Einwohner 0 bis 14 Jahre",
            "value": 5112,
            "score": 5.7
        },
        "hh": {
            "name": "Anzahl Haushalte",
            "value": 18586,
            "score": 5.7
        },
        "ew_zz": {
            "name": "Zuzüge insgesamt",
            "value": 3462,
            "score": 1.1
        },
        "p25ew": {
            "name": "Einwohner insgesamt - Prognose 2025",
            "value": 40568,
            "score": 1.1
        },
        "p30ew": {
            "name": "Einwohner insgesamt - Prognose 2030",
            "value": 41939,
            "score": 1.1
        },
        "bap_gesamt": {
            "name": "Büroarbeitsplätze insgesamt",
            "value": 12400,
            "score": 1.1
        },
        "cfiw_abs": {
            "name": "Affinität für Fitness/Wellness absolut",
            "value": 10023,
            "score": 1.1
        },
        "lohas_abs": {
            "name": "Lifestyles of Health and Sustainability absolut",
            "value": 6370,
            "score": 1.1
        },
        "sysgastro": {
            "name": "Systemgastronomie",
            "value": 3,
            "score": 1.1
        },
        "kk_ew": {
            "name": "Kaufkraft pro Einwohner",
            "value": 27163,
            "score": 1.1
        },
        "tech_prueforga": {
            "name": "Technische Prüforganisationen",
            "value": 2,
            "score": 1.1
        }
    },
    "fz_data": {
      "fz_1903": {
        "name": "Firmenzähler: Entsorgung und Recycling",
        "value": 4
      },
      "fz_k_1903": {
        "name": "Firmenzähler (kleine Betriebe): Entsorgung und Recycling",
        "value": 1
      },
      "fz_m_1903": {
        "name": "Firmenzähler (mittlere Betriebe): Entsorgung und Recycling",
        "value": 3
      },
      "fz_g_1903": {
        "name": "Firmenzähler (große Betriebe): Entsorgung und Recycling",
        "value": 0
      }
    },
    "layer": [],
    "own_layer": [],
    "input": {
        "radius": "3000",
        "minuten": null,
        "latitude": "48.27679550566659",
        "longitude": "11.574096679687498",
        "geocode": {
            "postalCode": null,
            "city": null,
            "street": null,
            "houseNumber": null,
            "country": null,
            "address": null,
            "countryCode": null
        },
        "layer_ids": null,
        "layer_names": null,
        "own_layer_ids": null,
        "own_layer_names": true,
        "all_layers": null,
        "all_own_layers": null,
        "grid200": false
    }
}
```

<https://www.geospot.de/api/whitespot_location.json?lat=48.27679550566659&lon=11.574096679687498&radius=3000&all_own_layers=true&all_layers=true>

```json
{
    "data": {
        "ew": {
            "name": "Einwohner",
            "value": 55238,
            "score": 5.7
        },
        "ew_0014": {
            "name": "Einwohner 0 bis 14 Jahre",
            "value": 7671,
            "score": 5.7
        },
        "hh": {
            "name": "Anzahl Haushalte",
            "value": 26892,
            "score": 5.7
        },
        "ew_zz": {
            "name": "Zuzüge insgesamt",
            "value": 5313,
            "score": 1.1
        },
        "p25ew": {
            "name": "Einwohner insgesamt - Prognose 2025",
            "value": 60750,
            "score": 1.1
        },
        "p30ew": {
            "name": "Einwohner insgesamt - Prognose 2030",
            "value": 62903,
            "score": 1.1
        },
        "bap_gesamt": {
            "name": "Büroarbeitsplätze insgesamt",
            "value": 21989,
            "score": 1.1
        },
        "cfiw_abs": {
            "name": "Affinität für Fitness/Wellness absolut",
            "value": 15191,
            "score": 1.1
        },
        "lohas_abs": {
            "name": "Lifestyles of Health and Sustainability absolut",
            "value": 9516,
            "score": 1.1
        },
        "sysgastro": {
            "name": "Systemgastronomie",
            "value": 3,
            "score": 1.1
        },
        "kk_ew": {
            "name": "Kaufkraft pro Einwohner",
            "value": 26675,
            "score": 1.1
        },
        "tech_prueforga": {
            "name": "Technische Prüforganisationen",
            "value": 6,
            "score": 1.1
        }
    },
    "layer": [{
        "name": "Kfz-Handel",
        "id": 135,
        "data": [{
            "Name": "Auto-Service-Team GmbH",
            "Adresse": "Hauptstraße 41, 85716 Unterschleißheim",
            "Entfernung (Meter)": 662
        }, {
            "Name": "KölblKratzmeier GmbH \u0026 Co. KG",
            "Adresse": "Carl-von-Linde-Straße 31, 85716 Unterschleißheim",
            "Entfernung (Meter)": 680
        }, {
            "Name": "KölblKratzmeier GmbH \u0026 Co. KG",
            "Adresse": "Carl-von-Linde-Straße 31, 85716 Unterschleißheim",
            "Entfernung (Meter)": 680
        }, {
            "Name": "Auto Kölbl GmbH",
            "Adresse": "Beim Pfarracker 55, 85716 Unterschleißheim",
            "Entfernung (Meter)": 719
        }, {
            "Name": "Auto Kölbl GmbH",
            "Adresse": "Beim Pfarracker 55, 85716 Unterschleißheim",
            "Entfernung (Meter)": 719
        }, {
            "Name": "Auto Forum Auto Kölbl Vertriebs GmbH \u0026 Co. KG",
            "Adresse": "Landshuter Straße 25, 85716 Unterschleißheim",
            "Entfernung (Meter)": 736
        }, {
            "Name": "Autohaus Berker GmbH",
            "Adresse": "Landshuter Straße 23, 85716 Unterschleißheim",
            "Entfernung (Meter)": 785
        }, {
            "Name": "Autohaus Berker GmbH",
            "Adresse": "Landshuter Straße 23, 85716 Unterschleißheim",
            "Entfernung (Meter)": 785
        }, {
            "Name": "Dennemarck GmbH",
            "Adresse": "Sportplatzstraße 1, 85716 Unterschleißheim",
            "Entfernung (Meter)": 1136
        }, {
            "Name": "Dennemarck GmbH",
            "Adresse": "Sportplatzstraße 1, 85716 Unterschleißheim",
            "Entfernung (Meter)": 1136
        }, {
            "Name": "Autohaus Dill",
            "Adresse": "Obere Hauptstraße 8, 85386 Eching",
            "Entfernung (Meter)": 3970
        }, {
            "Name": "BMW AG Niederlassung München",
            "Adresse": "Schleißheimer Straße 82, 85748 Garching bei München",
            "Entfernung (Meter)": 4953
        }]
    }, {
        "name": "TÜV Rheinland",
        "id": 127,
        "data": []
    }, {
        "name": "GTÜ",
        "id": 128,
        "data": [{
            "Name": "Kfz-Prüfstelle Unterschleißheim Schubert Kfz-Sachverständige GmbH",
            "Adresse": "Einsteinstr. 6, 85716 Unterschleißheim",
            "Entfernung (Meter)": 1230
        }]
    }, {
        "name": "FSP",
        "id": 129,
        "data": []
    }, {
        "name": "KÜS",
        "id": 130,
        "data": [{
            "Name": "Dipl.-Ing. (FH) Bernd Daniel-Soldner",
            "Adresse": "Dieselstr. 1a, 85716 Unterschleißheim",
            "Entfernung (Meter)": 550
        }, {
            "Name": "Ingenieurbüro Johannes Kreuch",
            "Adresse": "Eggentaler Str. 27, 85778 Haimhausen",
            "Entfernung (Meter)": 4096
        }]
    }, {
        "name": "TÜV Thüringen",
        "id": 131,
        "data": []
    }, {
        "name": "TÜV NORD",
        "id": 132,
        "data": []
    }, {
        "name": "TÜV SÜD",
        "id": 133,
        "data": [{
            "Name": "TÜV SÜD Service-Center Garching",
            "Adresse": "Schleißheimer Str. 126a, 85748 Garching b.München",
            "Entfernung (Meter)": 3750
        }]
    }, {
        "name": "Unterhaltungselektronik-Fachmarkt",
        "id": 134,
        "data": []
    }],
    "own_layer": [{
        "name": "Schüco-Partner",
        "id": 10,
        "data": []
    }, {
        "name": "PLZ Zentroide",
        "id": 11,
        "data": [{
            "name": "85716",
            "description": "Unterschleißheim, St",
            "Entfernung (Meter)": 839
        }, {
            "name": "85764",
            "description": "Oberschleißheim",
            "Entfernung (Meter)": 3306
        }, {
            "name": "85386",
            "description": "Eching",
            "Entfernung (Meter)": 4547
        }, {
            "name": "85778",
            "description": "Haimhausen",
            "Entfernung (Meter)": 4954
        }]
    }],
    "input": {
        "radius": "5000",
        "minuten": null,
        "latitude": "48.27679550566659",
        "longitude": "11.574096679687498",
        "geocode": {
            "postalCode": null,
            "city": null,
            "street": null,
            "houseNumber": null,
            "country": null,
            "address": null,
            "countryCode": null
        },
        "layer_ids": null,
        "layer_names": null,
        "own_layer_ids": null,
        "own_layer_names": true,
        "all_layers": "true",
        "all_own_layers": "true",
        "grid200": false
    },
    "image": "data:image/png;base64,iVBORw0...."
}
```
