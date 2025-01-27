// Tombol "Pilih Fotomu"
document.getElementById('uploadBtn').addEventListener('click', () => {
    const input = document.createElement('input');
    input.type = 'file';
    input.accept = 'image/*';
    input.click();

    input.onchange = (event) => {
        const file = event.target.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = (e) => {
                document.getElementById('userImage').src = e.target.result;
                document.getElementById('popup').style.display = 'flex';
            };
            reader.readAsDataURL(file);
        }
    };
});

// Tombol "Ganti Foto"
document.getElementById('changePhoto').addEventListener('click', () => {
    const input = document.createElement('input');
    input.type = 'file';
    input.accept = 'image/*';
    input.click();

    input.onchange = (event) => {
        const file = event.target.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = (e) => {
                document.getElementById('userImage').src = e.target.result;
            };
            reader.readAsDataURL(file);
        }
    };
});

// Tombol "Unduh"
document.getElementById('downloadBtn').addEventListener('click', () => {
    const canvas = document.createElement('canvas');
    const userImage = document.getElementById('userImage');
    const frameOverlay = document.getElementById('frameOverlay');

    canvas.width = frameOverlay.width;
    canvas.height = frameOverlay.height;

    const ctx = canvas.getContext('2d');
    ctx.drawImage(userImage, 0, 0, canvas.width, canvas.height);
    ctx.drawImage(frameOverlay, 0, 0, canvas.width, canvas.height);

    const link = document.createElement('a');
    link.download = 'frame-result.png';
    link.href = canvas.toDataURL('image/png');
    link.click();
});
