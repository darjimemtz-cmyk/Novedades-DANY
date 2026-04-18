[index.html](https://github.com/user-attachments/files/26847889/index.html)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Novedades DANY - Catálogo</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        .product-card:hover { transform: translateY(-5px); transition: 0.3s; }
    </style>
</head>
<body class="bg-gray-100">
    <nav class="bg-blue-600 text-white p-4 shadow-lg sticky top-0 z-50">
        <div class="container mx-auto flex justify-between items-center">
            <h1 class="text-2xl font-bold">Novedades "DANY"</h1>
            <span class="bg-yellow-400 text-blue-900 px-3 py-1 rounded-full text-sm font-bold">San Luis Potosí</span>
        </div>
    </nav>

    <div class="container mx-auto p-6">
        <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Nuestro Catálogo Actualizado</h2>
        
        <div id="productos" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            </div>
    </div>

    <script>
        // Esta es la base de datos que tomamos de tu código de Python
        const inventario = [
            { id: "1028", p: "Pantalón Recto T28", m: "W", pr: 309, cat: "Caballero" },
            { id: "1032", p: "Pantalón Recto T32", m: "W", pr: 309, cat: "Caballero" },
            { id: "1038", p: "Pantalón Recto T38", m: "W", pr: 319, cat: "Caballero" },
            { id: "1102", p: "Camisa Muski M", m: "Muski", pr: 229, cat: "Caballero" },
            { id: "1202", p: "Camisa Joskar M", m: "Joskar", pr: 269, cat: "Caballero" },
            { id: "1205", p: "Camisa Joskar XXL", m: "Joskar", pr: 299, cat: "Caballero" },
            { id: "2001", p: "Blusa Alicia", m: "Alicia", pr: 229, cat: "Dama" },
            { id: "3006", p: "Pantalón Niño T6", m: "W", pr: 179, cat: "Niño" },
            { id: "3012", p: "Pantalón Niño T12", m: "W", pr: 189, cat: "Niño" }
        ];

        const contenedor = document.getElementById('productos');

        inventario.forEach(item => {
            const card = `
                <div class="product-card bg-white rounded-xl shadow-md overflow-hidden border border-gray-200">
                    <div class="bg-gray-200 h-48 flex items-center justify-center">
                        <i class="fa-solid fa-shirt text-6xl text-gray-400"></i>
                    </div>
                    <div class="p-5">
                        <div class="flex justify-between items-start mb-2">
                            <span class="text-xs font-bold uppercase px-2 py-1 bg-blue-100 text-blue-600 rounded">${item.cat}</span>
                            <span class="text-gray-500 text-xs">Mod. ${item.id}</span>
                        </div>
                        <h3 class="text-xl font-bold text-gray-900">${item.p}</h3>
                        <p class="text-gray-600 mb-4 font-medium">Marca: ${item.m}</p>
                        <div class="flex justify-between items-center">
                            <span class="text-2xl font-bold text-green-600">$${item.pr}</span>
                            <a href="https://wa.me/5214441234567?text=Hola,%20me%20interesa%20el%20producto:%20${item.p}" 
                               target="_blank"
                               class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded-lg font-bold flex items-center gap-2 transition">
                                <i class="fa-brands fa-whatsapp text-xl"></i> Pedir
                            </a>
                        </div>
                    </div>
                </div>
            `;
            contenedor.innerHTML += card;
        });
    </script>
</body>
</html>
