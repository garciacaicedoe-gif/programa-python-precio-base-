# programa-python-precio-base-
este es un  ejercicio de precios base y promociones de un negocio de comidas rápidas 


menu = [
    ["Hamburguesa", "Comida Rápida", 12000],
    ["Pizza", "Comida Rápida", 15000],
    ["Ensalada César", "Saludable", 10000],
    ["Jugo Natural", "Bebida", 5000],
    ["Café", "Bebida", 4000],
    ["Filete de Res", "Gourmet", 25000],
]

def calcular_precio_final(producto, categoria_objetivo, umbral):
    nombre, categoria, precio_base = producto
    if categoria == categoria_objetivo and precio_base > umbral:
        precio_final = precio_base * 0.85  # aplica 15% descuento
    else:
        precio_final = precio_base
    return precio_final

def mostrar_promocion(menu, categoria_objetivo, umbral):
    print("\n--- PROMOCIÓN DEL MENÚ ---")
    for producto in menu:
    
        nombre, categoria, precio_base = producto
        precio_final = calcular_precio_final(producto, categoria_objetivo, umbral)
        print(f"{nombre} ({categoria}) - Base: ${precio_base:.2f} -> Final: ${precio_final:.2f}")

if __name__ == "__main__":
    # Ejemplo: aplicar promoción a la categoría 'Comida Rápida' para productos con precio > 13000
    mostrar_promocion(menu, "Comida Rápida", 13000)
