English
---

# 🌌 Interactive Bloch Sphere Visualizer

An interactive, web-based tool to visualize a qubit's state on the **Bloch Sphere** using **Three.js**. This project allows users to intuitively understand quantum state transitions by manipulating complex coefficients in real-time.

## 🧪 Mathematical Background

### 1. Qubit State Representation
A qubit state $|\psi\rangle$ is represented as a linear combination (superposition) of the basis states $|0\rangle$ and $|1\rangle$:
$$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$$
where $\alpha, \beta \in \mathbb{C}$. To remain a physically valid state, it must satisfy the **Normalization Condition**:
$$|\alpha|^2 + |\beta|^2 = 1$$

### 2. Measuring Probabilities
According to the Born rule, the probability of measuring the qubit in a specific basis state is the square of the amplitude's magnitude:
* **Probability of State $|0\rangle$:** $P(0) = |\alpha|^2$
* **Probability of State $|1\rangle$:** $P(1) = |\beta|^2$

### 3. Bloch Sphere Mapping
To map the complex coefficients $(\alpha, \beta)$ to 3D Cartesian coordinates $(x, y, z)$ on the Bloch sphere, we use the following transformations:

$$x = 2 \text{Re}(\alpha^* \beta)$$
$$y = 2 \text{Im}(\alpha^* \beta)$$
$$z = |\alpha|^2 - |\beta|^2$$



In spherical coordinates $(\theta, \phi)$, the state is expressed as:
$$|\psi\rangle = \cos\left(\frac{\theta}{2}\right)|0\rangle + e^{i\phi}\sin\left(\frac{\theta}{2}\right)|1\rangle$$
* $\theta$: The angle from the Z-axis (determines the weighting of the states).
* $\phi$: The azimuthal angle (determines the **relative phase** between states).

---

## 🛠 Features

* **Real-time Interaction:** Adjust $Re(\alpha)$, $Im(\alpha)$, and $Re(\beta)$ via sliders to see instant vector movement.
* **Automatic Normalization:** Ensures the state vector always stays on the surface of the sphere ($r=1$), regardless of input values.
* **3D Visualization:** High-performance rendering using Three.js with OrbitControls for 360-degree rotation and zoom.
* **Live Probability Feedback:** Displays calculated $P(0)$ and $P(1)$ values instantly.

## 🚀 Quick Start

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YOUR_USERNAME/bloch-sphere-visualizer.git
    ```
2.  **Open the project:**
    Simply open `index.html` in your favorite web browser.
3.  **Pro Tip:** Use the **Live Server** extension in VS Code for the best experience with ES Modules.

---

## 📚 Tech Stack

* [Three.js](https://threejs.org/) - 3D Engine (ESM version)
* [OrbitControls](https://threejs.org/docs/#examples/en/controls/OrbitControls) - Interactive camera handling
* **HTML5/CSS3** - Responsive UI and modern glassmorphism design

---

### 💡 Deployment
This project is a static site. You can host it for free using **GitHub Pages**:
1. Go to **Settings > Pages**.
2. Select the `main` branch as your source.
3. Your visualizer will be live at `https://YOUR_USERNAME.github.io/bloch-sphere-visualizer/`.

---
한국어
---

# 🌌 Interactive Bloch Sphere Visualizer

Three.js를 활용하여 큐비트(Qubit)의 상태를 3차원 Bloch 구 위에 실시간으로 시각화하는 웹 도구입니다. 복소 계수 $\alpha$와 $\beta$를 직접 조정하며 양자 상태의 변화를 직관적으로 이해할 수 있습니다.

## 🧪 Mathematical Background

### 1. Qubit State Representation
큐비트의 상태 $|\psi\rangle$은 두 기저 상태 $|0\rangle$과 $|1\rangle$의 선형 조합(중첩)으로 표현됩니다:
$$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$$
여기서 $\alpha, \beta \in \mathbb{C}$이며, 물리적으로 유효한 상태를 유지하기 위해 다음 **정규화 조건(Normalization)**을 만족해야 합니다:
$$|\alpha|^2 + |\beta|^2 = 1$$

### 2. Measuring Probabilities
큐비트를 측정했을 때 각 상태가 나타날 확률은 계수의 절대값 제곱과 같습니다:
* **State $|0\rangle$이 측정될 확률:** $P(0) = |\alpha|^2$
* **State $|1\rangle$이 측정될 확률:** $P(1) = |\beta|^2$

### 3. Bloch Sphere Mapping
복소 계수 $(\alpha, \beta)$를 3차원 데카르트 좌표계 $(x, y, z)$로 변환하여 Bloch 구 위에 점을 찍기 위해 다음 공식을 사용합니다:

$$x = 2 \text{Re}(\alpha^* \beta)$$
$$y = 2 \text{Im}(\alpha^* \beta)$$
$$z = |\alpha|^2 - |\beta|^2$$



구면 좌표계 $(\theta, \phi)$ 관점에서는 다음과 같이 표현됩니다:
$$|\psi\rangle = \cos\left(\frac{\theta}{2}\right)|0\rangle + e^{i\phi}\sin\left(\frac{\theta}{2}\right)|1\rangle$$
* $\theta$: Z축으로부터 기울어진 각도 (상태 비중 결정)
* $\phi$: X-Y 평면에서의 회전각 (상태 간의 상대적 위상 결정)

---

## 🛠 Features

* **Real-time Interaction:** 슬라이더를 통해 $Re(\alpha)$, $Im(\alpha)$, $Re(\beta)$를 실시간 조절.
* **Automatic Normalization:** 입력값이 정규화 조건을 벗어나도 자동으로 벡터 길이를 $1$로 조정.
* **3D Visualization:** Three.js 기반의 부드러운 3D 렌더링 및 마우스 드래그를 통한 시점 회전.
* **Probability Feedback:** 각 상태에 대한 측정 확률을 수치로 즉시 표시.

## 🚀 Quick Start

1. 이 저장소를 클론합니다.
   ```bash
   git clone https://github.com/YOUR_USERNAME/bloch-sphere-visualizer.git
   ```
2. `index.html` 파일을 브라우저에서 엽니다.
3. (권장) VS Code의 **Live Server** 확장을 사용하여 실행하면 더 안정적인 모듈 로딩이 가능합니다.

---

## 📚 Technologies Used

* [Three.js](https://threejs.org/) - 3D Engine
* [OrbitControls](https://threejs.org/docs/#examples/en/controls/OrbitControls) - Camera interaction
* [HTML5/CSS3] - UI components

---

### 💡 Tip for GitHub Pages
이 프로젝트는 서버 사이드 로직이 없는 정적 페이지이므로, **GitHub Settings > Pages**에서 `main` 브랜치를 선택하는 것만으로 무료 호스팅이 가능합니다!

---
