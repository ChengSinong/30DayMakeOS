
src=boot.asm
bootstrap=boot.img

boot:
		nasm $(src) -o $(bootstrap)
fat12:
		@dd if=/dev/zero of=$(bootstrap) seek=1 count=2879 >> /dev/zero

run:boot fat12
		qemu-system-i386 -drive file=$(bootstrap),if=floppy