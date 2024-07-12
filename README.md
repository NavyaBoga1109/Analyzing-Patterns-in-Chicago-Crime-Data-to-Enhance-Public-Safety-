# Crime Patterns Analysis in Chicago

This project focuses on analyzing crime patterns in Chicago using machine learning models and statistical techniques. Here’s an overview of what was implemented in Python:
[Uploading Ch<!DOCTYPE html>
<html>
<head>
    
    <meta http-equiv="content-type" content="text/html; charset=UTF-8" />
    
        <script>
            L_NO_TOUCH = false;
            L_DISABLE_3D = false;
        </script>
    
    <style>html, body {width: 100%;height: 100%;margin: 0;padding: 0;}</style>
    <style>#map {position:absolute;top:0;bottom:0;right:0;left:0;}</style>
    <script src="https://cdn.jsdelivr.net/npm/leaflet@1.9.3/dist/leaflet.js"></script>
    <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.js"></script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/leaflet@1.9.3/dist/leaflet.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css"/>
    <link rel="stylesheet" href="https://netdna.bootstrapcdn.com/bootstrap/3.0.0/css/bootstrap.min.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.2.0/css/all.min.css"/>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/python-visualization/folium/folium/templates/leaflet.awesome.rotate.min.css"/>
    
            <meta name="viewport" content="width=device-width,
                initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
            <style>
                #map_f31ce70f357afcff6520e0ee17497e19 {
                    position: relative;
                    width: 100.0%;
                    height: 100.0%;
                    left: 0.0%;
                    top: 0.0%;
                }
                .leaflet-container { font-size: 1rem; }
            </style>
        
</head>
<body>
    
    
            <div class="folium-map" id="map_f31ce70f357afcff6520e0ee17497e19" ></div>
        
</body>
<script>
    
    
            var map_f31ce70f357afcff6520e0ee17497e19 = L.map(
                "map_f31ce70f357afcff6520e0ee17497e19",
                {
                    center: [41.8781, -87.6298],
                    crs: L.CRS.EPSG3857,
                    zoom: 11,
                    zoomControl: true,
                    preferCanvas: false,
                }
            );

            

        
    
            var tile_layer_c985bafd7d9fa2f8e6e3c24062d4d036 = L.tileLayer(
                "https://tile.openstreetmap.org/{z}/{x}/{y}.png",
                {"attribution": "\u0026copy; \u003ca href=\"https://www.openstreetmap.org/copyright\"\u003eOpenStreetMap\u003c/a\u003e contributors", "detectRetina": false, "maxNativeZoom": 19, "maxZoom": 19, "minZoom": 0, "noWrap": false, "opacity": 1, "subdomains": "abc", "tms": false}
            );
        
    
            tile_layer_c985bafd7d9fa2f8e6e3c24062d4d036.addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_446f8317ca2722e5c169a85f4dd07c13 = L.circleMarker(
                [41.741047754, -87.64007146],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_773b11611990dbb4bf0a4e4312c7a45e = L.circleMarker(
                [41.770162902, -87.626696779],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ac0475ee70cbddb5818daa9ecab8f0de = L.circleMarker(
                [41.755929033, -87.657389725],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d30b30a0bb8711e49c0d289799cc7edf = L.circleMarker(
                [41.985587556, -87.694380844],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ede7530f022cd6e99cde296aa931fe80 = L.circleMarker(
                [41.994345158, -87.802247128],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b95649dcc46a48b6458ec8e7c46a1952 = L.circleMarker(
                [41.716736461, -87.6479477],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_231d0a5029abd7815492474486fee401 = L.circleMarker(
                [41.803967555, -87.743506114],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_78a93e501aaa0c432b9cdffa76d1d70d = L.circleMarker(
                [41.793935909, -87.625680278],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_86f82bb01541bd3ed4f22da35c9cb1ee = L.circleMarker(
                [41.879256403, -87.630816943],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_73e201ca0fc9cb1d189f91e0991a9dd3 = L.circleMarker(
                [41.712770582, -87.562158108],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_44d7520baba93cf2ee801e5bfe3087f3 = L.circleMarker(
                [41.936965953, -87.79565942],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_aabddc941781de10ec91caa22da0ded3 = L.circleMarker(
                [41.703230009, -87.628173505],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e8e1a01d91ffa36a868a6ec53a91fc4b = L.circleMarker(
                [41.769065813, -87.610040671],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d14c68a507f111c9dbe30c5061b96f76 = L.circleMarker(
                [41.964707715, -87.70747722],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dd6024a287753e3a2a5b2d5188d0e6e1 = L.circleMarker(
                [41.998692163, -87.683816395],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_31d5a176e09cb49a86686cc8140a0533 = L.circleMarker(
                [41.887472275, -87.646173514],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d57a809c698c80e93299a9fd5fc9b887 = L.circleMarker(
                [41.798758937, -87.66957783],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3985d86b26a3f246459201a430e9a357 = L.circleMarker(
                [41.767757885, -87.656613078],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0dde06605a88d9835c0b93835f282cda = L.circleMarker(
                [41.91401764, -87.685906425],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_88f1ea396cc63fce16b3fdb95ef8272a = L.circleMarker(
                [41.912195867, -87.763099498],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b20fd59d8d122c396d570fe36f344c63 = L.circleMarker(
                [41.975559264, -87.654987667],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2e9c1ffb1858df6bc00b54c003a9333e = L.circleMarker(
                [41.803117224, -87.609654164],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_79da55c76d9123cdc573cfcf69014e74 = L.circleMarker(
                [42.016974195, -87.690199116],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f84c736aa96fbb0971f38d71a4c87449 = L.circleMarker(
                [41.910536878, -87.67414124],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_32dbc9ef6e0a11440c515fff28e2eba3 = L.circleMarker(
                [41.875894272, -87.709636977],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2f756086f4541097e0ba97de7a30b0f3 = L.circleMarker(
                [41.820367967, -87.686028851],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d1cf497a60725d649e9f1adac2c629da = L.circleMarker(
                [41.886146944, -87.624524028],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_75f3451ee8719e7716a12c51709a8d21 = L.circleMarker(
                [41.784902127, -87.612066361],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e69d05722a840b8dc471e5876cc3b65f = L.circleMarker(
                [41.957082985, -87.665360216],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_42864ad844e5c33fdeff3f2c0484e029 = L.circleMarker(
                [41.721439376, -87.614131833],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e2811a7e2f916c6eb9c52a98e9d104d2 = L.circleMarker(
                [41.84994342, -87.705895766],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_23d3a29d47720e6387898cf6858e5bfc = L.circleMarker(
                [41.968374092, -87.716115753],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9da1ae042494e0d335b4a4219ccbea3c = L.circleMarker(
                [41.917396919, -87.707392238],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3024cb112276549a960c5bb7b4adc348 = L.circleMarker(
                [41.750111323, -87.644030737],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_916e24f4705bc33c3929b7a75e7d4a02 = L.circleMarker(
                [41.872870422, -87.697186337],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fdb9114d0ea49fe6ae6e1e93e68883ed = L.circleMarker(
                [41.678612378, -87.540042376],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_39b4140028c16b76b29787263caf1f2e = L.circleMarker(
                [41.924715306, -87.70730601],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_00bf11298eeb928ea1d4700eb22ef040 = L.circleMarker(
                [41.881703396, -87.626203588],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_849a987c253c6d6f6f5e19ea0032d682 = L.circleMarker(
                [41.925915612, -87.687678623],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c9b8e0185c9217ef6613b3d85d30348e = L.circleMarker(
                [41.906087304, -87.675851147],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ffddf8e31ecbbae5e6b70f6e5e4269c6 = L.circleMarker(
                [41.729428428, -87.563365687],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2e355f39b9a2667de2a3bb0a51830a7b = L.circleMarker(
                [41.815744377, -87.599390896],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c5461297bf6d90e3f499e3b0629932e1 = L.circleMarker(
                [41.691413679, -87.668826246],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_16318cbc528a190ab2268dc61651f8b2 = L.circleMarker(
                [42.016461083, -87.690207966],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d4388e731747ade218aa3e811dfe491c = L.circleMarker(
                [41.772520766, -87.614833569],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e4266759cf51e494ac217f6d67da613a = L.circleMarker(
                [41.939898633, -87.754281422],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_049da509556738f076df04b629f54512 = L.circleMarker(
                [41.662344932, -87.638998635],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_91180aec080391acc80df3bc20dab3e0 = L.circleMarker(
                [41.908541875, -87.650205438],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8597a4898d468080cf612fcc1014bd4a = L.circleMarker(
                [41.720661741, -87.634880377],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_904fdc6405d2be8eb4885eba506bac6a = L.circleMarker(
                [41.890174212, -87.72945171],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e48ae76aae59f7f7687abe3ff0d15a68 = L.circleMarker(
                [41.998432855, -87.685033065],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7c47539f2a04305e5ae2263d5333f75c = L.circleMarker(
                [41.946858933, -87.678854658],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_90533e22fad924bec0d19ed56673ee7b = L.circleMarker(
                [41.809305232, -87.606558389],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_597b9ccba71f1baf5237df7c1972696f = L.circleMarker(
                [41.862419531, -87.713607897],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ca622fca1d786ad00811e0c2b4561126 = L.circleMarker(
                [41.909934052, -87.72192157],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_58ae13be38003c5dfe632e730a463d14 = L.circleMarker(
                [41.912619862, -87.708519057],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_70bb8754f30df736c34865c51b84f139 = L.circleMarker(
                [41.882889721, -87.774747822],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7e3cfeb299ece297e1594980ffea1b78 = L.circleMarker(
                [41.862842099, -87.702010464],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_963e8bab92aeb0c5f389980de9451c10 = L.circleMarker(
                [41.9389404, -87.764059494],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_097a85431dffbe8bf5119435d59379ae = L.circleMarker(
                [41.748853608, -87.577150669],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5ad937031a74572fe8cbe68b2be3f9ea = L.circleMarker(
                [41.801482671, -87.652931837],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f4faf887c5498c40f4b1a900453eeb3b = L.circleMarker(
                [41.980342364, -87.763510658],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dcfce9ff6183af0a066338a3a51d2b2a = L.circleMarker(
                [41.954499279, -87.716609926],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5a228df2d6811c68bc347fc6b9ef812f = L.circleMarker(
                [41.910390576, -87.682651328],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_81b8b7a2e0c79d38ed41dee02944745d = L.circleMarker(
                [41.800763793, -87.70800049],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f524b31c2e2e89ab2936142e9da3cf05 = L.circleMarker(
                [41.738810808, -87.663142255],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_af3cb1f690775e2a41bb9a22b6d66610 = L.circleMarker(
                [41.784205909, -87.658262453],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2686d6b8d6ca8ec998d0c34f9c08c028 = L.circleMarker(
                [41.776322631, -87.605838376],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3d2fb064228fdfcc5c8cc3a3bcca0181 = L.circleMarker(
                [41.896682402, -87.764703071],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e115ed9cf8f6003ab96078624eecf8ec = L.circleMarker(
                [41.880455266, -87.728111102],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_eb8f3f086b5866cc2fc7099816a9d766 = L.circleMarker(
                [41.708232864, -87.665371655],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_276598ce57303612815bf8464cac2774 = L.circleMarker(
                [41.880745357, -87.724326068],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7a55e7c09a49967ce6b0a6227f0302b9 = L.circleMarker(
                [41.982586227, -87.666539157],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b4b2f0e6b50054ebd3213ff6e7fe64e0 = L.circleMarker(
                [41.89652481, -87.639211587],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_138f22d85008ec3ad1745ff12c377904 = L.circleMarker(
                [41.877822179, -87.655181405],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_04cc8f8b8fd40258a068acaa80f22a97 = L.circleMarker(
                [41.817773913, -87.631243518],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_de8e71544e8738b9255c4110ab9ca14d = L.circleMarker(
                [41.942723124, -87.648230744],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6ba14b0f8148c29b555cdcf1e313b801 = L.circleMarker(
                [41.897895128, -87.624096605],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8038c95d94a52f93c8fbebc350f137ae = L.circleMarker(
                [41.698699238, -87.560751697],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_975dcabaf2bd7b59edac88dd8e68bae7 = L.circleMarker(
                [41.750059737, -87.702402145],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_57f2c4c6d2c1a04b3aaa10f09069cc16 = L.circleMarker(
                [41.751270583, -87.605938082],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_514ed42af4f7cbe8fe1f97c05dba09bc = L.circleMarker(
                [41.908115186, -87.765869051],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5b909efc37160f9b778657305d944794 = L.circleMarker(
                [41.883500187, -87.627876698],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_45e833f0b2472f7c02ec0110fa34bc56 = L.circleMarker(
                [41.89823584, -87.660184984],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5ce4d90c6b57e5faaa153c20d0c561ec = L.circleMarker(
                [41.800729285, -87.667199258],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a89c6d672b578d9bca5b9832568a9d68 = L.circleMarker(
                [41.747771547, -87.556462439],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9ca496a74df6ee6134b9309e7638a2b4 = L.circleMarker(
                [41.685827243, -87.709147665],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e329686ea4fcbb100743820abd33ed73 = L.circleMarker(
                [41.900489748, -87.638224621],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1e6e22f8e4223f0a87b73ee6b8f9dee7 = L.circleMarker(
                [41.900190488, -87.628299103],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_53c76a4af042110eaa52a87509b9cee9 = L.circleMarker(
                [41.89628926, -87.728575022],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0f5cf75fd05e08a4f365fe9a6c649627 = L.circleMarker(
                [41.685744218, -87.66039469],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_64b5dc97f3e0201c0b5d7554c87f0db3 = L.circleMarker(
                [41.78386859, -87.644890262],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_25fa30c76e3f2cf699458f83763eb296 = L.circleMarker(
                [41.755289122, -87.556195869],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_48e54db5f40dcdc29c27606640f8e157 = L.circleMarker(
                [41.736259984, -87.628068782],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_38107ca37a95c87beeca739a85bfbde6 = L.circleMarker(
                [41.944793552, -87.659111],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_571ced11b01c8b069b78df26c6ca25f5 = L.circleMarker(
                [41.878300494, -87.676569346],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c820554e94c2a40c0971ab074cf5027b = L.circleMarker(
                [41.886017951, -87.624521781],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1d0c4976347d3beac2008a42c0662ab3 = L.circleMarker(
                [41.809759536, -87.661343173],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_13b73b59ead47efa5a9d5da704fd80ef = L.circleMarker(
                [41.900489748, -87.638224621],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ca832dc908875a9418c3db6688e183d9 = L.circleMarker(
                [41.679951972, -87.682012834],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3462feecb19d92e3f6916d6cb3e481e1 = L.circleMarker(
                [41.990339344, -87.656820786],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4fa7d403533963b5304f736ac5cad1de = L.circleMarker(
                [41.81061163, -87.616623598],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a61f341abf2e3d99c0e922744e8a2bb6 = L.circleMarker(
                [41.905530384, -87.710333124],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_415c8ebb974806f92cfd65c9e26c65b6 = L.circleMarker(
                [41.811731885, -87.671131278],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ba97c5769a7e0115e36b2e7ef7ea0135 = L.circleMarker(
                [41.972221847, -87.656302808],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9de1d0d4cf6b8b6b5da021a1625adf99 = L.circleMarker(
                [41.957415629, -87.75169636],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e235d34e1c6d8f0d6548e7712456637d = L.circleMarker(
                [42.010302869, -87.66848694],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_02614c03f5b6bbe35073f12f210de3cc = L.circleMarker(
                [41.841719488, -87.711055255],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e1daf057aeb0469ee021fc7c8789eefd = L.circleMarker(
                [41.902299811, -87.634421428],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_84bafe57f8fe4a40a9733d7f717c41ff = L.circleMarker(
                [41.895920184, -87.723649336],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_78fb595c08400f994d13400cd1fe50df = L.circleMarker(
                [41.890761164, -87.714953686],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c61b06b574ad66bca67fc5ed52ddbf17 = L.circleMarker(
                [41.938797346, -87.723377074],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e01afdc1cd1a50bdc79a500cfc159519 = L.circleMarker(
                [41.782364078, -87.594000617],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3f2953385d7c159306b1ff61bf74baa2 = L.circleMarker(
                [41.863690977, -87.721444549],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_888516a47c0352fc4d51e364ad9c531d = L.circleMarker(
                [41.691178831, -87.662414022],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3d82cd6f1e7edfd39c8a21e7298f6276 = L.circleMarker(
                [41.807680682, -87.671018947],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e51fc577dbd756d80b38127a573763cc = L.circleMarker(
                [41.881493402, -87.627755557],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3c3811e0525aad86875015fbd2630639 = L.circleMarker(
                [41.679828274, -87.624471853],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_14dff750002e30df6c6039dca13daf8a = L.circleMarker(
                [41.876502584, -87.629253507],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_865737dab4724163060ce5b422e4313f = L.circleMarker(
                [41.765965607, -87.589966186],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5d492f37433f629f48be152156ee9c31 = L.circleMarker(
                [41.87692822, -87.738484491],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4c623e805b31377c929a769a03e8a396 = L.circleMarker(
                [41.690992372, -87.538898073],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7c36febcdd9056b866054f35f778412c = L.circleMarker(
                [41.910063395, -87.785032787],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c05b443ce0d25e93bd828dddac6d3964 = L.circleMarker(
                [41.867786016, -87.660236513],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8f958535db27a05d233593691491ed17 = L.circleMarker(
                [41.90274766, -87.717442476],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_019e03fa1ce04baedfe06da4569639fb = L.circleMarker(
                [41.953900467, -87.907472601],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8baf11d2cbc340a5f799c6d7228682f5 = L.circleMarker(
                [41.733141, -87.667854106],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fc1b1f283d9810503b3c7dabc70d4b81 = L.circleMarker(
                [41.878365364, -87.694392535],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1802c94fe5602b1af8de2c481ca118c5 = L.circleMarker(
                [41.754473622, -87.562648619],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0a427b63e1614d5eda7e9c072d9d8019 = L.circleMarker(
                [41.796882513, -87.693885964],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7ec4ecd8879fbb0939dfae87bd8c00b3 = L.circleMarker(
                [41.939110037, -87.647486544],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fe003da2f59869585f7e50f8a3bec828 = L.circleMarker(
                [41.86559259, -87.676214817],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cc759a24afab914e8a3bcb0ceb74a54b = L.circleMarker(
                [41.795526092, -87.589815387],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5f38189c610925a66d40b08b8170ff94 = L.circleMarker(
                [41.928159105, -87.726175766],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_789a6e2d96416ba30ac84e4a12c4ba40 = L.circleMarker(
                [41.830020767, -87.638782055],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_96c36bbac453a8e0023462edc123900d = L.circleMarker(
                [41.781589382, -87.607212431],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3c7d33d21ab50723a6ace170d3d02708 = L.circleMarker(
                [41.808052976, -87.674675749],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4980e1f8d2990d7b7e741cc634b815e3 = L.circleMarker(
                [41.858941802, -87.71806122],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5aa54a0473eebf7ad356d14fc64d4370 = L.circleMarker(
                [41.680760376, -87.621650183],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c9df271aa80dbede5d643a6657202f42 = L.circleMarker(
                [41.903394595, -87.663400148],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2c84a39f71f40717d8602b816bfade12 = L.circleMarker(
                [41.75091483, -87.597905386],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_79b0ed8469cf19c11adf66ee31c1f58c = L.circleMarker(
                [41.781203659, -87.763073623],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d6a0d68cc62ce1da24ca1dc215abf695 = L.circleMarker(
                [41.704639865, -87.622265806],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cf9279d4674574fe3e60eba761466872 = L.circleMarker(
                [41.94672955, -87.689949888],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_33093ad51db4bf214e8991e31d67ab22 = L.circleMarker(
                [41.876559722, -87.626047325],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_04f976648564a8a44d250a674489825b = L.circleMarker(
                [41.909307068, -87.80576669],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4a6b997f5b037c2ceedc71c37d522cdd = L.circleMarker(
                [41.924491602, -87.725945966],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b2bce2bd55fd21b9ef1d786618e09462 = L.circleMarker(
                [41.844427676, -87.71148777],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d5d4b4e0a9ac48d96d5bbcd533181413 = L.circleMarker(
                [41.840106225, -87.724436322],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b9fa4988fdf55d44ff3970bad33131c0 = L.circleMarker(
                [41.883603086, -87.707659762],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_23d42a12d880dc79921bc7e2d99953f0 = L.circleMarker(
                [41.899831808, -87.71767987],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2b9bcb01fb417da3466211ceab63a927 = L.circleMarker(
                [41.909614875, -87.747016581],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_103cee2134dbbdf95ba2d6d1de2ab9ac = L.circleMarker(
                [41.808682769, -87.630898966],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3e4335e9ebb9cdca7d1223092308933f = L.circleMarker(
                [41.726182521, -87.570038686],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_91c021cbc2f8cbfb8b832ed54c965270 = L.circleMarker(
                [41.744564399, -87.55822701],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e0e90abf219f27539e0304b74ce8905f = L.circleMarker(
                [41.982951947, -87.717769841],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c6108787f6e115b326e2058958c0d401 = L.circleMarker(
                [41.849333018, -87.705178675],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ef2b8b266d210d41854df0ebbaf738a7 = L.circleMarker(
                [41.881770086, -87.748835561],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2f52a51b73cb99def567b565df4d05b8 = L.circleMarker(
                [41.932862434, -87.641702699],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4b3bc8e3b24bb0e7fb8974778270154b = L.circleMarker(
                [41.777972797, -87.742277863],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_be817b70736cd0d84dfa2077595ab903 = L.circleMarker(
                [41.813558308, -87.669960623],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_66de6f1e72e58394b59f1bdcd88e975b = L.circleMarker(
                [41.707455731, -87.605637491],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6aa008fdada5175365f3031d751fa118 = L.circleMarker(
                [41.790894568, -87.741528449],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0e29d58a84cb5ed64a12705a5f72853b = L.circleMarker(
                [41.777161615, -87.702246564],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f469ef6ad9939a6950371c293605da9e = L.circleMarker(
                [41.921292958, -87.726678123],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_07e9ae0ae0ddb2d18d6e16a0c469ac3d = L.circleMarker(
                [41.858070537, -87.722437864],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ec8d3fc8b8ca3c917d6ff9ea4574fb6c = L.circleMarker(
                [41.905040349, -87.733752929],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_26460f56f5d092021cf93a716f29d5f1 = L.circleMarker(
                [41.861333512, -87.663861403],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e54c1058b04ad76741659b33c4094eed = L.circleMarker(
                [41.943558167, -87.732146111],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a7857d29aa102bff4c01bb7d5dc71afb = L.circleMarker(
                [41.750302426, -87.667596262],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4c764758a1bef7624427e7be2c71e52c = L.circleMarker(
                [41.684421845, -87.628862153],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_33f4b44febc03f0bef5ba489796692f9 = L.circleMarker(
                [41.978495324, -87.689251423],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_05bae23c785f68828438e072966e5d06 = L.circleMarker(
                [41.870146749, -87.738932878],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_54e366ae11089478a1e641e4b5b1a1dd = L.circleMarker(
                [41.723589559, -87.621848112],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_630d1fbdc2ddec33ab1bc0063527c199 = L.circleMarker(
                [41.895922652, -87.638564315],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_83bbd39b5d3750d7c22be5d0d998b034 = L.circleMarker(
                [41.743079967, -87.613087912],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cdd9483d891bade1c5a442409a7039ec = L.circleMarker(
                [41.785709457, -87.722952947],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_573e0420bf190f4826e6df11d760c31e = L.circleMarker(
                [41.982423673, -87.656580926],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_11b65dadaee2d5aeb7e1752812c096bf = L.circleMarker(
                [41.73365047, -87.557845321],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b9056df2a16c65fa64c9b30fc5bda98f = L.circleMarker(
                [41.734366796, -87.597496998],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4559cce6626c141e9ecbd412cfab67d7 = L.circleMarker(
                [41.678453665, -87.640725361],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_93d64241590ebd907c7389a48f8cab05 = L.circleMarker(
                [41.798524746, -87.700038258],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b3ca593e7d43827337732a2b4f85f44a = L.circleMarker(
                [41.782339331, -87.652140635],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e93212c71ae64fff775d29c205f923d2 = L.circleMarker(
                [41.750794483, -87.633560686],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_79137797b38992f30eca765a231ab068 = L.circleMarker(
                [41.931832031, -87.723803596],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e4dcb293f4e9c550d32dad9f3826ad73 = L.circleMarker(
                [41.796437881, -87.693875715],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7893184fc719e31fffe61b52760bd49e = L.circleMarker(
                [41.787594577, -87.688749402],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cc7d4bb93fe5d3a4cec40f6bfb95ce88 = L.circleMarker(
                [41.738280662, -87.551447254],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9087a50e27ca61eaa241981b89bac953 = L.circleMarker(
                [41.812455606, -87.619680678],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_da7aa2c86bd7bf460aa208ee15c1e613 = L.circleMarker(
                [41.856326285, -87.631849815],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dd05fadaa95bff3eb5bc0edc05ec2c3c = L.circleMarker(
                [41.857890719, -87.660318264],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_502e8528ad4b0bfae5ded13788801901 = L.circleMarker(
                [41.844000177, -87.628442902],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_858d04953011e445069152c343adda3d = L.circleMarker(
                [41.875256983, -87.726423378],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4dd2b5d6e78a94617ba943ad9eae3037 = L.circleMarker(
                [41.890123156, -87.644789891],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0c0c1842f2da0b498148e32d0a56d913 = L.circleMarker(
                [41.750390067, -87.599098732],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6acded9527443af77498824fe10f620c = L.circleMarker(
                [41.857709786, -87.672162191],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_49997a6721506e68dfed12f4c48f9f01 = L.circleMarker(
                [41.824654911, -87.632324055],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d80a02a5bd055f07f2961ce4149ac63f = L.circleMarker(
                [41.924158759, -87.699399996],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c0fd8ce62124e2f89b1223f6850726a8 = L.circleMarker(
                [41.882825154, -87.76162742],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e4027a14e4b86ccb66b2e17d166c6549 = L.circleMarker(
                [41.795781229, -87.633034857],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5a53edb6c721ec761a7730016095990f = L.circleMarker(
                [41.996550675, -87.725209743],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d16673cbcb702a4e9ac6cac78daa58c3 = L.circleMarker(
                [41.815270245, -87.665141042],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8a2141b8155e1d3a575c1725fda2e2d2 = L.circleMarker(
                [41.979691348, -87.804674901],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2c6b70a4ad45b31623e28240df731b29 = L.circleMarker(
                [41.965457044, -87.652995284],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bcd414d2e6c41dd226d06befd4d1870f = L.circleMarker(
                [41.658871865, -87.559288387],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e455489df0788a9108686a6a50830ca2 = L.circleMarker(
                [41.737639763, -87.601207865],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_69fc68be661ca7b64e142144e5c2fdd8 = L.circleMarker(
                [41.970693122, -87.720759852],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b1a5305e2e479757432775b89c540791 = L.circleMarker(
                [41.745782809, -87.721960773],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fa242703bedea227e8820efd04453cdf = L.circleMarker(
                [41.771126721, -87.670060732],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_061dbe481e0ae6d8716677b8d520d57a = L.circleMarker(
                [41.725269859, -87.592442947],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e2935ff41221fe4c0a62bc4bf119d229 = L.circleMarker(
                [41.936893284, -87.755286254],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_aa1a913143a14d091c1ebe0750691dcd = L.circleMarker(
                [41.880685678, -87.729133452],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6cb3660fb43edf8aed0d734f1584594e = L.circleMarker(
                [41.877887422, -87.76477792],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fcc04a27ebc5f0c1fa9b7cfc71c3c58d = L.circleMarker(
                [41.882889456, -87.771879791],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5d2cad518bf04fcde800cacd7ae72dd9 = L.circleMarker(
                [41.933174769, -87.689266577],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_01f3f3703d8964350f6f35a1e2746ac7 = L.circleMarker(
                [41.89576841, -87.685407597],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ab7be95f4c6262b640ea172034713653 = L.circleMarker(
                [41.737094305, -87.572998178],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_803e37968fcbe2e54d436e0206a2ea7b = L.circleMarker(
                [41.880257857, -87.764103272],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b9654376299a77ca8d84f17cdc73b6e7 = L.circleMarker(
                [41.707253591, -87.586112758],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_41a3d7fdfc4d89176dd45361dc3937dd = L.circleMarker(
                [41.693112325, -87.683688835],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_05883150372b61747bc4acf1cb8b5523 = L.circleMarker(
                [41.702684248, -87.525274478],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_15e3f442abd5f81c531998b0ec932d3b = L.circleMarker(
                [41.826667972, -87.681995495],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a8be6bb51754df8df6a9f2b95aaa4831 = L.circleMarker(
                [41.88468277, -87.66689711],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_64b492fd8ab0aa80214f25887c4fa21a = L.circleMarker(
                [41.949500059, -87.721363493],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a46f1347985617935620fdbfe7a74e31 = L.circleMarker(
                [41.908744215, -87.72162433],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0a3a105cb8c7bde4f6709668ca7a27ed = L.circleMarker(
                [41.866290829, -87.6959042],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fc43e2f34c5c5c27ec86e5d613c22d3a = L.circleMarker(
                [41.826908418, -87.660859334],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_14782e1abcdefbc1f8dc65403d74dc48 = L.circleMarker(
                [41.868180939, -87.709271389],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6ea5fa094f9c2513665d56d370d6c602 = L.circleMarker(
                [41.879494129, -87.745955373],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3444bc534067a8f93c8061b677956b1e = L.circleMarker(
                [41.891133566, -87.624134682],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5524915fbd7835104a4b71f1cdbdd22e = L.circleMarker(
                [41.838239606, -87.61553376],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0c853ba8e5312f20ea874f8e44e2e0e6 = L.circleMarker(
                [41.758617623, -87.55736521],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a4a0eef8ae36cd9ef4b762defbcd231e = L.circleMarker(
                [41.760088836, -87.566396938],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_051669bbe36b55a78b4674dbcfc0dc06 = L.circleMarker(
                [41.912149595, -87.736181],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_02dcd2f522da4889a381e90102feb095 = L.circleMarker(
                [41.861359279, -87.694400341],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_65696cac785f6039169b7cd8a27ee1a1 = L.circleMarker(
                [41.734155961, -87.650012089],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_beddd192b535e9de37f1d373b902c860 = L.circleMarker(
                [41.891694878, -87.626155832],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d9f2018941fb41ac3d33225f06e50670 = L.circleMarker(
                [41.873699424, -87.704705156],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a9a1b9e1ea0629e6d2029d7a1f5969f8 = L.circleMarker(
                [41.77466492, -87.699367511],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b4f7758fc9248404aeecb40697847114 = L.circleMarker(
                [41.729843669, -87.662891098],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_40bcadc10e740c2348ebf3096011778c = L.circleMarker(
                [41.677799762, -87.642881123],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_357d5b3ac92879d2b471996eae3e4591 = L.circleMarker(
                [41.948631264, -87.682641213],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a0465e89b6e5d1264b5e03275245d85e = L.circleMarker(
                [41.796769983, -87.693883415],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5d4516a23781ee76ef2528069623a667 = L.circleMarker(
                [41.919743331, -87.731535617],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a0b1ed3ac45e4955067597e9189d9079 = L.circleMarker(
                [41.97198692, -87.659750985],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6c46382a42c47ee31fafdf6f5b54a639 = L.circleMarker(
                [41.885533988, -87.666983746],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c5c73b52a13449caf4336fe4c66a9911 = L.circleMarker(
                [41.756567668, -87.563898997],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4d1c62c0791677ee2895d03b5d0db4cc = L.circleMarker(
                [42.022526205, -87.672418956],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_163e5851937257895ee73cb9e18b438f = L.circleMarker(
                [41.706326697, -87.656188319],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_db8ac8e506ef6431fc03e90eea8cedbd = L.circleMarker(
                [41.998357581, -87.704553989],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dd590175978f2c3b5243ee230d455bee = L.circleMarker(
                [41.96026148, -87.783459205],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ea75800250005a2223c28cb26932bfe3 = L.circleMarker(
                [41.777552109, -87.789334272],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5ef4c67525b1fe3900d6908b63fe8e3a = L.circleMarker(
                [41.939367879, -87.702005997],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2109eaf126566a7dbba217d4d33ad26b = L.circleMarker(
                [42.017163906, -87.677652195],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_383945a884c6ea368dc839e38d155ac7 = L.circleMarker(
                [41.807002259, -87.72967957],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a98b51efaa40f9c201550d0f1dbc0df4 = L.circleMarker(
                [41.69156135, -87.701330173],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_740edb33494041ccbb004366919b93b9 = L.circleMarker(
                [41.881183782, -87.76322108],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2fc6dacd429053a064fb4515b41e4d0d = L.circleMarker(
                [41.788459267, -87.673325275],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5dcce1e08c4672acbe22ae27d8708dc7 = L.circleMarker(
                [41.869302512, -87.689239927],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6b7e01d80fbbf9767f98ceb6d0d51181 = L.circleMarker(
                [41.943196934, -87.680086716],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ef79ff07a2761447858ad30a8b6021b0 = L.circleMarker(
                [41.937857215, -87.669651615],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_31fa5aa94f42b36437417e6a1019b326 = L.circleMarker(
                [41.803671998, -87.703846021],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7eb06cde679b2407844a7776c82b04e4 = L.circleMarker(
                [41.974184283, -87.657756697],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0c043a3691033d8b03cc6cdf7c871b04 = L.circleMarker(
                [41.902709024, -87.775386931],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7d358876895b7a16173b91b5aa143408 = L.circleMarker(
                [41.893391805, -87.62098778],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3515c8da33827bb4546a13aaf704b38d = L.circleMarker(
                [41.764200183, -87.715353049],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f62fc27061944e5e6d8b5f79008101e2 = L.circleMarker(
                [41.770469009, -87.637280329],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3673516b383c2f5b015db93051210f95 = L.circleMarker(
                [41.982161273, -87.668500261],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dc0f8081131133a8d7165cb14814a56d = L.circleMarker(
                [41.882755842, -87.630903466],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d05665b07de7fa0f222ada129db8802d = L.circleMarker(
                [41.878370307, -87.707248137],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f15b0d0fa1b7e0fc5f64487a157c981c = L.circleMarker(
                [41.823320055, -87.623203203],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b8920f749406d44d42e5475133e39537 = L.circleMarker(
                [41.907153315, -87.639680572],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8f4b04ffb6bc1bae84f9c874d011b3d1 = L.circleMarker(
                [41.83055261, -87.661294527],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f66c24abed0384f330c383109032a6c3 = L.circleMarker(
                [41.925074833, -87.673973233],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_653a968502cd464b1daa8c5f1f83b683 = L.circleMarker(
                [41.853633845, -87.734570978],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0942534bb86d44c2b72ef93bb2a44ccb = L.circleMarker(
                [41.89786794, -87.671009825],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ab192e8aeee86e9a90cf4179c7cb8274 = L.circleMarker(
                [41.972177117, -87.650603352],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e8c6e34c665c56228b79a4c0343a9f84 = L.circleMarker(
                [41.778047465, -87.586387726],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_51164d5a6239eac9dec2e2867ada4ad8 = L.circleMarker(
                [41.782153386, -87.703227906],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5694d925c4081b9891ee4bbc3347e40b = L.circleMarker(
                [41.897231388, -87.75320881],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a571c421ee896b67f691b0f5ba8a1e59 = L.circleMarker(
                [41.97793325, -87.77813266],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_161e8c7760270f3b781e307834472435 = L.circleMarker(
                [41.800544961, -87.664758583],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d58969dcec5898b3b03f32b501bcdc2a = L.circleMarker(
                [41.8764809, -87.705992434],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e33eeac89e1b5b1c16567235e716128a = L.circleMarker(
                [41.935393468, -87.65240711],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a1fe98f884322b7cc46e613c6dae6c20 = L.circleMarker(
                [41.697625726, -87.613507428],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d89d3a77f8611ba5cf57730238ebca57 = L.circleMarker(
                [41.989414038, -87.810060529],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dcb9544a8bf748c6506fddd59799086c = L.circleMarker(
                [41.797949772, -87.619306201],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3c809495c465a1033eb0a3dd80cf330c = L.circleMarker(
                [41.912135958, -87.732514543],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_21ec244ed1e4506ca1721db2a10d9a88 = L.circleMarker(
                [41.97008868, -87.762690091],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_aaa6b363ba1f85db26fbf09ae1c5a23b = L.circleMarker(
                [41.92436229, -87.73687555],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_956e1c4b1dac95a42897a19fa12f0160 = L.circleMarker(
                [41.939967235, -87.754280801],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3f3b99031700078a0a43cb5e1e047a2c = L.circleMarker(
                [41.916979354, -87.741996341],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_587efa88b7f28a13b443ce753bdec72a = L.circleMarker(
                [41.926146366, -87.794096645],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ce6f92458018569b26e1be1d75b30868 = L.circleMarker(
                [41.812386271, -87.618239839],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0ad10e163d4a7fee9be0e53bb965163e = L.circleMarker(
                [41.843727932, -87.707453861],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7b01a477bfe68a0f6bfc7a4423d81983 = L.circleMarker(
                [41.976362279, -87.657137905],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_78e88d053cb9ae8685bf59db4621d6ac = L.circleMarker(
                [41.692171734, -87.657636587],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7d93c9d0c424a287f283a21eb5add5d4 = L.circleMarker(
                [41.781499104, -87.605955856],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7a605a3d0092fa7821c77d89774cd018 = L.circleMarker(
                [41.851138091, -87.699068091],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1f42471fcbaddc4196abfe7363b6331b = L.circleMarker(
                [41.722630518, -87.635965315],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a08b60abecca5c284929518344989807 = L.circleMarker(
                [41.851249556, -87.708892765],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_31ee8880a5fbe958a34f7e34a9636bf5 = L.circleMarker(
                [41.893179495, -87.634671454],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_eff7e69a611b7d9a0cf73f7f88587bcd = L.circleMarker(
                [41.945809065, -87.772960156],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7dd1c665f2f8a14ba4227d4638e4b0f0 = L.circleMarker(
                [41.718823567, -87.643141787],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_069ca60b57d51613f31dfe2211d750a3 = L.circleMarker(
                [41.821433172, -87.612815859],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2c84a4787d81e1f1362a3fa293b70684 = L.circleMarker(
                [41.980039853, -87.655800725],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7479373d7c7c737df5a991075a205880 = L.circleMarker(
                [41.713438071, -87.631625636],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d79b28c2eabe446e8ee902f3f429e0ea = L.circleMarker(
                [41.860260962, -87.712806445],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d5f51a06896ddc433f4a769c85ca7346 = L.circleMarker(
                [41.838009563, -87.648879044],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0e1c63a4e9ef920bdb74880a3b58c9a2 = L.circleMarker(
                [41.852396213, -87.712353914],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8f54a72baa99857ad92946093b664035 = L.circleMarker(
                [41.86324385, -87.715329039],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b317bb55e4dd633a6689c5aafeaee105 = L.circleMarker(
                [41.890051565, -87.62891376],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_80527d38bde72b9a44f779304d8e85ff = L.circleMarker(
                [42.014916096, -87.670904385],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0468a49566e763e9737d79c3b64fbd93 = L.circleMarker(
                [41.80210664, -87.677645084],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0349ff2fce063f8c6bd75917ca8fb88d = L.circleMarker(
                [41.884930978, -87.716221792],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7ef5e222d2b2f9246f8f55efa3dc1daf = L.circleMarker(
                [41.789665998, -87.663239856],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_efe1272d27c4f5e1496fff377d4334e8 = L.circleMarker(
                [41.802638207, -87.659950522],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fa6ca697f73c33cb00ee296d9d3e8d14 = L.circleMarker(
                [41.694184176, -87.6996971],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7403971d16ea0f5be23582e8416c575c = L.circleMarker(
                [41.763575683, -87.606752128],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5feab46e2a19c02f536d32e82f1a4280 = L.circleMarker(
                [41.737132553, -87.570487938],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4cd572604b06b9b96b97bcf8eb13078a = L.circleMarker(
                [41.90929398, -87.772320774],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0845d974ac915f18f6564891f53d63cc = L.circleMarker(
                [41.854954649, -87.730007045],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1a2dee95ffc54dc2df9d0734d27f9667 = L.circleMarker(
                [41.673514815, -87.638157521],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4632e9743a004950c09e38f80111c314 = L.circleMarker(
                [41.887979691, -87.773495215],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_62c467a55f282b47f7ec658ed2f98d75 = L.circleMarker(
                [41.743527769, -87.632694207],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b18ad3bdb3dc63e06c86fc7b7076d5d8 = L.circleMarker(
                [41.850610674, -87.627034305],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f2be685c200459e1aafb810e4a7a6776 = L.circleMarker(
                [41.697287938, -87.642533573],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1ce7749886802a5a4ef989b56d3143fb = L.circleMarker(
                [41.88320956, -87.630156699],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7e8163bbbc971a12efb59645e254f7e2 = L.circleMarker(
                [41.751104325, -87.615721106],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5c4c9d650d6739847c6c5433f7dc6ac5 = L.circleMarker(
                [41.801694608, -87.723406421],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a45bac528b49f41926f5b2eb54959361 = L.circleMarker(
                [41.758571453, -87.561511043],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7f7c7a32ee90f289a5cabedf0f056da9 = L.circleMarker(
                [41.79230014, -87.615918194],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7daf6018894a885a73706937e3620c27 = L.circleMarker(
                [41.919374816, -87.634940607],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b58726d5deb692552ce7afe7106861ec = L.circleMarker(
                [41.694336068, -87.629138436],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_81430f9bb3a268c6ecbaf0e8578ddfc0 = L.circleMarker(
                [41.798429303, -87.744521435],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1ef96e0b46ce93767d447e7c8f4314e2 = L.circleMarker(
                [41.649568403, -87.544734672],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e38e647511061c2e8120c9ca35c70641 = L.circleMarker(
                [41.97567305, -87.774949115],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_65491553c6828fb1e72beddeefeb7e8c = L.circleMarker(
                [41.937740894, -87.679028757],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3fb2592f50f68564daafa4ebb9ce0f47 = L.circleMarker(
                [41.721627204, -87.624485177],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8643789a0ac55dd2eca77b8f1921dd77 = L.circleMarker(
                [41.863049919, -87.639111208],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bd4bab71f6a5bf0230ea28b64612e7b6 = L.circleMarker(
                [41.8653515, -87.721491127],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_16777b3c39603dce455ea8e19a2a8ab5 = L.circleMarker(
                [41.810677154, -87.607826722],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3a8265a7811bf50d79fef370bee95728 = L.circleMarker(
                [42.021140845, -87.669168969],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3e46bb0e647ba91fede9372126a2dc83 = L.circleMarker(
                [41.961948442, -87.634920768],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c5bcc8aa7620e8da36595fd3028a81fb = L.circleMarker(
                [41.877748704, -87.742729014],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b8abdbcb7624bbd4bb6e971010d8d925 = L.circleMarker(
                [41.88107271, -87.696642296],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e06ef940e1f8c28f36f3d4c905c3d7db = L.circleMarker(
                [41.907926167, -87.64819515],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_520e1e5cfc2c8df4d354bfa58201f9eb = L.circleMarker(
                [41.779618833, -87.653841284],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4628667ebc7a4a261d52a9ddddb6f573 = L.circleMarker(
                [41.844112707, -87.628445336],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_723b1516b6764a0e495e0955cf4cfcdd = L.circleMarker(
                [41.970860793, -87.650753469],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c0c0ddea829422ea476364bf7a21f0f3 = L.circleMarker(
                [41.749211798, -87.566189275],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9ce288b7b3fb42a8b078ae56c5daa709 = L.circleMarker(
                [41.783009563, -87.671973213],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_65505cc3e262e74647c554125701e5c9 = L.circleMarker(
                [41.866478936, -87.698652145],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2fee714bac1c7bc3ac22f509627403ce = L.circleMarker(
                [41.711090771, -87.563342844],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_60f5c3684ee8186413c2ef76b36bdba2 = L.circleMarker(
                [41.773275806, -87.66161048],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d8647c612569a155f39f035946e8fb2a = L.circleMarker(
                [41.719852575, -87.597138803],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6a067fc049fc0317f3d72c51aead56db = L.circleMarker(
                [41.880775433, -87.627029031],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_764c3eb9618b4ead822cf37334954ecd = L.circleMarker(
                [41.931800684, -87.726174308],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_37e5554dfb34ab5e61344ce75f38d811 = L.circleMarker(
                [41.771382014, -87.661571584],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_53c91256a574d83e99bfcc7748b08232 = L.circleMarker(
                [41.743162531, -87.626828012],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c5e2dca5b9fe64e4e94807055590a91d = L.circleMarker(
                [41.894046711, -87.746461138],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8d907bc60d1a4da73b5cadbded8da7c0 = L.circleMarker(
                [41.766290949, -87.651720267],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_127fbe90d88af4d52f5a9d05a14d28a3 = L.circleMarker(
                [41.774514672, -87.689620928],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cf2f9ca4b7a6a7daf375444ad019c8a9 = L.circleMarker(
                [41.909770919, -87.735236961],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bb155c3e350e45a695a5b8aa8fbc58f9 = L.circleMarker(
                [41.810707298, -87.603919835],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_10404140107ea6b749207e2704de040a = L.circleMarker(
                [41.831086344, -87.618780276],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7e9c223264eaea2f2728099e80b5e957 = L.circleMarker(
                [41.789428872, -87.675390801],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_305c3b8a57fd750a432d75107408eb1c = L.circleMarker(
                [41.721590004, -87.633639541],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_48c74384ce5320a849206efbb1f34f2d = L.circleMarker(
                [41.767956594, -87.645709239],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a80643d1433317d039a2045a675c35fc = L.circleMarker(
                [41.880555964, -87.64192187],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_753c112edd004533803a390bac52aecc = L.circleMarker(
                [41.811443713, -87.598471599],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4c07bfd713c09e678a3973e3494f0082 = L.circleMarker(
                [41.896028512, -87.728566462],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e6d2245ab8de6549396a18655c259745 = L.circleMarker(
                [41.992696067, -87.697039242],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7d993f22a8df5eef1208cae5d630cd1a = L.circleMarker(
                [41.676081529, -87.633759304],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_adc711d822fe4c44c63d79a1c221e1ba = L.circleMarker(
                [41.81948083, -87.605665593],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bec6abc657a889f535ff01a680eb880a = L.circleMarker(
                [41.906174993, -87.662074305],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1bd77d2faedfac4718766298c2d9a399 = L.circleMarker(
                [41.741782857, -87.691003235],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_419bff625ac90d90efb59aa0906e25e6 = L.circleMarker(
                [41.868180939, -87.709271389],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1f55d6649546abd0810249bb27658178 = L.circleMarker(
                [41.911124622, -87.637932903],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bd15e549c3f23f8393d0388e63351ceb = L.circleMarker(
                [41.686500543, -87.668217814],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9c92e58366e28c7a9c46647bad0845b6 = L.circleMarker(
                [41.715095603, -87.537689312],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_aecd19f2a2ad09e3dcfc648f1c9d2cb8 = L.circleMarker(
                [42.002582195, -87.817667795],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_27a3dc3eb242a4d034fead375d42d82d = L.circleMarker(
                [41.830496901, -87.665859662],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cd714c9118c2685988b07ed4e1535f8b = L.circleMarker(
                [41.849900927, -87.709177489],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_79cb60bbbc4733cd3269c27fb3d0633b = L.circleMarker(
                [41.765539272, -87.588545212],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cceb2f29474b0438831c4580fd08694d = L.circleMarker(
                [41.930098265, -87.773498255],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2559d33ee4d3c76e2ae4fa55a8536351 = L.circleMarker(
                [41.759947729, -87.66365908],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c98ce5f6e67cd2ceb5124c37a7562642 = L.circleMarker(
                [41.76790158, -87.642029481],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_29229b2dd804d89a56edae599449b4bc = L.circleMarker(
                [41.909395666, -87.763987758],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_be3cde0976cb0bbe9475c2a24c92f3a3 = L.circleMarker(
                [41.896805991, -87.749411049],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f8d80e36f5ef1751ce345bfecd30bc2f = L.circleMarker(
                [41.880108035, -87.647309981],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_740319d88c35e44833684d9df7c7d931 = L.circleMarker(
                [41.756217734, -87.589521604],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e339d4da08a88636b812dc7f87836ac8 = L.circleMarker(
                [41.797456735, -87.598136319],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_51a58c75a9e73f5be221890ec7f88d91 = L.circleMarker(
                [41.885943666, -87.652150239],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_938a89fa46b8b711b03fe235e0ae3707 = L.circleMarker(
                [41.923976215, -87.766294416],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2f90faeb68b85db020794c617596e889 = L.circleMarker(
                [41.943349657, -87.724862787],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f6135348f9846a8ebc0a4e94da8def79 = L.circleMarker(
                [41.776070132, -87.58785513],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e82257696ec918de5bbe80d0cd2880c2 = L.circleMarker(
                [41.896888586, -87.628203192],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_95b32a711ef90b151cf0a2e440f87507 = L.circleMarker(
                [41.910118499, -87.706254665],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7cab954a445876776b591d59effb24c8 = L.circleMarker(
                [41.854317419, -87.621579371],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6f0142f6e26937d9334f7dcc3b1806e9 = L.circleMarker(
                [41.702055646, -87.563219944],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_81847deba794950c1a94d4e3ebd82791 = L.circleMarker(
                [41.905782884, -87.709327786],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3e2e7dbaa7f7e4a536261d9a76731cd6 = L.circleMarker(
                [41.9410481, -87.70615019],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_32b13fc9e9e1785da5ae726e9f796e23 = L.circleMarker(
                [41.700281436, -87.681426902],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f5ac628a1e6e8319d52a47023521a78f = L.circleMarker(
                [41.709918542, -87.622039167],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_87242eef1bd2a8a5b0c3a55b953fe6b4 = L.circleMarker(
                [41.840149886, -87.720777108],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d03548e806d74a2693b1d3040d39fba7 = L.circleMarker(
                [41.763036211, -87.61522896],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3e4c94599aba50585f2d36bf05abdf00 = L.circleMarker(
                [41.691844914, -87.642364809],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8444b43e5eb150a2e43c0e005cae05ad = L.circleMarker(
                [41.782213553, -87.684942472],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ae8d50d86b47a4b1f8c05879aa1c7721 = L.circleMarker(
                [41.877851597, -87.736092822],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6f35662e8eff57d48280c9377dd00262 = L.circleMarker(
                [41.790707994, -87.604942346],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_45ae38c51e8a91d454bcc605fcd205cd = L.circleMarker(
                [41.717415796, -87.618905382],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7aeabc32289abd885eb07c7eb6af096d = L.circleMarker(
                [41.919462416, -87.733967003],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_92fec4cdf19605dba8ca4d64c137a51a = L.circleMarker(
                [41.84905907, -87.6806563],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_841c16365817a0ecf6b43c2c0fc62ebf = L.circleMarker(
                [41.717766501, -87.561120409],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_89e3efedfdbee89e3d58000869bcc5d5 = L.circleMarker(
                [41.920597986, -87.638888282],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d12df15ee6b91a188da7673f811fca4c = L.circleMarker(
                [41.905835042, -87.709330952],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ad89b43438d7f14a40ee3398da00d48f = L.circleMarker(
                [41.786556226, -87.684183701],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8faa356d454133e72b7bc6894de53c49 = L.circleMarker(
                [41.926287021, -87.785547998],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d8c1c7228bf229a6ac8e5604c497ca3b = L.circleMarker(
                [41.895589775, -87.769068924],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_589f4e5aaa50988c10d8e1fdb5a4a230 = L.circleMarker(
                [41.891949919, -87.756716358],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8d43d17d04d0395116d891e07bb57ea9 = L.circleMarker(
                [41.773061957, -87.672529994],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_30bd7a91b842e7c6a67a82e3441a9e44 = L.circleMarker(
                [41.691359415, -87.658571406],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_953dddc04d5eeb08e5b501e10942b2f3 = L.circleMarker(
                [41.758737609, -87.589191963],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dbfa5a0b330d600c7cb2403a1c5b9260 = L.circleMarker(
                [41.757977126, -87.57612363],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_18e8e0e2899379fbe75b43d6e0ca120b = L.circleMarker(
                [41.84056097, -87.724802664],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9f677ab2516ad95530355be980afeda6 = L.circleMarker(
                [41.890300993, -87.763386087],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_68889c8af10a3f6714938a227e781ab7 = L.circleMarker(
                [41.693157608, -87.682476443],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8d4c2a3ad0b107fafe785c76de2d82e1 = L.circleMarker(
                [41.831101673, -87.617716013],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cd4f11633781d969f707a50465bd2c33 = L.circleMarker(
                [41.894539838, -87.624243916],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_da33fcfc77a9bb46820eec844210914f = L.circleMarker(
                [41.773556277, -87.664056445],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_79857c51160643a4393dd9109d9508ec = L.circleMarker(
                [41.918334501, -87.638064065],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5ee9d3041c2c164c3185bfe2cf3fc21a = L.circleMarker(
                [41.764497622, -87.582402912],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a2e1b188460550eb8f29802a701e5616 = L.circleMarker(
                [41.756302533, -87.605331512],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_58b55894d84c7b91201432e1f5e0b285 = L.circleMarker(
                [41.856631889, -87.653926009],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5ba1cbf87b90e4af3299fb47c560c85a = L.circleMarker(
                [41.965483756, -87.649178286],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5da14d4b0b637729328eb56f40821558 = L.circleMarker(
                [41.923894933, -87.771531453],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_760e42189d28c574c6a19a102f713c1a = L.circleMarker(
                [41.745435298, -87.598895016],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7e30c542f5b4c2addb0675e1ac13f1fd = L.circleMarker(
                [41.89652481, -87.639211587],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b7de00c9ce9cb203f5dff2d2647ebb27 = L.circleMarker(
                [41.781874547, -87.659416183],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_93b600474d273b27898f4790e35c4bbf = L.circleMarker(
                [41.747851897, -87.66337071],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_380dcc8809f35bb609d418dc00ecd95c = L.circleMarker(
                [41.751375148, -87.55895132],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e4d4c9acf9bbe21f7932d2c1fd29dc97 = L.circleMarker(
                [41.749871534, -87.645231645],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dfde721b97ea02ef4d4168903d07c63b = L.circleMarker(
                [41.97422231, -87.805904287],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5288227c56e4398afe1c18431c894483 = L.circleMarker(
                [41.798964595, -87.654986576],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_65b33212fb70b72e73cc6159d952c258 = L.circleMarker(
                [41.882424852, -87.624377884],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_32a6421847a8ad0f16bfe6a23b202221 = L.circleMarker(
                [41.851949553, -87.618995915],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3d9c3e156b8fe0033b27c81e1fd8fb8c = L.circleMarker(
                [42.016947128, -87.677654422],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c1039f90014744b7624488b8b4cfa210 = L.circleMarker(
                [41.928559823, -87.7647802],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f80b866898ecb08361ad486833089478 = L.circleMarker(
                [41.829875745, -87.612570753],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_de6e664641180dab729533ed83c986cc = L.circleMarker(
                [41.968763818, -87.688661831],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6672b4566a7e7ff0f531ffe759664577 = L.circleMarker(
                [41.814158135, -87.747466128],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_04c406dba616921846461c1e4950ba7f = L.circleMarker(
                [41.753946001, -87.60893507],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4c08deddad23e0f94e4c1dd2d0b3cf22 = L.circleMarker(
                [41.920062024, -87.743772004],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_de6e7a035cc8b13462b43f587511999e = L.circleMarker(
                [41.655794169, -87.596247691],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e305fd41c81b715276da5f6efc134d04 = L.circleMarker(
                [41.9070123, -87.721567391],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5999fbc4d521f36c238492ae30e7d8ae = L.circleMarker(
                [41.772704538, -87.582629798],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e7192b33fa4ec6ec6238b0793d0a582d = L.circleMarker(
                [41.938581442, -87.765830579],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0dcafa57d13279d736c207bb91e4351e = L.circleMarker(
                [41.953512438, -87.739721351],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b0259feccc70612b41fcb4489e23167f = L.circleMarker(
                [41.944815726, -87.731233724],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b362dadddda0bce3ebd54275c84e2be2 = L.circleMarker(
                [41.770060129, -87.654250097],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2b0de0a97fbdf284e4066b99b3e11f09 = L.circleMarker(
                [41.894207941, -87.711398126],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f34a2baa135905b380e9cf9c0a702703 = L.circleMarker(
                [41.906416693, -87.767019237],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6cd096ac4e847f643d3637dbbc5b097a = L.circleMarker(
                [41.892631323, -87.6182857],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_22451bfbf3b5ddf664b78fa582fb0bf6 = L.circleMarker(
                [41.907682054, -87.673997947],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_362e7f9a22af5d49491ca3a1ca0c037d = L.circleMarker(
                [41.815246276, -87.670001899],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cdeb77b69e2b56d4f2815b16ad16ab08 = L.circleMarker(
                [41.793926429, -87.673419543],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_33449ec31d02563307a5853f15930981 = L.circleMarker(
                [41.844135216, -87.73285389],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_208d489d7ada04cb46086a290237fdd0 = L.circleMarker(
                [41.899085036, -87.765544955],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e6e5369af46fb45d6e9fc34c3c2eac99 = L.circleMarker(
                [41.880443372, -87.624355722],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_227aa9e554c4b9f8437a3a146135e953 = L.circleMarker(
                [41.761273686, -87.560969185],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_896948de4d536f04b3d10c68f36946c7 = L.circleMarker(
                [41.825265586, -87.692227754],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4d7b32f0a78f628cf0a34749b227c4d6 = L.circleMarker(
                [41.884924096, -87.630953163],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_66c9334ea9d4e49516a57e1a37f35d83 = L.circleMarker(
                [41.969398556, -87.784366127],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bcf7c1399f830048104ed80b46ff44b8 = L.circleMarker(
                [41.804695984, -87.633253215],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_32794cb7d0b322c5ba4033b911826359 = L.circleMarker(
                [41.760547524, -87.563173381],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_57751377dfa7d60f97d4768a896692df = L.circleMarker(
                [41.896164467, -87.723658031],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_56357664472f3cc2e380fdade385deba = L.circleMarker(
                [41.771296232, -87.729149311],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6b89e1649449b875a04b278b7c867ebf = L.circleMarker(
                [41.751128283, -87.554098534],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ac2cb8d3b5b35bd1c7e4428bbdbe4e8f = L.circleMarker(
                [41.908787859, -87.717979565],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9f7eb2468a9f74a9f06fb22023cc4d9d = L.circleMarker(
                [41.789915718, -87.632875019],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e053f650b5bee04adb6e02e71fca01b0 = L.circleMarker(
                [41.921626977, -87.662412101],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3d2860798bdc83dc9133a436d5796dac = L.circleMarker(
                [41.953850303, -87.713303814],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1629a45c620cb698c76ba43d2ddddc39 = L.circleMarker(
                [41.924102822, -87.756452662],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4af3d981e2c412c6835c0e656615b947 = L.circleMarker(
                [41.882529537, -87.626223856],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5d2011aa14ad1fdf7b17bd1564b8bcb7 = L.circleMarker(
                [41.764929409, -87.576272815],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3637d287f832a491918ef39593c5973f = L.circleMarker(
                [41.731859652, -87.554778427],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0f939e23858a5892b8c26f41f1f254d9 = L.circleMarker(
                [41.754537438, -87.579715365],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dece05c4d589e0505f3b681f9dccffff = L.circleMarker(
                [41.839091599, -87.621913257],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bc23a327c986b4e0626c0fd5d11b966e = L.circleMarker(
                [41.978165506, -87.658586238],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3f076930994ba035fb299f56ff0bbade = L.circleMarker(
                [41.780344546, -87.785028313],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f111935a616a4f2ec6f7b899d337b756 = L.circleMarker(
                [42.019399237, -87.675049485],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_273175b57dafe89c34e2d39293e423c7 = L.circleMarker(
                [41.879595887, -87.73959442],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c706503c70c386d65397bdbaa63aebf9 = L.circleMarker(
                [42.019454319, -87.681334526],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e18af57c657e564fc2daf1f3b829c311 = L.circleMarker(
                [41.885350609, -87.709574392],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d60b03f9ad1b1ca936cabe2904ff50ae = L.circleMarker(
                [41.78381682, -87.588634381],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a496813689af4978d23b154728d789ed = L.circleMarker(
                [41.980483559, -87.661257632],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_085b8c8e75d5e48c8ce914d966bdf4ed = L.circleMarker(
                [41.945129044, -87.644893073],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f7fc98903c18c381ecc1d5f66d43b36b = L.circleMarker(
                [41.996126503, -87.761754899],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cee0eac93ea998537d38071483ea1b6d = L.circleMarker(
                [41.895922629, -87.749466845],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_45add8fa80efe94a3688bec752c54dd7 = L.circleMarker(
                [41.976840051, -87.836613167],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5c056173b2cb03f6e69f20e1e62c4625 = L.circleMarker(
                [41.880511063, -87.744117344],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_63718ce2eceb95321e0563c4f23a7a4a = L.circleMarker(
                [42.009295326, -87.702945041],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9340efdeacd720f399a0e8c60938573f = L.circleMarker(
                [41.738014715, -87.609711364],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5fa2b57dc57d35f5c5ff1346ad30c489 = L.circleMarker(
                [41.877565688, -87.684893829],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9b1a7f0b099dee97725fa7ad7e486800 = L.circleMarker(
                [41.889283859, -87.765800697],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2929fd3e7f358cdc62df00a1d3070679 = L.circleMarker(
                [41.913463243, -87.631705806],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b0ccac0adeed54a79c5d7a826ae055a5 = L.circleMarker(
                [41.742429809, -87.706276659],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_736eea6f9fafa4119371c6f2245f2672 = L.circleMarker(
                [41.949094948, -87.728289375],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_84a00f71b8344d26fc3238d9048d1d91 = L.circleMarker(
                [41.95208984, -87.647891491],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_41d0c357d8ea5f410680c5ca2e4d63ed = L.circleMarker(
                [41.89577577, -87.641507968],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1022b26fd48fc1ebd128ed829f24d3eb = L.circleMarker(
                [41.72657208, -87.614265084],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7f1c23a348f1e6dec5a81ba7b512d6ef = L.circleMarker(
                [41.687146871, -87.654379538],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9f7312aab4d41cd08e01c73ce357b803 = L.circleMarker(
                [42.011694602, -87.690237586],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f4cd3cce6cc85940287d89de060ad0d9 = L.circleMarker(
                [41.900669662, -87.737085073],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_110d2f3ceeb09682ed8803adc4f7aa5e = L.circleMarker(
                [41.936374044, -87.71411998],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c739736989df3b8391532967b8d2678e = L.circleMarker(
                [41.76335897, -87.616816153],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_df3565f6a127a02a0cb920935685dc5f = L.circleMarker(
                [41.735399233, -87.643598194],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8a792a6e5cca6b1190ae31c6c7a99cb1 = L.circleMarker(
                [41.858865391, -87.72535599],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_35113bd323ff6f958cabb38b82c59270 = L.circleMarker(
                [41.779273063, -87.676972155],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f39f1204fd1a41e1de87271a46e2b669 = L.circleMarker(
                [41.738681424, -87.556315527],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dc032126af2b0343709ce115756596ed = L.circleMarker(
                [41.782596589, -87.70397887],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b894324476ed6bffa44239f463cf0ea7 = L.circleMarker(
                [41.682627045, -87.674195589],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e0891fd352fbd32cecbf21bc0b840791 = L.circleMarker(
                [41.902099209, -87.634827684],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_42d99b4032de11cf89175135af52afb5 = L.circleMarker(
                [41.79980262, -87.715993995],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d3da6cfe98bb699f1c15775bc2040987 = L.circleMarker(
                [41.77268594, -87.605758495],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1448b519665c7bcdee726d1b59df018b = L.circleMarker(
                [41.719214167, -87.652031163],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8b2d93dc685c9537a2fb6c878d62c2b4 = L.circleMarker(
                [42.002848755, -87.660794204],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_35831079950f80093ab22ca4e4598d77 = L.circleMarker(
                [41.933582379, -87.645517082],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4b5f61b0b981f92fdcb44124b1fe1475 = L.circleMarker(
                [41.881370455, -87.761577961],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_09a01e6139bec1e864a67e5055fdf42f = L.circleMarker(
                [41.911054487, -87.670146097],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_000029d2eefd234ed059570355f8ce07 = L.circleMarker(
                [41.777938449, -87.613152615],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_69ced3a71d54ab5d2a214e594304c908 = L.circleMarker(
                [41.784264083, -87.669184692],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4f60bcdd088c525dc712ce33fef71846 = L.circleMarker(
                [41.79183892, -87.658457397],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a58ce1d89233f5a241caf1f10107278b = L.circleMarker(
                [41.894197714, -87.670805335],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bc07567c3465a8e9498e572a9cb8c9b4 = L.circleMarker(
                [41.800228473, -87.686653342],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9538b7257d80dfe9b940d8b4270ec4ee = L.circleMarker(
                [41.990467833, -87.695071404],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d9ffbe0ea9c623c302ca57db9b152974 = L.circleMarker(
                [41.737369771, -87.582755662],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ae389357f34ec23aed5897a9f7f05d51 = L.circleMarker(
                [41.736345248, -87.623198545],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8b394acd217a23b3ebfcd1ea04590337 = L.circleMarker(
                [41.931267974, -87.710233412],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f55253533a654e3115e1800609b46d32 = L.circleMarker(
                [41.885487535, -87.726422045],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7d2af86eaca89f8c20fade7272467c48 = L.circleMarker(
                [41.973263481, -87.658435722],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4d1e5ec57f08131bb0be441e148fd1f6 = L.circleMarker(
                [41.94714472, -87.6594722],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cf21a1acb139d2b8c550323de444d6cb = L.circleMarker(
                [41.755608031, -87.64172529],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_762cb440496124fbeb130f060ad576d9 = L.circleMarker(
                [42.016730742, -87.675327242],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_91543e1d1c0fd3dd3fa40cea794f0bf3 = L.circleMarker(
                [41.743700608, -87.567328522],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_13e8e47b4d1e6e5c4beda966552bdd33 = L.circleMarker(
                [41.755004079, -87.73034298],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7dceaeb4d063c6669bbe01d27ff1cf22 = L.circleMarker(
                [41.900885473, -87.721765462],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b79c52bf9255c2b341d5f9f943b1f37a = L.circleMarker(
                [41.852540096, -87.727996269],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_03f1015510f90a1103be8f4f7d7331a9 = L.circleMarker(
                [41.835659225, -87.623356707],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1b57365e2e27a1ed41c2d9fb34bdecc5 = L.circleMarker(
                [41.872877317, -87.760541139],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7e14dc1c46a5b697ba8012933e3b850a = L.circleMarker(
                [41.728926112, -87.563349705],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a3c163fb749a904d1b2c8099262c6417 = L.circleMarker(
                [41.93257779, -87.65749767],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_35ae49cd1a3517cbcccc787e2f0153f8 = L.circleMarker(
                [41.785621131, -87.688695836],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_18044af656ac4e6439b95f4703a38128 = L.circleMarker(
                [41.81411177, -87.598140299],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a38eacf6e026c87ba9055f101038b94a = L.circleMarker(
                [41.940412833, -87.651052567],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4889714ca300e868fee5479fd5b991d8 = L.circleMarker(
                [41.924055919, -87.665759946],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_67bfa73b2c81b0a4685d3dcc94669d25 = L.circleMarker(
                [41.878851273, -87.657043254],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2737ee48fca3ed51eb182742c0c0aa18 = L.circleMarker(
                [41.746012078, -87.547930876],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7ac420dd01f6fc1d8bc3f7b78eb73a54 = L.circleMarker(
                [41.945399848, -87.799970169],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9f5d49529f2a0d7ff41efa9531d06c98 = L.circleMarker(
                [41.756487034, -87.715045885],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7b5533378aa541bc8947514e2aefea87 = L.circleMarker(
                [41.715672509, -87.646710019],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3cdf1c8a76b8dc508be00f9a0542a5eb = L.circleMarker(
                [41.866843668, -87.625816668],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b692d61de8341c1a3cff95dd70a2a6e2 = L.circleMarker(
                [41.886524557, -87.744282439],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7f1d2eccdf2c4e98eda820f41d3e6c37 = L.circleMarker(
                [41.895683044, -87.692691989],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ad2e1aeddd3fa6501454a30fcf9c120e = L.circleMarker(
                [41.786670801, -87.62063773],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1e6f1f6b5bef98123674a660e2ed7ddb = L.circleMarker(
                [41.677210266, -87.626268618],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d3759cadbba27f0ebacba0cdcc2952f5 = L.circleMarker(
                [41.768056035, -87.568945009],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c34d2e71e1f8437ba6868a6694673672 = L.circleMarker(
                [41.909635441, -87.676303351],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c736534739217ab7636f04bc784641ab = L.circleMarker(
                [41.892534793, -87.712567618],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_78db16cec3f78e9920b8b3694317a5d0 = L.circleMarker(
                [41.90035626, -87.761801663],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ad1169139091a90192e303d10ec1607d = L.circleMarker(
                [41.759668763, -87.579219169],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6089e530b0cead608e6dd15ad43aac02 = L.circleMarker(
                [41.895442156, -87.628167681],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_09d1479d43480fc939cf2bf9314829c5 = L.circleMarker(
                [41.769434364, -87.589537569],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_714c86ac9f8bc632a9a7467c3db0142a = L.circleMarker(
                [41.980963017, -87.845202105],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_37679db4a6f149aa8efff03e302b6e05 = L.circleMarker(
                [42.006862961, -87.673467835],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d2a96c127179c64751f6a92c9689c756 = L.circleMarker(
                [41.782847294, -87.687832652],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ca63ef0cea2d11d4a3edda616f2caf35 = L.circleMarker(
                [41.750391287, -87.602734083],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_77abeb82bae1b6e38bb2303d44f85dc2 = L.circleMarker(
                [41.961080071, -87.717153134],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_15eca0becc5bca73d83b9c818bdba115 = L.circleMarker(
                [41.806022407, -87.660036124],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d82b7433ea031d6546f2552b3c8b4980 = L.circleMarker(
                [41.899468916, -87.641864812],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_44dc99261dbbfbf1a314482d20e85248 = L.circleMarker(
                [41.882407782, -87.627844648],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1e44b2e242fa3032814ecfbaf3bc5767 = L.circleMarker(
                [41.830679557, -87.734333624],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b90ab43a3c677887648ea4f33ac4a481 = L.circleMarker(
                [41.987870213, -87.66019784],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7b61ae1192d562c44f53001ca0b1932c = L.circleMarker(
                [41.891350929, -87.748968588],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7bf16ed2a2eaf5f458d00c3cf0414571 = L.circleMarker(
                [41.866389063, -87.707276938],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9cb8c82a1ff4705ab48d2fcaaf9ff49f = L.circleMarker(
                [41.997553379, -87.700033256],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4228774eb71d2384817b776d5b874f2a = L.circleMarker(
                [41.868780233, -87.627458476],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0cadfbb1718a7dfcc791e3de8e0ce21b = L.circleMarker(
                [41.779200334, -87.687869227],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_03c635ac7a0c7629041dba70c546f2f3 = L.circleMarker(
                [41.965917872, -87.770552017],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0b17f8f473fbb43512c37321ce86cc7b = L.circleMarker(
                [41.98443411, -87.764092092],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_42157a371b00ffbc4f12911f5a258aaf = L.circleMarker(
                [42.015202809, -87.812215335],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6fd1b1a997955c5e84e69b9fd6e53775 = L.circleMarker(
                [41.748846713, -87.642288924],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_df7c80b62941a4f62e1ad06f2a9ce52b = L.circleMarker(
                [41.847124524, -87.691396634],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d0e4e4f3714e235fa0bf789d1596a2b1 = L.circleMarker(
                [41.755923803, -87.65743376],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d6afa2e1c2bfd993400319db020e7c0f = L.circleMarker(
                [41.886288459, -87.769969735],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_03e77805046dd17f84adcf6861ef1fe3 = L.circleMarker(
                [41.915691891, -87.695269563],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b62424b58d79c9fb75f6fa0769574a4c = L.circleMarker(
                [41.845525185, -87.698906996],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2bd9cfac46f404c97d754f3e61aeddd4 = L.circleMarker(
                [41.876132309, -87.682796997],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0e75bf51cdacea7177671a8d4d1ab02a = L.circleMarker(
                [41.727096769, -87.603034703],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5cd3b643c33b39146292b65b17e25e9f = L.circleMarker(
                [41.935343672, -87.654656897],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fc03a2c9475081f48a55971159495692 = L.circleMarker(
                [41.753680698, -87.556156634],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9775a25401f63aa0949c2612933a5262 = L.circleMarker(
                [41.88018827, -87.626154195],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e19a143b4e736624d73ba2d0ebf70ec9 = L.circleMarker(
                [41.874400423, -87.640067886],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_343c587ac5537410bb77f46adcce8884 = L.circleMarker(
                [41.943552694, -87.688162342],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_74abcbcfc39e6b50a07663ea3458f35c = L.circleMarker(
                [41.759355486, -87.55812601],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_34322a6bc457724b6e8f668d9290ed1e = L.circleMarker(
                [41.877918244, -87.702368831],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7eccd2ac4309521a88d3ab9ac641fbe5 = L.circleMarker(
                [41.938372454, -87.782077877],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_74b42961c71a38df2720be77ad9b1969 = L.circleMarker(
                [41.752545308, -87.586053123],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_94080656c898e52c253659b4cd254464 = L.circleMarker(
                [41.773286383, -87.685919559],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8ce2faa241aa760beb39b2247c2d558d = L.circleMarker(
                [41.863397289, -87.658252408],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2da231796c83a7c8e82a0d1ce51a6d34 = L.circleMarker(
                [41.865899027, -87.68913091],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0c99ca76081596f268f7dd399eab0b41 = L.circleMarker(
                [41.798203319, -87.702469251],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5243dc3f0079139d9b6f97b3bd4c7e49 = L.circleMarker(
                [41.75420485, -87.649378012],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d7c4ebbedfb9a205d12dcb8164558875 = L.circleMarker(
                [41.779295906, -87.644774188],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3c2aee289b0df38d32f2a8ab3a3d7919 = L.circleMarker(
                [41.932281371, -87.744170328],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d874c6f5cab15a0d7accab26ca450ae2 = L.circleMarker(
                [41.972410835, -87.726932445],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4967a0efd3b7a38156ed7f01d26d3d04 = L.circleMarker(
                [41.977017622, -87.692447486],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dbc440ad4f90cbeb8870f7f35889b57e = L.circleMarker(
                [41.899410159, -87.624131266],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_53ee403ffbdd83c54c45a3dd81f9118c = L.circleMarker(
                [41.891640287, -87.630225839],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_43ae6f18d626617ea376d8873eb96cd0 = L.circleMarker(
                [41.755742588, -87.716951499],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9b757bd41cf43eec964eb032b3e8a28a = L.circleMarker(
                [41.975099794, -87.679374655],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_188964639870e8fcf20231dc11c9af51 = L.circleMarker(
                [41.798993672, -87.622576983],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_915135829a3b62feeaffaf15c1295ef9 = L.circleMarker(
                [41.906585521, -87.696076603],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ba5733a45c5e317f44be4d40680e096a = L.circleMarker(
                [41.801122852, -87.749095927],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3482e4b332a69586604c61846320b4b5 = L.circleMarker(
                [41.991439996, -87.658258453],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c4dd6b932c0b1232eb25ed115b4df765 = L.circleMarker(
                [41.916123092, -87.717960543],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a3e0c91acf56e22f102d2f362f2691ad = L.circleMarker(
                [41.716668688, -87.665804426],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_661603251ea489c5e55c665ca36e6279 = L.circleMarker(
                [41.792139018, -87.792445312],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f0635583b67ce2c519c4d185e1bbeaa5 = L.circleMarker(
                [41.878563019, -87.747946784],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d23199f282f8efdc489c96fc233fe345 = L.circleMarker(
                [41.920472825, -87.693384732],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ac046e9f9271aeab76aa3633148fb3f5 = L.circleMarker(
                [41.707855465, -87.646507547],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e3bdd1f30a878d35cfabd5f086d440b1 = L.circleMarker(
                [41.783298944, -87.594708522],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_535bfdfe6131d063997365c5fcfa840b = L.circleMarker(
                [41.671515216, -87.650228441],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_66f2ff42935c639ae5775f0891d89744 = L.circleMarker(
                [41.898215508, -87.721284045],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_26f7c623cc918f5c6d49a5732eaeb215 = L.circleMarker(
                [41.919573251, -87.77557074],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9b68f745eb641f05ccf9b93e7722ca2f = L.circleMarker(
                [41.918570075, -87.690258545],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fb443d1cbace5387d0528494bb0848c5 = L.circleMarker(
                [41.924430694, -87.68519117],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_806c7f6614adcda51376c7cd43b07b3b = L.circleMarker(
                [41.889551923, -87.626649565],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8c6f0f0376d583e56a7e34552f75b243 = L.circleMarker(
                [41.806392948, -87.660046916],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a11d4e5bbe97d7e3c5b35727db4ffc96 = L.circleMarker(
                [41.997723659, -87.690186971],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dc82c8cf105c847165803999b295784c = L.circleMarker(
                [41.817101454, -87.631225183],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a08bc71db171cb9098ef3f0ef128d730 = L.circleMarker(
                [41.891803729, -87.715417417],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_960ebb2ad844ab10bc7db30db555f6e1 = L.circleMarker(
                [41.925901886, -87.690122449],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_306eb3456ad73879e6d9c7240f56f912 = L.circleMarker(
                [41.754669202, -87.579721153],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1e736be822867a9187c0d80b2d8aa9b2 = L.circleMarker(
                [41.93854098, -87.820212911],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_54568d0ae9f7b578bba3a8c44cba5453 = L.circleMarker(
                [41.751345114, -87.552890215],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3cdb788d82fe8273f7bee46a33239ac2 = L.circleMarker(
                [41.978495324, -87.689251423],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ecd73c2726f35c93d9619ce57351fe7e = L.circleMarker(
                [41.763442537, -87.640735801],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a1be521f9392d96abb505301fa21a801 = L.circleMarker(
                [41.887123664, -87.754163303],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_316c7d57d72449be8b8844c053f9a85b = L.circleMarker(
                [41.924614888, -87.716129816],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_874671c34fb0a1bedd83050b6c869d42 = L.circleMarker(
                [41.863157551, -87.659018523],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_924c84e0b83636eb6dee5fc5d17fa034 = L.circleMarker(
                [41.87766908, -87.629284766],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bd3d643b962ee2e8dc7f290cb4f689e0 = L.circleMarker(
                [41.678976467, -87.619865148],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4ec26251244682532d4a5699a69e96e5 = L.circleMarker(
                [41.791394801, -87.660874956],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_21c907ab6619d8cd100c11a5a2ab4ce4 = L.circleMarker(
                [41.913810131, -87.782344396],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e443240550c68f03a8f4fd2d877ce1eb = L.circleMarker(
                [41.961108341, -87.714755626],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d610fa54b9a30d7496cac0317bcfa338 = L.circleMarker(
                [41.925115037, -87.752019232],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1b4e07e068cd64324d426a7a7e538b90 = L.circleMarker(
                [41.830697249, -87.614476891],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1446c5b794a32fd6ce0819661c94a84f = L.circleMarker(
                [41.776150283, -87.615522623],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_baec612ffcd32518fe5e11aa249fec62 = L.circleMarker(
                [41.925076902, -87.673855622],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6be1ad1e5985f807bc594f4bd233ccf7 = L.circleMarker(
                [41.882863063, -87.769852936],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1f95d6f1854efef4b030b888811cb64f = L.circleMarker(
                [41.870256281, -87.745819659],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e3f5e67824e2f5afbacdad6c084f6b44 = L.circleMarker(
                [41.76063512, -87.601771219],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6c9c92ddb381e436456b7517f2848910 = L.circleMarker(
                [41.758571453, -87.561511043],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f185aa4dbd65051bdfebb6c14abe8d30 = L.circleMarker(
                [41.769285935, -87.57149277],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_57846c0de38d03087f1949a8989c8462 = L.circleMarker(
                [41.898843171, -87.736782498],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7e5f6259ddf733515b07024e376d2b6b = L.circleMarker(
                [41.781311691, -87.725275189],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c048774f6ba02108187b8599e2ca6967 = L.circleMarker(
                [41.878278472, -87.623961046],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_228fe6ae9d835ba35eeeb31c299e6087 = L.circleMarker(
                [41.930976045, -87.78651851],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0a6332c27d4f808a815bc638a2379b7f = L.circleMarker(
                [41.766316323, -87.660213178],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4341f16011fb6c6cbc4ab798f83847c7 = L.circleMarker(
                [41.791056773, -87.623394402],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c7e3b615c5b64d94cf77bf22f50cd682 = L.circleMarker(
                [41.939253632, -87.714286923],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9098a4c5768ecadc5e9c386e7b39d915 = L.circleMarker(
                [41.656906037, -87.597596302],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9f76bb3220a0965ade8ef2b20d300d29 = L.circleMarker(
                [41.819426039, -87.610897661],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d5969c36ff5d406cd0afbe5cb7140f5e = L.circleMarker(
                [41.932623105, -87.734373021],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_310a0732cee13cba404adcd071b3d5c8 = L.circleMarker(
                [41.844807219, -87.645224608],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a10f7042bc8d7aeca066c4d41d6f17e7 = L.circleMarker(
                [41.765029984, -87.655670382],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2756151525e3005191fa8d71d6c97087 = L.circleMarker(
                [41.955470379, -87.656160286],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e57238a2018f0baf54ea9605382fbc40 = L.circleMarker(
                [41.990816774, -87.668553657],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_94947511add41bf5da1b3d7f75a46fab = L.circleMarker(
                [41.884493832, -87.627021129],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_02751c9a2e10b8528e32528312242995 = L.circleMarker(
                [41.721699431, -87.625517364],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_444e30831c35d14df3fecf2ac710a50d = L.circleMarker(
                [41.721180629, -87.623717187],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6ff037799c3ed1fceadf5d9639cc8ae4 = L.circleMarker(
                [41.750764865, -87.608857231],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_03aa271df1c630ecee62592e1ceeaccf = L.circleMarker(
                [41.761528585, -87.711027943],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6148af0981a3c1ff7c14ff444f0a7ed2 = L.circleMarker(
                [41.932778943, -87.704996369],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_84152cb63aba5010fe1619fafaf49902 = L.circleMarker(
                [41.981712678, -87.708829703],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_48e389186e99e7ca0f69fd382e80efd0 = L.circleMarker(
                [41.689793022, -87.628946343],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c461771c9bda74255cff619b50f4127e = L.circleMarker(
                [41.734456691, -87.589296443],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6e61be127c856751ff10474f0521c7b0 = L.circleMarker(
                [41.92384641, -87.646521939],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c409967056a1ffec768e9b323ac07900 = L.circleMarker(
                [41.763181359, -87.657709477],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5660143ad5e5488d5372c0322249194d = L.circleMarker(
                [41.763506317, -87.636307274],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5178cc6c0d5d121ef8d292974e5349f1 = L.circleMarker(
                [41.782500506, -87.65712539],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c66165bcf1fd5d004b53a39772745580 = L.circleMarker(
                [41.958900737, -87.670756881],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_de9db77322cea0b4f133884e63d61cdc = L.circleMarker(
                [41.761886136, -87.570073857],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a9af6c3ad0cbd519e8ea2eb510a9b857 = L.circleMarker(
                [41.666319459, -87.639116969],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6f05b2f8cd85a5d7dd90c1f89e8d8c79 = L.circleMarker(
                [41.771562545, -87.653075829],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6c51b482ec4613003f1552dc05ff1662 = L.circleMarker(
                [41.693484249, -87.624054648],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_913415444445dc814bdaf2266c424389 = L.circleMarker(
                [41.968221339, -87.747722354],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a7a028387246120258e9539df203eb70 = L.circleMarker(
                [41.834196595, -87.664988254],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_82def14abc9bb014a72680429bba5469 = L.circleMarker(
                [41.772424314, -87.613016341],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8c87b1727e91f0cbc506e07b6d9cd41a = L.circleMarker(
                [41.849045571, -87.708829783],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1cefd0f56de22ba02ca2b7e34be7bd2e = L.circleMarker(
                [41.901905162, -87.684548444],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_43967ad08a683e2e2ff39233629fc0f4 = L.circleMarker(
                [41.780799978, -87.666675944],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_87dbf4dd19144bba9ab72e5ed91d6a51 = L.circleMarker(
                [41.941440161, -87.674719881],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_762f778f86b239527bb7d9078c98ef95 = L.circleMarker(
                [41.902437713, -87.687011559],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d2cf9e3f48d5564f9681ec4179282a17 = L.circleMarker(
                [41.889112403, -87.701439693],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bb59a55f8a902367cd93b30f25387805 = L.circleMarker(
                [41.861628294, -87.716500973],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f7328c34123ce06e91e2ea5ba305bb88 = L.circleMarker(
                [41.815071052, -87.633532754],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b2b715354e34ac22db8a1abeaa522873 = L.circleMarker(
                [41.828256319, -87.69558452],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_28f47087b7781fa9131ce8cc033dfbcc = L.circleMarker(
                [41.826052399, -87.672715493],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b9e69c9bd640c9781477aead759227c1 = L.circleMarker(
                [41.768310521, -87.624917247],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_25156024acfa77ceef79656038209a2b = L.circleMarker(
                [41.929700376, -87.648910326],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7ec186a9ed17b22775a36af84ed793c1 = L.circleMarker(
                [41.944006745, -87.663934529],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7541488f99b5792f75e87075b9d78cbc = L.circleMarker(
                [41.961346137, -87.773382909],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_72d4c2ee35f6b8bdaef279defdc0f96e = L.circleMarker(
                [41.852368074, -87.664340305],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_eb6c692f37a138469aec67a8c9e59394 = L.circleMarker(
                [41.80215809, -87.612052585],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e8fb26b6c75bc5b3bd6ea4966057877c = L.circleMarker(
                [41.780349946, -87.68733707],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_80211d42d65c036a9a998f115e438c51 = L.circleMarker(
                [41.89922365, -87.623259112],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_577f3d8633783cb7d7f3a2f4ef5c669d = L.circleMarker(
                [41.73667328, -87.659438285],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ef4867e4b6b9bd139b631c6748c5a743 = L.circleMarker(
                [41.736148121, -87.629070243],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4d4b24be11b7c892f02b3d136bdb9601 = L.circleMarker(
                [41.863174623, -87.63028816],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_026f6c71702226fd00f5fa55855d798f = L.circleMarker(
                [41.810721851, -87.729886746],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5508bb95c864fb4a277763d2f254c8cb = L.circleMarker(
                [41.859818368, -87.653066321],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d4e340d7151a3e19df07332ca696e4b0 = L.circleMarker(
                [41.808210113, -87.606534087],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_962df55e470eb74833785347b2e8c210 = L.circleMarker(
                [41.768833001, -87.584412494],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_16c32a33f0b169729ade9b087866f0af = L.circleMarker(
                [41.792296538, -87.622401614],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_638621f62f5c1aaba9d99bda3f6cecd5 = L.circleMarker(
                [41.795265307, -87.663405235],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1a8729bafffbdb27d91d5d18562a50da = L.circleMarker(
                [41.926831492, -87.759371576],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_522e166e1eaecd11a34691c0f11374cf = L.circleMarker(
                [42.004183649, -87.762896932],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cb80eabd4d6e67bc12bed75ed385c175 = L.circleMarker(
                [41.852889008, -87.668511943],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c43d4037df0a7c9d672878db8d8b3627 = L.circleMarker(
                [41.953436358, -87.746273229],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5cf8d9a8e895f0eae7ab3a26dc354143 = L.circleMarker(
                [41.759782914, -87.605427789],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ed93afce79018e47a4a1d381075652eb = L.circleMarker(
                [41.787727659, -87.685088587],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3eefd3f8009b9036107773063807af8f = L.circleMarker(
                [41.926161575, -87.802662337],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_73e52a805479213bcf7baf33a3c96db2 = L.circleMarker(
                [41.975874105, -87.807052779],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f78c1a4c08e98be725fee7cbe1cc4635 = L.circleMarker(
                [41.755412283, -87.562256233],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d95c8fb52cb11b9a5b0db6fb0ebb2ecb = L.circleMarker(
                [41.757630995, -87.585708249],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0f4b7e364057579a985222e3cdef9e97 = L.circleMarker(
                [41.966356855, -87.656195766],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_762afbe3da35bb306da9edc2e3402b71 = L.circleMarker(
                [41.771117937, -87.693185122],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_166c15baf7ad385a0119b240f10cb5bb = L.circleMarker(
                [41.896425594, -87.717565664],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b27772013911b2e47878e97b648a268f = L.circleMarker(
                [41.984756469, -87.65522475],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6b6600447b0dee1cf6b56fb9d40b78bd = L.circleMarker(
                [41.739477344, -87.624222953],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_decfeff0e2243a307db2518fbab77c93 = L.circleMarker(
                [41.768011368, -87.573381014],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ee1a32b9360d03782e9df8f40f18d6db = L.circleMarker(
                [41.692669318, -87.616997089],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8f15e70ae6ed30e5deee8c7ca79b2d64 = L.circleMarker(
                [41.882914412, -87.694721785],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_21220928d01d6e05c0bd99236615af80 = L.circleMarker(
                [41.742506796, -87.664452263],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c43c7e37c0d15535089e8fc2c2fc9b96 = L.circleMarker(
                [41.894353346, -87.717501093],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b2e866805532caacb55829526cfc1822 = L.circleMarker(
                [41.862000933, -87.706761745],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e1d6e029b5f930ad984520a9d80c7604 = L.circleMarker(
                [41.707099379, -87.628599988],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_118c7d789c6cff4530471e5fe31614fc = L.circleMarker(
                [41.746032049, -87.585051315],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_892da4076b301eebb43bed76505dce20 = L.circleMarker(
                [41.756064436, -87.632356295],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bb80b1a3cd7e8a49c96d26d966e43ead = L.circleMarker(
                [41.96558038, -87.761123474],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c386b021c7dfe24ee9a3a4ca456d99db = L.circleMarker(
                [41.895383688, -87.724425762],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_97fb33db654585c2f33b7a0fb2110601 = L.circleMarker(
                [42.017877621, -87.684452879],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_fdbf2aa7932e4e4d6b574ac393313d5a = L.circleMarker(
                [41.972771638, -87.796649159],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_50206c586a79fecaf1fd1ac4f6b1412c = L.circleMarker(
                [41.899927469, -87.723780187],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1b44412bbccae6d02741ab6f491abeb2 = L.circleMarker(
                [41.763024779, -87.633387493],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5b52945149ead6664d850d459106362f = L.circleMarker(
                [41.924037319, -87.761461754],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_aca25960ca3047ebfa41486f9c913dca = L.circleMarker(
                [41.823042962, -87.68057571],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_61a1de63022ed4b9d78763a9b4b393db = L.circleMarker(
                [41.656298529, -87.597010402],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1219b781623cd79e0c2a3dd9c6234346 = L.circleMarker(
                [41.9916184, -87.658263925],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c03c7b9f1c32916544d9388d59ddaffb = L.circleMarker(
                [41.743283936, -87.606691467],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5e8f4def3dfbf46e683c08025ff62612 = L.circleMarker(
                [41.928753945, -87.6700069],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f089b9a55cc1f8372c5254bb786c69db = L.circleMarker(
                [41.915729613, -87.746056778],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_86e6f89ea502f5b47c1beeeb6b554a36 = L.circleMarker(
                [41.851101943, -87.722265596],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1e0aeff6b4d1177ef4fd5582d3867f49 = L.circleMarker(
                [42.019232277, -87.66703966],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e6abf181cc3d90449835c18220e15070 = L.circleMarker(
                [41.751336731, -87.558951782],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bc89a269754f3b38dad8be6badc8a59f = L.circleMarker(
                [41.893049197, -87.684979649],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8ed38737f6c5d97360124a4cc1fb6f4a = L.circleMarker(
                [41.972526031, -87.753478508],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a1bebbb552542c0cbf7249c0ae2f4de4 = L.circleMarker(
                [41.770749314, -87.702950943],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_46092ba64261ad73daf592fbe2649e11 = L.circleMarker(
                [41.761746531, -87.705186955],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3df3a0ba1ffb37c22d74fd3c1cf764bc = L.circleMarker(
                [41.924639878, -87.714145265],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3f14763a1d455f9ad2ac970a631a6a6a = L.circleMarker(
                [41.904522401, -87.773016431],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c3c5fff4381c71ffa1407ed40c8017e3 = L.circleMarker(
                [41.958474197, -87.65087832],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_398e076092c354f3a0328cfc2fed8c93 = L.circleMarker(
                [41.749675058, -87.634503664],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9dfada527acfa6a347c399eb151520da = L.circleMarker(
                [41.877439615, -87.636656859],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8d3baed3445f30f3e65b45a775d3a2d8 = L.circleMarker(
                [41.777168301, -87.652008383],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e817941c3637f9fe0ee131338b57413e = L.circleMarker(
                [41.880932451, -87.760142384],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a4fcb005eb13a8ac6b454fe8f6dc2e5a = L.circleMarker(
                [41.858489603, -87.71766176],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_84e2b78660a1a6e5e9472e98fa00b62f = L.circleMarker(
                [41.877585867, -87.683123746],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_aac58aa06b40d1a8e74e0f770d3df92d = L.circleMarker(
                [41.858508309, -87.703899533],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a1d04649ce2f1f23d22e15f3fc2103cb = L.circleMarker(
                [41.797157302, -87.704390201],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b765d8c384fc0c8574e9d5bcceaf2234 = L.circleMarker(
                [41.873635421, -87.710081187],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b483c1ca5b430466e3e1cce0b57d61e3 = L.circleMarker(
                [41.956806543, -87.670694015],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6c4d88e3d87016d9ac16a37dac8589af = L.circleMarker(
                [41.756351018, -87.583428802],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3bde03b527b3702b6582bbb926254161 = L.circleMarker(
                [41.860911204, -87.695744714],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9ac628b182035b48c222cf5abcca02c8 = L.circleMarker(
                [41.932856636, -87.642107024],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9ad633a28fee2b83abc1822223aa20d6 = L.circleMarker(
                [41.964231677, -87.649978542],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9c18a87986ebede3078f1c66455147a7 = L.circleMarker(
                [41.963626209, -87.653382451],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9f5b3f9c69765167bddbd0f6bdff2123 = L.circleMarker(
                [41.867293196, -87.711552595],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f0ad118850cc29cbcdc542fbfd7ff00e = L.circleMarker(
                [41.765014339, -87.656740878],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_066e5fb2cc7cafe80bfdd3cde215f39d = L.circleMarker(
                [41.929865972, -87.647688475],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a870e28a1a5692403a59f97e4bab2dbc = L.circleMarker(
                [41.764293597, -87.580162023],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e87e818e93c5c2dce93c36902e897bdb = L.circleMarker(
                [41.732976618, -87.606305726],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1ff23ddf12ef430d9cebe1e3fa32f5ed = L.circleMarker(
                [41.870867709, -87.713860414],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_52c9080de48ecce707ed8cbb64f18b1b = L.circleMarker(
                [41.884110362, -87.700075138],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a43aaf254e273e1b67598f188bc3bc38 = L.circleMarker(
                [41.88465574, -87.625238257],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9bd3ff50cd50ed966a91e02ed3916daf = L.circleMarker(
                [41.767282365, -87.686984316],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2caa62a1f52791e0c301e130fc35308e = L.circleMarker(
                [41.762410973, -87.671037519],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_59ae91ba65fed11a3f34996cefd0db72 = L.circleMarker(
                [41.789546441, -87.801429076],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_472385e8f5f4322db92203d098219714 = L.circleMarker(
                [41.882350368, -87.756681491],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_beb85035a3cdf589008610c0d2f4b821 = L.circleMarker(
                [41.72251071, -87.642025379],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9ad12c6e4a394a4450186c7aa269e94a = L.circleMarker(
                [41.728685281, -87.585472463],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0287a0214fec86a63507396a63cc16ba = L.circleMarker(
                [41.74693632, -87.710377352],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_28211913b69e935905d67db143e96771 = L.circleMarker(
                [41.770469009, -87.637280329],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9939aa0fee2ec98d78055bbeceb9469b = L.circleMarker(
                [41.900853597, -87.725582308],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6d8a043674da8e5bf1db49fe97276902 = L.circleMarker(
                [41.794796091, -87.674327426],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c5ef333296eccaefc6e81afd94dc3c1b = L.circleMarker(
                [41.945603374, -87.728112866],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5f19131c6d4fdb6a4e7756d965ad2415 = L.circleMarker(
                [41.721439376, -87.614131833],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ad8b5fa3fcd6be14d98539ccb7ab7d27 = L.circleMarker(
                [41.79050194, -87.634053068],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e42ac0ac5090fb6ddea1a6cf7c2ee456 = L.circleMarker(
                [41.756187925, -87.57364146],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_39ff23a60221ba92e4f814f0e16baf84 = L.circleMarker(
                [41.882060519, -87.62760243],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_837cb2a9c2acd5c973d30b00d4037b3e = L.circleMarker(
                [41.806745172, -87.74680009],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c58388fecac822b8489669d63fe65bb0 = L.circleMarker(
                [41.833533963, -87.646170991],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f386c2054359b016f3c504ab7a6fe7de = L.circleMarker(
                [41.660989993, -87.645516321],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5df64a03a4bdaa6e0325e0ccf2f93885 = L.circleMarker(
                [41.897895128, -87.624096605],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_db96ac7de9a3901982e6b12bb3084253 = L.circleMarker(
                [41.739004946, -87.64491897],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1884f819b705ad819728940a869767a7 = L.circleMarker(
                [41.897712122, -87.678291519],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4a0f647d4eaabcc419e92c59cc429980 = L.circleMarker(
                [41.785519673, -87.738567526],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_527ca09ec915bffca01143955aae8a34 = L.circleMarker(
                [41.765318105, -87.583654287],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a1f1f296e4fe9bd9b8467fc0d5f0cac9 = L.circleMarker(
                [41.762668947, -87.650413405],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6639629323ab5c534abe1035a67b4aaf = L.circleMarker(
                [41.735645619, -87.610899397],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ee5260fa0be864641686037733b99ed3 = L.circleMarker(
                [41.715834721, -87.649521263],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_83972521cb35c38cac627fa0009a3267 = L.circleMarker(
                [41.875744032, -87.755951435],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_354b6ee57311fc27a6c88fbe2d486334 = L.circleMarker(
                [41.928487179, -87.648868172],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4c6e97da673e203489bc0136bf87145c = L.circleMarker(
                [41.75607377, -87.607778656],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8718f616d9d86adaba0c3fb98c37c5eb = L.circleMarker(
                [42.006036283, -87.661054978],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d9f1a012c266a247fe85439c3f8029b4 = L.circleMarker(
                [41.736259984, -87.628068782],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a6215e9b4d08192a1dfb9a4a1534d4cc = L.circleMarker(
                [41.799283276, -87.752706766],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3de5930010b7984e2969503f7cf90aa8 = L.circleMarker(
                [41.957297846, -87.747421631],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3357ff175fec1deecfb4cab4d8325766 = L.circleMarker(
                [41.808193033, -87.699572578],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8b500d09e99bbeb4bf92732f0a620c75 = L.circleMarker(
                [41.86586383, -87.708086073],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d3580d7863ca543e70a165994a68343a = L.circleMarker(
                [41.851746966, -87.631987943],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e5bede0cfdf232d834de68d5f552b61f = L.circleMarker(
                [41.802240107, -87.606777604],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0f5335c6b08dc6681803a1e9c59b759a = L.circleMarker(
                [41.707298382, -87.614648361],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d1857f9e67213f81bc49516582337164 = L.circleMarker(
                [41.903838027, -87.635561788],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_82a02a3e67bbf1be20aed53766258854 = L.circleMarker(
                [41.939870181, -87.722315651],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5318947638f2b8c40ea568fac067cf2b = L.circleMarker(
                [41.843471238, -87.690295454],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_89962dea3756c246f3bf2065cb5c787e = L.circleMarker(
                [41.944872304, -87.731556663],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cfeba79b7914cd8e97c93c9bbf13e669 = L.circleMarker(
                [41.858233936, -87.727380936],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_73912bc858cc6694f5d8a16913d41861 = L.circleMarker(
                [41.964291084, -87.656765502],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_32c2541fe526acc705c5b56d40df0bfc = L.circleMarker(
                [41.965455019, -87.653116647],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3c6924741b25e9b4b8f89099db766f90 = L.circleMarker(
                [41.81943906, -87.623106676],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9c830da62efa7282a99077dc31e76046 = L.circleMarker(
                [41.966419743, -87.687104335],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b5ce18604fee0cf30f95e2200c953eed = L.circleMarker(
                [41.913175448, -87.711783489],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b3fe84056225faef61333465230da04c = L.circleMarker(
                [41.927177003, -87.704316385],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6adcf17a8ac15649ad311bf6d48c5794 = L.circleMarker(
                [41.854807142, -87.684327237],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_da61eda3200cea6dbbd49a4e20d63243 = L.circleMarker(
                [41.9518807, -87.724208167],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_195607a7712dc1a4305561ff4e42f7fb = L.circleMarker(
                [41.733123316, -87.551330284],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2e4b67e520927f6618e4a65b0c569aeb = L.circleMarker(
                [41.849131083, -87.706391857],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_de00226188d7b67819c69458b8155efe = L.circleMarker(
                [41.699773106, -87.631466621],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_23cf29f5bf2dc461ef7a76be84f0fb8e = L.circleMarker(
                [41.789608278, -87.77682713],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7f782fb708e9b5c5a867f70d70876a32 = L.circleMarker(
                [41.795134094, -87.648598307],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0bfe7c04248d7720100e70941a7b4b8f = L.circleMarker(
                [41.881738489, -87.751259495],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_696f5a440bdeebf8f36c336ba07950ca = L.circleMarker(
                [41.773109884, -87.586294711],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1ebb2189b4d3f4ed32151eff3dd5e1d8 = L.circleMarker(
                [41.800183156, -87.706198045],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a8505c6276513778b96d1d1b6b53e5db = L.circleMarker(
                [41.728606433, -87.629914617],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b4f6e3f806af3c04e35e6794c327b57c = L.circleMarker(
                [41.774053355, -87.61547635],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_65cae59ec1806aa5602660b1be70a67c = L.circleMarker(
                [41.814997162, -87.745176752],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_54c74b1b14b4df5b18e31c56ae2a26e3 = L.circleMarker(
                [41.702214417, -87.563979733],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1546ab1bb7f7c5b54a966ffc4adf8faf = L.circleMarker(
                [41.936335635, -87.650710119],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9fd5f98dcd4dd32fbb75de1fd424e3de = L.circleMarker(
                [41.757122147, -87.646634887],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bf8e464db5d164c58c3a6adb84e3d979 = L.circleMarker(
                [41.736899333, -87.664308936],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_79f9e9efa6e779aaec7cb5c35b345a97 = L.circleMarker(
                [41.759383704, -87.618333785],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e2235dc1bb8e3702b1e6b2115e7ab944 = L.circleMarker(
                [41.781047752, -87.76428493],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3d23d6b824e641cf8cd9540412a0d39a = L.circleMarker(
                [41.852510867, -87.730264924],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d6ecbd1d851da67f874d376c5c7372ac = L.circleMarker(
                [41.885487535, -87.726422045],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_911b46b2e23d0250fa862e9f76bdcd7b = L.circleMarker(
                [41.823848842, -87.615999036],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4ad6891a0412121b153d74abab6fe13b = L.circleMarker(
                [41.916124853, -87.730188129],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ed07a15eed09d247b3fe39e1a7a22d23 = L.circleMarker(
                [41.904192368, -87.647000785],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_718f7d8168358c5ffc13c8e247eec41b = L.circleMarker(
                [41.906822127, -87.7239938],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_eebe9a4a48432aa18d0b0872295d332f = L.circleMarker(
                [41.705888742, -87.622299653],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c4ed577684a5e224320dacd947faf677 = L.circleMarker(
                [41.764014937, -87.662744409],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5025dc85876c85a0ed17ce924e21373b = L.circleMarker(
                [41.837887206, -87.65787839],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c5b76e4074801402794777b67e245d35 = L.circleMarker(
                [41.748439329, -87.63482489],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b79463a731ec02041d26b1eafabbcf8f = L.circleMarker(
                [41.91357685, -87.798592911],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d82a5df37f0dd3819d1fca32f9ecb863 = L.circleMarker(
                [41.804270279, -87.64867709],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f4c6dd6557cfc6877297a4edb783e39d = L.circleMarker(
                [41.895226353, -87.634164316],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b705b6d155e032aff0708ec335371848 = L.circleMarker(
                [41.986935361, -87.66505191],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_231b094caf9e8c503ee8480598f64131 = L.circleMarker(
                [41.793938009, -87.645453608],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_542aa06bed204263feb247416f4f511d = L.circleMarker(
                [41.76105267, -87.643085297],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_26192a95a9606b223faac739ef85eba8 = L.circleMarker(
                [41.793192941, -87.663331471],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_69b5489701f437009e2b4fac8c3a0797 = L.circleMarker(
                [41.896009303, -87.728566644],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8619461b3ab67f3916269b3198f40037 = L.circleMarker(
                [42.019374219, -87.671653016],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ce18a5e57a6b73361ff8b5c824a38a71 = L.circleMarker(
                [41.746834554, -87.601422217],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_44a55fa8e7875d3aa620f5e88bafee0c = L.circleMarker(
                [41.745368292, -87.602589491],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7b1549957c2ee0e6b8af2a67f017cef4 = L.circleMarker(
                [41.793218316, -87.693783034],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d38d9a7f387dcf9a54af218bdb7cb760 = L.circleMarker(
                [41.880775433, -87.627029031],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d986939e75c3805036ab0e7d293a6489 = L.circleMarker(
                [41.699915041, -87.620197668],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5ebab1e9c8dcfe695043397fd61faa19 = L.circleMarker(
                [41.882834439, -87.702595884],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0793ce63027f9617ed912d2a445dc2ed = L.circleMarker(
                [41.929644221, -87.684131464],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cb2ba2f0783a3ca2882bfbc104b455ea = L.circleMarker(
                [41.89318177, -87.6345943],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f7bcb3bce5980068a8c6ed538330a02b = L.circleMarker(
                [41.994848863, -87.700759019],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e8332f70f4c420db724f6efb60aef0f4 = L.circleMarker(
                [41.649561966, -87.536242317],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d0ca766e4eae293002eac95e733ab846 = L.circleMarker(
                [41.750637034, -87.60643264],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3d0d4e7fa4e5a919ab7664c80a8c576f = L.circleMarker(
                [41.739338035, -87.691067904],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bd0f39457f6b071e27bb63480374b59e = L.circleMarker(
                [41.821177006, -87.614854869],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_555a4f4a3e06ab48fdb9e9fe2d29c74a = L.circleMarker(
                [41.700051321, -87.537699023],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1fa899e4ff953ca1e51beefbb6f00b85 = L.circleMarker(
                [41.726636483, -87.551031632],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_463a4cda5e9f22574824319fdae1cc36 = L.circleMarker(
                [41.872336473, -87.718053942],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_350d2145f961835dd96ba1cee3aedc03 = L.circleMarker(
                [41.934285506, -87.642418688],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b63001db928489fad81c3aee9eb799fe = L.circleMarker(
                [41.91573969, -87.732620361],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b2c4b7662955403f99ec18f93d3b403e = L.circleMarker(
                [41.780247905, -87.615146952],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9d188ea7b2a585d788f8e24a8e69bc3b = L.circleMarker(
                [41.836877375, -87.72465408],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b6f5645615e46cbd3625710fb8bd5cb1 = L.circleMarker(
                [41.869146271, -87.704624937],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_190835961b779b5c9748b233ac802377 = L.circleMarker(
                [41.88233367, -87.627841791],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f6f4092e61f8e0531dffefa46c7c26dd = L.circleMarker(
                [41.943203768, -87.734696711],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_57bdf98c394678b26599dddabd881f81 = L.circleMarker(
                [41.968101258, -87.74089867],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9ac44af4c77c55efd0b37f7bce1375b8 = L.circleMarker(
                [41.744799407, -87.60505473],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e8ad61f33d874ed765f3c969894affff = L.circleMarker(
                [42.018154229, -87.669005007],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6bce98a8bff6dce7820fd5af168adc9b = L.circleMarker(
                [41.801220544, -87.621008323],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0e2578e61c42595945fb8b8510038716 = L.circleMarker(
                [41.681610873, -87.628288785],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_202f4303449402b9069408fa0fdfa8da = L.circleMarker(
                [42.0159781, -87.675198844],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_67f89e53a3c2a7822e44bd940ab7777a = L.circleMarker(
                [41.936051054, -87.700182684],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5f7ca1c58913ca8821e811b0393c54c3 = L.circleMarker(
                [41.861559271, -87.65976218],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_0e9ab438567788b519ef622fb2569671 = L.circleMarker(
                [41.896588511, -87.668529054],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b88dfdd4eb3ee68acf0fa86160e8c9b1 = L.circleMarker(
                [41.890824298, -87.71495675],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_de2ad48d4a2e4d7a44a8777057f7a6b9 = L.circleMarker(
                [41.809297059, -87.591967028],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_60e59ad731337f7ff44af8dd4c555ee4 = L.circleMarker(
                [41.9059766, -87.74713069],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9491084cb75885214e03491e8fb00cec = L.circleMarker(
                [41.77446642, -87.628559557],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bd0c10163e9b83261c35e01ecf241866 = L.circleMarker(
                [41.778864596, -87.6642029],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5ad5cc56e9a163891f6f58a778846f8b = L.circleMarker(
                [41.786388084, -87.648603379],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a750b6ecb9bf61db08ee33228b622fed = L.circleMarker(
                [41.892753031, -87.624193896],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_17c89026641f481ff263cd3c2d59e9fc = L.circleMarker(
                [41.949345425, -87.666496033],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3ec34bffb357f40e0071f96cee0d0c48 = L.circleMarker(
                [41.881173546, -87.737949377],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1c870dd172112f40f08d5c248225ce17 = L.circleMarker(
                [41.893990113, -87.702155577],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1aad5e91d1c751355081202e052473f4 = L.circleMarker(
                [41.784549833, -87.650980582],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_6531efca748f4fe4147152cac6914263 = L.circleMarker(
                [41.800610439, -87.591814105],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_8f89c1ce87cbd74490caa0f10cc6b09f = L.circleMarker(
                [41.96137851, -87.65474101],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d39d3306980d43724b5fdf53cb734b37 = L.circleMarker(
                [41.95208984, -87.647891491],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_724962fb8d2b5c3794f02f0da35930a5 = L.circleMarker(
                [41.794533814, -87.631438536],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bae365570008e56317da567ca4fae0a9 = L.circleMarker(
                [41.751164599, -87.612198632],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2e4641fa802c5e1d3ea7cc9f5b3c095b = L.circleMarker(
                [41.796553275, -87.691439468],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_91c86415750b691cf17117a1e2192bf6 = L.circleMarker(
                [41.770791156, -87.588015234],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e87645b02d530a35a9eb2456fd77be63 = L.circleMarker(
                [41.803223633, -87.727121973],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3d4e6b1b8d7c3dbb3e0371f24fda6e1e = L.circleMarker(
                [41.698451226, -87.536488407],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e6d3538f1a22fd41161590bc6d1d2227 = L.circleMarker(
                [41.951696764, -87.787481069],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_27f2007a4fb9ba6bd34c8010e6039eb5 = L.circleMarker(
                [41.689874933, -87.62219411],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5c078b47cda9181121712719234c3747 = L.circleMarker(
                [41.759485715, -87.612699239],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_13b91384b172fb73a15158d6adbf8076 = L.circleMarker(
                [41.838593883, -87.735885511],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_914e438fddcae63dd424d316ca314a70 = L.circleMarker(
                [41.972241055, -87.656302604],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_15a6a6755b390eea109cf4236cb41358 = L.circleMarker(
                [41.930667898, -87.696395556],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1a4f6e656bf323e4efa5298913151021 = L.circleMarker(
                [41.900527585, -87.644046325],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d0b0dcbbcf521b0387ba0499e8baa133 = L.circleMarker(
                [41.913225827, -87.680315266],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3c0352812c74d36eff23047915ece9ca = L.circleMarker(
                [41.886024969, -87.769961033],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2669b00fa28e287b6f4931203b0b0db6 = L.circleMarker(
                [41.908467485, -87.768305283],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7aa868d3c60238fa93022e3e994a8d91 = L.circleMarker(
                [41.944474619, -87.652961102],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5ffa552e50aae3c014a3d0baea395539 = L.circleMarker(
                [41.89411155, -87.675867473],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_002fb8fb3dc5a330247e6e7a9165c3f7 = L.circleMarker(
                [41.934368945, -87.678188525],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7c659eb5f05c39ba6e69f0b53f41dfc8 = L.circleMarker(
                [41.706070186, -87.653645803],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_e07b6dd1d8b3003971391f958738f974 = L.circleMarker(
                [41.732384977, -87.585107147],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_567db837e7ccee5a8eac669a32d460d7 = L.circleMarker(
                [41.784042702, -87.606766759],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_81f4da2379bf5f4d1410610c0eff5b2b = L.circleMarker(
                [41.883144597, -87.647549246],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4ef1ab9daf40e449c05af73c640ec9ba = L.circleMarker(
                [41.888189539, -87.623777956],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_bd59d5e0b42507973e1f10cc45c69a51 = L.circleMarker(
                [41.941813684, -87.648045671],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a33b8e3a231b3c0620d1a5bb3facf315 = L.circleMarker(
                [41.908242144, -87.71041697],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2cebe7a9686b631dd87aa885ed851407 = L.circleMarker(
                [41.747817039, -87.712875387],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_575803ffd0db774f9624ff7105fff8ce = L.circleMarker(
                [41.897024418, -87.73691329],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_550f0cf1500c2f9d0cd1ca9858f243f9 = L.circleMarker(
                [41.70984209, -87.567858803],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_25e318ab484c38607d8ecac051f9eb0c = L.circleMarker(
                [41.671893527, -87.629690555],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_342d9ee78c0f0a1d668ee8e3200968b8 = L.circleMarker(
                [41.934396495, -87.804931514],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5fd29621597609736ad2f25e3030bc2a = L.circleMarker(
                [41.954808512, -87.706820422],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ed430d49467bb5003ed7a59a0ff85310 = L.circleMarker(
                [41.718624999, -87.538909468],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ffd1157d6093144461ac3fe6098d2a3c = L.circleMarker(
                [41.887192632, -87.624545521],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cf399a9dce44bc1298222c7f811dffb2 = L.circleMarker(
                [41.655365015, -87.605126361],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3e17aa3d8b5159fd5ab7a09ccb2a172f = L.circleMarker(
                [41.800538968, -87.598200112],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_7df1952bf1191b541b0ffb2af433acc8 = L.circleMarker(
                [41.904404863, -87.648118921],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_91a038f46b8b6679744dc94c8fcb35fb = L.circleMarker(
                [41.835175287, -87.656846415],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_44925cbe512e694ccb46236b0179aba9 = L.circleMarker(
                [41.886393351, -87.765080772],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_63da43aac8cb2b7b535899910b371c9c = L.circleMarker(
                [41.945238279, -87.712670479],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_5d8034cb091d73c255f61eff4e1a20a5 = L.circleMarker(
                [41.889778118, -87.750518091],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_57b8e57b4e0d4b3e7a39219ea9149f4a = L.circleMarker(
                [41.904192368, -87.647000785],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_3ddcf77f0ed681c2ea8c6570ee97f9f2 = L.circleMarker(
                [41.858726016, -87.664725558],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_c889b450ed3f3d90e6a5d67227c3e487 = L.circleMarker(
                [41.967169681, -87.718215967],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_adc3e9973ce6a1e1e5f1e9a070279ba3 = L.circleMarker(
                [41.962398697, -87.646324994],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_a3c95a1624eed28360707afb2faad3b7 = L.circleMarker(
                [41.93212776, -87.693422596],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cef9cc51a51f2e7391076aa9617b0079 = L.circleMarker(
                [41.883841714, -87.746627983],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9602550907431fc5ba1f67018ea6b38e = L.circleMarker(
                [41.884472413, -87.650245233],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1e97c8a94dc0c4c167cfb8ad50b812cd = L.circleMarker(
                [41.938636968, -87.64960867],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_f1d09b1cc2fed93b066f23a9d1daa4d6 = L.circleMarker(
                [41.881919907, -87.755121004],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_cbf6ec13bb1644db81626469d46ae7f5 = L.circleMarker(
                [41.732332334, -87.648393762],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_64d7fee2109511f54de7d6d5493a8ea6 = L.circleMarker(
                [41.688108834, -87.68553314],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d98e0a37075d81756f0e323475688518 = L.circleMarker(
                [41.8960672, -87.667597844],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_dd6de99ee57c5da261b66f6cf36d5736 = L.circleMarker(
                [41.782634781, -87.701437594],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_ceed4ba2faad7f5a8efc22661c3eec77 = L.circleMarker(
                [41.915757633, -87.754275574],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2d3dbf182f493259ee9c221bdc2fef2e = L.circleMarker(
                [41.923548381, -87.801328068],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1dc06ffcf2b73695294e120e5937ebe0 = L.circleMarker(
                [41.911674513, -87.78508513],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_d05f2b5ee4ad7ff2be00565b7f80c0b4 = L.circleMarker(
                [41.900771022, -87.626757289],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_559a5562321757ec099a322313a6d9e1 = L.circleMarker(
                [41.783778075, -87.687427324],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_2794a27f6c041408fae8485d65cad3a5 = L.circleMarker(
                [41.886868369, -87.74550589],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_4703a2d5e97b73610fddb373cb7e1eb7 = L.circleMarker(
                [41.956078254, -87.672889047],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_64140fff913e89f9fa26d8ee95a9dcf8 = L.circleMarker(
                [41.884469953, -87.650293],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_76d9ac6284a42c5f5d023a3151cd041c = L.circleMarker(
                [41.757614433, -87.586115266],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_1b629579557ee6f596aa8d15a66aa2c6 = L.circleMarker(
                [41.904867331, -87.764472487],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_b677762b9c468afc0528ff6f2ca359b5 = L.circleMarker(
                [41.750933717, -87.626270055],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_9bfcfbf23035ce41fb117d388680ebff = L.circleMarker(
                [41.678519693, -87.662497935],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_359b422fac29be2ffab4969faf97e8fa = L.circleMarker(
                [41.929597339, -87.678773892],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_725c6598f0e3014a26fc7fa884f4582d = L.circleMarker(
                [41.834095849, -87.670809065],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
    
            var circle_marker_513537b82b23df2a58eb394d50965799 = L.circleMarker(
                [41.770144861, -87.615376962],
                {"bubblingMouseEvents": true, "color": "blue", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "blue", "fillOpacity": 0.2, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 3, "stroke": true, "weight": 3}
            ).addTo(map_f31ce70f357afcff6520e0ee17497e19);
        
</script>
</html>icago_Crime_Map.html…]()

## 1. Data Preparation and Exploration
- **Dataset**: Used the "Crimes - 2001 to Present" dataset from the Chicago Police Department.
![plot6](https://github.com/user-attachments/assets/4fd91a11-29e5-45a2-8d27-68b00eb79810)

- **Data Cleaning**: Addressed missing values, inconsistencies, and formatted data for analysis.
![plot7](https://github.com/user-attachments/assets/d079b386-02e5-4816-a6b4-43b1a371ac8b)

- **Feature Engineering**: Extracted relevant features such as time, location coordinates, and crime types.
![plot0](https://github.com/user-attachments/assets/e08b8a97-db72-43fe-9a1d-1639eba6ae06)

## 2. Time Series Analysis with ARIMA
- **Model**: Implemented ARIMA(1, 0, 1) for time series forecasting of crime trends.
- **Stationarity Check**: Used the Augmented Dickey-Fuller test to ensure data stationarity.
- **Model Evaluation**: Assessed model performance and forecast accuracy using historical crime data.

## 3. Machine Learning Models
- **Classification Models**: Developed Decision Trees (DT) and Random Forests (RF) to classify crime types.
![plot01](https://github.com/user-attachments/assets/11682039-eb8b-4850-a9bd-2e5906a53ff5)

- **Feature Importance**: Evaluated and visualized the importance of features in predicting crime occurrences.
![plot1](https://github.com/user-attachments/assets/c09d7913-6f25-4c88-bee6-9424bd099a5e)

- **Model Evaluation**: Calculated precision, recall, and F1-score to measure model performance across crime categories.
![plot2](https://github.com/user-attachments/assets/d98d1a31-328d-45fa-85c1-ed9b18e7c689)

## 4. Data Visualization and Insights
- **Visualizations**: Created charts (bar charts, line graphs, maps) to illustrate crime trends, geographical hotspots, and seasonal variations.
![plot8](https://github.com/user-attachments/assets/d5ae4b28-c57a-4167-920f-544eeef5ec29)

- **Insights**: Analyzed spatial-temporal patterns in crime data to identify high-crime areas and understand factors influencing crime rates.
![plot9](https://github.com/user-attachments/assets/66b34251-9e1b-42a6-8ac9-76305ff00e3a)

![plot12](https://github.com/user-attachments/assets/fca28832-9957-4438-ab65-5ca0efe740c1)

## 5. Documentation and Reporting
- **Notebooks**: Used Jupyter notebooks for detailed analysis steps, including data exploration, model training, and evaluation.
- **Scripts**: Python scripts for data preprocessing, model building, and visualization.
- **Results**: Stored model outputs, visualizations, and performance metrics for documentation and future reference.

## Conclusion
This Python-based project enhances understanding of crime dynamics in Chicago through data-driven insights and predictive models. By leveraging machine learning and statistical techniques, it aims to support informed decision-making in public safety and urban planning.
