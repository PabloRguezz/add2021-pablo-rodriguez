# Salt-stack
## 3. Minion
### 3.4 Comprobamos conectividad
Desde el Máster comprobamos:

Conectividad hacia los Minions.

 **"salt '*' test.ping"**

 ![](1.png)
 
Versión de Salt instalada en los Minions

**"salt '*' test.version"**

![](2.png)

## 4. Salt States

### 4.5 Aplicar el nuevo estado
Ir al Master:

Consultar los estados en detalle y verificar que no hay errores en las definiciones.

![](3.png)

**"salt '*' state.show_lowstate"**

![](4.png)

**"salt '*' state.show_highstate"**,

![](5.png)

**"salt '*' state.apply apache"**, para aplicar el nuevo estado en todos los minions. OJO: Esta acción puede tardar un tiempo.

![](6.png)

## 5. Crear más estados

### 5.1 Crear estado "users"
Vamos a crear un estado llamado users que nos servirá para crear un grupo y usuarios en las máquinas Minions 

Crear directorio /srv/salt/base/users.

![](7.png)

Crear fichero /srv/salt/base/users/init.sls con las definiciones para crear los siguiente:

* Grupo mazingerz

![](8.png)

 * Usuarios kojiXX, drinfiernoXX dentro de dicho grupo.


 ![](9.png)

Aplicar el estado.

![](11.png)

![](12.png)
### 5.2 Crear estado "dirs"
Gestión de ficheros

Crear estado dirs para crear las carpetas private (700), public (755) y group (750) en el HOME del usuario koji.

![](13.png)

![](14.png)

![](15.png)

![](17.png)

Aplicar el estado dirs.

![](18.png)
