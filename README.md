# PROMESAS-Y-CALLBACKS-EN-JS
Breve explicacion y ejemplo de Promises y Callback en Javascript, usadas para las API's


/*USO DE LAS PROMISE y CALLBACKS */

/*PROMESAS: Se usan en codigo asincrono, y generalmente cuando se usan API'S*/
/*CALLBACKS: Tambien se usan en codigo asincrono, y son funciones dentro de otras funciones*/
//EJEMPLOS

/*Las promises deben instanciarse de la siguiente manera:

    const nombrePromesa = new Promise(parametro1, parametro2);

    estos parametros, son: 
                        resolve = cuando la promesa se cumple
                        reject  = cuando no se cumple.

Cuando una promesa se cumple, debe ser llamada con .then
si no se cumple, debe ser tomado el error con .catch

si no son llamadas o tomadas, NO SE EJECUTAN
*/

//ejemplo
const aplicarDescuento = new Promise(function(resolve, reject){
    const descuento = false; //cambiar a false o true, si se cumple o no
    if(descuento){
        resolve('Se aplicó el descuento');
    }else{
        reject('No se pudo aplicar el descuento');
    }
});

//aHORA LAS LLAMAMOS

aplicarDescuento
.then(function(resultado){
    console.log(resultado);
})
.catch(function(error){
    console.log(error);
});
