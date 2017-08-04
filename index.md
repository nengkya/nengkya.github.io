# ThreeJs Game Engine


## Instalasi

   1. Download dan extract threejs game engine dari website resmi di  https://threejs.org/ 
   2. Copas file https://threejs.org/build/three.js dan taro satu folder pada script html / js yang nanti akan kamu buat.

## Membuat scene

   Untuk dapat menampilkan apapun dengan threejs, kita butuh 3 hal :
   1. sebuah scene (adegan/kejadian/event)
   2. sebuah camera
   3. sebuah renderer (penggambar)
   
   agar kita dapat menggambar(render) scene (event/kejadian) dengan camera tersebut.
   ```markdown
   <html>
    <head>
     <title> My first three.js app </title>
     <style>
      body{margin: 0}
      canvas{width: 100%; height: 100%}
     </style>
    </head>

   <body>
    <script src = "three.js"> </script>

    <script>
     var scene    = new THREE.Scene()
     var camera   = new THREE.PerspectiveCamera(25, window.innerWidth / window.innerHeight, 0.1, 1000)
     var renderer = new THREE.WebGLRenderer()   
     renderer.setSize( window.innerWidth, window.innerHeight );
     document.body.appendChild( renderer.domElement );
   ```
   Ada beberapa jenis view camera di dalam three.js. Salah satunya adalah PerspectiveCamera. Parameternya adalah

   a. 25 = the field of view (luas pemandangan). Angka semakin kecil, akan semakin zoom in.

   b. Attribute ke-2 adalah aspect ratio, rasio aspek antara lebar screen dibagi dengan tinggi screen.
      Agar tampilan tidak lonjong/gepeng wide screen.

   c. The next two attributes are the near and far clipping plane. What that means, is that objects further
      away from the camera than the value of far or closer than near won't be rendered. You don't have to
      worry about this now, but you may want to use other values in your apps to get better performance.

### Mempersiapkan object cubus berputar spinning

    var geometry = new THREE.BoxGeometry(1, 1, 1)
    var material = new THREE.MeshBasicMaterial({color: 0x00ff00})
    var cube     = new THREE.Mesh(geometry, material)
    
    scene.add(cube)
    
    camera.position.z = 5    //angka semakin kecil, semakin zoom in
    
   Untuk membuat kubus, kita perlu object BoxGeometry(panjang, lebar, tinggi).

## Rendering (menggambar) scene/kejadian/event









You can use the [editor on GitHub](https://github.com/nengkya/nengkya.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/nengkya/nengkya.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
