<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    // Recoge los datos del formulario
    $nombreEmpresa = $_POST['nombre-empresa'];
    $nombreContacto = $_POST['nombre-contacto'];
    $contactoWhatsapp = $_POST['contacto-whatsapp'];
    $direccion = $_POST['direccion'];

    // Configuración del correo
    $to = 'alfredfullstack@gmail.com'; // Asegúrate de cambiar esto por tu correo real
    $subject = 'Registro desde el Formulario de Tienda';
    $message = "Nombre de Empresa: $nombreEmpresa\nNombre de Contacto: $nombreContacto\nContacto de WHATSAPP: $contactoWhatsapp\nDirección: $direccion";
    $headers = "From: gerencia@alfredfullstack.com"; // Ajusta esto según tu dominio

    // Envía el correo
    if (mail($to, $subject, $message, $headers)) {
        // Número de WhatsApp donde enviar el mensaje (incluye el código de país)
        $whatsappNumber = "+573232490214";  // Cambia esto por el número real de WhatsApp
        $whatsappMessage = urlencode("Hola, acabo de registrar mi negocio en TIENDASAPP y estoy adjuntando las imagenes de mi megocio: Logotipo y 2 fotos adicionales.");

        // Redirección a WhatsApp
        echo "<script>window.location.href = 'https://api.whatsapp.com/send?phone=$whatsappNumber&text=$whatsappMessage';</script>";
    } else {
        echo "<script>alert('Error al enviar el email.'); window.location.href='/';</script>";
    }
}
?>
