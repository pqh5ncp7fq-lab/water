<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Global Perspectives on Jewish Civilization - Premium Platform</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600;700&family=Playfair+Display:wght@400;500;600;700&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #0a1931;
            --secondary-color: #f7f7f7;
            --accent-color: #d4af37;
            --accent-light: #f4e4a6;
            --danger-color: #c53d3d;
            --dark-bg: #0a0e17;
            --dark-card: #1a2238;
            --text-dark: #2c2c2c;
            --text-light: #666666;
            --background-light: #f5f7fa;
            --border-color: #e0e0e0;
            --shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            --shadow-heavy: 0 20px 50px rgba(0, 0, 0, 0.15);
            --glow: 0 0 25px rgba(212, 175, 55, 0.4);
            --transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Lato', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, var(--background-light) 0%, #e6e9f0 100%);
            color: var(--text-dark);
            line-height: 1.7;
            min-height: 100vh;
            overflow-x: hidden;
            transition: var(--transition);
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 30px;
        }

        h1, h2, h3, h4, h5, h6 {
            font-family: 'Cinzel', serif;
            font-weight: 600;
            letter-spacing: 0.5px;
        }

        /* 第一部分：首页 */
        #hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(rgba(10, 25, 49, 0.85), rgba(26, 58, 107, 0.85)), 
                        url('https://youimg1.c-ctrip.com/target/100h160000010n7h25CA5.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            position: relative;
            overflow: hidden;
        }

        #hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.1)"/></svg>');
            background-size: cover;
        }

        .hero-content {
            max-width: 900px;
            position: relative;
            z-index: 1;
        }

        .hero-content h1 {
            font-size: clamp(3rem, 7vw, 5rem);
            margin-bottom: 2rem;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.5);
            font-weight: 700;
            letter-spacing: 1px;
        }

        .hero-content p {
            font-size: clamp(1.3rem, 3vw, 1.8rem);
            margin-bottom: 3rem;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
            line-height: 1.8;
            font-family: 'Playfair Display', serif;
        }

        .explore-btn {
            padding: 20px 50px;
            border-radius: 50px;
            font-size: 1.4rem;
            position: relative;
            overflow: hidden;
            font-weight: 600;
            border: none;
            background: linear-gradient(135deg, var(--accent-color), #b8941f);
            color: var(--text-dark);
            box-shadow: 0 10px 25px rgba(212, 175, 55, 0.4);
            cursor: pointer;
            transition: var(--transition);
            font-family: 'Playfair Display', serif;
            letter-spacing: 0.5px;
        }

        .explore-btn:hover {
            background: linear-gradient(135deg, #b8941f, var(--accent-color));
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(212, 175, 55, 0.6);
        }

        /* 第二部分：登录选择页面 */
        #login-selection {
            min-height: 100vh;
            display: none;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(rgba(10, 25, 49, 0.9), rgba(26, 58, 107, 0.9)), 
                        url('https://youimg1.c-ctrip.com/target/100h160000010n7h25CA5.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .login-content {
            max-width: 800px;
            position: relative;
            z-index: 1;
        }

        .login-content h2 {
            font-size: clamp(2.5rem, 5vw, 3.5rem);
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            font-weight: 700;
        }

        .login-content p {
            font-size: clamp(1.1rem, 2.5vw, 1.4rem);
            margin-bottom: 3rem;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
            line-height: 1.7;
            font-family: 'Playfair Display', serif;
        }

        .login-options {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .login-card {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px 30px;
            width: 300px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.2);
            cursor: pointer;
        }

        .login-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.25);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }

        .login-card i {
            font-size: 3.5rem;
            color: var(--accent-color);
            margin-bottom: 20px;
        }

        .login-card h3 {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: white;
        }

        .login-card p {
            font-size: 1rem;
            margin-bottom: 25px;
            color: rgba(255, 255, 255, 0.9);
        }

        .login-btn {
            padding: 12px 30px;
            border-radius: 30px;
            font-size: 1.1rem;
            background: var(--accent-color);
            color: var(--text-dark);
            border: none;
            cursor: pointer;
            transition: var(--transition);
            font-weight: 600;
            font-family: 'Playfair Display', serif;
            width: 100%;
        }

        .login-btn:hover {
            background: #e6c34c;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.4);
        }

        /* 学生登录模态框 */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(8px);
        }

        .modal-content {
            background-color: var(--secondary-color);
            padding: 50px;
            border-radius: 20px;
            box-shadow: var(--shadow);
            max-width: 500px;
            width: 90%;
            text-align: center;
            transition: var(--transition);
            position: relative;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }

        .modal-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--primary-color);
            font-weight: 700;
        }

        .modal-text {
            margin-bottom: 30px;
            line-height: 1.7;
            font-size: 1.1rem;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-bottom: 20px;
            text-align: left;
        }

        .form-group label {
            font-weight: 600;
            font-size: 1.1rem;
            color: var(--primary-color);
            font-family: 'Playfair Display', serif;
        }

        .form-control {
            width: 100%;
            padding: 14px;
            border: 1px solid var(--border-color);
            border-radius: 10px;
            font-size: 1rem;
            background: var(--background-light);
            transition: var(--transition);
            font-family: 'Lato', sans-serif;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(10, 25, 49, 0.1);
        }

        .note {
            font-size: 0.9rem;
            color: var(--text-light);
            margin-top: 5px;
            font-style: italic;
        }

        .modal-actions {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .btn {
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            transition: var(--transition);
            padding: 14px 28px;
            font-family: 'Playfair Display', serif;
            letter-spacing: 0.5px;
            position: relative;
            overflow: hidden;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary-color), #1a3a6b);
            color: white;
            box-shadow: 0 8px 20px rgba(10, 25, 49, 0.3);
        }

        .btn-primary:hover {
            background: linear-gradient(135deg, #1a3a6b, var(--primary-color));
            transform: translateY(-3px);
            box-shadow: 0 12px 25px rgba(10, 25, 49, 0.4);
        }

        .btn-secondary {
            background: rgba(0, 0, 0, 0.1);
            color: var(--text-dark);
        }

        .btn-secondary:hover {
            background: rgba(0, 0, 0, 0.15);
        }

        /* 第三部分：平台内容 */
        #platform {
            display: none;
        }

        /* 头部样式 */
        header {
            background: linear-gradient(135deg, var(--primary-color), #1a3a6b);
            color: var(--secondary-color);
            padding: 1.8rem 0;
            box-shadow: var(--shadow-heavy);
            position: relative;
            overflow: hidden;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .logo-text h1 {
            font-size: 2.2rem;
            margin-bottom: 8px;
            font-weight: 700;
        }

        .logo-text p {
            font-size: 1.1rem;
            opacity: 0.9;
            font-family: 'Playfair Display', serif;
        }

        .header-controls {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .user-info {
            background: rgba(255, 255, 255, 0.15);
            padding: 10px 20px;
            border-radius: 30px;
            backdrop-filter: blur(5px);
            font-weight: 600;
        }

        .theme-toggle {
            background: rgba(255, 255, 255, 0.2);
            border: none;
            color: white;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: var(--transition);
            backdrop-filter: blur(5px);
        }

        .theme-toggle:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: rotate(15deg);
        }

        /* 语言切换按钮样式 */
        .language-toggle {
            background: rgba(255, 255, 255, 0.2);
            border: none;
            color: white;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: var(--transition);
            backdrop-filter: blur(5px);
            margin-left: 10px;
        }
        
        .language-toggle:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: scale(1.1);
        }

        /* 导航栏 */
        nav {
            background-color: var(--secondary-color);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 100;
            transition: var(--transition);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 30px;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            padding: 1.2rem 1.8rem;
            position: relative;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            transition: var(--transition);
            position: relative;
            font-family: 'Playfair Display', serif;
            font-size: 1.1rem;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent-color);
            transition: var(--transition);
        }

        .nav-links a:hover::after,
        .nav-links a.active::after {
            width: 100%;
        }

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text-dark);
            cursor: pointer;
        }

        /* 主内容区 */
        main {
            display: flex;
            flex-direction: column;
            gap: 50px;
            padding: 50px 0;
        }

        /* 犹太文化图案 */
        .jewish-pattern {
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 40px 0;
            gap: 30px;
            flex-wrap: wrap;
        }

        .star-of-david {
            width: 100px;
            height: 100px;
            background: var(--accent-color);
            clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
            animation: rotate 15s linear infinite;
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.5);
        }

        .menorah {
            width: 80px;
            height: 100px;
            position: relative;
        }

        .menorah::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 12px;
            height: 70px;
            background: var(--accent-color);
            border-radius: 6px;
            box-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
        }

        .menorah::after {
            content: '';
            position: absolute;
            bottom: 70px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 12px;
            background: var(--accent-color);
            border-radius: 6px;
            box-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
        }

        .menorah .flame {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 18px;
            height: 25px;
            background: #ffb347;
            background: linear-gradient(to bottom, #ffcc33, #ffb347);
            border-radius: 50% 50% 20% 20%;
            box-shadow: 0 0 15px #ff9900;
            animation: flicker 2s infinite alternate;
        }

        .dead-sea-scroll {
            width: 100px;
            height: 120px;
            background: #d2b48c;
            border-radius: 8px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
            border: 1px solid #b8941f;
        }

        .dead-sea-scroll::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent 0%, rgba(255,255,255,0.3) 50%, transparent 100%);
            animation: scroll-shine 4s infinite;
        }

        .dead-sea-scroll::after {
            content: '';
            position: absolute;
            top: 15px;
            left: 15px;
            right: 15px;
            bottom: 15px;
            border: 1px solid rgba(0,0,0,0.2);
            border-radius: 5px;
        }

        /* 上传作业区域 */
        .upload-section {
            margin-bottom: 50px;
            position: relative;
        }

        .section-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--border-color);
        }

        .section-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--accent-color), #b8941f);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.8rem;
            box-shadow: 0 5px 15px rgba(212, 175, 55, 0.4);
        }

        .section-title {
            font-size: 2.2rem;
            color: var(--primary-color);
            font-weight: 700;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -17px;
            left: 0;
            width: 100px;
            height: 2px;
            background: var(--accent-color);
        }

        .section {
            background: var(--secondary-color);
            border-radius: 20px;
            padding: 40px;
            box-shadow: var(--shadow-heavy);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--accent-color), var(--primary-color));
        }

        .upload-form {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .form-group label {
            font-weight: 600;
            font-size: 1.1rem;
            color: var(--primary-color);
            font-family: 'Playfair Display', serif;
        }

        .file-upload {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .file-types {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .file-type-btn {
            padding: 12px 20px;
            background: var(--background-light);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 500;
        }

        .file-type-btn.active {
            background: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
        }

        .file-input {
            display: none;
        }

        .file-preview {
            margin-top: 15px;
            padding: 20px;
            border: 2px dashed var(--border-color);
            border-radius: 15px;
            min-height: 100px;
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            background: rgba(245, 247, 250, 0.5);
        }

        .file-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px 15px;
            background: var(--background-light);
            border-radius: 10px;
            font-size: 0.95rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            transition: var(--transition);
        }

        .file-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .file-item .remove-file {
            color: var(--danger-color);
            cursor: pointer;
            transition: var(--transition);
        }

        .file-item .remove-file:hover {
            transform: scale(1.2);
        }

        .btn-accent {
            background: linear-gradient(135deg, var(--accent-color), #b8941f);
            color: var(--text-dark);
            box-shadow: 0 10px 25px rgba(212, 175, 55, 0.4);
        }

        .btn-accent:hover {
            background: linear-gradient(135deg, #b8941f, var(--accent-color));
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(212, 175, 55, 0.6);
        }

        .btn-text {
            background: none;
            color: var(--text-light);
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 8px 16px;
        }

        .btn-text:hover {
            color: var(--primary-color);
            background: rgba(10, 25, 49, 0.05);
        }

        /* 作业展示区 */
        .assignments-section {
            position: relative;
        }

        .assignment-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(380px, 1fr));
            gap: 35px;
        }

        .assignment-card {
            background: var(--secondary-color);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .assignment-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .assignment-cover {
            height: 220px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .assignment-cover-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .assignment-card:hover .assignment-cover-image {
            transform: scale(1.05);
        }

        .assignment-cover::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 70px;
            background: linear-gradient(transparent, rgba(0, 0, 0, 0.5));
        }

        .assignment-content {
            padding: 30px;
        }

        .assignment-title {
            font-size: 1.5rem;
            margin-bottom: 12px;
            color: var(--primary-color);
            font-weight: 600;
            font-family: 'Playfair Display', serif;
        }

        .assignment-meta {
            display: flex;
            justify-content: space-between;
            font-size: 0.95rem;
            color: var(--text-light);
            margin-bottom: 18px;
        }

        .assignment-description {
            margin-bottom: 25px;
            line-height: 1.7;
        }

        .assignment-files {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 25px;
        }

        .file-badge {
            display: flex;
            align-items: center;
            gap: 6px;
            padding: 8px 14px;
            background: var(--background-light);
            border-radius: 20px;
            font-size: 0.85rem;
            color: var(--text-light);
            transition: var(--transition);
        }

        .file-badge:hover {
            background: var(--primary-color);
            color: white;
            transform: translateY(-3px);
        }

        .assignment-actions {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* 删除按钮样式 */
        .delete-btn {
            background: var(--danger-color);
            color: white;
            border: none;
            border-radius: 8px;
            padding: 8px 16px;
            cursor: pointer;
            transition: var(--transition);
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 6px;
            font-size: 0.9rem;
        }

        .delete-btn:hover {
            background: #a52a2a;
            transform: translateY(-2px);
        }

        /* 评论删除按钮样式 */
        .comment-delete-btn {
            background: rgba(197, 61, 61, 0.1);
            color: var(--danger-color);
            border: 1px solid var(--danger-color);
            border-radius: 6px;
            padding: 4px 10px;
            cursor: pointer;
            transition: var(--transition);
            font-size: 0.8rem;
            margin-left: auto;
        }

        .comment-delete-btn:hover {
            background: var(--danger-color);
            color: white;
        }

        /* 论坛评论头部布局 */
        .forum-comment-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

        /* 页脚 */
        footer {
            background: linear-gradient(135deg, var(--primary-color), #1a3a6b);
            color: var(--secondary-color);
            padding: 60px 0 25px;
            margin-top: 80px;
            position: relative;
        }

        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--accent-color), var(--primary-color));
        }

        .contact-info {
            text-align: center;
            margin-bottom: 50px;
        }

        .contact-info h3 {
            font-size: 2rem;
            margin-bottom: 30px;
            font-weight: 700;
            font-family: 'Cinzel', serif;
        }

        .contact-details {
            display: flex;
            flex-direction: column;
            gap: 20px;
            align-items: center;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            font-size: 1.2rem;
        }

        .contact-item i {
            color: var(--accent-color);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            font-size: 0.95rem;
            color: rgba(255, 255, 255, 0.7);
        }

        /* 语言切换相关样式 */
        [data-lang="en"] {
            display: none;
        }

        body.english-mode [data-lang="zh"] {
            display: none;
        }

        body.english-mode [data-lang="en"] {
            display: block;
        }

        /* 作业展示增强样式 */
        .assignment-media {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 25px;
        }

        .media-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: var(--transition);
        }

        .media-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }

        .media-image {
            width: 200px;
            height: 150px;
            object-fit: cover;
        }

        .media-video {
            width: 200px;
            height: 150px;
            object-fit: cover;
            background: #000;
        }

        .media-file {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            width: 200px;
            height: 150px;
            background: var(--background-light);
            padding: 15px;
        }

        .media-file i {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--primary-color);
        }

        .media-file-name {
            font-size: 0.9rem;
            text-align: center;
            word-break: break-word;
            width: 100%;
        }

        .media-actions {
            position: absolute;
            top: 10px;
            right: 10px;
            display: flex;
            gap: 5px;
        }

        .media-action-btn {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: rgba(0,0,0,0.7);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: var(--transition);
        }

        .media-action-btn:hover {
            background: var(--danger-color);
            transform: scale(1.1);
        }

        /* 模态框样式 */
        .media-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(5px);
        }

        .media-modal-content {
            max-width: 90%;
            max-height: 90%;
            position: relative;
        }

        .media-modal-content img,
        .media-modal-content video {
            max-width: 100%;
            max-height: 100%;
            border-radius: 10px;
        }

        .media-modal-close {
            position: absolute;
            top: -40px;
            right: 0;
            color: white;
            font-size: 2rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .media-modal-close:hover {
            color: var(--accent-color);
        }

        /* 文件下载按钮 */
        .download-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 8px 15px;
            background: var(--primary-color);
            color: white;
            border-radius: 20px;
            text-decoration: none;
            font-size: 0.9rem;
            transition: var(--transition);
            margin-top: 10px;
        }

        .download-btn:hover {
            background: #1a3a6b;
            transform: translateY(-3px);
        }

        /* 作业详情模态框 */
        .assignment-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(8px);
            padding: 20px;
            overflow-y: auto;
        }

        .assignment-modal-content {
            background-color: var(--secondary-color);
            border-radius: 20px;
            box-shadow: var(--shadow);
            max-width: 900px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
            transition: var(--transition);
            position: relative;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }

        .dark-mode .assignment-modal-content {
            background: var(--dark-card);
        }

        .assignment-modal-header {
            padding: 30px 30px 20px;
            border-bottom: 1px solid var(--border-color);
        }

        .assignment-modal-title {
            font-size: 2rem;
            color: var(--primary-color);
            margin-bottom: 10px;
            font-weight: 700;
        }

        .dark-mode .assignment-modal-title {
            color: var(--accent-color);
        }

        .assignment-modal-meta {
            display: flex;
            justify-content: space-between;
            color: var(--text-light);
            font-size: 1rem;
        }

        .assignment-modal-body {
            padding: 30px;
        }

        .assignment-modal-description {
            margin-bottom: 30px;
            line-height: 1.7;
            font-size: 1.1rem;
        }

        .assignment-modal-close {
            position: absolute;
            top: 20px;
            right: 20px;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(0,0,0,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: var(--transition);
        }

        .assignment-modal-close:hover {
            background: var(--danger-color);
            color: white;
        }

        /* 文件上传预览增强 */
        .file-preview-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }

        .preview-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            height: 120px;
            background: var(--background-light);
            display: flex;
            flex-direction: column;
        }

        .preview-item img {
            width: 100%;
            height: 80px;
            object-fit: cover;
        }

        .preview-item .file-info {
            padding: 8px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            font-size: 0.8rem;
        }

        .preview-item .remove-preview {
            position: absolute;
            top: 5px;
            right: 5px;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: rgba(0,0,0,0.7);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 0.7rem;
        }

        /* 默认封面样式 */
        .default-cover {
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--primary-color), #1a3a6b);
            color: white;
            text-align: center;
            padding: 20px;
            position: relative;
            overflow: hidden;
        }

        .default-cover::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.1)"/></svg>');
            background-size: cover;
        }

        .default-cover i {
            font-size: 3rem;
            margin-bottom: 15px;
            color: var(--accent-color);
            z-index: 1;
        }

        .default-cover h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            z-index: 1;
            font-family: 'Cinzel', serif;
        }

        .default-cover p {
            font-size: 1rem;
            opacity: 0.9;
            z-index: 1;
        }

        /* 论坛评论样式 */
        .forum-comment {
            position: relative;
            padding: 20px;
            background: var(--background-light);
            border-radius: 10px;
            margin-bottom: 15px;
            transition: var(--transition);
        }

        .forum-comment:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .forum-comment-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

        .forum-comment-author {
            font-weight: 600;
            color: var(--primary-color);
        }

        .forum-comment-date {
            font-size: 0.9rem;
            color: var(--text-light);
        }

        .forum-comment-text {
            line-height: 1.6;
            margin-bottom: 10px;
        }

        .forum-comment-actions {
            display: flex;
            justify-content: flex-end;
            margin-top: 10px;
        }

        /* 深色模式 */
        .dark-mode {
            background: linear-gradient(135deg, var(--dark-bg) 0%, #1a2238 100%);
            color: #e6e9f0;
        }

        .dark-mode nav {
            background-color: var(--dark-card);
        }

        .dark-mode .nav-links a {
            color: #e6e9f0;
        }

        .dark-mode .section,
        .dark-mode .assignment-card,
        .dark-mode .modal-content {
            background: var(--dark-card);
        }

        .dark-mode .assignments-section h2, 
        .dark-mode .forum-section h2,
        .dark-mode .modal-title,
        .dark-mode .forum-comment-author,
        .dark-mode .assignment-title,
        .dark-mode .assignment-comment-author {
            color: var(--accent-color);
        }

        .dark-mode .assignments-section h2, 
        .dark-mode .forum-section h2 {
            border-color: rgba(255, 255, 255, 0.1);
        }

        .dark-mode .assignment-meta,
        .dark-mode .forum-comment-date,
        .dark-mode .file-badge,
        .dark-mode .like-btn, 
        .dark-mode .delete-btn,
        .dark-mode .assignment-comment-date {
            color: rgba(255, 255, 255, 0.7);
        }

        .dark-mode .assignment-description,
        .dark-mode .modal-text,
        .dark-mode .assignment-comment-text {
            color: rgba(255, 255, 255, 0.8);
        }

        .dark-mode .assignment-comments,
        .dark-mode .file-preview {
            border-color: rgba(255, 255, 255, 0.1);
        }

        .dark-mode .form-control,
        .dark-mode .file-type-btn,
        .dark-mode .file-item {
            background: rgba(255, 255, 255, 0.1);
            border-color: rgba(255, 255, 255, 0.2);
            color: #e6e9f0;
        }

        .dark-mode .forum-comment,
        .dark-mode .assignment-comment {
            background: rgba(255, 255, 255, 0.05);
            border-color: rgba(212, 175, 55, 0.4);
        }

        .dark-mode .modal-btn.cancel {
            background-color: rgba(255, 255, 255, 0.1);
            color: #e6e9f0;
        }

        .dark-mode .modal-btn.cancel:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }

        /* 响应式设计 */
        @media (max-width: 1200px) {
            .assignment-grid {
                grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            }
        }

        @media (max-width: 992px) {
            .assignment-grid {
                grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            }
            
            .jewish-pattern {
                gap: 20px;
            }
            
            .star-of-david, .menorah, .dead-sea-scroll {
                transform: scale(0.9);
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
                gap: 25px;
            }
            
            .assignment-grid {
                grid-template-columns: 1fr;
            }
            
            .nav-container {
                padding: 0 15px;
            }
            
            .nav-links {
                display: none;
                flex-direction: column;
                width: 100%;
                position: absolute;
                top: 100%;
                left: 0;
                background-color: var(--secondary-color);
                box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            }

            .dark-mode .nav-links {
                background-color: var(--dark-card);
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .menu-toggle {
                display: block;
            }
            
            .assignment-actions {
                flex-wrap: wrap;
                gap: 20px;
            }
            
            .file-types {
                justify-content: center;
            }
            
            .modal-actions {
                flex-direction: column;
            }
            
            .container {
                padding: 0 20px;
            }
            
            .section {
                padding: 30px 25px;
            }
            
            .hero-content h1 {
                font-size: clamp(2.5rem, 8vw, 4rem);
            }
            
            .jewish-pattern {
                gap: 15px;
            }
            
            .star-of-david, .menorah, .dead-sea-scroll {
                transform: scale(0.8);
            }
            
            .login-options {
                flex-direction: column;
                align-items: center;
            }
            
            .login-card {
                width: 100%;
                max-width: 350px;
            }
            
            .modal-content {
                padding: 30px 20px;
            }
            
            .assignment-modal-content {
                max-width: 95%;
            }
            
            .assignment-media {
                justify-content: center;
            }
            
            .media-item {
                width: 100%;
                max-width: 300px;
            }
            
            .media-image, .media-video, .media-file {
                width: 100%;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 15px;
            }
            
            .section {
                padding: 25px 20px;
            }
            
            .btn {
                padding: 12px 20px;
            }
            
            .explore-btn {
                padding: 16px 35px;
            }
            
            .hero-content h1 {
                font-size: clamp(2.2rem, 9vw, 3.5rem);
            }
            
            .jewish-pattern {
                gap: 10px;
            }
            
            .star-of-david, .menorah, .dead-sea-scroll {
                transform: scale(0.7);
            }
        }

        /* 动画 */
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        @keyframes flicker {
            0%, 100% { transform: translateX(-50%) scaleY(1); opacity: 1; }
            50% { transform: translateX(-50%) scaleY(1.1); opacity: 0.8; }
        }

        @keyframes scroll-shine {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .fade-in {
            animation: fadeIn 0.6s ease forwards;
        }
    </style>
</head>
<body>
    <!-- 第一部分：首页 -->
    <section id="hero">
        <div class="hero-content">
            <h1 data-lang="zh">全球视野下的犹太文明</h1>
            <h1 data-lang="en">Global Perspectives on Jewish Civilization</h1>
            <p data-lang="zh">通过创意作业和协作讨论，探索犹太历史、文化和知识贡献的丰富图景</p>
            <p data-lang="en">Discover the rich tapestry of Jewish history, culture, and intellectual contributions through creative assignments and collaborative discussions</p>
            <button class="explore-btn" id="exploreBtn">
                <span data-lang="zh">开始探索</span>
                <span data-lang="en">Start Exploring</span>
            </button>
        </div>
    </section>

    <!-- 第二部分：登录选择页面 -->
    <section id="login-selection">
        <div class="login-content">
            <h2 data-lang="zh">欢迎来到平台</h2>
            <h2 data-lang="en">Welcome to the Platform</h2>
            <p data-lang="zh">请选择您的访问方式以继续</p>
            <p data-lang="en">Please choose your access method to continue</p>
            
            <div class="login-options">
                <div class="login-card" id="guestLogin">
                    <i class="fas fa-user"></i>
                    <h3 data-lang="zh">访客访问</h3>
                    <h3 data-lang="en">Guest Access</h3>
                    <p data-lang="zh">浏览作业并参与讨论，无需提交作品</p>
                    <p data-lang="en">Browse assignments and participate in discussions without submitting work</p>
                    <button class="login-btn">
                        <span data-lang="zh">以访客身份进入</span>
                        <span data-lang="en">Enter as Guest</span>
                    </button>
                </div>
                
                <div class="login-card" id="studentLogin">
                    <i class="fas fa-graduation-cap"></i>
                    <h3 data-lang="zh">学生与教职工</h3>
                    <h3 data-lang="en">Student & Staff</h3>
                    <p data-lang="zh">提交作业并完全参与平台所有功能</p>
                    <p data-lang="en">Submit assignments and fully participate in all platform features</p>
                    <button class="login-btn">
                        <span data-lang="zh">学生/教职工登录</span>
                        <span data-lang="en">Student/Staff Login</span>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- 学生登录模态框 -->
    <div class="modal" id="studentModal">
        <div class="modal-content">
            <h3 class="modal-title" data-lang="zh">学生与教职工登录</h3>
            <h3 class="modal-title" data-lang="en">Student & Staff Login</h3>
            <p class="modal-text" data-lang="zh">请提供您的信息以访问平台</p>
            <p class="modal-text" data-lang="en">Please provide your information to access the platform</p>
            
            <form id="studentForm">
                <div class="form-group">
                    <label for="userName" data-lang="zh">全名</label>
                    <label for="userName" data-lang="en">Full Name</label>
                    <input type="text" id="userName" class="form-control" data-lang-placeholder-zh="请输入您的全名" data-lang-placeholder-en="Enter your full name" required>
                </div>
                
                <div class="form-group">
                    <label for="studentId" data-lang="zh">学号</label>
                    <label for="studentId" data-lang="en">Student ID</label>
                    <input type="text" id="studentId" class="form-control" data-lang-placeholder-zh="请输入您的学号" data-lang-placeholder-en="Enter your student ID">
                    <div class="note" data-lang="zh">教师和教职工可以留空此字段</div>
                    <div class="note" data-lang="en">Teachers and staff members can leave this field blank</div>
                </div>
            </form>
            
            <div class="modal-actions">
                <button class="btn btn-secondary" id="cancelLogin">
                    <span data-lang="zh">取消</span>
                    <span data-lang="en">Cancel</span>
                </button>
                <button class="btn btn-primary" id="confirmLogin">
                    <span data-lang="zh">进入平台</span>
                    <span data-lang="en">Continue to Platform</span>
                </button>
            </div>
        </div>
    </div>

    <!-- 第三部分：平台内容 -->
    <section id="platform">
        <!-- 头部 -->
        <header>
            <div class="container">
                <div class="header-content">
                    <div class="logo">
                        <div class="logo-placeholder">
                            <i class="fas fa-star-of-david" style="font-size: 60px; color: var(--accent-color);"></i>
                        </div>
                        <div class="logo-text">
                            <h1 data-lang="zh">全球视野下的犹太文明</h1>
                            <h1 data-lang="en">Global Perspectives on Jewish Civilization</h1>
                            <p data-lang="zh">创意作业平台</p>
                            <p data-lang="en">Creative Assignment Platform</p>
                        </div>
                    </div>
                    <div class="header-controls">
                        <div class="user-info">
                            <span id="userDisplay">Guest User</span>
                        </div>
                        <button class="theme-toggle" id="themeToggle">
                            <i class="fas fa-moon"></i>
                        </button>
                        <button class="language-toggle" id="languageToggle">
                            <i class="fas fa-language"></i>
                        </button>
                    </div>
                </div>
            </div>
        </header>

        <!-- 导航栏 -->
        <nav>
            <div class="container nav-container">
                <button class="menu-toggle" id="menuToggle">
                    <i class="fas fa-bars"></i>
                </button>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#" class="active" data-text="home">
                        <span data-lang="zh">首页</span>
                        <span data-lang="en">Home</span>
                    </a></li>
                    <li><a href="#" data-text="assignments">
                        <span data-lang="zh">作业展示</span>
                        <span data-lang="en">Assignments</span>
                    </a></li>
                    <li><a href="#" data-text="submit" id="submitTab">
                        <span data-lang="zh">提交作业</span>
                        <span data-lang="en">Submit Work</span>
                    </a></li>
                    <li><a href="#" data-text="forum">
                        <span data-lang="zh">课堂论坛</span>
                        <span data-lang="en">Class Forum</span>
                    </a></li>
                </ul>
            </div>
        </nav>

        <!-- 犹太文化图案 -->
        <div class="container">
            <div class="jewish-pattern">
                <div class="star-of-david"></div>
                <div class="menorah">
                    <div class="flame"></div>
                </div>
                <div class="dead-sea-scroll"></div>
            </div>
        </div>

        <!-- 主内容区 -->
        <div class="container">
            <!-- 上传作业区域 -->
            <section class="section upload-section" id="uploadSection">
                <div class="section-header">
                    <div class="section-icon">
                        <i class="fas fa-upload"></i>
                    </div>
                    <h2 class="section-title" data-lang="zh">提交创意作业</h2>
                    <h2 class="section-title" data-lang="en">Submit Creative Assignment</h2>
                </div>
                <form class="upload-form" id="assignmentForm">
                    <div class="form-group">
                        <label for="assignmentTitle" data-lang="zh">作业标题</label>
                        <label for="assignmentTitle" data-lang="en">Assignment Title</label>
                        <input type="text" id="assignmentTitle" class="form-control" data-lang-placeholder-zh="请输入作业标题" data-lang-placeholder-en="Enter assignment title" required>
                    </div>
                    <div class="form-group">
                        <label for="assignmentAuthor" data-lang="zh">作者姓名</label>
                        <label for="assignmentAuthor" data-lang="en">Author Name</label>
                        <input type="text" id="assignmentAuthor" class="form-control" data-lang-placeholder-zh="请输入您的姓名" data-lang-placeholder-en="Enter your name" required readonly>
                    </div>
                    <div class="form-group">
                        <label for="assignmentDescription" data-lang="zh">作业描述</label>
                        <label for="assignmentDescription" data-lang="en">Assignment Description</label>
                        <textarea id="assignmentDescription" class="form-control" data-lang-placeholder-zh="描述您的作业..." data-lang-placeholder-en="Describe your assignment..." required></textarea>
                    </div>
                    
                    <!-- 文件上传区域 -->
                    <div class="form-group file-upload">
                        <label data-lang="zh">上传作业文件</label>
                        <label data-lang="en">Upload Assignment Files</label>
                        <div class="file-types">
                            <button type="button" class="file-type-btn active" data-type="all">
                                <i class="fas fa-file"></i> 
                                <span data-lang="zh">所有文件</span>
                                <span data-lang="en">All Files</span>
                            </button>
                            <button type="button" class="file-type-btn" data-type="video">
                                <i class="fas fa-video"></i> 
                                <span data-lang="zh">视频</span>
                                <span data-lang="en">Video</span>
                            </button>
                            <button type="button" class="file-type-btn" data-type="document">
                                <i class="fas fa-file-pdf"></i> 
                                <span data-lang="zh">文档</span>
                                <span data-lang="en">Documents</span>
                            </button>
                            <button type="button" class="file-type-btn" data-type="image">
                                <i class="fas fa-image"></i> 
                                <span data-lang="zh">图片</span>
                                <span data-lang="en">Images</span>
                            </button>
                        </div>
                        <input type="file" id="assignmentFiles" class="file-input" multiple>
                        <button type="button" id="selectFiles" class="btn btn-accent" style="width: fit-content;">
                            <i class="fas fa-plus"></i> 
                            <span data-lang="zh">选择文件</span>
                            <span data-lang="en">Select Files</span>
                        </button>
                        <div class="file-preview" id="filePreview">
                            <p data-lang="zh">未选择文件</p>
                            <p data-lang="en">No files selected</p>
                        </div>
                    </div>
                    
                    <button type="submit" class="btn btn-primary">
                        <span data-lang="zh">提交作业</span>
                        <span data-lang="en">Submit Assignment</span>
                    </button>
                </form>
            </section>

            <main>
                <!-- 作业展示区 -->
                <section class="section assignments-section">
                    <div class="section-header">
                        <div class="section-icon">
                            <i class="fas fa-images"></i>
                        </div>
                        <h2 class="section-title" data-lang="zh">创意作业展示</h2>
                        <h2 class="section-title" data-lang="en">Creative Assignment Gallery</h2>
                    </div>
                    
                    <div class="assignment-grid" id="assignmentGrid">
                        <!-- 作业将在这里动态显示 -->
                        <div class="no-assignments" id="noAssignments">
                            <p data-lang="zh">还没有提交的作业。成为第一个提交的人！</p>
                            <p data-lang="en">No assignments submitted yet. Be the first to submit one!</p>
                        </div>
                    </div>
                </section>
                
                <!-- 课堂论坛区 -->
                <section class="section forum-section">
                    <div class="section-header">
                        <div class="section-icon">
                            <i class="fas fa-comments"></i>
                        </div>
                        <h2 class="section-title" data-lang="zh">课堂论坛</h2>
                        <h2 class="section-title" data-lang="en">Class Forum</h2>
                    </div>
                    
                    <div class="forum-form">
                        <textarea id="forumText" class="form-control" data-lang-placeholder-zh="分享您的想法..." data-lang-placeholder-en="Share your thoughts..."></textarea>
                        <button id="submitForum" class="btn btn-primary">
                            <span data-lang="zh">发表评论</span>
                            <span data-lang="en">Post Comment</span>
                        </button>
                    </div>
                    
                    <div class="forum-list" id="forumList">
                        <!-- 论坛评论将在这里动态显示 -->
                        <div class="no-comments" id="noForumComments">
                            <p data-lang="zh">还没有评论。成为第一个评论的人！</p>
                            <p data-lang="en">No comments yet. Be the first to comment!</p>
                        </div>
                    </div>
                </section>
            </main>
        </div>

        <!-- 页脚 -->
        <footer>
            <div class="container">
                <div class="contact-info">
                    <h3 data-lang="zh">联系我们</h3>
                    <h3 data-lang="en">Contact Us</h3>
                    <div class="contact-details">
                        <div class="contact-item">
                            <i class="fas fa-user"></i>
                            <span data-lang="zh">教师：杨梦</span>
                            <span data-lang="en">Instructor: Yang Meng</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <span>Email: allshallpass@gmail.com</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <span data-lang="zh">课程邮箱：pkuytwm@gmail.com</span>
                            <span data-lang="en">Course Email: pkuytwm@gmail.com</span>
                        </div>
                        <div class="contact-item">
                            <i class="fab fa-weixin"></i>
                            <span data-lang="zh">课程微信：aibeida</span>
                            <span data-lang="en">Course WeChat: aibeida</span>
                        </div>
                    </div>
                </div>
                
                <div class="copyright">
                    <p data-lang="zh">© 2023 北京大学"全球视野下的犹太文明"课程 - 创意作业平台</p>
                    <p data-lang="en">© 2023 Peking University "Global Perspectives on Jewish Civilization" Course - Creative Assignment Platform</p>
                </div>
            </div>
        </footer>
    </section>

    <!-- 媒体查看模态框 -->
    <div class="media-modal" id="mediaModal">
        <div class="media-modal-content">
            <span class="media-modal-close" id="mediaModalClose">&times;</span>
            <img id="modalImage" src="" alt="">
            <video id="modalVideo" controls>
                Your browser does not support the video tag.
            </video>
        </div>
    </div>

    <!-- 作业详情模态框 -->
    <div class="assignment-modal" id="assignmentModal">
        <div class="assignment-modal-content">
            <div class="assignment-modal-close" id="assignmentModalClose">
                <i class="fas fa-times"></i>
            </div>
            <div class="assignment-modal-header">
                <h2 class="assignment-modal-title" id="modalAssignmentTitle"></h2>
                <div class="assignment-modal-meta">
                    <span id="modalAssignmentAuthor"></span>
                    <span id="modalAssignmentDate"></span>
                </div>
            </div>
            <div class="assignment-modal-body">
                <p class="assignment-modal-description" id="modalAssignmentDescription"></p>
                <div class="assignment-media" id="modalAssignmentMedia"></div>
                <div class="assignment-actions">
                    <button class="btn-text like-btn" id="modalLikeBtn">
                        <i class="far fa-heart"></i> <span id="modalLikesCount">0</span>
                    </button>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 应用程序状态管理
        const app = {
            state: {
                assignments: [],
                forumComments: [],
                selectedFiles: [],
                isDarkMode: false,
                currentUser: '',
                currentStudentId: '',
                userType: '', // 'guest' or 'student'
                coverPatterns: ['menorah-cover', 'star-cover', 'scroll-cover'],
                currentLanguage: 'zh', // 'zh' or 'en'
                currentAssignmentId: null, // 当前查看的作业ID
                hasInitialized: false, // 标记是否已初始化
                deleteKey: '1223334444Jewish' // 删除密钥
            },
            
            // 初始化应用
            init() {
                // 从本地存储加载数据
                this.loadFromLocalStorage();
                
                // 只在第一次初始化时添加示例作业
                if (!this.state.hasInitialized && this.state.assignments.length === 0) {
                    this.addSampleAssignments();
                    this.state.hasInitialized = true;
                }
                
                this.setupEventListeners();
                this.updatePlaceholders();
            },
            
            // 从本地存储加载数据
            loadFromLocalStorage() {
                const storedAssignments = localStorage.getItem('assignments');
                const storedForumComments = localStorage.getItem('forumComments');
                
                this.state.assignments = storedAssignments ? JSON.parse(storedAssignments) : [];
                this.state.forumComments = storedForumComments ? JSON.parse(storedForumComments) : [];
            },
            
            // 添加示例作业
            addSampleAssignments() {
                // 示例作业数据
                const sampleAssignments = [
                    {
                        id: 1,
                        title: "耶路撒冷全景",
                        studentId: "",
                        author: "系统示例",
                        description: "耶路撒冷是犹太教、基督教和伊斯兰教的圣地，拥有三千多年的历史，是犹太文明的精神中心。",
                        files: [
                            {
                                name: "耶路撒冷全景.jpg",
                                type: "image/jpeg",
                                size: 0,
                                preview: "https://youimg1.c-ctrip.com/target/100h160000010n7h25CA5.jpg",
                                thumbnail: "https://youimg1.c-ctrip.com/target/100h160000010n7h25CA5.jpg",
                                content: "https://youimg1.c-ctrip.com/target/100h160000010n7h25CA5.jpg"
                            }
                        ],
                        coverPattern: "star-cover",
                        date: "2023-11-15",
                        likes: 42,
                        comments: [],
                        commentCount: 0
                    },
                    {
                        id: 2,
                        title: "亚伯拉罕始祖时代",
                        studentId: "",
                        author: "系统示例",
                        description: "亚伯拉罕被认为是犹太民族的始祖，他与上帝立约，开创了一神教传统，对后世产生了深远影响。",
                        files: [
                            {
                                name: "亚伯拉罕始祖时代.jpg",
                                type: "image/jpeg",
                                size: 0,
                                preview: "https://ts1.tc.mm.bing.net/th/id/R-C.3a833c52e4a7a57dc833186660b12e9a?rik=vPe4Sz%2bWDFd46g&riu=http%3a%2f%2fwww.zgaxr.com%2fUploadFiles%2fPhoto%2f2011%2f5%2f201105040416171856.jpg&ehk=weBWM2ka2pksvEM6dBdQKZzcQEFgjx0%2bcYiL83GoM9g%3d&risl=&pid=ImgRaw&r=0",
                                thumbnail: "https://ts1.tc.mm.bing.net/th/id/R-C.3a833c52e4a7a57dc833186660b12e9a?rik=vPe4Sz%2bWDFd46g&riu=http%3a%2f%2fwww.zgaxr.com%2fUploadFiles%2fPhoto%2f2011%2f5%2f201105040416171856.jpg&ehk=weBWM2ka2pksvEM6dBdQKZzcQEFgjx0%2bcYiL83GoM9g%3d&risl=&pid=ImgRaw&r=0",
                                content: "https://ts1.tc.mm.bing.net/th/id/R-C.3a833c52e4a7a57dc833186660b12e9a?rik=vPe4Sz%2bWDFd46g&riu=http%3a%2f%2fwww.zgaxr.com%2fUploadFiles%2fPhoto%2f2011%2f5%2f201105040416171856.jpg&ehk=weBWM2ka2pksvEM6dBdQKZzcQEFgjx0%2bcYiL83GoM9g%3d&risl=&pid=ImgRaw&r=0"
                            }
                        ],
                        coverPattern: "scroll-cover",
                        date: "2023-11-10",
                        likes: 35,
                        comments: [],
                        commentCount: 0
                    },
                    {
                        id: 3,
                        title: "出埃及记",
                        studentId: "",
                        author: "系统示例",
                        description: "摩西带领以色列人离开埃及，摆脱奴役，这一事件成为犹太民族身份认同的核心叙事，也是自由与解放的象征。",
                        files: [
                            {
                                name: "出埃及记.jpg",
                                type: "image/jpeg",
                                size: 0,
                                preview: "https://p1.ssl.qhimg.com/t01abdd93ef0f17ad6d.jpg",
                                thumbnail: "https://p1.ssl.qhimg.com/t01abdd93ef0f17ad6d.jpg",
                                content: "https://p1.ssl.qhimg.com/t01abdd93ef0f17ad6d.jpg"
                            }
                        ],
                        coverPattern: "menorah-cover",
                        date: "2023-11-05",
                        likes: 28,
                        comments: [],
                        commentCount: 0
                    },
                    {
                        id: 4,
                        title: "以色列王国时期",
                        studentId: "",
                        author: "系统示例",
                        description: "大卫王和所罗门王统治时期是以色列王国的黄金时代，所罗门王建造了第一圣殿，使耶路撒冷成为宗教和政治中心。",
                        files: [
                            {
                                name: "以色列王国.jpg",
                                type: "image/jpeg",
                                size: 0,
                                preview: "https://bkimg.cdn.bcebos.com/pic/83025aafa40f4bfb7f23ca620e4f78f0f7361810",
                                thumbnail: "https://bkimg.cdn.bcebos.com/pic/83025aafa40f4bfb7f23ca620e4f78f0f7361810",
                                content: "https://bkimg.cdn.bcebos.com/pic/83025aafa40f4bfb7f23ca620e4f78f0f7361810"
                            }
                        ],
                        coverPattern: "star-cover",
                        date: "2023-10-28",
                        likes: 31,
                        comments: [],
                        commentCount: 0
                    },
                    {
                        id: 5,
                        title: "犹太科学家的贡献",
                        studentId: "",
                        author: "系统示例",
                        description: "阿尔伯特·爱因斯坦等犹太科学家对现代物理学做出了巨大贡献，他们的成就体现了犹太民族在知识追求方面的卓越表现。",
                        files: [
                            {
                                name: "阿尔伯特·爱因斯坦.jpg",
                                type: "image/jpeg",
                                size: 0,
                                preview: "https://p3-sdbk2-media.byteimg.com/tos-cn-i-xv4ileqgde/4e2c2e63c6274a6c8fba156ff172ebeb~tplv-xv4ileqgde-resize-w:360.image",
                                thumbnail: "https://p3-sdbk2-media.byteimg.com/tos-cn-i-xv4ileqgde/4e2c2e63c6274a6c8fba156ff172ebeb~tplv-xv4ileqgde-resize-w:360.image",
                                content: "https://p3-sdbk2-media.byteimg.com/tos-cn-i-xv4ileqgde/4e2c2e63c6274a6c8fba156ff172ebeb~tplv-xv4ileqgde-resize-w:360.image"
                            }
                        ],
                        coverPattern: "scroll-cover",
                        date: "2023-10-20",
                        likes: 47,
                        comments: [],
                        commentCount: 0
                    },
                    {
                        id: 6,
                        title: "上海犹太难民区",
                        studentId: "",
                        author: "系统示例",
                        description: "二战期间，上海为约2万名犹太难民提供了避难所，成为他们逃离纳粹迫害的安全港湾，这段历史是中犹友谊的重要见证。",
                        files: [
                            {
                                name: "上海犹太难民区.jpg",
                                type: "image/jpeg",
                                size: 0,
                                preview: "https://www.bijingdi.com/uploadfile/2023/1031/20231031184509683.jpg",
                                thumbnail: "https://www.bijingdi.com/uploadfile/2023/1031/20231031184509683.jpg",
                                content: "https://www.bijingdi.com/uploadfile/2023/1031/20231031184509683.jpg"
                            }
                        ],
                        coverPattern: "menorah-cover",
                        date: "2023-10-15",
                        likes: 39,
                        comments: [],
                        commentCount: 0
                    }
                ];
                
                // 将示例作业添加到状态中
                this.state.assignments = sampleAssignments.concat(this.state.assignments);
                this.saveToLocalStorage('assignments', this.state.assignments);
            },
            
            // 设置事件监听器
            setupEventListeners() {
                // 页面元素引用
                const elements = {
                    exploreBtn: document.getElementById('exploreBtn'),
                    hero: document.getElementById('hero'),
                    loginSelection: document.getElementById('login-selection'),
                    guestLogin: document.getElementById('guestLogin'),
                    studentLogin: document.getElementById('studentLogin'),
                    studentModal: document.getElementById('studentModal'),
                    cancelLogin: document.getElementById('cancelLogin'),
                    confirmLogin: document.getElementById('confirmLogin'),
                    studentForm: document.getElementById('studentForm'),
                    platform: document.getElementById('platform'),
                    userDisplay: document.getElementById('userDisplay'),
                    uploadSection: document.getElementById('uploadSection'),
                    submitTab: document.getElementById('submitTab'),
                    assignmentAuthor: document.getElementById('assignmentAuthor'),
                    themeToggle: document.getElementById('themeToggle'),
                    languageToggle: document.getElementById('languageToggle'),
                    mediaModal: document.getElementById('mediaModal'),
                    mediaModalClose: document.getElementById('mediaModalClose'),
                    assignmentModal: document.getElementById('assignmentModal'),
                    assignmentModalClose: document.getElementById('assignmentModalClose')
                };

                // 开始探索按钮
                elements.exploreBtn.addEventListener('click', () => {
                    elements.hero.style.display = 'none';
                    elements.loginSelection.style.display = 'flex';
                });
                
                // 游客登录
                elements.guestLogin.addEventListener('click', () => {
                    this.state.userType = 'guest';
                    this.state.currentUser = 'Guest User';
                    this.state.currentStudentId = '';
                    
                    // 更新用户显示
                    elements.userDisplay.textContent = 'Guest User';
                    
                    // 隐藏提交作业部分
                    elements.uploadSection.style.display = 'none';
                    elements.submitTab.style.display = 'none';
                    
                    // 进入平台
                    elements.loginSelection.style.display = 'none';
                    elements.platform.style.display = 'block';
                    
                    // 初始化平台功能
                    this.initPlatform();
                });
                
                // 学生/教职工登录
                elements.studentLogin.addEventListener('click', () => {
                    elements.studentModal.style.display = 'flex';
                });
                
                // 取消登录
                elements.cancelLogin.addEventListener('click', () => {
                    elements.studentModal.style.display = 'none';
                });
                
                // 确认登录
                elements.confirmLogin.addEventListener('click', () => {
                    const userName = document.getElementById('userName').value;
                    
                    if (!userName) {
                        alert(this.state.currentLanguage === 'zh' ? '请输入您的姓名' : 'Please enter your name');
                        return;
                    }
                    
                    this.state.userType = 'student';
                    this.state.currentUser = userName;
                    this.state.currentStudentId = document.getElementById('studentId').value || '';
                    
                    // 更新用户显示
                    elements.userDisplay.textContent = userName + (this.state.currentStudentId ? ` (${this.state.currentStudentId})` : '');
                    
                    // 设置作业作者字段
                    elements.assignmentAuthor.value = userName;
                    
                    // 显示提交作业部分
                    elements.uploadSection.style.display = 'block';
                    elements.submitTab.style.display = 'block';
                    
                    // 进入平台
                    elements.studentModal.style.display = 'none';
                    elements.loginSelection.style.display = 'none';
                    elements.platform.style.display = 'block';
                    
                    // 初始化平台功能
                    this.initPlatform();
                });
                
                // 主题切换
                elements.themeToggle.addEventListener('click', () => {
                    this.toggleTheme();
                });
                
                // 语言切换
                elements.languageToggle.addEventListener('click', () => {
                    this.toggleLanguage();
                });
                
                // 媒体模态框关闭
                elements.mediaModalClose.addEventListener('click', () => {
                    elements.mediaModal.style.display = 'none';
                    const video = document.getElementById('modalVideo');
                    if (video) {
                        video.pause();
                        video.currentTime = 0;
                    }
                });
                
                // 作业详情模态框关闭
                elements.assignmentModalClose.addEventListener('click', () => {
                    elements.assignmentModal.style.display = 'none';
                });
                
                // 设置平台事件监听器
                this.setupPlatformEventListeners();
            },
            
            // 切换主题
            toggleTheme() {
                this.state.isDarkMode = !this.state.isDarkMode;
                document.body.classList.toggle('dark-mode', this.state.isDarkMode);
                document.getElementById('themeToggle').innerHTML = this.state.isDarkMode ? 
                    '<i class="fas fa-sun"></i>' : '<i class="fas fa-moon"></i>';
            },
            
            // 切换语言
            toggleLanguage() {
                this.state.currentLanguage = this.state.currentLanguage === 'zh' ? 'en' : 'zh';
                document.body.classList.toggle('english-mode', this.state.currentLanguage === 'en');
                this.updatePlaceholders();
                
                // 更新语言切换按钮图标
                const languageToggle = document.getElementById('languageToggle');
                languageToggle.innerHTML = this.state.currentLanguage === 'zh' ? 
                    '<i class="fas fa-language"></i>' : '<i class="fas fa-language"></i>';
            },
            
            // 更新输入框占位符
            updatePlaceholders() {
                document.querySelectorAll('[data-lang-placeholder-zh], [data-lang-placeholder-en]').forEach(element => {
                    const placeholder = this.state.currentLanguage === 'zh' ? 
                        element.getAttribute('data-lang-placeholder-zh') : 
                        element.getAttribute('data-lang-placeholder-en');
                    element.setAttribute('placeholder', placeholder);
                });
            },
            
            // 初始化平台功能
            initPlatform() {
                this.displayAssignments();
                this.displayForumComments();
                this.updateFilePreview();
                this.setupPlatformEventListeners();
            },
            
            // 设置平台事件监听器
            setupPlatformEventListeners() {
                // 文件类型切换
                document.addEventListener('click', (e) => {
                    if (e.target.closest('.file-type-btn')) {
                        const btn = e.target.closest('.file-type-btn');
                        document.querySelectorAll('.file-type-btn').forEach(b => b.classList.remove('active'));
                        btn.classList.add('active');
                        this.updateFileInputAccept(btn.getAttribute('data-type'));
                    }
                });
                
                // 选择文件
                document.getElementById('selectFiles').addEventListener('click', () => {
                    document.getElementById('assignmentFiles').click();
                });
                
                // 文件选择处理
                document.getElementById('assignmentFiles').addEventListener('change', (e) => {
                    const files = Array.from(e.target.files);
                    
                    // 为图片和视频文件生成预览
                    files.forEach(file => {
                        if (file.type.startsWith('image/')) {
                            const reader = new FileReader();
                            reader.onload = (e) => {
                                file.preview = e.target.result;
                                this.state.selectedFiles.push(file);
                                this.updateFilePreview();
                            };
                            reader.readAsDataURL(file);
                        } else if (file.type.startsWith('video/')) {
                            // 为视频文件生成缩略图
                            const video = document.createElement('video');
                            video.src = URL.createObjectURL(file);
                            video.currentTime = 1; // 取第一秒作为缩略图
                            
                            video.addEventListener('loadeddata', () => {
                                const canvas = document.createElement('canvas');
                                canvas.width = video.videoWidth;
                                canvas.height = video.videoHeight;
                                const ctx = canvas.getContext('2d');
                                ctx.drawImage(video, 0, 0, canvas.width, canvas.height);
                                file.thumbnail = canvas.toDataURL();
                                this.state.selectedFiles.push(file);
                                this.updateFilePreview();
                                URL.revokeObjectURL(video.src);
                            });
                        } else {
                            this.state.selectedFiles.push(file);
                            this.updateFilePreview();
                        }
                    });
                    
                    e.target.value = ''; // 允许重复选择同一文件
                });
                
                // 移除文件
                document.addEventListener('click', (e) => {
                    if (e.target.closest('.remove-file')) {
                        const index = parseInt(e.target.closest('.remove-file').getAttribute('data-index'));
                        this.state.selectedFiles.splice(index, 1);
                        this.updateFilePreview();
                    }
                    
                    if (e.target.closest('.remove-preview')) {
                        const index = parseInt(e.target.closest('.remove-preview').getAttribute('data-index'));
                        this.state.selectedFiles.splice(index, 1);
                        this.updateFilePreview();
                    }
                });
                
                // 提交作业表单
                document.getElementById('assignmentForm').addEventListener('submit', (e) => {
                    e.preventDefault();
                    this.handleAssignmentSubmit();
                });
                
                // 提交论坛评论
                document.getElementById('submitForum').addEventListener('click', () => this.handleForumSubmit());
                
                // 作业卡片操作（事件委托）
                document.getElementById('assignmentGrid').addEventListener('click', (e) => {
                    // 点赞
                    if (e.target.closest('.like-btn')) {
                        const id = parseInt(e.target.closest('.like-btn').getAttribute('data-id'));
                        this.handleLike(id, e.target.closest('.like-btn'));
                    }
                    
                    // 删除作业
                    if (e.target.closest('.assignment-delete-btn')) {
                        const btn = e.target.closest('.assignment-delete-btn');
                        const id = parseInt(btn.getAttribute('data-id'));
                        const author = btn.getAttribute('data-author');
                        this.handleDelete(id, author, 'assignment');
                    }
                    
                    // 查看作业详情
                    if (e.target.closest('.assignment-card') && !e.target.closest('.assignment-actions')) {
                        const card = e.target.closest('.assignment-card');
                        const id = parseInt(card.querySelector('.like-btn').getAttribute('data-id'));
                        this.showAssignmentDetail(id);
                    }
                    
                    // 查看媒体文件
                    if (e.target.closest('.media-item')) {
                        const mediaItem = e.target.closest('.media-item');
                        const type = mediaItem.getAttribute('data-type');
                        const src = mediaItem.getAttribute('data-src');
                        const name = mediaItem.getAttribute('data-name');
                        this.showMedia(type, src, name);
                    }
                });
                
                // 删除论坛评论
                document.getElementById('forumList').addEventListener('click', (e) => {
                    if (e.target.closest('.forum-delete-btn')) {
                        const btn = e.target.closest('.forum-delete-btn');
                        const id = parseInt(btn.getAttribute('data-id'));
                        const author = btn.getAttribute('data-author');
                        this.handleDelete(id, author, 'comment');
                    }
                });
                
                // 移动端菜单切换
                document.getElementById('menuToggle').addEventListener('click', () => {
                    document.getElementById('navLinks').classList.toggle('active');
                });
                
                // 导航链接点击
                document.addEventListener('click', (e) => {
                    if (e.target.closest('.nav-links a')) {
                        e.preventDefault();
                        const link = e.target.closest('.nav-links a');
                        document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
                        link.classList.add('active');
                        
                        // 移动端自动关闭菜单
                        document.getElementById('navLinks').classList.remove('active');
                        
                        // 滚动到对应区域
                        const target = link.getAttribute('data-text');
                        if (target === 'submit') {
                            document.querySelector('.upload-section').scrollIntoView({ behavior: 'smooth' });
                        } else if (target === 'assignments') {
                            document.querySelector('.assignments-section').scrollIntoView({ behavior: 'smooth' });
                        } else if (target === 'forum') {
                            document.querySelector('.forum-section').scrollIntoView({ behavior: 'smooth' });
                        }
                    }
                });
            },
            
            // 更新文件输入类型
            updateFileInputAccept(fileType) {
                const fileInput = document.getElementById('assignmentFiles');
                
                switch(fileType) {
                    case 'video':
                        fileInput.setAttribute('accept', 'video/*,.mp4,.avi,.mov,.wmv');
                        break;
                    case 'document':
                        fileInput.setAttribute('accept', '.pdf,.doc,.docx,.txt,.ppt,.pptx');
                        break;
                    case 'image':
                        fileInput.setAttribute('accept', 'image/*,.jpg,.jpeg,.png,.gif');
                        break;
                    default:
                        fileInput.setAttribute('accept', '*');
                }
            },
            
            // 更新文件预览
            updateFilePreview() {
                const filePreview = document.getElementById('filePreview');
                filePreview.innerHTML = '';
                
                if (this.state.selectedFiles.length === 0) {
                    filePreview.innerHTML = `
                        <p data-lang="zh">未选择文件</p>
                        <p data-lang="en">No files selected</p>
                    `;
                    return;
                }
                
                // 创建网格布局
                const grid = document.createElement('div');
                grid.className = 'file-preview-grid';
                
                this.state.selectedFiles.forEach((file, index) => {
                    const previewItem = document.createElement('div');
                    previewItem.className = 'preview-item';
                    
                    if (file.type.startsWith('image/') && file.preview) {
                        previewItem.innerHTML = `
                            <img src="${file.preview}" alt="${file.name}">
                            <div class="file-info">
                                <span>${file.name}</span>
                            </div>
                            <div class="remove-preview" data-index="${index}">
                                <i class="fas fa-times"></i>
                            </div>
                        `;
                    } else if (file.type.startsWith('video/') && file.thumbnail) {
                        previewItem.innerHTML = `
                            <img src="${file.thumbnail}" alt="${file.name}">
                            <div class="file-info">
                                <span>${file.name}</span>
                            </div>
                            <div class="remove-preview" data-index="${index}">
                                <i class="fas fa-times"></i>
                            </div>
                        `;
                    } else {
                        let fileIcon = 'fa-file';
                        if (file.type.startsWith('video/')) {
                            fileIcon = 'fa-video';
                        } else if (file.type.includes('pdf')) {
                            fileIcon = 'fa-file-pdf';
                        } else if (file.type.includes('document')) {
                            fileIcon = 'fa-file-word';
                        }
                        
                        previewItem.innerHTML = `
                            <div class="file-info" style="height: 100%; justify-content: center;">
                                <i class="fas ${fileIcon}" style="font-size: 2rem;"></i>
                                <span>${file.name}</span>
                            </div>
                            <div class="remove-preview" data-index="${index}">
                                <i class="fas fa-times"></i>
                            </div>
                        `;
                    }
                    
                    grid.appendChild(previewItem);
                });
                
                filePreview.appendChild(grid);
            },
            
            // 处理作业提交
            handleAssignmentSubmit() {
                const title = document.getElementById('assignmentTitle').value;
                const author = document.getElementById('assignmentAuthor').value;
                const description = document.getElementById('assignmentDescription').value;
                
                if (!title || !author || !description) {
                    alert(this.state.currentLanguage === 'zh' ? '请填写所有必填字段' : 'Please fill in all required fields');
                    return;
                }
                
                // 添加提交确认
                const confirmMessage = this.state.currentLanguage === 'zh' ? 
                    '是否确认提交作业？' : 
                    'Are you sure you want to submit the assignment?';
                
                if (!confirm(confirmMessage)) {
                    return;
                }
                
                // 创建新作业
                const randomPattern = this.state.coverPatterns[Math.floor(Math.random() * this.state.coverPatterns.length)];
                const newAssignment = {
                    id: Date.now(),
                    title: title,
                    studentId: this.state.currentStudentId,
                    author: author,
                    description: description,
                    files: this.state.selectedFiles.map(file => ({
                        name: file.name,
                        type: file.type,
                        size: file.size,
                        preview: file.preview || null,
                        thumbnail: file.thumbnail || null,
                        content: file.type.startsWith('image/') ? file.preview : null
                    })),
                    coverPattern: randomPattern,
                    date: new Date().toISOString().split('T')[0],
                    likes: 0,
                    comments: [],
                    commentCount: 0
                };
                
                // 保存作业
                this.state.assignments.unshift(newAssignment);
                this.saveToLocalStorage('assignments', this.state.assignments);
                
                // 重置表单
                document.getElementById('assignmentForm').reset();
                document.getElementById('assignmentAuthor').value = this.state.currentUser;
                this.state.selectedFiles = [];
                this.updateFilePreview();
                
                this.displayAssignments();
                
                alert(this.state.currentLanguage === 'zh' ? '作业提交成功！' : 'Assignment submitted successfully!');
            },
            
            // 处理论坛提交
            handleForumSubmit() {
                const forumText = document.getElementById('forumText').value.trim();
                if (!forumText) {
                    alert(this.state.currentLanguage === 'zh' ? '请输入评论内容' : 'Please enter comment content');
                    return;
                }
                
                // 创建新评论
                const newComment = {
                    id: Date.now(),
                    author: this.state.currentUser,
                    studentId: this.state.currentStudentId || '',
                    text: forumText,
                    date: new Date().toISOString().split('T')[0]
                };
                
                // 保存评论
                this.state.forumComments.unshift(newComment);
                this.saveToLocalStorage('forumComments', this.state.forumComments);
                
                // 重置并更新
                document.getElementById('forumText').value = '';
                this.displayForumComments();
                alert(this.state.currentLanguage === 'zh' ? '评论发布成功！' : 'Comment posted successfully!');
            },
            
            // 显示作业
            displayAssignments() {
                const assignmentGrid = document.getElementById('assignmentGrid');
                const noAssignments = document.getElementById('noAssignments');
                assignmentGrid.innerHTML = '';
                
                if (this.state.assignments.length === 0) {
                    noAssignments.style.display = 'block';
                    assignmentGrid.appendChild(noAssignments);
                    return;
                }
                
                noAssignments.style.display = 'none';
                const fragment = document.createDocumentFragment();
                
                this.state.assignments.forEach(assignment => {
                    const assignmentCard = document.createElement('div');
                    assignmentCard.className = 'assignment-card fade-in';
                    
                    // 生成文件徽章和媒体预览
                    let fileBadges = '';
                    let mediaPreview = '';
                    
                    if (assignment.files && assignment.files.length > 0) {
                        // 文件徽章
                        assignment.files.forEach(file => {
                            let fileIcon = 'fa-file';
                            let fileType = this.state.currentLanguage === 'zh' ? '文件' : 'File';
                            
                            if (file.type.startsWith('video/')) {
                                fileIcon = 'fa-video';
                                fileType = this.state.currentLanguage === 'zh' ? '视频' : 'Video';
                            } else if (file.type.startsWith('image/')) {
                                fileIcon = 'fa-image';
                                fileType = this.state.currentLanguage === 'zh' ? '图片' : 'Image';
                            } else if (file.type.includes('pdf')) {
                                fileIcon = 'fa-file-pdf';
                                fileType = 'PDF';
                            } else if (file.type.includes('document')) {
                                fileIcon = 'fa-file-word';
                                fileType = this.state.currentLanguage === 'zh' ? '文档' : 'Document';
                            }
                            
                            fileBadges += `
                                <div class="file-badge">
                                    <i class="fas ${fileIcon}"></i>
                                    <span>${fileType}</span>
                                </div>
                            `;
                        });
                        
                        // 媒体预览（仅显示前3个）
                        mediaPreview = '<div class="assignment-media">';
                        assignment.files.slice(0, 3).forEach((file, index) => {
                            if (file.type.startsWith('image/') && file.preview) {
                                mediaPreview += `
                                    <div class="media-item" data-type="image" data-src="${file.preview}" data-name="${file.name}">
                                        <img src="${file.preview}" alt="${file.name}" class="media-image">
                                        <div class="media-actions">
                                            <div class="media-action-btn view-media" title="${this.state.currentLanguage === 'zh' ? '查看' : 'View'}">
                                                <i class="fas fa-expand"></i>
                                            </div>
                                        </div>
                                    </div>
                                `;
                            } else if (file.type.startsWith('video/') && file.thumbnail) {
                                mediaPreview += `
                                    <div class="media-item" data-type="video" data-src="${file.preview || ''}" data-name="${file.name}">
                                        <img src="${file.thumbnail}" alt="${file.name}" class="media-image">
                                        <div class="media-actions">
                                            <div class="media-action-btn view-media" title="${this.state.currentLanguage === 'zh' ? '查看' : 'View'}">
                                                <i class="fas fa-play"></i>
                                            </div>
                                        </div>
                                    </div>
                                `;
                            } else {
                                let fileIcon = 'fa-file';
                                if (file.type.startsWith('video/')) {
                                    fileIcon = 'fa-video';
                                } else if (file.type.includes('pdf')) {
                                    fileIcon = 'fa-file-pdf';
                                } else if (file.type.includes('document')) {
                                    fileIcon = 'fa-file-word';
                                }
                                
                                mediaPreview += `
                                    <div class="media-item" data-type="file" data-src="${file.name}" data-name="${file.name}">
                                        <div class="media-file">
                                            <i class="fas ${fileIcon}"></i>
                                            <div class="media-file-name">${file.name}</div>
                                        </div>
                                    </div>
                                `;
                            }
                        });
                        
                        // 如果文件超过3个，显示更多提示
                        if (assignment.files.length > 3) {
                            mediaPreview += `
                                <div class="media-item">
                                    <div class="media-file">
                                        <i class="fas fa-plus"></i>
                                        <div class="media-file-name">+${assignment.files.length - 3} ${this.state.currentLanguage === 'zh' ? '更多' : 'more'}</div>
                                    </div>
                                </div>
                            `;
                        }
                        
                        mediaPreview += '</div>';
                    }
                    
                    // 检查是否有图片文件
                    const hasImages = assignment.files && assignment.files.some(file => file.type.startsWith('image/'));
                    
                    assignmentCard.innerHTML = `
                        <div class="assignment-cover">
                            ${hasImages ? 
                                `<img src="${assignment.files[0].preview}" alt="${assignment.title}" class="assignment-cover-image">` :
                                `<div class="default-cover">
                                    <i class="fas fa-star-of-david"></i>
                                    <h3>${assignment.title}</h3>
                                    <p>${this.state.currentLanguage === 'zh' ? '全球视野下的犹太文明' : 'Global Perspectives on Jewish Civilization'}</p>
                                </div>`
                            }
                        </div>
                        <div class="assignment-content">
                            <h3 class="assignment-title">${assignment.title}</h3>
                            <div class="assignment-meta">
                                <span>${this.state.currentLanguage === 'zh' ? '作者：' : 'Author: '}${assignment.author} ${assignment.studentId ? `(${assignment.studentId})` : ''}</span>
                                <span>${assignment.date}</span>
                            </div>
                            <p class="assignment-description">${assignment.description}</p>
                            ${mediaPreview}
                            ${fileBadges ? `<div class="assignment-files">${fileBadges}</div>` : ''}
                            <div class="assignment-actions">
                                <button class="btn-text like-btn" data-id="${assignment.id}">
                                    <i class="far fa-heart"></i> <span>${assignment.likes}</span>
                                </button>
                                <button class="delete-btn assignment-delete-btn" data-id="${assignment.id}" data-author="${assignment.author}">
                                    <i class="fas fa-trash"></i> ${this.state.currentLanguage === 'zh' ? '删除' : 'Delete'}
                                </button>
                            </div>
                        </div>
                    `;
                    fragment.appendChild(assignmentCard);
                });
                
                assignmentGrid.appendChild(fragment);
            },
            
            // 显示论坛评论
            displayForumComments() {
                const forumList = document.getElementById('forumList');
                const noForumComments = document.getElementById('noForumComments');
                forumList.innerHTML = '';
                
                if (this.state.forumComments.length === 0) {
                    noForumComments.style.display = 'block';
                    forumList.appendChild(noForumComments);
                    return;
                }
                
                noForumComments.style.display = 'none';
                const fragment = document.createDocumentFragment();
                
                this.state.forumComments.forEach(comment => {
                    const commentElement = document.createElement('div');
                    commentElement.className = 'forum-comment fade-in';
                    commentElement.innerHTML = `
                        <div class="forum-comment-header">
                            <span class="forum-comment-author">${comment.author}${comment.studentId ? ` (${comment.studentId})` : ''}</span>
                            <span class="forum-comment-date">${comment.date}</span>
                        </div>
                        <p class="forum-comment-text">${comment.text}</p>
                        <div class="forum-comment-actions">
                            <button class="comment-delete-btn forum-delete-btn" data-id="${comment.id}" data-author="${comment.author}">
                                <i class="fas fa-trash"></i> ${this.state.currentLanguage === 'zh' ? '删除' : 'Delete'}
                            </button>
                        </div>
                    `;
                    fragment.appendChild(commentElement);
                });
                
                forumList.appendChild(fragment);
            },
            
            // 处理点赞
            handleLike(id, element) {
                const assignment = this.state.assignments.find(a => a.id === id);
                if (!assignment) return;
                
                assignment.likes += 1;
                this.saveToLocalStorage('assignments', this.state.assignments);
                element.querySelector('span').textContent = assignment.likes;
                
                // 动画效果
                const icon = element.querySelector('i');
                icon.classList.remove('far');
                icon.classList.add('fas');
                element.style.transform = 'scale(1.2)';
                setTimeout(() => element.style.transform = 'scale(1)', 300);
            },
            
            // 处理删除
            handleDelete(id, author, type) {
                const isAuthor = author === this.state.currentUser;
                
                if (isAuthor) {
                    // 本人直接删除
                    const confirmMessage = this.state.currentLanguage === 'zh' ? 
                        '确定要删除吗？此操作无法撤销。' : 
                        'Are you sure you want to delete? This action cannot be undone.';
                    
                    if (confirm(confirmMessage)) {
                        this.performDelete(id, type);
                    }
                } else {
                    // 非本人需要验证密钥
                    const key = prompt(this.state.currentLanguage === 'zh' ? 
                        '请输入删除密钥：' : 
                        'Please enter the delete key:');
                    
                    if (key === this.state.deleteKey) {
                        const confirmMessage = this.state.currentLanguage === 'zh' ? 
                            '密钥正确，确定要删除吗？此操作无法撤销。' : 
                            'Key verified. Are you sure you want to delete? This action cannot be undone.';
                        
                        if (confirm(confirmMessage)) {
                            this.performDelete(id, type);
                        }
                    } else {
                        alert(this.state.currentLanguage === 'zh' ? '密钥错误！' : 'Incorrect key!');
                    }
                }
            },
            
            // 执行删除
            performDelete(id, type) {
                if (type === 'assignment') {
                    this.state.assignments = this.state.assignments.filter(
                        assignment => assignment.id !== id
                    );
                    this.saveToLocalStorage('assignments', this.state.assignments);
                    this.displayAssignments();
                    alert(this.state.currentLanguage === 'zh' ? '作业删除成功！' : 'Assignment deleted successfully!');
                } else if (type === 'comment') {
                    this.state.forumComments = this.state.forumComments.filter(
                        comment => comment.id !== id
                    );
                    this.saveToLocalStorage('forumComments', this.state.forumComments);
                    this.displayForumComments();
                    alert(this.state.currentLanguage === 'zh' ? '评论删除成功！' : 'Comment deleted successfully!');
                }
            },
            
            // 显示作业详情
            showAssignmentDetail(id) {
                const assignment = this.state.assignments.find(a => a.id === id);
                if (!assignment) return;
                
                this.state.currentAssignmentId = id;
                
                // 更新模态框内容
                document.getElementById('modalAssignmentTitle').textContent = assignment.title;
                document.getElementById('modalAssignmentAuthor').textContent = 
                    `${this.state.currentLanguage === 'zh' ? '作者：' : 'Author: '}${assignment.author} ${assignment.studentId ? `(${assignment.studentId})` : ''}`;
                document.getElementById('modalAssignmentDate').textContent = assignment.date;
                document.getElementById('modalAssignmentDescription').textContent = assignment.description;
                document.getElementById('modalLikesCount').textContent = assignment.likes;
                
                // 更新媒体内容
                const modalMedia = document.getElementById('modalAssignmentMedia');
                modalMedia.innerHTML = '';
                
                if (assignment.files && assignment.files.length > 0) {
                    assignment.files.forEach((file, index) => {
                        if (file.type.startsWith('image/') && file.preview) {
                            modalMedia.innerHTML += `
                                <div class="media-item" data-type="image" data-src="${file.preview}" data-name="${file.name}">
                                    <img src="${file.preview}" alt="${file.name}" class="media-image">
                                    <div class="media-actions">
                                        <div class="media-action-btn view-media" title="${this.state.currentLanguage === 'zh' ? '查看' : 'View'}">
                                            <i class="fas fa-expand"></i>
                                        </div>
                                    </div>
                                </div>
                            `;
                        } else if (file.type.startsWith('video/') && file.thumbnail) {
                            modalMedia.innerHTML += `
                                <div class="media-item" data-type="video" data-src="${file.preview || ''}" data-name="${file.name}">
                                    <img src="${file.thumbnail}" alt="${file.name}" class="media-image">
                                    <div class="media-actions">
                                        <div class="media-action-btn view-media" title="${this.state.currentLanguage === 'zh' ? '查看' : 'View'}">
                                            <i class="fas fa-play"></i>
                                        </div>
                                        <a href="${file.preview || '#'}" class="media-action-btn download-btn" title="${this.state.currentLanguage === 'zh' ? '下载' : 'Download'}" download="${file.name}">
                                            <i class="fas fa-download"></i>
                                        </a>
                                    </div>
                                </div>
                            `;
                        } else {
                            let fileIcon = 'fa-file';
                            if (file.type.startsWith('video/')) {
                                fileIcon = 'fa-video';
                            } else if (file.type.includes('pdf')) {
                                fileIcon = 'fa-file-pdf';
                            } else if (file.type.includes('document')) {
                                fileIcon = 'fa-file-word';
                            }
                            
                            modalMedia.innerHTML += `
                                <div class="media-item" data-type="file" data-src="${file.name}" data-name="${file.name}">
                                    <div class="media-file">
                                        <i class="fas ${fileIcon}"></i>
                                        <div class="media-file-name">${file.name}</div>
                                        <a href="${file.preview || '#'}" class="download-btn" download="${file.name}">
                                            <i class="fas fa-download"></i> ${this.state.currentLanguage === 'zh' ? '下载' : 'Download'}
                                        </a>
                                    </div>
                                </div>
                            `;
                        }
                    });
                }
                
                // 显示模态框
                document.getElementById('assignmentModal').style.display = 'flex';
            },
            
            // 显示媒体文件
            showMedia(type, src, name) {
                const modal = document.getElementById('mediaModal');
                const modalImage = document.getElementById('modalImage');
                const modalVideo = document.getElementById('modalVideo');
                
                modalImage.style.display = 'none';
                modalVideo.style.display = 'none';
                
                if (type === 'image') {
                    modalImage.src = src;
                    modalImage.alt = name;
                    modalImage.style.display = 'block';
                } else if (type === 'video') {
                    modalVideo.src = src;
                    modalVideo.style.display = 'block';
                }
                
                modal.style.display = 'flex';
            },
            
            // 本地存储操作
            saveToLocalStorage(key, data) {
                localStorage.setItem(key, JSON.stringify(data));
            }
        };

        // 初始化应用
        document.addEventListener('DOMContentLoaded', () => app.init());
    </script>
</body>
</html>
