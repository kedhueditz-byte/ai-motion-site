const imageInput = document.getElementById("imageInput");
const videoInput = document.getElementById("videoInput");
const character = document.getElementById("character");
const video = document.getElementById("motionVideo");

imageInput.onchange = e => {
  character.src = URL.createObjectURL(e.target.files[0]);
};

videoInput.onchange = e => {
  video.src = URL.createObjectURL(e.target.files[0]);
};

function startMotion() {
  video.play();
  animate();
}

function animate() {
  if (!video.paused) {
    let scale = 1 + Math.sin(video.currentTime * 5) * 0.05;
    let rotate = Math.sin(video.currentTime * 3) * 10;
    let moveX = Math.sin(video.currentTime * 4) * 30;

    character.style.transform =
      `translateX(${moveX}px) scale(${scale}) rotate(${rotate}deg)`;

    requestAnimationFrame(animate);
  }
}
