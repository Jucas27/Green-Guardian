@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);

    // Layout principal
    LinearLayout mainLayout = new LinearLayout(this);
    mainLayout.setOrientation(LinearLayout.VERTICAL);
    mainLayout.setBackgroundColor(Color.parseColor("#66d18b"));
    mainLayout.setPadding(32, 32, 32, 32);
    mainLayout.setGravity(Gravity.CENTER_HORIZONTAL);

    // Título superior
    TextView title = new TextView(this);
    title.setText("Green Guardian");
    title.setTextColor(Color.WHITE);
    title.setTextSize(24);
    title.setGravity(Gravity.CENTER);
    title.setPadding(0, 0, 0, 8);
    title.setTypeface(null, android.graphics.Typeface.BOLD);
    mainLayout.addView(title);

    // Subtítulo
    TextView subtitle = new TextView(this);
    subtitle.setText("cuida tu jardín");
    subtitle.setTextColor(Color.WHITE);
    subtitle.setTextSize(14);
    subtitle.setGravity(Gravity.CENTER);
    subtitle.setPadding(0, 0, 0, 32);
    mainLayout.addView(subtitle);

    // Imagen en el centro
    ImageView logo = new ImageView(this);
    logo.setImageResource(R.drawable.your_image_here); // Reemplazar con la imagen correspondiente
    LinearLayout.LayoutParams imageParams = new LinearLayout.LayoutParams(200, 200);
    imageParams.gravity = Gravity.CENTER;
    logo.setLayoutParams(imageParams);
    mainLayout.addView(logo);

    // Texto de bienvenida
    TextView welcome = new TextView(this);
    welcome.setText("Bienvenido!!");
    welcome.setTextColor(Color.WHITE);
    welcome.setTextSize(24);
    welcome.setGravity(Gravity.CENTER);
    welcome.setPadding(0, 32, 0, 16);
    welcome.setTypeface(null, android.graphics.Typeface.BOLD);
    mainLayout.addView(welcome);

    // Campo de Usuario
    EditText username = new EditText(this);
    username.setHint("Usuario");
    username.setTextColor(Color.WHITE);
    username.setHintTextColor(Color.LTGRAY);
    username.setBackground(null);
    mainLayout.addView(username);

    // Campo de Correo
    EditText email = new EditText(this);
    email.setHint("Correo");
    email.setTextColor(Color.WHITE);
    email.setHintTextColor(Color.LTGRAY);
    email.setBackground(null);
    mainLayout.addView(email);

    // Campo de Contraseña
    EditText password = new EditText(this);
    password.setHint("Contraseña");
    password.setInputType(android.text.InputType.TYPE_CLASS_TEXT | android.text.InputType.TYPE_TEXT_VARIATION_PASSWORD);
    password.setTextColor(Color.WHITE);
    password.setHintTextColor(Color.LTGRAY);
    password.setBackground(null);
    mainLayout.addView(password);

    // Botón Iniciar
    Button btnLogin = new Button(this);
    btnLogin.setText("iniciar");
    btnLogin.setBackgroundColor(Color.parseColor("#388E3C"));
    btnLogin.setTextColor(Color.WHITE);
    mainLayout.addView(btnLogin);

    // LinearLayout para los botones de redes sociales
    LinearLayout socialLayout = new LinearLayout(this);
    socialLayout.setOrientation(LinearLayout.HORIZONTAL);
    socialLayout.setGravity(Gravity.CENTER);
    socialLayout.setPadding(0, 16, 0, 32);

    // Botón de Twitter
    ImageButton twitterBtn = new ImageButton(this);
    twitterBtn.setImageResource(R.drawable.twitter_icon); // Reemplazar con la imagen correspondiente
    twitterBtn.setBackgroundColor(Color.TRANSPARENT);
    socialLayout.addView(twitterBtn);

    // Botón de Google
    ImageButton googleBtn = new ImageButton(this);
    googleBtn.setImageResource(R.drawable.google_icon); // Reemplazar con la imagen correspondiente
    googleBtn.setBackgroundColor(Color.TRANSPARENT);
    googleBtn.setPadding(16, 0, 16, 0);
    socialLayout.addView(googleBtn);

    // Botón de Instagram
    ImageButton instagramBtn = new ImageButton(this);
    instagramBtn.setImageResource(R.drawable.instagram_icon); // Reemplazar con la imagen correspondiente
    instagramBtn.setBackgroundColor(Color.TRANSPARENT);
    socialLayout.addView(instagramBtn);

    mainLayout.addView(socialLayout);

    // Pie de página: ¿Ya tienes una cuenta? Ingresa
    LinearLayout footerLayout = new LinearLayout(this);
    footerLayout.setOrientation(LinearLayout.HORIZONTAL);
    footerLayout.setGravity(Gravity.CENTER);

    TextView haveAccount = new TextView(this);
    haveAccount.setText("Ya tienes una cuenta? ");
    haveAccount.setTextColor(Color.WHITE);
    footerLayout.addView(haveAccount);

    TextView login = new TextView(this);
    login.setText("Ingresa");
    login.setTextColor(Color.WHITE);
    login.setTypeface(null, android.graphics.Typeface.BOLD);
    footerLayout.addView(login);

    mainLayout.addView(footerLayout);

    // ¿Olvidaste tu contraseña?
    TextView forgotPassword = new TextView(this);
    forgotPassword.setText("olvidaste tu contraseña?");
    forgotPassword.setTextColor(Color.WHITE);
    forgotPassword.setGravity(Gravity.CENTER);
    mainLayout.addView(forgotPassword);

    // Establecer el layout principal como la vista de la actividad
    setContentView(mainLayout);
}
