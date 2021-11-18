# CristianGarridoSalinas.github.io
<!DOCTYPE HTML>
<html>

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tour 360</title>
    <link rel="stylesheet" href="css/pannellum.css">
    <script type="application/javascript" src="js/vendor/pannellum.js"></script>
    <style>
        #panorama {
            width: 960px;
            height: 540px;
        }
    </style>
</head>

<body>

    <div id="panorama"></div>

    <script>
        
        pannellum.viewer('panorama', {
            "default": {
                "firstScene": "circle",
                "title": "Santuario de la Virgen del Tránsito de Metrenco",
                "author": "CG",
                "horizonRoll": -1,
                "sceneFadeDuration": 1000,
                "compass": false
            },

            "scenes": {
                "circle": {
                    "title": "Frontis",
                    "hfov": 300,
                    "pitch": 15,
                    "yaw": -7,
                    "type": "equirectangular",
                    "panorama": "/images/santuario-frente.jpg",
                    "autoRotate": 1,
                    "autoLoad": true,
                    "hotSpots": [
                        {
                            "pitch": -10,
                            "yaw": -58,
                            "type": "scene",
                            "text": "Costado",
                            "sceneId": "house"
                        },
                         {
                            "pitch": -10,
                            "yaw": -5,
                            "type": "scene",
                            "text": "recepción",
                            "sceneId": "virgen"
                        },
                        {
                            "pitch": -30,
                            "yaw": -5,
                            "type": "info",
                            "text": "Comunas Mágicas",
                            "URL": "https://comunasmagicas.cl/padre-las-casas/"
                        }
                    ]
               },
                
                 "virgen": {
                    "title": "Recepción",
                    "hfov": 110,
                    "yaw": 0,
                    "pitch": 0,
                    "type": "equirectangular",
                    "panorama": "/images/9.jpg",
                    "hotSpots": [
                        {
                            "pitch": 5,
                            "yaw": 4,
                            "type": "scene",
                            "text": "Frontis",
                            "sceneId": "circle",
                            "targetYaw": -7,
                            "targetPitch": 15
                        },
                        {
                            "pitch": 0,
                            "yaw": 115,
                            "type": "scene",
                            "text": "Interior",
                            "sceneId": "coco",
                            "targetYaw": 0,
                            "targetPitch": 0
                        },
                        {
                            "pitch": 0,
                            "yaw": -115,
                            "type": "scene",
                            "text": "Interior",
                            "sceneId": "coco",
                            "targetYaw": 0,
                            "targetPitch": 0
                        }
                        
                    ]
                },

                "house": {
                    "title": "Costado",
                    "hfov": 100,
                    "yaw": -10,
                    "pitch": 20,
                    "type": "equirectangular",
                    "horizonRoll":1,
                    "panorama": "/images/santuario-costado-1.jpg",
                    "hotSpots": [
                        {
                            "pitch": -0.6,
                            "yaw": 30,
                            "type": "scene",
                            "text": "Frontis",
                            "sceneId": "circle",
                            "targetYaw": -7,
                            "targetPitch": 15
                        },
                        {
                            "pitch": -5,
                            "yaw": -8,
                            "type": "scene",
                            "text": "Interior",
                            "sceneId": "coco",
                            "targetYaw": 0,
                            "targetPitch": 0
                        }
                    ]
                },
                
                 "coco": {
                    "title": "Interior",
                    "hfov": 110,
                    "yaw": 10,
                    "pitch": 0,
                    "type": "equirectangular",
                    "panorama": "/images/santurio-adentro-centro-1.jpg",
                    "hotSpots": [
                        {
                            "pitch": -3,
                            "yaw": 109,
                            "type": "scene",
                            "text": "costado",
                            "sceneId": "house",
                            "targetYaw": -10,
                            "targetPitch": 20
                        },
                        {
                            "pitch": -3,
                            "yaw": 180,
                            "type": "scene",
                            "text": "Interior",
                            "sceneId": "pepo",
                            "targetYaw": 0,
                            "targetPitch": 0
                        }
                        
                    ]
                },
                
                "pepo": {
                    "title": "Interior",
                    "hfov": 110,
                    "pitch": 0,
                    "yaw": 5,
                    "type": "equirectangular",
                    "panorama": "/images/santurio-adentro-centro-3.jpg",
                    "hotSpots": [
                        {
                            "pitch": 10,
                            "yaw": 0,
                            "type": "scene",
                            "text": "",
                            "sceneId": "coco",
                            "targetYaw": 5,
                            "targetPitch": 0
                        },
                        {
                            "pitch": 40,
                            "yaw": 183,
                            "type": "info",
                            "text": "Obra de Digirolamo"
                            
                        }
                    ]
                }
            }
        });

    </script>
</body>

</html>
