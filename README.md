# Documentacion-Devops
## COMANDOS PARA GESTIONAR METADATA SALESFORCE DX DESDE LA CONSOLA 🚀

_Para crear un proyecto desde la terminal CMD de windows_ 
```
sfdx force:project:create --projectname myproject --manifest
```

_Luego nos ubicamos en la carpeta del proyecto creado_
```
cd myprojectname
```
_Realizamos el login se puede nombrar un alias y username para el proyecto_
```
sfdx force:auth:web:login --setalias userOrgNewFeatures --setdefaultusername
```

_En caso de que sea un sandbox realizamos el login de la siguiente manera_
```
sfdx force:auth:web:login --setalias userOrgNewFeatures --setdefaultusername --instanceurl https://test.salesforce.com
```

_Hacer pull de la data en Salesforce_
```
sfdx force:source:retrieve --manifest manifest/package.xml
```

_Realizar Push hacia la org de salesforce de toda una carpeta (No es recomendable si compartimos el sandbox con el equipo)_
```
sfdx force:source:deploy --loglevel fatal --sourcepath force-app/main/default/Nombredelacarperta
```

_Realizar Push hacia la org de salesforce de un archivo en específico_
```
sfdx force:source:deploy --loglevel fatal --sourcepath force-app/main/defaultNombredelacarperta/Archivo.APEX
```
##
## COMANDOS DE GITHUB DESDE LA CONSOLA SI YA TENEMOS UBICADO EL REPOSITORIO REMOTO ⌨️

```
git add *
git commit -m "Título de cambio para reconocer la version subida"
git push origin [Nombre de la rama]
```

_Buscar valores dentro de todo el repositorio_
```
git grep "[Valor buscado]"
```

_Agregar repositorio remoto y subir carpeta local_
```
git remote add origin [url repositorio]
git push -u origin master
```

_Iniciar Git_
```
git init
```

##
## Documentar las cabeceras de nuestro código en los proyectos :space_invader:
```
/*--------------------------------------------------------------------------------------------------------
Autor: [Nombre y apellido]
Empresa: Bxtoolkit
Descripción: [Descripción de la clase, componente, VF, etc]
Modificado: [Fecha de ultima modificación]
Método de prueba: [En caso de ser una clase, cual es su método de prueba]
---------------------------------------------------------------------------------------------------------*/
```
