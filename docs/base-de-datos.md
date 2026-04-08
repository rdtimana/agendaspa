# Base de Datos

## Tablas

### 1. Usuarios
```sql
CREATE TABLE usuarios (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    contrasena VARCHAR(255) NOT NULL,
    telefono VARCHAR(15),
    fecha_creacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 2. Servicios
```sql
CREATE TABLE servicios (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(100) NOT NULL,
    descripcion TEXT,
    precio DECIMAL(10, 2) NOT NULL,
    duracion INT NOT NULL  -- Duración en minutos
);
```

### 3. Empleados
```sql
CREATE TABLE empleados (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(100) NOT NULL,
    especialidad VARCHAR(100),
    telefono VARCHAR(15),
    email VARCHAR(100) UNIQUE NOT NULL,
    fecha_creacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 4. Citas
```sql
CREATE TABLE citas (
    id INT PRIMARY KEY AUTO_INCREMENT,
    usuario_id INT,
    servicio_id INT,
    empleado_id INT,
    fecha_hora DATETIME NOT NULL,
    estado ENUM('pendiente', 'confirmada', 'cancelada') DEFAULT 'pendiente',
    FOREIGN KEY (usuario_id) REFERENCES usuarios(id),
    FOREIGN KEY (servicio_id) REFERENCES servicios(id),
    FOREIGN KEY (empleado_id) REFERENCES empleados(id)
);
```

### 5. Disponibilidad
```sql
CREATE TABLE disponibilidad (
    id INT PRIMARY KEY AUTO_INCREMENT,
    empleado_id INT,
    fecha DATE NOT NULL,
    hora_inicio TIME NOT NULL,
    hora_fin TIME NOT NULL,
    FOREIGN KEY (empleado_id) REFERENCES empleados(id)
);
```
