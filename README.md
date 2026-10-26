import { useState } from 'react';

function Contador() {
  // Declaración del estado 'contador' con valor inicial 0
  const [contador, setContador] = useState(0);

  return (
    <div style={{ textAlign: 'center', marginTop: '20px' }}>
      <h2>Contador en React</h2>
      <p>Has hecho clic {contador} veces</p>
      <button onClick={() => setContador(contador + 1)}>
        Haz clic aquí
      </button>
    </div>
  );
}

export default Contador;
