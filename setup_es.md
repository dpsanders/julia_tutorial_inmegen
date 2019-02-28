## Correr Julia en línea: JuliaBox
La forma más fácil de correr Julia es en línea, utilizando el servicio [JuliaBox](http://www.juliabox.com).
Este provee una versión en línea de una [Jupyter notebook](http://www.jupyter.org), que se usará durante el curso. Se utiliza `Shift-Enter` para ejecutar una celda.

Una alternativa es [CoCalc](http://www.cocalc.com), que permite la edición simultánea de las notebooks por distintas personas.

## Instalar Julia y Jupyter localmente
Para instalar Julia y Jupyter localmente en sus computadoras, se siguen los siguientes pasos.

[Nota que *no* es necesario instalar Anaconda de manera separada; Julia hará esto por ti.]

1. Descarga e instala la versión estable de Julia (1.0.3) desde [aquí](http://www.julialang.org/downloads) para el sistema operativo que uses.

2. Corre la copia de Julia que instalaste.

    Ejecuta los siguientes comandos en la teminal del entorno de Julia ("REPL"), en donde veras un `julia> `.

3. Si usas Linux, primero teclea:
```jl
julia> ENV["JUPYTER"] = ""
```

4. Ahora instala el paquete IJulia, que automáticamente instalará Jupyter (usando `miniconda`):
```
julia> Pkg.add("IJulia")
```

5. Abre la libreta como sigue.
```jl
julia> using IJulia
julia> notebook()
```
Por default, notebooks nuevas serán creadas en tu directorio principal. Abre o crea una carpeta diferente de tu preferencia para guardarlos en la locación de tu elección.

6. Instala algunos otros paquetes que usaremos durante el curso (Necesitaras una conexión a Internet):
```jl
julia> packages = split(
    """Plots Interact
    BenchmarkTools
    """)    

julia> using Pkg

julia> for package in packages
    Pkg.add(package)
end
```
## Poniéndose al día con la sintaxis básica de Julia

Si no has tenido un acercamiento a Julia, puedes usar [este video tutorial](https://youtu.be/4igzy3bGVkQ) para ponerte al día con la sintaxis basica de Julia, en particular las notebooks del 1 al 8 (incluyendo "Plotting"). Las libretas están disponibles directamente en JuliaBox o [aquí](https://github.com/JuliaComputing/JuliaBoxTutorials/tree/master/intro-to-julia).

Sugerimos que añadas a favoritos, descargues o incluso imprimas los siguientes "acordeones" que resume la sintaxis basica de Julia:
- [Resumen de una página por Steven Johnson](https://github.com/stevengj/1806/blob/master/julia/Julia-cheatsheet.pdf)

- [Resumen más detallado](https://juliadocs.github.io/Julia-Cheat-Sheet)

Existe una siempre creciente lista de recursos (principalmente en inglés) para aprender Julia, disponibles en la [página de aprendizaje de Julia](http://www.julialang.org/learning) de Julia; en particular revisa [QuantEcon lectures](https://lectures.quantecon.org/jl).


## Julia IDE: Juno

Existen dos IDEs (Integrated Development Environments) disponibles para Julia: Juno, basada en el editor de texto [Atom](https://atom.io/), y una extensión de Julia para el editor Visual Studio Code.

Descarga Atom e instale el paqeute `uber-juno`. Más información está disponible en [Juno IDE homepage](http://junolab.org/).


## Preguntas y comentarios
Por favor contactar a [David](dpsanders@ciencias.unam.mx) si tienes alguna duda o comentario.
