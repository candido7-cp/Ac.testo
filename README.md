<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Catálogo de Produtos</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        inter: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .bg-gym {
                background-image: url('https://images.unsplash.com/photo-1534438327276-14e5300c3a48?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');
                background-size: cover;
                background-position: center;
                background-attachment: fixed;
                position: relative;
            }
            .bg-overlay {
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background-color: rgba(0, 0, 0, 0.85);
                z-index: 1;
            }
            .content-wrapper {
                position: relative;
                z-index: 2;
            }
            .category-card {
                @apply bg-white/10 backdrop-blur-md rounded-2xl border border-white/20 overflow-hidden transition-all duration-500;
            }
            .product-item {
                @apply flex justify-between items-center py-3 px-4 bg-white/90 rounded-lg shadow-sm hover:bg-white transition-colors;
            }
            .qty-btn {
                @apply w-8 h-8 flex items-center justify-center rounded-full font-bold text-white transition-colors;
            }
        }
    </style>
</head>
<body class="font-inter bg-gym">

    <div class="bg-overlay"></div>

    <div class="content-wrapper">
        <!-- Cabeçalho -->
        <header class="bg-transparent py-8">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h1 class="text-5xl font-bold text-white mb-2">Catálogo de Produtos</h1>
                <p class="text-gray-300 text-lg">Adicione os itens que deseja e finalize o pedido</p>
            </div>
        </header>

        <!-- Conteúdo Principal -->
        <main class="max-w-4xl mx-auto px-4 pb-16 sm:px-6 lg:px-8">
            
            <!-- Categoria 1: Landerlan -->
            <div class="category-card mb-8">
                <button onclick="toggleCategory('landerlan')" class="w-full px-6 py-5 flex justify-between items-center text-white hover:bg-white/5 transition-colors">
                    <h2 class="text-3xl font-bold">Landerlan</h2>
                    <span id="icon-landerlan" class="text-2xl transition-transform duration-500">+</span>
                </button>
                <div id="landerlan" class="hidden bg-white/95 rounded-b-2xl p-6">
                    <div class="space-y-3" id="list-landerlan">
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Enan 220</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 220,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Dura 220</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 220,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Deca 220</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 220,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Master 220</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 220,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Enantato de trembo 220</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 220,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Hemogenin</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 170,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Oxan 5mg</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 260,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Categoria 2: Neopharma -->
            <div class="category-card mb-8">
                <button onclick="toggleCategory('neopharma')" class="w-full px-6 py-5 flex justify-between items-center text-white hover:bg-white/5 transition-colors">
                    <h2 class="text-3xl font-bold">Neopharma</h2>
                    <span id="icon-neopharma" class="text-2xl transition-transform duration-500">+</span>
                </button>
                <div id="neopharma" class="hidden bg-white/95 rounded-b-2xl p-6">
                    <div class="space-y-3" id="list-neopharma">
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">durateston 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Enantato 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Deca 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Cipionato 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Próprionato 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Trenbolona acetato 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Enantato de trenbolona 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Stanozolol 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Emoginin 💊</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 170,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Stanasolol 💊</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Categoria 3: Max -->
            <div class="category-card mb-8">
                <button onclick="toggleCategory('max')" class="w-full px-6 py-5 flex justify-between items-center text-white hover:bg-white/5 transition-colors">
                    <h2 class="text-3xl font-bold">Max</h2>
                    <span id="icon-max" class="text-2xl transition-transform duration-500">+</span>
                </button>
                <div id="max" class="hidden bg-white/95 rounded-b-2xl p-6">
                    <div class="space-y-3" id="list-max">
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">durateston 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Stanozolol 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Enantato 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Deca 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Cipionato 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Próprionato 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Trenbolona acetato 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Enantato de trenbolona 💉</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Emoginin 💊</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Stanasolol 💊</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 180,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Oxan 10mg 💊</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 170,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <span class="text-lg font-medium text-gray-800">Oxan 20mg 💊</span>
                            <div class="flex items-center gap-4">
                                <span class="text-green-600 font-bold">$ 200,00</span>
                                <div class="flex items-center gap-2">
                                    <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                    <span class="qty font-bold w-6 text-center">0</span>
                                    <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Botão Finalizar -->
            <div class="text-center mt-10">
                <button onclick="finalizarPedido()" class="bg-green-500 hover:bg-green-600 text-white font-bold py-4 px-10 rounded-full text-xl shadow-lg transform hover:scale-105 transition-all">
                    ✅ FINALIZAR PEDIDO
                </button>
            </div>

        </main>
    </div>

    <script>
        function toggleCategory(id) {
            const content = document.getElementById(id);
            const icon = document.getElementById('icon-' + id);
            
            content.classList.toggle('hidden');
            
            if(content.classList.contains('hidden')) {
                icon.innerHTML = '+';
                icon.style.transform = 'rotate(0deg)';
            } else {
                icon.innerHTML = '−';
                icon.style.transform = 'rotate(180deg)';
            }
        }

        function changeQty(button, delta) {
            const item = button.parentElement;
            const qtySpan = item.querySelector('.qty');
            let qty = parseInt(qtySpan.innerText);
            
            qty += delta;
            if(qty < 0) qty = 0;
            
            qtySpan.innerText = qty;
        }

        function finalizarPedido() {
            let mensagem = "*🛒 PEDIDO REALIZADO*\n\n";
            let totalGeral = 0;

            function lerCategoria(nome, id) {
                const lista = document.getElementById(id);
                const items = lista.querySelectorAll('.product-item');
                let temItem = false;
                let categoriaTexto = `*📦 ${nome}*\n`;

                items.forEach(item => {
                    const nomeProd = item.querySelector('span:first-child').innerText;
                    const precoTexto = item.querySelector('.text-green-600').innerText;
                    const qty = parseInt(item.querySelector('.qty').innerText);
                    
                    if(qty > 0) {
                        temItem = true;
                        const preco = parseFloat(precoTexto.replace('$ ', '').replace('.', '').replace(',', '.'));
                        const totalItem = preco * qty;
                        totalGeral += totalItem;
                        
                        categoriaTexto += `${qty}x - ${nomeProd} - ${precoTexto}\n`;
                    }
                });

                if(temItem) {
                    mensagem += categoriaTexto + "\n";
                }
            }

            lerCategoria('Landerlan', 'list-landerlan');
            lerCategoria('Neopharma', 'list-neopharma');
            lerCategoria('Max', 'list-max');

            if(totalGeral === 0) {
                alert('Adicione pelo menos um item antes de finalizar!');
                return;
            }

            mensagem += `*💵 TOTAL DO PEDIDO: $ ${totalGeral.toFixed(2).replace('.', ',')}*\n\n`;
            mensagem += `📲 *Pagamento via PIX*\n`;
            mensagem += `Chave PIX: 85996640269\n`;
            mensagem += `Nome: Maria Edileuda Cândido Cosmo\n\n`;
            mensagem += `Favor enviar o comprovante! ✅`;

            const mensagemCodificada = encodeURIComponent(mensagem);
            const numeroWhatsapp = "5585920076331";
            const link = `https://wa.me/${numeroWhatsapp}?text=${mensagemCodificada}`;

            window.open(link, '_blank');
        }
    </script>

</body>
</html>
