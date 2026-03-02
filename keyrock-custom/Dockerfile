FROM fiware/idm:8.3.3

# 1. Copiamos tu archivo de estilos personalizado
COPY ./theme/style.css /opt/fiware-idm/public/stylesheets/style.css

# 2. Reemplazamos la vista de Login normal
COPY ./theme/login.ejs /opt/fiware-idm/views/auth/login.ejs

# 3. REEMPLAZAMOS LA VISTA DE AUTORIZACIÓN (La que te sale a ti)
COPY ./theme/login.ejs /opt/fiware-idm/views/oauth2/authorize.ejs