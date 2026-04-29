# 📸 updatefotosldap

Script en **Perl** diseñado para automatizar la carga y actualización masiva de las fotografías del alumnado en el servidor LDAP del centro, utilizando los datos exportados desde **Rayuela**.

## 📝 Descripción

Este script facilita la gestión de identidades visuales en el centro. Procesa el archivo comprimido de exportación de Rayuela, extrae las imágenes de los alumnos y las vincula a sus correspondientes registros en LDAP mediante el atributo binario `jpegPhoto`.

Esta última versión instala las librerías Perl necesarias automáticamente si no se encuentran instaladas.

- **Servidor LDAP:** Configurable mediante la variable `$ldapserver`.
- **Formato de entrada:** Archivo `.zip` (`ExportacionDatosAlumnado.zip`).
- **Atributo destino:** `jpegPhoto`.

---

## 🛠️ Sintaxis

```bash
updatefotosldap ExportacionDatosAlumnado.zip
```
## ⚙️ Configuración

Por defecto, la variable `$ldapserver` tiene el valor servidor, que coincide con el nombre por defecto del servidor del centro:

```perl
my $ldapserver = "servidor";
my $base_dn    = "ou=People,dc=instituto,dc=extremadura,dc=es";
```

Si queréis, podéis cambiarlo:

```perl
my $ldapserver = "172.19.144.2";
my $base_dn    = "ou=People,dc=instituto,dc=extremadura,dc=es";
```
