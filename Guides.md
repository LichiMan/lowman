# Guides #

Las guías son jerarquías de nodos que forman visualmente un esqueleto o parte de él. Se componen de:
  * **GIS** _(Guide Implicit Sphere)_: Es un nodo _implicitSphere_ que representa el _joint_
  * **GUO** _(Guide Up Object)_: Es un _locator_ usado para el _World Up Object_ del _Aim Constraint_
  * **GUC** _(Guide Union Curve)_: Es una curva que une dos _GIS_ representando el _bone_

## GIS ##

El _Guide Implicit Sphere_ tiene un atributo _float_ y otro _string_:

  * **rotateAim**: _float_ que controla el atributo _rotateY_ de su _GUO_
  * **anatomyPart**: _string_ con el tipo de parte del cuerpo al que corresponde (_spine_, _head_, _leg_, _hand_) o con la palabra _skip_. Los _GIS_ que no son el _padre_ de esa parte del cuerpo son _skip_. Este atributo sirve para saber que script tenemos que lanzar en ese futuro joint

## GUO ##

El _Guide Up Object_ está emparentado al _GIS_ y trasladado -1 en el eje Z de forma local. Tiene todos sus atributos bloqueados y ocultos. Tiene su _Display Type_ en _Reference_ para que nadie pueda tocarlo.

## GUC ##

Los _Guide Union Curve_ son curvas lineales de sólo 2 CVs cada uno con un _cluster_ constreñido a su respectivo _GIS_. Su _NAME_ viene dado por el _GIS padre_ y _GIS hijo_ juntos: _`roothip_C_GUC (NAME_SIDE_TYPE)`_

Tienen sus atributos bloqueados y ocultos al igual que los _GUO_ y también su _Display Type_ en _Reference_ para que nadie tenga acceso a ellos.

Los _GUC_ tienen dos atributos _string_:
  * **parent**: El cual tiene el nombre de su _GIS_ padre
  * **child**: El cual tiene el nombre de su _GIS_ hijo