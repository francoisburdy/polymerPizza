##### 1 -- myview1.html : commenter ça 

 <!--     
 	<div class="card">
      <div class="circle">1</div>
      <h1>View One</h1>
      <p>Ut labores minimum atomorum pro. Laudem tibique ut has.
      <p>Lorem ipsum dolor sit amet, per in nusquam nominavi periculis, sit elit oportere ea.Lorem ipsum dolor sit amet, per in nusquam nominavi periculis, sit elit oportere ea.Cu mei vide viris gloriatur, at populo eripuit sit.</p>
    </div> 
   -->

##### 2 -- myview1.html : Ajouter une paper-card dans un <div class="card">

	bower install --save PolymerElements/paper-input

#### 3 -- myview1.html : Ajouter un <link/>

	<link rel="import" href="../bower_components/paper-input/paper-input.html">

#### 4

	bower install --save GoogleWebComponents/google-map

#### 5  -- myview1.html : Ajouter :

 	<google-map-search map="[[map]]" query="{{recherche}}" results="{{results}}"></google-map-search>

    <google-map map="{{map}}" latitude="45.18" longitude="5.73" api-key="AIzaSyCMwoD7JpzLCf5VRKm1J9u8EPXAnTsLEg0">
      	<template is="dom-repeat" items="{{results}}" as="marker">
        	<google-map-marker latitude="{{marker.latitude}}" longitude="{{marker.longitude}}">{{marker.name}}</google-map-marker>
    	</template>
	</google-map> 


##### 6 --- 

	google-map {
		height: 200px;
	}

##### 7 --- 

	<template is="dom-repeat" items="{{results}}" as="result">
        <div class="card" style="max-width:300px; display: inline-block">
          {{result.name}}<br />
          {{result.formatted_address}}
        </div>
    </template>
