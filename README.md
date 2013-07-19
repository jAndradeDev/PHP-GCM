PHP-GCM
=======

## Clase PHP para enviar mensajes con GCM(Google Cloud Messaging)##
====

Ejemplo de uso:
===

    $ids = (
      '123jb,3jb123v4,123jn 1,j3hbg4k1hj23g4kuyg',
      '12341234123lhk213hjv4b123hf4v1k23hj42l3hj'
    );
    $msg = (
      'descripcion' => 'esto es un mensaje de ejemlpo',
      'User' => 'jAndradeDev',
      'Hora' => date('H:i:s')
    );
    $gcm = new GCM($apykey);
    if($gcm->send($ids,$msg)){
      echo "Mensaje enviado";
    }else{
      echo $gcm->_error();
    }
