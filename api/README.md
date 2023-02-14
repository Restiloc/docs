# Restiloc API Documentation

Documentation de l'API, disponible en cliquant [ici](https://restiloc.space/docs/).

## Introduction

Cette documentation décrit les fonctionnalités et les opérations disponibles via l'API. Il fournit également des informations sur la manière de s'authentifier, les définitions des end points, les paramètres requis et facultatifs, ainsi que des exemples de code pour vous aider à démarrer.

Restiloc est une API simple permettant aux experts de consulter des missions et de créer des ressources comme par exemple un nouveau vehicule.

## Authentification

Pour accéder à l'API, vous devez d'abord vous authentifier. L'authentification se fait en envoyant une demande `POST` avec vos informations d'identification à l'URL d'authentification. Les informations d'identification requises sont un **nom d'utilisateur** ou **adresse mail** et un **mot de passe**.

Si l'authentification réussit, une jeton d'accès sera renvoyé dans le corps de la réponse. Ce jeton d'accès doit être inclus dans les en-têtes de toutes les requêtes futures à l'API pour fournir une **preuve** d'authentification.

## Endpoint

L'API propose les end points suivants :

### Récupérer la liste des missions

##### Route GET méthode `index`

```bash
GET|HEAD        api/missions
```

#### Réponse

```json
codeHTTP 200 OK
Content-Type: application/json

[
	{
		"id": 1,
		"dateMission": "2023-02-22",
		"startedAt": null,
		"kilometersCounter": 98726,
		"nameExpertFile": "Bulah Harber",
		"isFinished": 1,
		"route": "http:\/\/127.0.0.1:8000\/api\/missions\/1",
		"vehicle": {
			"id": 38,
			"licencePlate": "WBAPK53549A473174",
			"color": "Orange",
			"releaseYear": 2008,
			"route": "http:\/\/127.0.0.1:8000\/api\/vehicles\/38"
		},
		"expert": {
			"id": 8,
			"lastName": "Murphy",
			"firstName": "Rosanna",
			"email": "lwuckert@gmail.com",
			"phoneNumber": "+1-251-664-7522",
			"username": "hill.trent",
			"route": "http:\/\/127.0.0.1:8000\/api\/experts\/8"
		},
		"garage": {
			"id": 79,
			"name": "in aut excepturi",
			"addressNumber": "72478 Manley Villages Apt. 471",
			"street": "Doug Union",
			"postalCode": "25058-6937",
			"city": "South Archibaldstad",
			"phoneNumber": "+1-619-482-6070",
			"latitude": "-63.299811",
			"longitude": "102.932155",
			"url": "http:\/\/127.0.0.1:8000\/api\/garages\/79"
		},
		"unavailability": {
			"id": 1,
			"customerResponsible": 0,
			"route": "http:\/\/127.0.0.1:8000\/api\/unavailabilities\/1"
		},
		"pree": [
			{
				"id": 16,
				"label": "eum",
				"description": "autem dolores quo corporis vel et sed quidem laborum unde laborum distinctio enim consectetur et ea laboriosam magni eos aliquid",
				"image": "\/tmp\/1c744a992aa298c0e371bc266724328d.png",
				"signature": "\/tmp\/6e0289155a3236193900c47a05ca01f6.png",
				"route": "http:\/\/127.0.0.1:8000\/api\/pree\/16"
			},
			{
				"id": 19,
				"label": "quia",
				"description": "voluptas maxime rerum id perferendis perspiciatis voluptas sequi vel quibusdam in omnis quae iste at omnis aspernatur dicta ut et",
				"image": "\/tmp\/7b61aa98cd4d1068796fcef20dfdffeb.png",
				"signature": "\/tmp\/d74411cec3b90e6190aac15f0f7953db.png",
				"route": "http:\/\/127.0.0.1:8000\/api\/pree\/19"
			},
			{
				"id": 20,
				"label": "excepturi",
				"description": "eaque provident eaque eaque explicabo corporis hic dolores ut molestiae praesentium laboriosam omnis recusandae voluptatem eos aut dolores mollitia quisquam",
				"image": "\/tmp\/60f5d234226c713f06d3c35cb495d893.png",
				"signature": "\/tmp\/1e4818828132951a7c1e93c414d0675f.png",
				"route": "http:\/\/127.0.0.1:8000\/api\/pree\/20"
			}
		]
	},
    {
			"id": 2,
			"dateMission": "2023-02-15",
			"startedAt": null,
			"kilometersCounter": 196228,
			"nameExpertFile": "Ulices Crist",
			"isFinished": 1,
			"route": "http:\/\/127.0.0.1:8000\/api\/missions\/2",
			"vehicle": {
				"id": 19,
				"licencePlate": "WAUMF98P66A420495",
				"color": "Turquoise",
				"releaseYear": 1999,
				"route": "http:\/\/127.0.0.1:8000\/api\/vehicles\/19"
			},
			"expert": {
				"id": 8,
				"lastName": "Murphy",
				"firstName": "Rosanna",
				"email": "lwuckert@gmail.com",
				"phoneNumber": "+1-251-664-7522",
				"username": "hill.trent",
				"route": "http:\/\/127.0.0.1:8000\/api\/experts\/8"
			},
			"garage": {
				"id": 26,
				"name": "alias tempore voluptas",
				"addressNumber": "6456 Elmira Manors",
				"street": "Daugherty Road",
				"postalCode": "31847",
				"city": "Port Angelberg",
				"phoneNumber": "432.382.6595",
				"latitude": "25.674442",
				"longitude": "133.038127",
				"url": "http:\/\/127.0.0.1:8000\/api\/garages\/26"
			},
			"unavailability": {
				"id": 2,
				"customerResponsible": 0,
				"route": "http:\/\/127.0.0.1:8000\/api\/unavailabilities\/2"
			},
			"pree": [
				{
					"id": 29,
					"label": "tempora",
					"description": "omnis magni fugiat expedita aspernatur ducimus quos temporibus delectus libero doloremque illo ab aut nemo soluta corporis repudiandae fugiat facilis",
					"image": "\/tmp\/1e8b4dce3681c0b5dfcb0fd2152e2b33.png",
					"signature": "\/tmp\/2880baa4560e6de51ef14dc082159849.png",
					"route": "http:\/\/127.0.0.1:8000\/api\/pree\/29"
				},
				{
					"id": 38,
					"label": "at",
					"description": "aut quis assumenda ut ut possimus est aut quos sapiente dolore ut quibusdam nihil ut totam nam laborum est et",
					"image": "\/tmp\/73227ff4069dadc23baf36be6d790174.png",
					"signature": "\/tmp\/2cc60c8a430f171ff9f9719896051a81.png",
					"route": "http:\/\/127.0.0.1:8000\/api\/pree\/38"
				}
			]
		},
]
...
```

### Créer un véhicule

##### Route POST méthode `store`

- Header

```bash
POST 	api/vehicles
```

- Body

```json
{
  "licencePlate": "WA1WYBFE2AD448606",
  "color": "Yellow",
  "releaseYear": 2014
}
```

#### Réponse

```json
codeHTTP 201 Created
Content-Type: application/json

{
	"success": "true",
	"message": "Vehicle added successfully"
}

or

codeHTTP 400 Bad Request
Content-Type: application/json

{
	"success": "false",
	"message": "Failed to add vehicle"
}
```

### Récupérer une mission spécifique

##### Route GET méthode `show`

```bash
GET|HEAD        api/missions/{id}
```

#### Paramètres

- `id` : identifiant de l'article à récupérer

#### Requête

```bash
GET|HEAD        api/missions/11
```

#### Réponse

```json
codeHTTP 200 OK
Content-Type: application/json

{
	"id": 11,
	"dateMission": "2023-02-26",
	"startedAt": null,
	"kilometersCounter": 120357,
	"nameExpertFile": "Prof. Belle Johns IV",
	"isFinished": 0,
	"route": "http:\/\/127.0.0.1:8000\/api\/missions\/11",
	"vehicle": {
		"id": 50,
		"licencePlate": "3C63DPML9CG620139",
		"color": "Violet",
		"releaseYear": 2000,
		"route": "http:\/\/127.0.0.1:8000\/api\/vehicles\/50"
	},
	"expert": {
		"id": 7,
		"lastName": "Becker",
		"firstName": "Brennan",
		"email": "bo56@yahoo.com",
		"phoneNumber": "1-215-898-8708",
		"username": "zmccullough",
		"route": "http:\/\/127.0.0.1:8000\/api\/experts\/7"
	},
	"garage": {
		"id": 78,
		"name": "dignissimos et et",
		"addressNumber": "4014 Jaiden Fords",
		"street": "Brian Islands",
		"postalCode": "90149",
		"city": "West Ovafurt",
		"phoneNumber": "(469) 215-1148",
		"latitude": "85.379642",
		"longitude": "-25.654986",
		"url": "http:\/\/127.0.0.1:8000\/api\/garages\/78"
	},
	"unavailability": null,
	"pree": [
		{
			"id": 10,
			"label": "maiores",
			"description": "praesentium nihil ipsum temporibus aut eos porro debitis possimus quod occaecati voluptatibus quis maxime quis illo consequatur laborum sit vero",
			"image": "\/tmp\/0b3f897b3ba12472448167f6f7f09435.png",
			"signature": "\/tmp\/6bed29cd3b1a2f12bf1c46d5ec04e082.png",
			"route": "http:\/\/127.0.0.1:8000\/api\/pree\/10"
		}
	]
}
```

### Modifier un véhicule

##### Route PUT|PATCH méthode `update`

```bash
PUT|PATCH 	api/vehicles/{id}
```

#### Paramètres

- `id` : identifiant de l'article à récupérer

#### Requête

- Header

```bash
PUT|PATCH       api/vehicles/51
```

- Body

```json
{
  "licencePlate": "WA1WYBFE2AD448886",
  "color": "Grey",
  "releaseYear": 2001
}
```

#### Réponse

```json
codeHTTP 200 OK
Content-Type: application/json

{
	"success": "true",
	"message": "Vehicle updated successfully"
}

or

codeHTTP 400 Bad Request
Content-Type: application/json

{
	"success": "false",
	"message": "Failed to updated vehicle"
}
```

### Supprimer un véhicule

##### Route DESTROY méthode `delete`

```bash
DESTROY  	api/vehicles/{id}
```

#### Paramètres

- `id` : identifiant de l'article à récupérer

#### Requête

- Header

```bash
DESTROY        api/vehicles/51
```

#### Réponse

```json
codeHTTP 200 OK
Content-Type: application/json

{
	"success": "true",
	"message": "Vehicle deleted successfully"
}

or

codeHTTP 400 Bad Request
Content-Type: application/json

{
	"success": "false",
	"message": "Failed to delete vehicle"
}

or

codeHTTP 404 Not Found
Content-Type: application/json

{
	"success": "false",
	"message": "Vehicle not found"
}
```

## Exemples de code

### Contrôleur

Voici un exemple de **contrôleur** pour vous aider à démarrer avec l'API en utilisant Laravel 9 :

```php
<?php

namespace App\Http\Controllers\Api;

use App\Http\Resources\Vehicle as ResourcesVehicle;
use App\Http\Controllers\Controller;
use App\Models\Vehicle;
use Illuminate\Http\Request;

class VehicleController extends Controller
{
    /**
     * Display a listing of the resource.
     *
     * @return \Illuminate\Http\Response
     */
    public function index()
    {
        return ResourcesVehicle::collection(Vehicle::with('model', 'missions')->get());
    }

    /**
     * Store a newly created resource in storage.
     *
     * @param  \Illuminate\Http\Request  $request
     * @return \Illuminate\Http\Response
     */
    public function store(Request $request)
    {
        $validatedData = $request->validate([
            'licencePlate' => 'required|string',
            'color' => 'required|string',
            'releaseYear' => 'required|integer',
        ]);

        if (Vehicle::create($validatedData)) {
            return response()->json([
                'success' => 'true',
                'message' => 'Vehicle added successfully',
            ], 201);
        } else {
            return response()->json([
                'success' => 'false',
                'message' => 'Failed to add vehicle',
            ], 400);
        }
    }

    /**
     * Display the specified resource.
     *
     * @param  \App\Models\Vehicle  $vehicle
     * @return \Illuminate\Http\Response
     */
    public function show(Vehicle $vehicle)
    {
        return new ResourcesVehicle($vehicle->load('model', 'missions'));
    }

    /**
     * Update the specified resource in storage.
     *
     * @param  \Illuminate\Http\Request  $request
     * @param  \App\Models\Vehicle  $vehicle
     * @return \Illuminate\Http\Response
     */
    public function update(Request $request, Vehicle $vehicle)
    {
        $request->validate([
            'licencePlate' => 'required|string',
            'color' => 'required|string',
            'releaseYear' => 'required|integer',
        ]);

        if ($vehicle->update($request->all())) {
            return response()->json([
                'success' => 'true',
                'message' => 'Vehicle updated successfully',
            ], 200);
        } else {
            return response()->json([
                'success' => 'false',
                'message' => 'Failed to update vehicle',
            ], 400);
        }
    }

    /**
     * Remove the specified resource from storage.
     *
     * @param  \App\Models\Vehicle  $vehicle
     * @return \Illuminate\Http\Response
     */
    public function destroy(Vehicle $vehicle)
    {
        if (!$vehicle) {
            return response()->json([
                'success' => 'false',
                'message' => 'Vehicle not found',
            ], 404);
        }

        if ($vehicle->delete()) {
            return response()->json([
                'success' => 'true',
                'message' => 'Vehicle deleted successfully',
            ], 200);
        } else {
            return response()->json([
                'success' => 'false',
                'message' => 'Failed to delete vehicle',
            ], 400);
        }
    }
}

```

L'exemple ci-dessus représente le contrôleur pour les véhicules.

Toutes les **méthodes** sont présentes :

- `index`
- `store`
- `show`
- `update`
- `delete`

Ainsi que les codes retours :

###### Succes

- `200 : OK`
- `201 : Created`

###### Errors

- `404: Not Found`
- `400 : Bad Request`

### Ressources

Voici un exemple de **ressource** pour vous aider à démarrer avec l'API en utilisant Laravel 9 :

```php
<?php

namespace App\Http\Resources;

use Illuminate\Http\Resources\Json\JsonResource;

class Vehicle extends JsonResource
{
    /**
     * Transform the resource into an array.
     *
     * @param  \Illuminate\Http\Request  $request
     * @return array|\Illuminate\Contracts\Support\Arrayable|\JsonSerializable
     */
    public function toArray($request)
    {
        return [
            'id' => $this->id,
            'licencePlate' => $this->licencePlate,
            'color' => $this->color,
            'releaseYear' => $this->releaseYear,
            'route' => route('vehicles.index') . "/" . $this->id,
            'missions' => Mission::collection($this->whenLoaded('missions')),
        ];
    }
}

```

Dans cet exemple on renseigne les données que notre API va nous retourner ainsi que toutes les relations existantes.
