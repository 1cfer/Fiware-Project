# Moreha | FIWARE-based IoT Infrastructure

Infraestructura centralizada para la gestión de datos de contexto en tiempo real, diseñada específicamente para el ecosistema **Moreha**. Este repositorio facilita el despliegue de un entorno **FIWARE** robusto, optimizado para la interoperabilidad entre dispositivos IoT y aplicaciones de monitoreo ambiental.

## Arquitectura del Sistema
El despliegue se basa en la orquestación de contenedores mediante **Docker Compose**, integrando los siguientes componentes clave:

* **Orion Context Broker**: Gestión y persistencia de entidades de contexto bajo el estándar NGSI.
* **IoT Agents**: Capa de abstracción para la comunicación con dispositivos finales, permitiendo la traducción de protocolos específicos a entidades FIWARE.
* **Seguridad y Acceso**: Integración de **Keyrock** para la gestión de identidades y control de acceso basado en roles (RBAC).
* **Persistencia**: Uso de **MongoDB** como motor de base de datos para el almacenamiento de entidades de contexto.

## Integración de Hardware (Ecosistema TARS)
La infraestructura está configurada para recibir y procesar datos provenientes del prototipo **TARS**. Se incluye soporte nativo para el procesamiento de variables ambientales mediante:

* Sensores de temperatura de alta precisión como el **DS18B20**.
* Sensores de humedad y temperatura **SHT31**.
* Protocolos de comunicación optimizados para hardware basado en **ESP32**.

## Guía de Despliegue

### Requisitos Previos
* Docker Engine v20.10+
* Docker Compose v2.0+

### Ejecución
1. **Clonar el repositorio**:
   ```bash
   git clone [https://github.com/1cfer/fiware-project.git](https://github.com/1cfer/fiware-project.git)
   ```
 2. **Desplegar los servicios en segundo plano**:  
    ```bash
    docker-compose up
    ```
 3. **Verificar el estado de los contenedores**:  
    ```bash
    docker ps
    ```

Desarrollado por: Fernando Castro - Ingeniería Electrónica.
