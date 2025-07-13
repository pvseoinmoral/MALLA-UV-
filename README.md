<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Malla UV – Obstetricia</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f3f4f6; padding: 20px; }
    h1 { text-align: center; color: #333; }
    .semestre {
      margin: 10px 0;
      background: #fff;
      border: 1px solid #ccc;
      border-radius: 6px;
      padding: 12px 16px;
      cursor: pointer;
      transition: background 0.3s;
    }
    .semestre:hover { background: #e0f0ff; }
    .asignaturas { display: none; padding: 10px 25px; color: #444; }
    .asignatura { margin-bottom: 6px; }
  </style>
</head>
<body>

  <h1>Malla Curricular UV – Obstetricia y Puericultura</h1>

  <!-- Genera un bloque por semestre -->
  NOMBRE_SEMESTRE

  <script>
    function toggle(el) {
      const asgs = el.querySelector('.asignaturas');
      asgs.style.display = asgs.style.display === 'block' ? 'none' : 'block';
    }
    document.addEventListener('DOMContentLoaded', () => {
      const container = document.body;
      const malla = {
        "1º Semestre": ["Anatomía","Química General y Orgánica","Biología","Histología","Psicología General","Introducción a la Matronería","Autorregulación","Lenguaje y Comunicación"],
        "2º Semestre": ["Embriología","Bioquímica","Microbiología","Fisiología","Atención de Matronería I","Matemática Aplicada en Salud","Inglés","Educación en Salud e Interculturalidad"],
        "3º Semestre": ["Fisiopatología","Salud Fetal y Neonatal I","Salud Ginecológica I","Salud Obstétrica I","Atención de Matronería II","Farmacología Aplicada","Salud Pública","Inglés II"],
        "4º Semestre": ["Salud Familiar y Comunitaria","Salud Fetal y Neonatal II","Salud Ginecológica II","Salud Obstétrica II","Atención de Matronería III","Módulo Práctico Obstétrico","Sexualidad y Afectividad","Bioestadística para el Diseño de Investigación"],
        "5º Semestre": ["Salud Familiar Aplicada I","Salud Neonatal Aplicada I","Salud Ginecológica Aplicada I","Salud Obstétrica Aplicada I","Módulo Práctico Integrado I","Gerontología","Metodología de la Investigación I","TIPE I"],
        "6º Semestre": ["Salud Familiar Aplicada II","Salud Neonatal Aplicada II","Salud Ginecológica Aplicada II","Salud Obstétrica Aplicada II","Módulo Práctico Integrado II","Metodología de la Investigación II","Gerenciamiento y Liderazgo I"],
        "7º Semestre": ["Salud Familiar Integrada I","Salud Neonatal Integrada I","Salud Gineco‑Obstétrica Integrada I","Módulo Práctico Integrado III","Seminario de Tesis I","Gerenciamiento y Liderazgo II"],
        "8º Semestre": ["Salud Familiar Integrada II","Salud Neonatal Integrada II","Salud Gineco‑Obstétrica Integrada II","Módulo Práctico Integrado IV","Seminario de Tesis II","TIPE II"],
        "9º Semestre": ["Internado Intrahospitalario I","Internado Salud Familiar y Gestión I"],
        "10º Semestre": ["Internado Intrahospitalario II","Internado Salud Familiar y Gestión II"]
      };
      Object.entries(malla).forEach(([sem, asigns]) => {
        const div = document.createElement('div');
        div.className = 'semestre';
        div.onclick = () => toggle(div);
        div.innerHTML = `<strong>${sem}</strong><div class="asignaturas">${asigns.map(a=>`<div class="asignatura">${a}</div>`).join('')}</div>`;
        container.appendChild(div);
      });
    });
  </script>
</body>
</html>
