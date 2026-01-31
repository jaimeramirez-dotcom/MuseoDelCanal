<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rally: Las Llaves del Istmo</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a3a5f 0%, #0d2a4d 100%);
            color: #333;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 15px 50px rgba(0, 0, 0, 0.4);
            overflow: hidden;
            position: relative;
        }
        
        .header {
            background: linear-gradient(120deg, #0d2a4d 0%, #1a3a5f 100%);
            color: white;
            padding: 35px 30px;
            text-align: center;
            position: relative;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }
        
        .header h1 {
            font-size: 2.8rem;
            margin-bottom: 15px;
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
            letter-spacing: -0.5px;
            position: relative;
            display: inline-block;
        }
        
        .header h1::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80%;
            height: 4px;
            background: linear-gradient(90deg, #ffd700, #ff8c00, #ffd700);
            border-radius: 2px;
        }
        
        .header p {
            font-size: 1.35rem;
            margin-top: 25px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0.95;
            font-weight: 300;
        }
        
        .panama-flag {
            position: absolute;
            top: 20px;
            right: 25px;
            font-size: 2.5rem;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .progress-container {
            padding: 25px 30px 15px;
            background: #f5f7fa;
            border-bottom: 1px solid #e1e5eb;
        }
        
        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            font-weight: 600;
            color: #2c3e50;
            font-size: 0.95rem;
        }
        
        .progress-bar {
            background: #e9ecef;
            height: 16px;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.1);
        }
        
        .progress {
            background: linear-gradient(90deg, #2c7873 0%, #25839a 50%, #1e8ec6 100%);
            height: 100%;
            width: 0%;
            border-radius: 8px;
            transition: width 0.6s ease;
            position: relative;
        }
        
        .progress::after {
            content: "";
            position: absolute;
            top: -3px;
            right: -3px;
            width: 8px;
            height: 22px;
            background: #ffd700;
            border-radius: 4px;
            box-shadow: 0 0 8px rgba(255, 215, 0, 0.7);
            animation: shine 2s infinite;
        }
        
        @keyframes shine {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }
        
        .station {
            padding: 35px;
            display: none;
            animation: fadeIn 0.6s ease;
        }
        
        .station.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { 
                opacity: 0; 
                transform: translateY(20px);
            }
            to { 
                opacity: 1; 
                transform: translateY(0);
            }
        }
        
        .station-title {
            color: #1a3a5f;
            font-size: 2.1rem;
            margin-bottom: 25px;
            text-align: center;
            position: relative;
            padding-bottom: 15px;
        }
        
        .station-title::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 70%;
            height: 3px;
            background: linear-gradient(90deg, #ffd700, #ff8c00);
            border-radius: 3px;
        }
        
        .riddle-box {
            background: linear-gradient(145deg, #f8f9ff, #eef2f7);
            border-left: 6px solid #25839a;
            padding: 25px;
            margin: 25px 0;
            border-radius: 0 12px 12px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            position: relative;
            overflow: hidden;
        }
        
        .riddle-box::before {
            content: "❝";
            position: absolute;
            top: -20px;
            left: 10px;
            font-size: 8rem;
            color: rgba(37, 131, 154, 0.1);
            font-family: Georgia, serif;
            line-height: 1;
        }
        
        .riddle-box h3 {
            color: #1e8ec6;
            margin-bottom: 15px;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .riddle-box h3::before {
            content: "❓";
            font-size: 1.8rem;
        }
        
        .riddle-box p {
            font-size: 1.25rem;
            line-height: 1.7;
            margin-left: 25px;
            font-style: italic;
            color: #2c3e50;
            position: relative;
            z-index: 2;
        }
        
        .instructions {
            background: #e8f4ff;
            border: 2px solid #a9c9e6;
            border-radius: 15px;
            padding: 25px;
            margin: 25px 0;
            position: relative;
        }
        
        .instructions h3 {
            color: #1a3a5f;
            margin-bottom: 15px;
            font-size: 1.6rem;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .instructions h3::before {
            content: "🔍";
            font-size: 1.7rem;
        }
        
        .instructions p {
            font-size: 1.15rem;
            line-height: 1.8;
            margin-left: 5px;
        }
        
        .materials-list {
            background: linear-gradient(145deg, #f9f7f0, #e8e4d9);
            border: 2px solid #d4c8a8;
            border-radius: 15px;
            padding: 25px;
            margin: 25px 0;
            position: relative;
        }
        
        .materials-list::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #d4af37, #a67c00, #d4af37);
        }
        
        .materials-list h3 {
            color: #5d4037;
            margin-bottom: 20px;
            font-size: 1.7rem;
            text-align: center;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;
        }
        
        .materials-list h3::before,
        .materials-list h3::after {
            content: "📜";
            font-size: 1.8rem;
        }
        
        .materials-list ul {
            list-style-type: none;
            padding-left: 15px;
        }
        
        .materials-list li {
            padding: 12px 0 12px 40px;
            border-bottom: 1px dashed #c8b99a;
            font-size: 1.15rem;
            position: relative;
            line-height: 1.6;
        }
        
        .materials-list li:last-child {
            border-bottom: none;
        }
        
        .materials-list li::before {
            content: "✓";
            position: absolute;
            left: 0;
            top: 12px;
            width: 28px;
            height: 28px;
            background: #d4af37;
            color: #3e2723;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.1rem;
        }
        
        .answer-section {
            background: white;
            border-radius: 18px;
            padding: 30px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.12);
            margin: 30px 0;
            border: 2px solid #eaeff5;
        }
        
        .answer-section h3 {
            color: #1a3a5f;
            margin-bottom: 20px;
            font-size: 1.65rem;
            text-align: center;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 12px;
        }
        
        .answer-section h3::before {
            content: "🗝️";
            font-size: 1.9rem;
        }
        
        .input-group {
            margin: 25px 0;
        }
        
        .input-group label {
            display: block;
            margin-bottom: 12px;
            font-weight: 600;
            font-size: 1.25rem;
            color: #2c3e50;
            text-align: center;
        }
        
        .answer-input {
            width: 100%;
            padding: 18px 25px;
            font-size: 1.4rem;
            border: 3px solid #a9c9e6;
            border-radius: 14px;
            text-align: center;
            font-weight: 600;
            letter-spacing: 1px;
            transition: all 0.3s;
            background: #f8fbff;
            color: #1a3a5f;
        }
        
        .answer-input:focus {
            outline: none;
            border-color: #25839a;
            box-shadow: 0 0 0 4px rgba(37, 131, 154, 0.2);
            background: white;
        }
        
        .answer-input::placeholder {
            color: #a0b0c0;
            opacity: 1;
            font-weight: 400;
            letter-spacing: 0;
        }
        
        .btn-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 15px;
        }
        
        .btn {
            padding: 16px 25px;
            font-size: 1.35rem;
            border: none;
            border-radius: 14px;
            cursor: pointer;
            font-weight: 700;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }
        
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
        }
        
        .btn:active {
            transform: translateY(1px);
        }
        
        .submit-btn {
            background: linear-gradient(120deg, #2c7873 0%, #25839a 100%);
            color: white;
            width: 100%;
            font-size: 1.45rem;
            padding: 18px;
        }
        
        .submit-btn:hover {
            background: linear-gradient(120deg, #256a65 0%, #1e748c 100%);
            box-shadow: 0 0 25px rgba(37, 131, 154, 0.6);
        }
        
        .hint-btn {
            background: linear-gradient(120deg, #f5a623 0%, #f08c00 100%);
            color: white;
            width: 100%;
            font-size: 1.25rem;
            padding: 15px;
        }
        
        .hint-btn:hover {
            background: linear-gradient(120deg, #e69500 0%, #d47a00 100%);
            box-shadow: 0 0 25px rgba(240, 140, 0, 0.5);
        }
        
        .next-btn {
            background: linear-gradient(120deg, #43a047 0%, #2e7d32 100%);
            color: white;
            width: 100%;
            font-size: 1.5rem;
            padding: 18px;
            margin-top: 15px;
            display: none;
        }
        
        .next-btn.show {
            display: flex;
        }
        
        .next-btn:hover {
            background: linear-gradient(120deg, #388e3c 0%, #1b5e20 100%);
            box-shadow: 0 0 25px rgba(46, 125, 50, 0.6);
            transform: translateY(-2px) scale(1.02);
        }
        
        .hint {
            background: linear-gradient(145deg, #fff8e1, #ffecb3);
            border-left: 6px solid #ffc107;
            padding: 22px;
            margin: 25px 0;
            border-radius: 0 12px 12px 0;
            display: none;
            position: relative;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .hint.show {
            display: block;
            animation: slideDown 0.4s ease;
        }
        
        @keyframes slideDown {
            from { 
                opacity: 0; 
                transform: translateY(-15px);
            }
            to { 
                opacity: 1; 
                transform: translateY(0);
            }
        }
        
        .hint h4 {
            color: #5d4037;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.4rem;
        }
        
        .hint h4::before {
            content: "💡";
            font-size: 1.6rem;
        }
        
        .hint p {
            font-size: 1.15rem;
            line-height: 1.7;
            margin-left: 5px;
        }
        
        .success-message {
            background: linear-gradient(145deg, #e8f5e9, #c8e6c9);
            border-left: 6px solid #4caf50;
            padding: 25px;
            margin: 30px 0;
            border-radius: 0 12px 12px 0;
            display: none;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        
        .success-message::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(76, 175, 80, 0.15) 0%, rgba(255, 255, 255, 0) 70%);
            z-index: 0;
        }
        
        .success-message.show {
            display: block;
            animation: slideUp 0.6s ease;
        }
        
        @keyframes slideUp {
            from { 
                opacity: 0; 
                transform: translateY(30px);
            }
            to { 
                opacity: 1; 
                transform: translateY(0);
            }
        }
        
        .success-message strong {
            color: #2e7d32;
            font-size: 1.3rem;
            display: block;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }
        
        .success-message p {
            font-size: 1.2rem;
            line-height: 1.7;
            margin-left: 5px;
            position: relative;
            z-index: 1;
        }
        
        .final-activity {
            text-align: center;
            padding: 20px;
        }
        
        .final-instructions {
            background: #e3f2fd;
            border-radius: 18px;
            padding: 30px;
            margin: 25px 0;
            border: 2px solid #bbdefb;
        }
        
        .final-instructions h3 {
            color: #0d47a1;
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .final-instructions p {
            font-size: 1.3rem;
            line-height: 1.8;
            margin: 15px 0;
        }
        
        .phrase-container {
            background: linear-gradient(145deg, #f8fbff, #eef2f7);
            border: 3px solid #a9c9e6;
            border-radius: 20px;
            padding: 35px;
            margin: 30px 0;
            font-size: 1.5rem;
            line-height: 2.0;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
            position: relative;
            overflow: hidden;
        }
        
        .phrase-container::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 8px;
            background: linear-gradient(90deg, #ffd700, #25839a, #ffd700);
        }
        
        .blank-input {
            width: 180px;
            padding: 10px 15px;
            margin: 8px 5px;
            border: 3px solid #a9c9e6;
            border-radius: 12px;
            text-align: center;
            font-weight: bold;
            font-size: 1.35rem;
            transition: all 0.3s;
            background: white;
            min-width: 150px;
        }
        
        .blank-input:focus {
            outline: none;
            border-color: #25839a;
            box-shadow: 0 0 0 4px rgba(37, 131, 154, 0.3);
            background: #f0f7ff;
        }
        
        .blank-input.correct {
            border-color: #4caf50;
            background-color: #e8f5e9;
            box-shadow: 0 0 0 4px rgba(76, 175, 80, 0.3);
            font-weight: bold;
            position: relative;
        }
        
        .blank-input.correct::after {
            content: "✓";
            position: absolute;
            right: -15px;
            top: 50%;
            transform: translateY(-50%);
            color: #4caf50;
            font-weight: bold;
            font-size: 1.5rem;
        }
        
        .blank-input.incorrect {
            border-color: #f44336;
            background-color: #ffebee;
            box-shadow: 0 0 0 4px rgba(244, 67, 54, 0.3);
            animation: shake 0.5s;
        }
        
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            20%, 60% { transform: translateX(-5px); }
            40%, 80% { transform: translateX(5px); }
        }
        
        .verify-btn {
            background: linear-gradient(120deg, #673ab7 0%, #4527a0 100%);
            color: white;
            width: 100%;
            font-size: 1.6rem;
            padding: 20px;
            margin: 25px 0;
            box-shadow: 0 6px 20px rgba(69, 39, 160, 0.4);
        }
        
        .verify-btn:hover {
            background: linear-gradient(120deg, #5e35b1 0%, #311b92 100%);
            box-shadow: 0 8px 25px rgba(69, 39, 160, 0.6);
        }
        
        .final-success {
            background: linear-gradient(145deg, #e8f5e9, #c8e6c9);
            border: 4px solid #4caf50;
            border-radius: 25px;
            padding: 40px;
            margin: 35px 0;
            display: none;
            animation: fadeIn 0.8s ease, pulse 2s infinite;
            position: relative;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
            text-align: center;
        }
        
        .final-success.show {
            display: block;
        }
        
        @keyframes pulse {
            0%, 100% { box-shadow: 0 0 25px rgba(76, 175, 80, 0.5); }
            50% { box-shadow: 0 0 40px rgba(76, 175, 80, 0.8); }
        }
        
        .final-success h3 {
            color: #1b5e20;
            font-size: 2.2rem;
            margin-bottom: 20px;
            text-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .final-success p {
            font-size: 1.6rem;
            line-height: 1.7;
            margin: 15px 0;
            font-weight: 500;
        }
        
        .completed-phrase {
            font-size: 1.8rem;
            line-height: 1.8;
            margin: 25px 0;
            padding: 25px;
            background: white;
            border-radius: 18px;
            border-left: 6px solid #4caf50;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
        }
        
        .completed-phrase strong {
            color: #1a3a5f;
            background: linear-gradient(120deg, #ffd700, #ff8c00);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 800;
            position: relative;
        }
        
        .completed-phrase strong::after {
            content: "";
            position: absolute;
            bottom: 5px;
            left: 0;
            width: 100%;
            height: 8px;
            background: linear-gradient(120deg, #ffd700, #ff8c00);
            z-index: -1;
            opacity: 0.4;
            border-radius: 4px;
        }
        
        .congratulations {
            text-align: center;
            padding: 50px 30px;
            background: linear-gradient(135deg, #1a3a5f 0%, #0d2a4d 100%);
            color: white;
        }
        
        .congratulations h2 {
            font-size: 3.2rem;
            margin-bottom: 25px;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
            background: linear-gradient(90deg, #ffd700, #ffffff, #ffd700);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            position: relative;
            display: inline-block;
        }
        
        .congratulations h2::after {
            content: "🏆";
            position: absolute;
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 4rem;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateX(-50%) translateY(0); }
            50% { transform: translateX(-50%) translateY(-20px); }
        }
        
        .congratulations p {
            font-size: 1.8rem;
            margin: 25px 0;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.6;
            font-weight: 300;
        }
        
        .diploma {
            background: linear-gradient(145deg, #f9f4e5, #e8e0ce);
            border: 20px solid #d4af37;
            border-radius: 15px;
            padding: 40px;
            margin: 35px auto;
            max-width: 700px;
            box-shadow: 0 15px 50px rgba(0, 0, 0, 0.4);
            position: relative;
            font-size: 1.5rem;
            line-height: 1.8;
            color: #5d4037;
            font-style: italic;
            text-align: center;
            font-weight: 500;
        }
        
        .diploma::before,
        .diploma::after {
            content: "";
            position: absolute;
            width: 15px;
            height: 15px;
            background: #d4af37;
            border-radius: 50%;
        }
        
        .diploma::before {
            top: -10px;
            left: -10px;
        }
        
        .diploma::after {
            bottom: -10px;
            right: -10px;
        }
        
        .restart-btn {
            background: linear-gradient(120deg, #ffd700 0%, #ff8c00 100%);
            color: #3e2723;
            padding: 20px 60px;
            font-size: 1.8rem;
            margin-top: 30px;
            font-weight: 800;
            letter-spacing: 2px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }
        
        .restart-btn:hover {
            background: linear-gradient(120deg, #ffcc00 0%, #e67e00 100%);
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
        }
        
        .hidden {
            display: none;
        }
        
        .debriefing {
            background: #e8f4ff;
            border-radius: 18px;
            padding: 30px;
            margin: 30px 0;
            border: 2px solid #a9c9e6;
        }
        
        .debriefing h3 {
            color: #0d47a1;
            text-align: center;
            margin-bottom: 20px;
            font-size: 1.9rem;
        }
        
        .debriefing ul {
            padding-left: 25px;
            margin-top: 15px;
        }
        
        .debriefing li {
            font-size: 1.25rem;
            line-height: 1.8;
            margin-bottom: 12px;
        }
        
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.3rem;
            }
            
            .header p {
                font-size: 1.15rem;
            }
            
            .station {
                padding: 25px;
            }
            
            .station-title {
                font-size: 1.8rem;
            }
            
            .answer-input {
                font-size: 1.25rem;
                padding: 15px;
            }
            
            .btn {
                font-size: 1.2rem;
                padding: 14px;
            }
            
            .next-btn {
                font-size: 1.3rem;
                padding: 16px;
            }
            
            .blank-input {
                width: 140px;
                font-size: 1.2rem;
                padding: 8px 12px;
                min-width: 120px;
            }
            
            .phrase-container {
                font-size: 1.3rem;
                padding: 25px 15px;
            }
            
            .verify-btn {
                font-size: 1.4rem;
                padding: 16px;
            }
            
            .final-success h3 {
                font-size: 1.8rem;
            }
            
            .final-success p {
                font-size: 1.4rem;
            }
            
            .completed-phrase {
                font-size: 1.5rem;
            }
            
            .congratulations h2 {
                font-size: 2.5rem;
            }
            
            .congratulations p {
                font-size: 1.5rem;
            }
            
            .diploma {
                font-size: 1.3rem;
                padding: 25px 20px;
            }
        }
        
        @media (max-width: 480px) {
            .header h1 {
                font-size: 2rem;
            }
            
            .header p {
                font-size: 1rem;
            }
            
            .station {
                padding: 20px 15px;
            }
            
            .materials-list li {
                font-size: 1rem;
                padding-left: 35px;
            }
            
            .blank-input {
                width: 120px;
                font-size: 1.1rem;
                padding: 7px 10px;
                min-width: 100px;
                margin: 6px 3px;
            }
            
            .phrase-container {
                font-size: 1.2rem;
                padding: 20px 10px;
                line-height: 1.8;
            }
            
            .completed-phrase {
                font-size: 1.4rem;
                padding: 20px 15px;
            }
            
            .btn, .next-btn, .verify-btn {
                font-size: 1.15rem;
                padding: 12px;
            }
            
            .restart-btn {
                font-size: 1.5rem;
                padding: 16px 40px;
            }
            
            .final-success {
                padding: 25px 15px;
            }
            
            .final-success h3 {
                font-size: 1.6rem;
            }
            
            .final-success p {
                font-size: 1.3rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="panama-flag">🇵🇦</div>
            <h1>Rally: "Las Llaves del Istmo"</h1>
            <p>Comisiones de Investigación Histórica - Museo del Canal de Panamá</p>
        </div>
        
        <div class="progress-container">
            <div class="progress-label">
                <span>Estación <span id="current-step">0</span> de 6</span>
                <span><span id="progress-percent">0</span>% Completado</span>
            </div>
            <div class="progress-bar">
                <div class="progress" id="progress"></div>
            </div>
        </div>
        
        <!-- Estación 0: Introducción -->
        <div class="station active" id="station-intro">
            <div class="station-title">Bienvenidos, Comisiones de Investigación</div>
            
            <div class="instructions">
                <h3>🎯 Concepto del Rally</h3>
                <p>Ustedes son "comisiones de investigación histórica" que deben descifrar una serie de acertijos. Cada respuesta correcta les dará una pieza de un rompecabezas final. El objetivo es recuperar todas las "llaves" (conocimientos) para entender la historia completa del Canal de Panamá.</p>
            </div>
            
            <div class="materials-list">
                <h3>Materiales por Equipo</h3>
                <ul>
                    <li>Un sobre inicial con las Reglas y el Primer Acertijo</li>
                    <li>Un mapa o plano del museo (marcado con zonas clave)</li>
                    <li>Una hoja de respuestas con espacios para anotar las pistas</li>
                    <li>Un sobre final misterioso que solo se abrirá al tener todas las piezas</li>
                </ul>
            </div>
            
            <div class="instructions">
                <h3>⏱️ Duración y Logística</h3>
                <p><strong>Duración:</strong> 1.5 - 2 horas de visita activa</p>
                <p><strong>Equipos:</strong> Grupos de 4-5 estudiantes, con un portavoz y un anotador</p>
                <p><strong>Supervisión:</strong> Cada equipo puede tener un "guía fantasma" (docente o acompañante) que solo interviene si se pierden o para asegurar el comportamiento adecuado</p>
            </div>
            
            <div class="debriefing">
                <h3>💡 Importante: Debriefing Post-Rally</h3>
                <p>Al finalizar, se reunirán todos para discutir:</p>
                <ul>
                    <li>¿Qué aprendieron que no sabían?</li>
                    <li>¿Qué acertijo fue más difícil y por qué?</li>
                    <li>¿Cómo se conectan todas las piezas que encontraron?</li>
                </ul>
                <p>Esto solidifica el aprendizaje y va más allá de la competencia.</p>
            </div>
            
            <button class="submit-btn" onclick="nextStation()">
                <span>¡Comenzar la Aventura!</span>
                <span>▶️</span>
            </button>
        </div>
        
        <!-- Estación 1: Galería de Banderas / Entrada -->
        <div class="station" id="station-1">
            <div class="station-title">📍 Estación 1: Galería de Banderas / Entrada</div>
            
            <div class="riddle-box">
                <h3>Acertijo Inicial</h3>
                <p>"No soy un país, pero fui un estado dentro de otro. Mi bandera no ondeaba aquí, pero mis leyes se cumplían. Para encontrar la primera pista, busquen donde las banderas cuentan una historia de ausencia y presencia."</p>
            </div>
            
            <div class="instructions">
                <h3>🔍 Qué deben hacer:</h3>
                <p>En la Galería de Banderas, deben identificar la bandera que NO está (la de la Zona del Canal, que era una bandera de EE.UU. con un sello distintivo). Junto a la explicación de esta ausencia, habrá un código QR o un símbolo escondido (ej: un número en el borde de un panel) que les dará la primera palabra clave.</p>
            </div>
            
            <div class="answer-section">
                <h3>¿Cuál es la primera palabra clave?</h3>
                <div class="input-group">
                    <input type="text" id="answer1" class="answer-input" placeholder="Escribe tu respuesta aquí..." autocomplete="off">
                </div>
                <div class="btn-container">
                    <button class="hint-btn" onclick="toggleHint('hint1')">
                        <span>💡 Necesito una pista</span>
                    </button>
                    <button class="submit-btn" onclick="checkAnswer(1, ['ENCLAVE'], 'ENCLAVE')">
                        <span>Verificar Respuesta</span>
                        <span>✅</span>
                    </button>
                </div>
                
                <div class="hint" id="hint1">
                    <h4>Pista:</h4>
                    <p>Piensen en el concepto de un territorio controlado por otro país dentro de sus fronteras. ¿Cómo se llama esto? Busquen la explicación sobre la bandera ausente de la Zona del Canal.</p>
                </div>
                
                <div class="success-message" id="success1">
                    <strong>✅ ¡Correcto!</strong> Han descubierto la primera llave: <strong>"ENCLAVE"</strong>
                    <p>Esta palabra representa cómo la Zona del Canal fue un territorio estadounidense dentro de Panamá, con sus propias leyes y administración.</p>
                </div>
                
                <button class="next-btn" id="next-btn-1" onclick="nextStation()">
                    <span>➡️ Siguiente Estación: Panamá Antes del Canal</span>
                </button>
            </div>
        </div>
        
        <!-- Estación 2: Panamá Antes del Canal -->
        <div class="station" id="station-2">
            <div class="station-title">📍 Estación 2: Panamá Antes del Canal</div>
            
            <div class="riddle-box">
                <h3>Acertijo</h3>
                <p>"Puente biológico, cuna de culturas. Antes de cortar la tierra, la naturaleza la unió. Encuentren al gigante que ya no está y anoten el número de sus colmillos. Ese número es su próxima clave."</p>
            </div>
            
            <div class="instructions">
                <h3>🔍 Qué deben hacer:</h3>
                <p>Buscar en la sala la información sobre el Gran Intercambio Americano y la megafauna (como el Mastodonte). Deben encontrar una ilustración o fósil y anotar un número clave (ej: 2 colmillos). Ese número se combina con una instrucción (ej: "Busca el panel número X que habla de las rutas de tránsito").</p>
            </div>
            
            <div class="answer-section">
                <h3>¿Cuál es la segunda palabra clave?</h3>
                <div class="input-group">
                    <input type="text" id="answer2" class="answer-input" placeholder="Escribe tu respuesta aquí..." autocomplete="off">
                </div>
                <div class="btn-container">
                    <button class="hint-btn" onclick="toggleHint('hint2')">
                        <span>💡 Necesito una pista</span>
                    </button>
                    <button class="submit-btn" onclick="checkAnswer(2, ['TRANSITO', 'TRÁNSITO', 'TRANSITO'], 'TRÁNSITO')">
                        <span>Verificar Respuesta</span>
                        <span>✅</span>
                    </button>
                </div>
                
                <div class="hint" id="hint2">
                    <h4>Pista:</h4>
                    <p>El número de colmillos (2) los guiará a un panel específico. Busquen en ese panel la palabra que describe el propósito fundamental del Canal: la conexión entre dos océanos.</p>
                </div>
                
                <div class="success-message" id="success2">
                    <strong>✅ ¡Correcto!</strong> Han descubierto la segunda llave: <strong>"TRÁNSITO"</strong>
                    <p>Esta palabra representa la función esencial del Canal como ruta de paso entre el Atlántico y el Pacífico, continuando el rol que Panamá ha tenido desde tiempos prehistóricos.</p>
                </div>
                
                <button class="next-btn" id="next-btn-2" onclick="nextStation()">
                    <span>➡️ Siguiente Estación: Imaginando un Canal / Construcción</span>
                </button>
            </div>
        </div>
        
        <!-- Estación 3: Imaginando un Canal / Construcción -->
        <div class="station" id="station-3">
            <div class="station-title">📍 Estación 3: Imaginando un Canal / Construcción</div>
            
            <div class="riddle-box">
                <h3>Acertijo</h3>
                <p>"El sueño de dos océanos unidos tuvo un precio alto en oro y sudor. No todos los que lo imaginaron lo vieron terminar. Encuentren la herramienta más humilde pero más numerosa, y su nombre en plural será su nueva llave."</p>
            </div>
            
            <div class="instructions">
                <h3>🔍 Qué deben hacer:</h3>
                <p>En la sala de la construcción, deben identificar la herramienta icónica del trabajador (la pala o el pico). En una foto grande de trabajadores, habrá una flecha discretamente dibujada que apunta a un tipo específico de pala. Al lado de esa imagen, en letra pequeña, encontrarán la pista.</p>
            </div>
            
            <div class="answer-section">
                <h3>¿Cuál es la tercera palabra clave?</h3>
                <div class="input-group">
                    <input type="text" id="answer3" class="answer-input" placeholder="Escribe tu respuesta aquí..." autocomplete="off">
                </div>
                <div class="btn-container">
                    <button class="hint-btn" onclick="toggleHint('hint3')">
                        <span>💡 Necesito una pista</span>
                    </button>
                    <button class="submit-btn" onclick="checkAnswer(3, ['PALAS', 'PICO', 'PICOS'], 'PALAS')">
                        <span>Verificar Respuesta</span>
                        <span>✅</span>
                    </button>
                </div>
                
                <div class="hint" id="hint3">
                    <h4>Pista:</h4>
                    <p>Piensen en las herramientas básicas que usaron miles de trabajadores para mover tierra. La más común era simple pero esencial para la construcción del Canal. Busquen en las fotografías de los trabajadores.</p>
                </div>
                
                <div class="success-message" id="success3">
                    <strong>✅ ¡Correcto!</strong> Han descubierto la tercera llave: <strong>"PALAS"</strong>
                    <p>Esta palabra representa el esfuerzo físico y el trabajo manual que construyó el Canal. Miles de trabajadores usaron estas herramientas básicas para mover millones de metros cúbicos de tierra.</p>
                </div>
                
                <button class="next-btn" id="next-btn-3" onclick="nextStation()">
                    <span>➡️ Siguiente Estación: La Vida en la Zona</span>
                </button>
            </div>
        </div>
        
        <!-- Estación 4: La Vida en la Zona -->
        <div class="station" id="station-4">
            <div class="station-title">📍 Estación 4: La Vida en la Zona</div>
            
            <div class="riddle-box">
                <h3>Acertijo (más analítico)</h3>
                <p>"Dos mundos en una misma franja. Oro para unos, plata para otros. La desigualdad se medía en colores y letreros. Encuentren la orden que separaba y, de sus palabras prohibidas, tomen la tercera."</p>
            </div>
            
            <div class="instructions">
                <h3>🔍 Qué deben hacer:</h3>
                <p>Buscar en los documentos o recreaciones los carteles de segregación ("For Gold Employees Only", "For Silver Employees Only"). Deben transcribir una frase completa. La "tercera palabra" de esa frase (ej: "Employees") es la pista. O encontrar una reglamentación y extraer una palabra clave como "SEGREGACIÓN".</p>
            </div>
            
            <div class="answer-section">
                <h3>¿Cuál es la cuarta palabra clave?</h3>
                <div class="input-group">
                    <input type="text" id="answer4" class="answer-input" placeholder="Escribe tu respuesta aquí..." autocomplete="off">
                </div>
                <div class="btn-container">
                    <button class="hint-btn" onclick="toggleHint('hint4')">
                        <span>💡 Necesito una pista</span>
                    </button>
                    <button class="submit-btn" onclick="checkAnswer(4, ['SEGREGACION', 'SEGREGACIÓN', 'EMPLOYEES'], 'SEGREGACIÓN')">
                        <span>Verificar Respuesta</span>
                        <span>✅</span>
                    </button>
                </div>
                
                <div class="hint" id="hint4">
                    <h4>Pista:</h4>
                    <p>Busquen los carteles que mostraban la discriminación. La tercera palabra de "For Gold Employees Only" es "Employees", pero la palabra clave que representa este sistema es "SEGREGACIÓN".</p>
                </div>
                
                <div class="success-message" id="success4">
                    <strong>✅ ¡Correcto!</strong> Han descubierto la cuarta llave: <strong>"SEGREGACIÓN"</strong>
                    <p>Esta palabra representa la desigualdad y discriminación que existió en la Zona del Canal, donde los trabajadores y residentes eran separados por su origen étnico y nacionalidad, creando dos mundos dentro de un mismo territorio.</p>
                </div>
                
                <button class="next-btn" id="next-btn-4" onclick="nextStation()">
                    <span>➡️ Siguiente Estación: La Ruta por la Soberanía</span>
                </button>
            </div>
        </div>
        
        <!-- Estación 5: La Ruta por la Soberanía -->
        <div class="station" id="station-5">
            <div class="station-title">📍 Estación 5: La Ruta por la Soberanía (1964-1999)</div>
            
            <div class="riddle-box">
                <h3>Acertijo (emocional y numérico)</h3>
                <p>"La chispa que encendió la llama final. Un número grabado en la memoria nacional: los mártires de enero. Encuentren sus nombres y sumen el día del mes en que cayeron. Esa suma es un código."</p>
            </div>
            
            <div class="instructions">
                <h3>🔍 Qué deben hacer:</h3>
                <p>En la sección del 9 de Enero de 1964, buscar los nombres de los mártires (Ascanio Arosemena, etc.) y la fecha. Deben sumar el día (9). El código "9" les indica que busquen un objeto relacionado con el Tratado Torrijos-Carter (por ejemplo, en el panel número 9 o en la vitrina 9). Allí encontrarán la pista final.</p>
            </div>
            
            <div class="answer-section">
                <h3>¿Cuál es la quinta palabra clave?</h3>
                <div class="input-group">
                    <input type="text" id="answer5" class="answer-input" placeholder="Escribe tu respuesta aquí..." autocomplete="off">
                </div>
                <div class="btn-container">
                    <button class="hint-btn" onclick="toggleHint('hint5')">
                        <span>💡 Necesito una pista</span>
                    </button>
                    <button class="submit-btn" onclick="checkAnswer(5, ['TRATADO', 'SOBERANIA', 'SOBERANÍA'], 'TRATADO')">
                        <span>Verificar Respuesta</span>
                        <span>✅</span>
                    </button>
                </div>
                
                <div class="hint" id="hint5">
                    <h4>Pista:</h4>
                    <p>El día 9 de enero es clave. Busquen en el panel o vitrina número 9 información sobre el acuerdo que devolvió el Canal a Panamá. La palabra clave está relacionada con este acuerdo histórico.</p>
                </div>
                
                <div class="success-message" id="success5">
                    <strong>✅ ¡Correcto!</strong> Han descubierto la quinta llave: <strong>"TRATADO"</strong>
                    <p>Esta palabra representa el Tratado Torrijos-Carter de 1977, que estableció la devolución del Canal de Panamá a su país, culminando décadas de lucha por la soberanía nacional.</p>
                </div>
                
                <button class="next-btn" id="next-btn-5" onclick="nextStation()">
                    <span>➡️ Siguiente: Actividad Final - Armando el Rompecabezas Histórico</span>
                </button>
            </div>
        </div>
        
        <!-- Estación Final: Actividad Final y Resolución -->
        <div class="station" id="station-final">
            <div class="station-title">🏆 Actividad Final: Armando el Rompecabezas Histórico</div>
            
            <div class="final-activity">
                <div class="final-instructions">
                    <h3>¡Han recolectado todas las llaves del pasado!</h3>
                    <p>Ahora deben usar sus palabras clave para completar la frase que define la historia del Canal de Panamá.</p>
                    <p><strong>Acertijo Final:</strong> Completen los espacios en blanco con las palabras que encontraron en cada estación.</p>
                </div>
                
                <div class="phrase-container">
                    <p>Una lucha por el control de un 
                        <input type="text" class="blank-input" id="final-answer-1" placeholder="_____">
                        , construido con 
                        <input type="text" class="blank-input" id="final-answer-2" placeholder="_____">
                        y marcado por la 
                        <input type="text" class="blank-input" id="final-answer-3" placeholder="_____">
                        , que comenzó como un 
                        <input type="text" class="blank-input" id="final-answer-4" placeholder="_____">
                        y culminó con un 
                        <input type="text" class="blank-input" id="final-answer-5" placeholder="_____">
                        que devolvió la 
                        <input type="text" class="blank-input" id="final-answer-6" placeholder="_____.">
                    </p>
                </div>
                
                <button class="verify-btn" onclick="checkFinalPhrase()">
                    <span>🔍 Verificar Frase Completa</span>
                </button>
                
                <div class="final-success" id="final-success">
                    <h3>🎉 ¡Felicidades Comisiones de Investigación! 🎉</h3>
                    <p>¡Han completado exitosamente el rompecabezas histórico!</p>
                    <p>La frase completa que define la historia del Canal de Panamá es:</p>
                    
                    <div class="completed-phrase">
                        "Una lucha por el control de un <strong>TRÁNSITO</strong>, construido con <strong>PALAS</strong> y marcado por la <strong>SEGREGACIÓN</strong>, que comenzó como un <strong>ENCLAVE</strong> y culminó con un <strong>TRATADO</strong> que devolvió la <strong>SOBERANÍA</strong>."
                    </div>
                    
                    <p>¡Excelente trabajo de investigación histórica!</p>
                </div>
                
                <button class="next-btn" id="next-btn-final" onclick="nextStation()">
                    <span>➡️ Continuar a la Ceremonia de Premiación</span>
                </button>
            </div>
        </div>
        
        <!-- Estación de Felicitaciones -->
        <div class="station" id="station-congrats">
            <div class="congratulations">
                <h2>¡Misión Cumplida!</h2>
                <p>Comisiones de Investigación Histórica</p>
                <p><strong>Rally: "Las Llaves del Istmo"</strong></p>
                <p>Gracias por participar en esta aventura educativa por la historia del Canal de Panamá.</p>
                
                <div class="diploma">
                    Este diploma acredita que el equipo ha completado exitosamente el Rally "Las Llaves del Istmo", demostrando excepcional capacidad de investigación histórica, trabajo en equipo y comprensión de la trascendental historia del Canal de Panamá.
                </div>
                
                <button class="restart-btn" onclick="restartRally()">
                    <span>🔄 Volver al Inicio</span>
                </button>
            </div>
        </div>
    </div>

    <script>
        let currentStation = 0;
        const totalStations = 6; // Introduction + 5 stations + final activity
        
        // Initialize progress
        updateProgress();
        
        function updateProgress() {
            const progress = document.getElementById('progress');
            const currentStepEl = document.getElementById('current-step');
            const progressPercentEl = document.getElementById('progress-percent');
            
            // Calculate progress percentage (excluding intro and congrats)
            const progressValue = Math.min(100, Math.round((currentStation / totalStations) * 100));
            
            progress.style.width = `${progressValue}%`;
            currentStepEl.textContent = currentStation;
            progressPercentEl.textContent = progressValue;
        }
        
        function nextStation() {
            // Hide current station
            document.querySelector('.station.active').classList.remove('active');
            
            // Move to next station
            currentStation++;
            
            // Show next station
            if (currentStation === 1) {
                document.getElementById('station-1').classList.add('active');
            } else if (currentStation === 2) {
                document.getElementById('station-2').classList.add('active');
            } else if (currentStation === 3) {
                document.getElementById('station-3').classList.add('active');
            } else if (currentStation === 4) {
                document.getElementById('station-4').classList.add('active');
            } else if (currentStation === 5) {
                document.getElementById('station-5').classList.add('active');
            } else if (currentStation === 6) {
                document.getElementById('station-final').classList.add('active');
            } else if (currentStation === 7) {
                document.getElementById('station-congrats').classList.add('active');
            }
            
            // Update progress bar
            updateProgress();
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        function normalizeAnswer(answer) {
            return answer.trim().toUpperCase()
                .normalize("NFD")
                .replace(/[\u0300-\u036f]/g, "")
                .replace(/\s+/g, "");
        }
        
        function checkAnswer(stationNumber, acceptableAnswers, intendedWord) {
            const inputId = `answer${stationNumber}`;
            const input = document.getElementById(inputId);
            const answer = normalizeAnswer(input.value);
            const successMessage = document.getElementById(`success${stationNumber}`);
            const nextButton = document.getElementById(`next-btn-${stationNumber}`);
            
            // Normalize acceptable answers
            const normalizedAcceptable = acceptableAnswers.map(a => normalizeAnswer(a));
            
            if (normalizedAcceptable.includes(answer)) {
                // Show success message
                successMessage.classList.add('show');
                
                // Show next button
                nextButton.classList.add('show');
                
                // Disable input and submit button
                input.disabled = true;
                input.style.borderColor = '#4caf50';
                input.style.backgroundColor = '#e8f5e9';
                
                // Disable the submit button for this station
                const submitBtn = input.closest('.answer-section').querySelector('.submit-btn');
                submitBtn.disabled = true;
                submitBtn.style.opacity = '0.6';
                submitBtn.style.cursor = 'not-allowed';
                
                // Remove hint button if visible
                const hintBtn = input.closest('.answer-section').querySelector('.hint-btn');
                if (hintBtn) {
                    hintBtn.disabled = true;
                    hintBtn.style.opacity = '0.6';
                    hintBtn.style.cursor = 'not-allowed';
                }
            } else {
                // Shake effect for wrong answer
                input.parentElement.classList.add('shake');
                setTimeout(() => {
                    input.parentElement.classList.remove('shake');
                }, 500);
                
                alert('❌ Respuesta incorrecta. ¡Sigan investigando en el museo!');
                input.value = '';
                input.focus();
            }
        }
        
        function toggleHint(hintId) {
            const hint = document.getElementById(hintId);
            hint.classList.toggle('show');
            
            // Change button text
            const button = event.target;
            if (hint.classList.contains('show')) {
                button.innerHTML = '<span>❌ Ocultar pista</span>';
            } else {
                button.innerHTML = '<span>💡 Necesito una pista</span>';
            }
        }
        
        function checkFinalPhrase() {
            // Define the correct answers for each blank (normalized)
            const correctAnswers = [
                ['TRANSITO', 'TRÁNSITO'], // Blank 1
                ['PALAS'],                // Blank 2
                ['SEGREGACION', 'SEGREGACIÓN'], // Blank 3
                ['ENCLAVE'],              // Blank 4
                ['TRATADO'],              // Blank 5
                ['SOBERANIA', 'SOBERANÍA'] // Blank 6
            ];
            
            let allCorrect = true;
            const inputs = [];
            const totalBlanks = 6;
            
            // Reset previous styles
            for (let i = 1; i <= totalBlanks; i++) {
                const input = document.getElementById(`final-answer-${i}`);
                input.classList.remove('correct', 'incorrect');
                inputs.push(input);
            }
            
            // Check each input
            for (let i = 0; i < totalBlanks; i++) {
                const input = inputs[i];
                const value = normalizeAnswer(input.value);
                const isCorrect = correctAnswers[i].some(ans => normalizeAnswer(ans) === value);
                
                if (isCorrect) {
                    input.classList.add('correct');
                } else {
                    input.classList.add('incorrect');
                    allCorrect = false;
                }
            }
            
            if (allCorrect) {
                // Show success message
                document.getElementById('final-success').classList.add('show');
                
                // Show next button with delay
                setTimeout(() => {
                    document.getElementById('next-btn-final').classList.add('show');
                }, 1500);
                
                // Disable the verify button
                const verifyButton = document.querySelector('#station-final .verify-btn');
                verifyButton.disabled = true;
                verifyButton.style.opacity = '0.6';
                verifyButton.style.cursor = 'not-allowed';
                verifyButton.innerHTML = '<span>Frase Verificada ✅</span>';
                
                // Disable all inputs
                inputs.forEach(input => {
                    input.disabled = true;
                });
            } else {
                // Show error message
                const incorrectCount = document.querySelectorAll('.blank-input.incorrect').length;
                alert(`❌ ${incorrectCount} respuesta(s) incorrecta(s). Revisen las palabras clave que encontraron en cada estación.`);
            }
        }
        
        function restartRally() {
            // Reset current station
            currentStation = 0;
            
            // Hide all stations and show intro
            document.querySelectorAll('.station').forEach(station => {
                station.classList.remove('active');
            });
            document.getElementById('station-intro').classList.add('active');
            
            // Reset progress
            updateProgress();
            
            // Reset all inputs and messages
            document.querySelectorAll('.answer-input').forEach(input => {
                input.value = '';
                input.disabled = false;
                input.style.borderColor = '#a9c9e6';
                input.style.backgroundColor = '#f8fbff';
            });
            
            document.querySelectorAll('.success-message').forEach(msg => {
                msg.classList.remove('show');
            });
            
            document.querySelectorAll('.hint').forEach(hint => {
                hint.classList.remove('show');
            });
            
            document.querySelectorAll('.hint-btn').forEach(button => {
                button.innerHTML = '<span>💡 Necesito una pista</span>';
                button.disabled = false;
                button.style.opacity = '1';
                button.style.cursor = 'pointer';
            });
            
            document.querySelectorAll('.next-btn').forEach(button => {
                button.classList.remove('show');
            });
            
            document.querySelectorAll('.submit-btn').forEach(button => {
                button.disabled = false;
                button.style.opacity = '1';
                button.style.cursor = 'pointer';
            });
            
            // Reset final activity
            document.querySelectorAll('.blank-input').forEach(input => {
                input.value = '';
                input.disabled = false;
                input.classList.remove('correct', 'incorrect');
                input.style.borderColor = '#a9c9e6';
                input.style.backgroundColor = 'white';
            });
            
            document.getElementById('final-success').classList.remove('show');
            
            const verifyButton = document.querySelector('#station-final .verify-btn');
            if (verifyButton) {
                verifyButton.disabled = false;
                verifyButton.style.opacity = '1';
                verifyButton.style.cursor = 'pointer';
                verifyButton.innerHTML = '<span>🔍 Verificar Frase Completa</span>';
            }
            
            document.getElementById('next-btn-final').classList.remove('show');
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        // Add shake animation style
        const style = document.createElement('style');
        style.textContent = `
            @keyframes shake {
                0%, 100% { transform: translateX(0); }
                10%, 30%, 50%, 70%, 90% { transform: translateX(-5px); }
                20%, 40%, 60%, 80% { transform: translateX(5px); }
            }
            .shake {
                animation: shake 0.5s;
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>

