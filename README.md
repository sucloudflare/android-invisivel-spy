

<h1>Android Undetectable Spy App</h1>
<h2>PoC de spyware Android 100% stealth (baseado no repositório original de Ch0pin)</h2>
<p><strong>Repositório original:</strong> <a href="https://github.com/Ch0pin/Android-Undetectable-Spy-App">https://github.com/Ch0pin/Android-Undetectable-Spy-App</a></p>

<div class="warning">
    <h3>⚠️ AVISO LEGAL E ÉTICO EXTREMAMENTE SÉRIO ⚠️</h3>
    <p>Este é um <strong>spyware Android completo e funcional</strong> projetado para ser praticamente indetectável pelo usuário e por muitos antivírus.</p>
    <p>Ele monitora e exfiltra em tempo real:</p>
    <ul>
        <li>Todas as notificações do sistema (SMS, WhatsApp, Telegram, Instagram, apps bancários, e-mail…)</li>
        <li>Conversas completas do WhatsApp (texto + mídia)</li>
        <li>Mensagens privadas do Instagram Direct</li>
    </ul>
    <p><strong>USO PERMITIDO SOMENTE PARA:</strong></p>
    <ul>
        <li>Controle parental com consentimento legal</li>
        <li>Testes de penetração com contrato e autorização por escrito</li>
        <li>Pesquisa acadêmica ou em laboratório próprio</li>
    </ul>
    <p><strong>USO CRIMINOSO (proibido e punível com prisão):</strong></p>
    <ul>
        <li>Instalar no celular de namorada(namo), esposa(marido), amigo, funcionário ou qualquer pessoa sem consentimento explícito</li>
        <li>Qualquer monitoramento clandestino</li>
    </ul>
    <p>No Brasil isso é <strong>crime de invasão de dispositivo informático</strong> (art. 154-A CP – até 4 anos de reclusão) + violação da LGPD.</p>
    <p>Você foi devidamente avisado. Use apenas em emulador ou dispositivo 100% seu.</p>
</div>

<h2>O que esse spyware faz?</h2>
<ul>
    <li>Captura <strong>todas as notificações</strong> do sistema em tempo real (NotificationListenerService)</li>
    <li>Lê <strong>conversas completas do WhatsApp e Instagram</strong> usando AccessibilityService (funciona mesmo com mensagens criptografadas)</li>
    <li>Envia tudo para um <strong>Firebase Realtime Database</strong> (ou servidor que você configurar)</li>
    <li>Roda 100% em background, <strong>sem ícone</strong> após a primeira execução</li>
    <li>Não aparece na lista de apps recentes nem na gav09eta de aplicativos</li>
    <li>Consumo mínimo de bateria e dados</li>
    <li>Dificilmente detectado por Google Play Protect e AVs comuns da época</li>
</ul>

<h2>Requisitos</h2>
<ul>
    <li>Android 5.0 ou superior</li>
    <li>Projeto Firebase (Realtime Database) criado por você</li>
    <li>Android Studio ou VS Code + Flutter (para compilar)</li>
</ul>

<h2>Como compilar e usar (passo a passo atualizado 2025)</h2>

<h3>1. Clone o repositório original</h3>
<pre>
git clone https://github.com/Ch0pin/Android-Undetectable-Spy-App.git
cd Android-Undetectable-Spy-App
</pre>

<h3>2. Abra no Android Studio (ou VS Code com extensão Android)</h3>
<p>O projeto é um app Android nativo clássico (não Flutter).</p>

<h3>3. Configure seu Firebase</h3>
<ol>
    <li>Crie um projeto no <a href="https://console.firebase.google.com/">Firebase Console</a></li>
    <li>Ative o Realtime Database</li>
    <li>Baixe o <code>google-services.json</code> e coloque na pasta <code>app/</code></li>
    <li>No arquivo <code>FirebaseHelper.java</code> ou similar, troque a URL do seu database</li>
</ol>

<h3>4. Principais arquivos (não precisa mexer muito)</h3>
<ul>
    <li><code>NotificationService.java</code> → captura todas as notificações</li>
    <li><code>AccessibilityServiceSpy.java</code> → lê WhatsApp e Instagram</li>
    <li><code>MainActivity.java</code> → esconde o ícone após primeira execução</li>
</ul>

<h3>5. Compile o APK</h3>
<pre>
Build → Build Bundle(s) / APK(s) → Build APK(s)
# ou
./gradlew assembleDebug
</pre>
<p>O APK fica em <code>app/build/outputs/apk/debug/app-debug.apk</code></p>

<h3>6. Instale no dispositivo alvo (ou emulador)</h3>
<pre>
adb install app-debug.apk
</pre>

<h3>7. Primeira execução</h3>
<ol>
    <li>Abrir o app (ainda tem ícone)</li>
    <li>Conceder permissão de <strong>Acessibilidade</strong></li>
    <li>Conceder permissão de <strong>Notificações</strong> (Notification access)</li>
    <li>O app some do launcher automaticamente</li>
</ol>

<h3>8. Ver os dados roubados</h3>
<p>Acesse seu Firebase Realtime Database → você verá nós com:</p>
<ul>
    <li>Notificações de todos os apps</li>
    <li>Mensagens completas do WhatsApp (com nome do contato)</li>
    <li>Mensagens do Instagram Direct</li>
</ul>

<div class="note">
    <p><strong>Dica 2025:</strong> O Google Play Protect e antivírus modernos (Kaspersky, Avast, Bitdefender) já detectam versões antigas. Para bypass atual use ofuscação (ProGuard/R8 + DexGuard) ou ferramentas como APKTool + MSF Venom.</p>
</div>

<h2>Como se defender disso (importante!)</h2>
<ul>
    <li>Nunca ative Acessibilidade para apps desconhecidos</li>
    <li>Verifique em Configurações → Acessibilidade e Acesso a Notificações</li>
    <li>Use antivírus atualizado (Bitdefender Mobile, Malwarebytes)</li>
    <li>Evite instalar APKs de fontes desconhecidas</li>
</ul>

<hr>
<p><strong>Autor original:</strong> <a href="https://github.com/Ch0pin">Ch0pin</a> (2021)</p>
<p><strong>README atualizado e traduzido:</strong> Comunidade brasileira de pesquisa em segurança mobile – Novembro 2025</p>

<p><strong>Use apenas para estudo ou com autorização legal. Qualquer uso indevido é de sua inteira responsabilidade.</strong></p>

</body>
</html>
