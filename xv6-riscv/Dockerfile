# Imagen base a utilizar
FROM ubuntu:24.04

# Para evitar las preguntas interactivas cuando se estan instalando recursos
ENV DEBIAN_FRONTEND=noninteractive

# Instalmos toolchain para RISC-V y QEMU
RUN apt-get update && apt-get install -y \
    git \
    build-essential \
    gdb-multiarch \
    qemu-system-misc \
    gcc-riscv64-linux-gnu \
    binutils-riscv64-linux-gnu \
    bc \
    && apt-get clean

# Creamos un directorio de trabajo  
WORKDIR /xv6

# Comando para mantener el contenedor corriendo
CMD ["/bin/bash"]