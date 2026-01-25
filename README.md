# ⚡ Boltons

*boltons debería ser parte de builtins.* 🔩

<!-- testing -->

<a href="https://boltons.readthedocs.io/en/latest/"><img src="https://img.shields.io/badge/docs-latest-brightgreen.svg?style=flat"></a>
<a href="https://pypi.python.org/pypi/boltons"><img src="https://img.shields.io/pypi/v/boltons.svg"></a>
<a href="https://anaconda.org/conda-forge/boltons"><img src="https://img.shields.io/conda/vn/conda-forge/boltons.svg"></a>
<a href="https://ports.macports.org/port/py-boltons/summary"><img src="https://repology.org/badge/version-for-repo/macports/python:boltons.svg?header=🍎 MacPorts"></a>
<a href="https://pypi.python.org/pypi/boltons"><img src="https://img.shields.io/pypi/pyversions/boltons.svg"></a>
<a href="http://calver.org"><img src="https://img.shields.io/badge/calver-YY.MINOR.MICRO-22bfda.svg"></a>

**Boltons** es un conjunto de más de 230 utilidades de Python puro con licencia BSD 🐍
con el mismo espíritu que — y sin embargo notablemente ausentes de —
[la biblioteca estándar][stdlib], incluyendo:

  * 💾 [Guardado atómico de archivos][atomic], incorporado con [fileutils][fileutils]
  * 📚 Un [OrderedMultiDict][omd] altamente optimizado, en [dictutils][dictutils]
  * 🔢 *Dos* tipos de [PriorityQueue][pq], en [queueutils][queueutils]
  * 🔄 Iteración [fragmentada][chunked] y [por ventana][windowed], en [iterutils][iterutils]
  * 🌳 [Iteración y fusión][remap] de estructuras de datos recursivas, con [iterutils.remap][iterutils.remap]
  * ⏰ Funcionalidad de retroceso exponencial, incluyendo jitter, a través de [iterutils.backoff][iterutils.backoff]
  * 🔍 Un tipo [TracebackInfo][tbinfo] completo, para representar trazas de pila,
    en [tbutils][tbutils]

**[Documentación completa y extensa disponible en Read The Docs.][rtd]** 📖 Consulta
las novedades [revisando el CHANGELOG][changelog]. ✨

Boltons está probado contra Python 2.6, 2.7, 3.4, 3.5, 3.6, 3.7, 3.8 y 3.9, así como CPython
_nightly_ y PyPy/PyPy3.

[stdlib]: https://docs.python.org/2.7/library/index.html
[rtd]: https://boltons.readthedocs.org/en/latest/
[changelog]: https://github.com/mahmoud/boltons/blob/master/CHANGELOG.md

[atomic]: https://boltons.readthedocs.org/en/latest/fileutils.html#boltons.fileutils.atomic_save
[omd]: https://boltons.readthedocs.org/en/latest/dictutils.html#boltons.dictutils.OrderedMultiDict
[pq]: https://boltons.readthedocs.org/en/latest/queueutils.html#boltons.queueutils.PriorityQueue
[chunked]: https://boltons.readthedocs.org/en/latest/iterutils.html#boltons.iterutils.chunked
[windowed]: https://boltons.readthedocs.org/en/latest/iterutils.html#boltons.iterutils.windowed
[tbinfo]: https://boltons.readthedocs.org/en/latest/tbutils.html#boltons.tbutils.TracebackInfo

[fileutils]: https://boltons.readthedocs.org/en/latest/fileutils.html#module-boltons.fileutils
[ioutils]: https://boltons.readthedocs.org/en/latest/ioutils.html#module-boltons.ioutils
[dictutils]: https://boltons.readthedocs.org/en/latest/dictutils.html#module-boltons.dictutils
[queueutils]: https://boltons.readthedocs.org/en/latest/queueutils.html#module-boltons.queueutils
[iterutils]: https://boltons.readthedocs.org/en/latest/iterutils.html#module-boltons.iterutils
[iterutils.remap]: http://boltons.readthedocs.org/en/latest/iterutils.html#boltons.iterutils.remap
[iterutils.backoff]: http://boltons.readthedocs.org/en/latest/iterutils.html#boltons.iterutils.backoff
[tbutils]: https://boltons.readthedocs.org/en/latest/tbutils.html#module-boltons.tbutils

[remap]: http://sedimental.org/remap.html

## 📦 Instalación

Boltons se puede agregar a un proyecto de varias maneras. Está la obvia:

```bash
pip install boltons
```
En macOS, también se puede instalar a través de [MacPorts](https://ports.macports.org/port/py-boltons/summary):

```bash
sudo port install py-boltons
```


Luego, [gracias a PyPI][boltons_pypi], docenas de boltons están a solo un import de distancia:

```python
from boltons.cacheutils import LRU
my_cache = LRU()
```

Sin embargo, debido a la naturaleza de las utilidades, los desarrolladores de aplicaciones
podrían querer considerar otras opciones, incluyendo la vendorización de módulos
individuales en un proyecto. Boltons es Python puro y no tiene
dependencias. Si el proyecto completo es demasiado grande, cada módulo es
independiente y se puede copiar directamente a un proyecto. Consulta la
sección de [Integración][integration] en la documentación para más detalles.

[boltons_pypi]: https://pypi.python.org/pypi/boltons
[integration]: https://boltons.readthedocs.org/en/latest/architecture.html#integration

## 🔌 Paquetes de terceros

La mayoría de los boltons se esfuerzan por ser "suficientemente buenos" para una amplia gama de
usos básicos, dejando los casos de uso avanzados a las [innumerables bibliotecas
especializadas de terceros][pypi] de Python. En muchos casos, el módulo ``boltons`` respectivo
describirá alternativas de terceros que vale la pena investigar cuando los casos de
uso superen a `boltons`. Si has encontrado una biblioteca de "siguiente paso" natural
que vale la pena mencionar, ¡consulta la siguiente sección!

[pypi]: https://pypi.python.org/pypi

## 🔧 Brechas

¿Encontraste algo que falta en la biblioteca estándar que debería estar en
`boltons`? ¿Encontraste algo que falta en `boltons`? Primero, tómate un
momento para leer la muy breve [declaración de arquitectura][architecture] para asegurarte
de que la funcionalidad sería una buena opción.

Luego, si estás muy motivado, envía [un Pull Request][prs]. De lo contrario,
envía una breve solicitud de característica en [la página de Issues][issues], y
nosotros resolveremos algo.

[architecture]: https://boltons.readthedocs.org/en/latest/architecture.html
[issues]: https://github.com/mahmoud/boltons/issues
[prs]: https://github.com/mahmoud/boltons/pulls
