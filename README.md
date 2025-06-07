# Preparando el ambiente

Para inicializar nuestro entorno de trabajo necesitamos instalar **react-native-community-cli** de la siguiente manera

```powershell
    $ npm i -g react-native-community/cli
```

Tambien tenenos que instalar android studio y nodeJS.

## Iniciando el app

Para construir nuestra app tenemos que correr el siguiente comando.

`$ npx @react-native-community/cli@latest init MyPokeApp`

Dirigirnos a nuestra carpeta

```shell
cd MyPokeApp
```

Al entrar en la carpeta veirificaremos que nuestro dispositivo este conectado por USB para esto listaremos nuestros dispositivos disponibles utilizando el commando.

```shell
adb devices
```

Esto nos lista los dispostivos conectados el dato que nos interesa son los ID's de coneccion.

Tambiren podemos utilizar el dispostivo de manera inalambrimba para esto hayque utilizar los siguientes comandos.

```shell
adb tcpip [puerto]
```

con seguimos la IP de nuestro dispositivo para despues ejecutar el comando

```shell
$ adb connect [IPDispositivo]:[Puerto del paso anterior]
```

es necesario usar la ip del dispositivo y desconectarlo del equipo
verificamos que este conectado

`$ adb devices`

Ya que esta conectado es necesario correr el comando

yarn android --device [ipe del dispositivo:port]

en caso de tener problemas con la maquina virtual de JAVA usar
` $ JAVA_HOME=~/jdks  PATH=$JAVA_HOME/bin:$PATH yarn android --device ZL7324QLG3 <= este el ide no se usa wifi`
` $ JAVA_HOME=~/jdks  PATH=$JAVA_HOME/bin:$PATH yarn android --device 192.168.1.100:5555`
