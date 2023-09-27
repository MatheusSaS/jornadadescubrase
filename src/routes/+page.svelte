<script>
  // Estilos personalizados para o componente
  const backgroundImageStyle = `
    background: linear-gradient(rgba(0, 0, 0, 1), rgba(0, 0, 0, 0.5)), url('fundo.png');
    background-size: cover;
    background-position: center;
  `;
</script>

<div
  class="h-screen flex flex-col items-center justify-center"
  style={backgroundImageStyle}
>
  <div class="text-black text-center w-full bg-white">
    <h1 class="text-lg">Venha fazer <strong>parte dessa jornada</strong></h1>
  </div>

  <!-- Formulário -->
  <div class="p-6 mt-4 flex flex-col items-center w-full">
    <div class="mb-4 w-full max-w-xs">
      <label for="nome" class="block text-gray-700 font-bold text-center"
        >Nome:</label
      >
      <input
        type="text"
        id="nome"
        name="nome"
        class="input input-bordered w-full"
        placeholder="Seu nome"
        required
      />
    </div>
    <div class="mb-4 w-full max-w-xs">
      <label for="email" class="block text-gray-700 font-bold text-center"
        >E-mail:</label
      >
      <input
        type="email"
        id="email"
        name="email"
        class="input input-bordered w-full"
        placeholder="Seu e-mail"
        required
      />
    </div>
    <button
      type="submit"
      class="btn btn-primary"
      >Enviar</button
    >
  </div>
  <div class="p-2 text-center">
    <p class="text-gray-300 mt-8 text-xs">
      A sua privacidade e a segurança dos seus dados são de extrema importância
      para nós. Por isso, queremos garantir que adotamos todas as medidas
      necessárias para proteger as suas informações.
    </p>

    <p class="text-gray-300 mt-8">
      <span class="text-[#b89748]">Bárbara Albuquerque Imóveis</span>
      | Todos os direitos reservados
      <span class="text-[#b89748]">@2023</span>
    </p>
  </div>
</div>
