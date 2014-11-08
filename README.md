# Eventario

## Acerca de Eventario:

Eventario es una aplicación que busca mostrarte cuáles son los eventos turisticos y culturales cercanos a ti.  Está compuesta por una aplicación Android y una iOS.

El backend de Eventario está desarrollado en Ruby

## ¿Cómo instalar?

### Modo desarrollo

Es muy sencillo, necesitas ejecutar los siguientes comandos

    bundle install
    rake db:migrate
    rails s

Y tendrás corriendo la aplicación en modo desarrollo.

Eventario utiliza **Elasticsearch** para ciertas busquedas, si utilizas OSX puedes utilizar Homebrew para instalarlo:

    brew install elasticsearch
    
En modo Desarrollo, Eventario utiliza SQLite. Sin embargo, en modo de producción recuerda instalar Postgresql.

Para poder agregar venues o eventos, recuerda que Eventario utiliza un administrador. registra un usuario y en la consola de rails obten tu usuario y cambia el campo de ```admin``` de **false** a **true**

    usuario = User.find_by "tucorreo@electronico"
    usuario.admin = true
    usuario.save
