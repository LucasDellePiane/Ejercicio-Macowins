# Ejercicio-Macowins

requerimentos:
saber precio de una prenda
saber tipo de una prenda
registrar cada venta con precio fecha y cantidad de prendas
saber ganancia en un dia determinado del negocio

class tipo{
var valorOriginal
}
class Prenda{
var estado
var tipo
method precio() = tipo.descuento(tipo.valorOriginal())
}

interfaz EstadoDePrenda {
method descuento(valor)
}

class nueva{
method descuento(valor)=valor
}
 class promocion{
var valorARestar
method descuento(valor) = valor - valorARestar
}
class liquidacion{
method descuento(valor) = valor/2
}

class venta{
var dia
var metodoPago
var prendas
var cantidad = prendas.size()
method valorVenta() = metodoPago.precioFinal(prendas.sum(prenda -> prenda.precio()))
method esDeDia(fecha) = fecha == dia
}

interfaz metodoPago{
method precioFinal(valor)
}

class pagoEnEfectivo{
method precioFinal(valor) = valor
}

class pagoConTarjeta{
var cuotas
method precioFinal(valor) = cuotas * coeficiente + valor * 0.01

class RegistroVentas{
var ventas
method ganaciaDe(dia) {
var ventasDeEseDia = ventas.filter(ventas -> venta.esDeDia(dia))
var ganancia = ventasDeEseDia.sum(ventasDeEseDia -> venta.valorVenta())
return ganacia}
