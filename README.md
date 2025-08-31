
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Diagramas Cadena Cliente-Proveedor</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 20px;
            background: #000000;
            min-height: 100vh;
            color: white;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .main-title {
            text-align: center;
            font-size: 2.8em;
            color: #ffffff;
            margin-bottom: 40px;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            letter-spacing: 2px;
        }

        .diagram-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            margin-top: 30px;
        }

        .column-title {
            text-align: center;
            font-size: 2.2em;
            font-weight: bold;
            margin-bottom: 30px;
            padding: 15px;
            border-radius: 15px;
        }

        .actual-title {
            background: linear-gradient(135deg, #e74c3c, #c0392b);
            color: white;
        }

        .proposed-title {
            background: linear-gradient(135deg, #3498db, #2980b9);
            color: white;
        }

        .flow-column {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }

        .process-step {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border: 2px solid #ffffff;
            border-radius: 15px;
            padding: 20px;
            min-width: 280px;
            max-width: 350px;
            text-align: center;
            font-weight: bold;
            box-shadow: 0 8px 25px rgba(255,255,255,0.1);
            transition: all 0.3s ease;
            color: white;
            font-size: 1em;
            line-height: 1.4;
        }

        .process-step:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(255,255,255,0.2);
        }

        .problem-step {
            border-color: #e74c3c;
            background: rgba(231, 76, 60, 0.2);
        }

        .solution-step {
            border-color: #3498db;
            background: rgba(52, 152, 219, 0.2);
        }

        .arrow-down {
            font-size: 2.5em;
            font-weight: bold;
            margin: 10px 0;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .problem-arrow {
            color: #e74c3c;
        }

        .solution-arrow {
            color: #3498db;
        }

        .final-result {
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(15px);
            border: 3px solid;
            border-radius: 20px;
            padding: 25px;
            text-align: center;
            font-weight: bold;
            font-size: 1.1em;
            margin-top: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .problem-result {
            border-color: #e74c3c;
            background: rgba(231, 76, 60, 0.3);
            color: #ff6b6b;
        }

        .solution-result {
            border-color: #3498db;
            background: rgba(52, 152, 219, 0.3);
            color: #74b9ff;
        }

        .result-icon {
            font-size: 2em;
            margin-bottom: 10px;
            display: block;
        }

        .metrics-comparison {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255,255,255,0.2);
            border-radius: 20px;
            padding: 30px;
            margin-top: 50px;
            text-align: center;
        }

        .metrics-title {
            font-size: 1.8em;
            font-weight: bold;
            margin-bottom: 25px;
            color: #FFD700;
        }

        .metrics-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .metric-card {
            background: rgba(255,255,255,0.1);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .metric-number {
            font-size: 2.2em;
            font-weight: bold;
            display: block;
            margin-bottom: 8px;
        }

        .current-metric { color: #e74c3c; }
        .proposed-metric { color: #3498db; }
        .improvement-metric { color: #2ecc71; }
    </style>
</head>
<body>
    <div class="container">
        <div class="main-title">CADENA CLIENTE-PROVEEDOR</div>
        
        <div class="diagram-container">
            <!-- SITUACIÓN ACTUAL -->
            <div class="flow-column">
                <div class="column-title actual-title">ACTUAL</div>
                
                <div class="process-step problem-step">
                    Proveedor entrega barras de acero sin pruebas de dureza
                </div>
                
                <div class="arrow-down problem-arrow">↓</div>
                
                <div class="process-step problem-step">
                    Recepción en planta sin inspección rigurosa
                </div>
                
                <div class="arrow-down problem-arrow">↓</div>
                
                <div class="process-step problem-step">
                    Proceso de mecanizado con herramientas CNC<br>
                    <small>(sin monitoreo de desgaste)</small>
                </div>
                
                <div class="arrow-down problem-arrow">↓</div>
                
                <div class="process-step problem-step">
                    Piezas defectuosas<br>
                    <small>(fracturas y fuera de tolerancia ±0.1 mm)</small>
                </div>
                
                <div class="arrow-down problem-arrow">↓</div>
                
                <div class="final-result problem-result">
                    <span class="result-icon">📉</span>
                    Cliente recibe con retraso<br>
                    <strong>20% de rechazo</strong>
                </div>
            </div>

            <!-- SITUACIÓN PROPUESTA -->
            <div class="flow-column">
                <div class="column-title proposed-title">PROPUESTA</div>
                
                <div class="process-step solution-step">
                    Proveedor entrega barras de acero con certificado y pruebas de dureza
                </div>
                
                <div class="arrow-down solution-arrow">↓</div>
                
                <div class="process-step solution-step">
                    Recepción con inspección de materiales<br>
                    <small>(formato y pruebas ASTM E10)</small>
                </div>
                
                <div class="arrow-down solution-arrow">↓</div>
                
                <div class="process-step solution-step">
                    Proceso de mecanizado CNC con control estadístico de procesos (CEP)
                </div>
                
                <div class="arrow-down solution-arrow">↓</div>
                
                <div class="process-step solution-step">
                    Operarios capacitados en uso de instrumentos de medición
                </div>
                
                <div class="arrow-down solution-arrow">↓</div>
                
                <div class="final-result solution-result">
                    <span class="result-icon">👤</span>
                    Cliente recibe a tiempo y con calidad garantizada<br>
                    <strong>5% de rechazo</strong>
                </div>
            </div>
        </div>

        <!-- MÉTRICAS COMPARATIVAS -->
        <div class="metrics-comparison">
            <div class="metrics-title">📊 Comparación de Resultados</div>
            <div class="metrics-grid">
                <div class="metric-card">
                    <span class="metric-number current-metric">20%</span>
                    <div>Rechazo Actual</div>
                </div>
                <div class="metric-card">
                    <span class="metric-number proposed-metric">5%</span>
                    <div>Rechazo Propuesto</div>
                </div>
                <div class="metric-card">
                    <span class="metric-number current-metric">$792K</span>
                    <div>Costo Actual</div>
                </div>
                <div class="metric-card">
                    <span class="metric-number proposed-metric">$570K</span>
                    <div>Inversión</div>
                </div>
                <div class="metric-card">
                    <span class="metric-number improvement-metric">75%</span>
                    <div>Reducción Costos</div>
                </div>
                <div class="metric-card">
                    <span class="metric-number improvement-metric">12</span>
                    <div>Meses ROI</div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
