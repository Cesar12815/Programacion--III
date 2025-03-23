# Programación 3 - Proyecto NestJS

## 📝 Descripción
Este repositorio contiene el proyecto de la clase de **Programación 3**, donde se enseña la metodología para trabajar con **DTOs (Data Transfer Objects)**, el uso de **interfaces** y el manejo de **seguridad** en aplicaciones backend. El proyecto está desarrollado utilizando **NestJS**, un framework progresivo de Node.js que permite construir aplicaciones escalables y mantenibles.

El objetivo principal es aprender a estructurar aplicaciones backend de manera profesional, implementando buenas prácticas de desarrollo, validación de datos y medidas de seguridad para proteger la información y los recursos.

---

## 📚 Contenidos

### 1. **DTOs (Data Transfer Objects)**
Los **DTOs** son objetos que se utilizan para transferir datos entre diferentes partes de una aplicación. En NestJS, los DTOs son fundamentales para:
- **Validar datos de entrada**: Garantizar que los datos enviados por el cliente cumplan con los requisitos esperados.
- **Estandarizar la estructura de datos**: Facilitar la comunicación entre el cliente y el servidor.
- **Proteger la lógica interna**: Evitar que datos no deseados o maliciosos lleguen a la capa de negocio.

#### Ejemplo de un DTO en NestJS:
```typescript
// filepath: src/cars/dto/create-car.dto.ts
import { IsString, IsInt, IsUUID } from 'class-validator';

export class CreateCarDto {
  @IsUUID()
  id: string;

  @IsString()
  brand: string;

  @IsString()
  model: string;

  @IsInt()
  year: number;
}