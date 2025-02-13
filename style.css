let currentPage = 1;
const productsPerPage = 6;
let cart = [];
const avaliacoes = [];
const produtos = [
    {
        id: 1,
        nome: "X-Burguer",
        preco: 8.00,
        descricao: "Delicioso hambúrguer com pão, carne e mussarela.",
        imagem: "imagens/xburguer.png",
        categoria: "burguer"
    },
    {
        id: 2,
        nome: "X-Salada",
        preco: 9.00,
        descricao: "Delicioso hambúrguer com pão, carne, mussarela e salada.",
        imagem: "imagens/xsalada.png",
        categoria: "burguer"
    },
    {
        id: 3,
        nome: "X-Frango",
        preco: 12.00,
        descricao: "Delicioso hambúrguer com pão, frango empanado e salada, alface e tomate.",
        imagem: "imagens/xfrango.png",
        categoria: "burguer"
    },
    {
        id: 4,
        nome: "X-Bacon",
        preco: 12.00,
        descricao: "Delicioso hambúrguer com pão, carne, bacon, mussarela e salada, alface e tomate.",
        imagem: "imagens/xbacon.png",
        categoria: "burguer"
    },
    {
        id: 5,
        nome: "X-Tudo",
        preco: 15.00,
        descricao: "Delicioso hambúrguer com pão, carne, presunto, bacon, milho, batata palha, ovo e salada, alface e tomate.",
        imagem: "imagens/xtudo.png",
        categoria: "burguer"
    },
    {
        id: 6,
        nome: "Duplo Burguer",
        preco: 14.00,
        descricao: "Um delicioso hambúrguer clássico, com pão, duas carnes, duas mussarela e salada, alface e tomate.",
        imagem: "imagens/duploburguer.png",
        categoria: "Duplos"
    },
    {
        id: 7,
        nome: "Duplo Cheddar",
        preco: 17.00,
        descricao: "Um delicioso hambúrguer clássico, com pão, duas carnes, dois cheddar, bacon e salada, alface e tomate.",
        imagem: "imagens/duplocheddar.png",
        categoria: "Duplos"
    },
    {
        id: 8,
        nome: "Especial Imperial",
        preco: 23.00,
        descricao: "Um deliciso hambúrguer especial, com pão, três carnes, três queijos, cheddar, bacon, ovo, batata palha, cebola e salada, alface e tomate.",
        imagem: "imagens/especialimperial.png",
        categoria: "Duplos"
    },
    {
        id: 9,
        nome: "Batata Frita P",
        preco: 7.00,
        descricao: "Deliciosa batata frita tamanho P, crocante e macia (serve 1 pessoa)",
        imagem: "imagens/batatap.png",
        categoria: "Porções"
    },
    {
        id: 10,
        nome: "Batata Frita G",
        preco: 9.00,
        descricao: "Deliciosa batata frita tamanho G, crocante e macia (serve até duas pessoas)",
        imagem: "imagens/batatag.png",
        categoria: "Porções"
    },
    {
        id: 11,
        nome: "Batata Frita Para Compartilhar",
        preco: 12.00,
        descricao: "Deliciosa batata frita para compartilhar com a galera, acompanha ketchup e molho de maionese. (serve até 4 pessoas)",
        imagem: "imagens/batatagg.png",
        categoria: "Porções"
    },
    {
        id: 12,
        nome: "Linguiça Imperial",
        preco: 15.00,
        descricao: "Deliciosa linguiça calabresa com cebola!",
        imagem: "imagens/linguica.png",
        categoria: "Porções"
    },
    {
        id: 13,
        nome: "Ketchup",
        preco: 1.00,
        descricao: "Molho de ketchup. O primeiro é grátis!",
        imagem: "imagens/ketchup.png",
        categoria: "molhos"
    },
    {
        id: 14,
        nome: "Maionese",
        preco: 1.00,
        descricao: "Molho de maionese. O primeiro é grátis!",
        imagem: "imagens/maionese.png",
        categoria: "molhos"
    },
    {
        id: 15,
        nome: "Molho Especial",
        preco: 2.00,
        descricao: "Molho de maionese temperada.",
        imagem: "imagens/molhoespecial.png",
        categoria: "molhos"
    },
    {
        id: 16,
        nome: "Refrigerante Laranja 250ml",
        preco: 3.00,
        descricao: "Geladinho para refrescar e acompanhar o seu lanche.",
        imagem: "imagens/laranja250ml.png",
        categoria: "Bebidas"
    },
    {
        id: 17,
        nome: "Refrigerante Uva 250ml",
        preco: 3.00,
        descricao: "Geladinho para refrescar e acompanhar o seu lanche.",
        imagem: "imagens/uva250ml.png",
        categoria: "Bebidas"
    },
    {
        id: 18,
        nome: "Refrigerante Guaraná 250ml",
        preco: 3.00,
        descricao: "Geladinho para refrescar e acompanhar o seu lanche.",
        imagem: "imagens/guarana250ml.png",
        categoria: "Bebidas"
    },
    {
        id: 19,
        nome: "Refrigerante Jeri Cola 250ml",
        preco: 3.00,
        descricao: "Geladinho para refrescar e acompanhar o seu lanche.",
        imagem: "imagens/jeri250ml.png",
        categoria: "Bebidas"
    },
];

let ketchupGratuito = 1;
let maioneseGratuita = 1;
const maquininhaTax = 4.00; // Valor da taxa de maquininha
let isCardPayment = false; // Variável para acompanhar se o pagamento é com cartão

function showCatalog() {
    document.getElementById("header").style.display = "none";
    document.getElementById("mainFooter").style.display = "block";
    document.body.style.overflow = "auto";
    document.getElementById("categorias").style.display = "block";
    document.getElementById("catalogo").style.display = "block";
    document.getElementById("cartIcon").style.display = "block";
    filterProducts('burguer');
}

function filterProducts(categoria) {
    const filteredProducts = produtos.filter(produto => produto.categoria.toLowerCase() === categoria.toLowerCase());
    renderFilteredPage(filteredProducts);
}

function renderFilteredPage(products) {
    const container = document.getElementById("produtos");
    container.innerHTML = '';
    if (products.length === 0) {
        container.innerHTML = '<p>Nenhum produto encontrado.</p>';
    } else {
        products.forEach(produto => {
            const productDiv = document.createElement('div');
            productDiv.classList.add('produto');

            const productImage = document.createElement('img');
            productImage.src = produto.imagem;
            productDiv.appendChild(productImage);

            const productName = document.createElement('h3');
            productName.textContent = produto.nome;
            productDiv.appendChild(productName);

            const productPrice = document.createElement('p');
            productPrice.innerHTML = `<strong> R$ ${produto.preco.toFixed(2)}</strong>`;
            productDiv.appendChild(productPrice);

            const productDescription = document.createElement('p');
            productDescription.textContent = produto.descricao;
            productDiv.appendChild(productDescription);

            const addToCartButton = document.createElement('button');
            addToCartButton.textContent = `Pedir Agora (${produto.quantity || 0})`;
            addToCartButton.onclick = () => addToCart(produto);
            productDiv.appendChild(addToCartButton);

            container.appendChild(productDiv);
        });
    }
}

function addToCart(produto) {
    const existingItem = cart.find(item => item.id === produto.id);

    if (existingItem) {
        existingItem.quantity += 1;
    } else {
        cart.push({ ...produto, quantity: 1 });
    }

    updateProductQuantity(produto.id);
    updateCart();
}

function updateProductQuantity(productId) {
    const products = document.querySelectorAll('.produto');
    products.forEach(productDiv => {
        const addToCartButton = productDiv.querySelector('button');
        const productName = productDiv.querySelector('h3').textContent;
        const product = produtos.find(p => p.nome === productName);
        if (product && product.id === productId) {
            addToCartButton.textContent = `Pedir Agora (${cart.find(item => item.id === productId)?.quantity || 0})`;
        }
    });
}

function updateCart(deliveryFee = 0) {
    const cartItemsContainer = document.getElementById('cartItems');
    const cartTotalContainer = document.getElementById('cartTotal');
    const cartCount = document.getElementById('cartCount');
    cartItemsContainer.innerHTML = '';
    let total = 0;

    cart.forEach(item => {
        const price = item.preco;
        const cartItemDiv = document.createElement('div');
        cartItemDiv.classList.add('cart-item');

        const itemName = document.createElement('p');
        if (item.nome === 'Ketchup' || item.nome === 'Maionese') {
            if (item.nome === 'Ketchup' && item.quantity <= ketchupGratuito) {
                itemName.textContent = `${item.nome} - Gratuito (${item.quantity}x)`;
            } else if (item.nome === 'Maionese' && item.quantity <= maioneseGratuita) {
                itemName.textContent = `${item.nome} - Gratuito (${item.quantity}x)`;
            } else {
                const extraQuantity = item.quantity - (item.nome === 'Ketchup' ? ketchupGratuito : maioneseGratuita);
                itemName.textContent = `${item.nome} - R$ ${(price * extraQuantity).toFixed(2)} (${item.quantity}x)`;
                total += price * extraQuantity;
            }
        } else {
            itemName.textContent = `${item.nome} - R$ ${(price * item.quantity).toFixed(2)} (${item.quantity}x)`;
            total += price * item.quantity;
        }
        cartItemDiv.appendChild(itemName);

        const adjustButtons = document.createElement('div');
        adjustButtons.classList.add('adjust-buttons');

        const decreaseButton = document.createElement('span');
        decreaseButton.textContent = '-';
        decreaseButton.onclick = () => updateItemQuantity(item, item.quantity - 1);
        adjustButtons.appendChild(decreaseButton);

        const quantityDisplay = document.createElement('span');
        quantityDisplay.textContent = item.quantity;
        adjustButtons.appendChild(quantityDisplay);

        const increaseButton = document.createElement('span');
        increaseButton.textContent = '+';
        increaseButton.onclick = () => updateItemQuantity(item, item.quantity + 1);
        adjustButtons.appendChild(increaseButton);
        cartItemDiv.appendChild(adjustButtons);

        const removeButton = document.createElement('span');
        removeButton.textContent = '🗑️';
        removeButton.classList.add('remove-item');
        removeButton.onclick = () => removeFromCart(item);
        cartItemDiv.appendChild(removeButton);

        cartItemsContainer.appendChild(cartItemDiv);
    });

    if (isCardPayment) {
        total += maquininhaTax; // Adicionar a taxa de maquininha se o pagamento for com cartão
    }

    total += deliveryFee;
    cartTotalContainer.textContent = `Total: R$ ${total.toFixed(2)} (incluindo taxa de entrega: R$ ${deliveryFee.toFixed(2)})`;
    cartCount.textContent = cart.length;
}

function handleDeliveryOptionChange(option) {
    const locationOption = document.getElementById('locationOption');
    const customerNameInput = document.getElementById('customerName');
    if (option === 'Delivery') {
        locationOption.style.display = 'block';
    } else {
        locationOption.style.display = 'none';
        updateDeliveryFee(0);
    }
    customerNameInput.style.display = 'block';
}

function updateDeliveryFee() {
    const locationSelect = document.getElementById('locationSelect');
    const selectedOption = locationSelect.options[locationSelect.selectedIndex];
    const deliveryFee = parseFloat(selectedOption.getAttribute('data-fee')) || 0;
    updateCart(deliveryFee);
}

function updateItemQuantity(item, newQuantity) {
    if (newQuantity <= 0) {
        removeFromCart(item);
    } else {
        item.quantity = newQuantity;
        updateCart();
    }
}

function removeFromCart(item) {
    const index = cart.findIndex(cartItem => cartItem.id === item.id);
    if (index > -1) {
        cart.splice(index, 1);
        updateCart();
    }
}

function toggleCart() {
    const cartDetails = document.getElementById('cartDetails');
    cartDetails.style.display = cartDetails.style.display === 'block' ? 'none' : 'block';
}

function checkPaymentOption() {
    const paymentOption = document.querySelector('input[name="paymentOption"]:checked').value;

    if (paymentOption === 'Cartão') {
        const agree = confirm(`Será cobrada uma taxa de maquininha de R$ ${maquininhaTax.toFixed(2)}. Você concorda?`);
        
        if (agree) {
            isCardPayment = true; // Definir que o pagamento é com cartão
            addTaxToTotal(maquininhaTax);
        } else {
            isCardPayment = false; // Redefinir a variável se o cliente não concordar
            // Desmarcar a opção se o cliente não concordar
            document.querySelector('input[name="paymentOption"]:checked').checked = false;
        }
    } else {
        isCardPayment = false; // Redefinir a variável se o pagamento não for com cartão
    }

    updateCart(); // Atualizar o carrinho para refletir a mudança
}

function addTaxToTotal(tax) {
    const totalElement = document.getElementById('cartTotal'); // Supondo que o total esteja em um elemento com ID 'cartTotal'
    const totalText = totalElement.textContent;
    const totalAmountMatch = totalText.match(/Total: R\$ (\d+\.\d+)/);
    let currentTotal = totalAmountMatch ? parseFloat(totalAmountMatch[1]) : 0;
    currentTotal += tax;
    totalElement.textContent = `Total: R$ ${currentTotal.toFixed(2)}`;
}

function finalizeOrder() {
    if (cart.length === 0) {
        alert("Por favor, adicione pelo menos um produto ao carrinho.");
        return;
    }

    const customerName = document.getElementById('nameInput').value.trim();
    if (!document.querySelector('input[name="paymentOption"]:checked')) {
        alert("Por favor, selecione um método de pagamento.");
        return;
    }
    if (!document.querySelector('input[name="deliveryOption"]:checked')) {
        alert("Por favor, selecione a opção de entrega.");
        return;
    }
    if (document.querySelector('input[name="deliveryOption"]:checked').value === 'Delivery' && !document.getElementById('locationSelect').value) {
        alert("Por favor, selecione sua localização.");
        return;
    }
    if (customerName === "") {
        alert("Por favor, insira seu nome.");
        return;
    }

    // Exibir tela de confirmação com mensagem personalizada e botão "Enviar Pedido"
    document.getElementById('orderConfirmation').style.display = 'block';
    document.getElementById('orderConfirmation').innerHTML = `
        <h1>Pedido Finalizado!</h1>
        <p>"Seu pedido já está a caminho da cozinha!" 🍔</p>
        <p>Vamos prepará-lo com carinho, e em cerca de 30 a 40 minutos ele estará prontinho para você. Enquanto isso, que tal nos acompanhar nas redes sociais?</p>
        <div class="social-icons">
            <a href="https://www.instagram.com/_imperial.burguer" target="_blank">
                <i class="fab fa-instagram instagram-icon"></i>
            </a>
            <a href="https://wa.me/5588993467578" target="_blank">
                <i class="fab fa-whatsapp whatsapp-icon"></i>
            </a>
        </div>
        <button onclick="sendOrderAndReturnToCatalog()">Enviar Pedido</button>
        <p class="credit">© 2025 Desenvolvido por Ismael Rocha | @_ismaelrocha</p>
    `;
}

function sendOrderAndReturnToCatalog() {
    sendOrder();

    // Retornar o catálogo à capa no navegador
    document.getElementById('header').style.display = 'block';
    document.getElementById('categorias').style.display = 'none';
    document.getElementById('catalogo').style.display = 'none';
    document.getElementById('cartIcon').style.display = 'none';
    document.getElementById('mainFooter').style.display = 'none';
    document.getElementById('orderConfirmation').style.display = 'none'; // Ocultar a tela de confirmação
    document.getElementById('cartDetails').style.display = 'none'; // Ocultar o carrinho

    cart = []; // Esvaziar o carrinho após a finalização do pedido
    updateCart(); // Atualizar o carrinho na interface
}

function sendOrder() {
    const customerName = document.getElementById('nameInput').value.trim();
    if (cart.length === 0) {
        alert("Por favor, adicione pelo menos um produto ao carrinho.");
        return;
    }
    let orderDetails = cart.map(item => {
        const price = item.preco;
        if ((item.nome === 'Ketchup' && item.quantity <= ketchupGratuito) || (item.nome === 'Maionese' && item.quantity <= maioneseGratuita)) {
            return `*${item.nome}* - Gratuito (${item.quantity}x)`;
        } else if (item.nome === 'Ketchup' || item.nome === 'Maionese') {
            const extraQuantity = item.quantity - (item.nome === 'Ketchup' ? ketchupGratuito : maioneseGratuita);
            return `*${item.nome}* - R$ ${(price * extraQuantity).toFixed(2)} (${item.quantity}x)`;
        } else {
            return `*${item.nome}* - R$ ${(price * item.quantity).toFixed(2)} (${item.quantity}x)`;
        }
    }).join('\n');

    let totalAmount = cart.reduce((sum, item) => {
        const price = item.preco;
        if ((item.nome === 'Ketchup' && item.quantity <= ketchupGratuito) || (item.nome === 'Maionese' && item.quantity <= maioneseGratuita)) {
            return sum;
        } else if (item.nome === 'Ketchup' || item.nome === 'Maionese') {
            const extraQuantity = item.quantity - (item.nome === 'Ketchup' ? ketchupGratuito : maioneseGratuita);
            return sum + price * extraQuantity;
        } else {
            return sum + price * item.quantity;
        }
    }, 0).toFixed(2);

    const orderNotes = document.getElementById('orderNotes').value;
    const deliveryOption = document.querySelector('input[name="deliveryOption"]:checked')?.value || '';
    const paymentOption = document.querySelector('input[name="paymentOption"]:checked')?.value || '';
    const locationSelect = document.getElementById('locationSelect');
    const location = locationSelect ? locationSelect.value : '';
    const deliveryFee = parseFloat(locationSelect.options[locationSelect.selectedIndex]?.getAttribute('data-fee')) || 0;

    // Adicionar a taxa de maquininha ao total se o pagamento for com cartão
    if (isCardPayment) {
        totalAmount = (parseFloat(totalAmount) + maquininhaTax).toFixed(2);
    }

    totalAmount = (parseFloat(totalAmount) + deliveryFee).toFixed(2);

    let phoneNumber = '5588993467578';
    let message = `Olá, meu nome é ${customerName}, estou enviando o meu pedido:\n\n${orderDetails}\n\nTaxa de entrega: R$ ${deliveryFee.toFixed(2)}\nTotal: R$ ${totalAmount}`;
    if (orderNotes) {
        message += `\n\nObservações: ${orderNotes}`;
    }
    if (deliveryOption) {
        message += `\n\nOpção de entrega: ${deliveryOption}`;
    }
    if (location) {
        message += `\n\nLocalização: ${location}`;
    }
    if (paymentOption) {
        message += `\n\nForma de pagamento: ${paymentOption}`;
    }
    message += `\n\nObrigado(a) Aguardando a confirmação!`;

    let whatsappLink = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
    window.open(whatsappLink, '_blank');
}

function showFinalizeButton() {
    document.getElementById('finalizeOrderSection').style.display = 'block';
}

function goToCatalog() {
    document.getElementById('orderConfirmation').style.display = 'none';
    document.getElementById('header').style.display = 'block';
    document.getElementById('categorias').style.display = 'none';
    document.getElementById('catalogo').style.display = 'none';
    document.getElementById('cartIcon').style.display = 'none';
}
