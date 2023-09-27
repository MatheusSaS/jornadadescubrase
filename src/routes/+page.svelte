<script>
  // Estilos personalizados para o componente
  const backgroundImageStyle = `
    background: linear-gradient(rgba(0, 226, 227, 1), rgba(0, 226, 227, 0.01)), url('backgroud.jpg');
    background-size: cover;
    background-position: center;
  `;

  let email = "";
  let telefone = "";
  let mensagem = "";

  function onSubmit() {
    if (email == "" || email == undefined) {
      alert("Preencha o email corretamente");
      return;
    }
    if (telefone == "" || telefone == undefined) {
      alert("Preencha o telefone corretamente");
      return;
    }
    mensagem = `
          Olá, vim através do seu formulário.%0A
          %0A•Email%3A ${email} %0A
          %0A•Telefone%3A ${telefone} %0A
          %0A•E vou entrar no grupo%3A https://chat.whatsapp.com/ENDv3HrzInFCu7FhX0QfJT %0A
          `;

    window.open(`
        https://api.whatsapp.com/send/?phone=5517991635816&text=${mensagem}
      `);
  }
</script>

<div
  class="w-full h-full flex flex-col items-center justify-center"
  style={backgroundImageStyle}
>
  <img src="frases.png" alt="" class="sm:w-96" />
  <!-- Formulário -->
  <div class="p-6 mt-4 flex flex-col items-center w-full">
    <div class="mb-4 w-full max-w-xs">
      <label
        for="nome"
        class="block text-white font-bold text-center bg-[#00e2e3] mb-2 rounded-md"
        >E-mail:</label
      >
      <input
        type="email"
        id="email"
        name="email"
        class="input input-bordered w-full"
        placeholder="Seu e-mail"
        required
        bind:value={email}
      />
    </div>
    <div class="mb-4 w-full max-w-xs">
      <label
        for="email"
        class="block text-white font-bold text-center bg-[#00e2e3] mb-2 rounded-md"
        >Telefone:</label
      >
      <input
        type="tel"
        id="telefone"
        name="telefone"
        class="input input-bordered w-full"
        placeholder="Seu telefone"
        required
        bind:value={telefone}
      />
    </div>
    <button
      on:click={() => onSubmit()}
      class="btn bg-[#00e2e3] hover:bg-[#00e2e3]">Enviar</button
    >
  </div>
  <div class="p-2 text-center">
    <p class="text-gray-300 mt-8 text-xs">
      A sua privacidade e a segurança dos seus dados são de extrema importância
      para nós. Por isso, queremos garantir que adotamos todas as medidas
      necessárias para proteger as suas informações.
    </p>

    <p class="text-gray-300 mt-8">
      <span class="text-[#00e2e3]">Tayse Reis</span>
      | Todos os direitos reservados
      <span class="text-[#00e2e3]">@2023</span>
    </p>
  </div>
</div>
