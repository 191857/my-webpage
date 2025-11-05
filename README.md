# my-webpage
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的网页 - GitHub仓库</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f6f8fa;
            color: #24292f;
            line-height: 1.5;
        }
        
        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 16px;
        }
        
        header {
            background-color: #24292f;
            color: white;
            padding: 16px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 20px;
            font-weight: 600;
        }
        
        .logo i {
            font-size: 32px;
        }
        
        .search-bar {
            flex: 1;
            max-width: 272px;
            margin: 0 16px;
        }
        
        .search-bar input {
            width: 100%;
            padding: 8px 12px;
            background-color: #24292f;
            border: 1px solid #57606a;
            border-radius: 6px;
            color: white;
            font-size: 14px;
        }
        
        .search-bar input::placeholder {
            color: #8b949e;
        }
        
        .nav-links {
            display: flex;
            gap: 16px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 14px;
            font-weight: 500;
        }
        
        .user-menu {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background-color: #8b949e;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        .repo-header {
            padding: 16px 0;
            border-bottom: 1px solid #d0d7de;
        }
        
        .repo-title {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 8px;
        }
        
        .repo-title h1 {
            font-size: 24px;
            font-weight: 600;
        }
        
        .repo-status {
            display: flex;
            gap: 16px;
            font-size: 14px;
        }
        
        .repo-status span {
            padding: 2px 8px;
            border: 1px solid #d0d7de;
            border-radius: 12px;
            background-color: white;
        }
        
        .repo-nav {
            display: flex;
            margin-top: 16px;
            border-bottom: 1px solid #d0d7de;
        }
        
        .repo-nav a {
            padding: 8px 16px;
            text-decoration: none;
            color: #24292f;
            font-size: 14px;
            font-weight: 500;
            border-bottom: 2px solid transparent;
        }
        
        .repo-nav a.active {
            border-bottom-color: #fd8c73;
            font-weight: 600;
        }
        
        .main-content {
            display: flex;
            margin-top: 16px;
            gap: 24px;
        }
        
        .sidebar {
            width: 25%;
        }
        
        .content {
            width: 75%;
        }
        
        .card {
            background-color: white;
            border: 1px solid #d0d7de;
            border-radius: 6px;
            margin-bottom: 16px;
        }
        
        .card-header {
            padding: 16px;
            border-bottom: 1px solid #d0d7de;
            font-weight: 600;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .card-body {
            padding: 16px;
        }
        
        .file-list {
            list-style: none;
        }
        
        .file-list li {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 8px 0;
            border-bottom: 1px solid #f6f8fa;
        }
        
        .file-list li:last-child {
            border-bottom: none;
        }
        
        .file-list i {
            color: #656d76;
            width: 16px;
        }
        
        .file-list a {
            color: #0969da;
            text-decoration: none;
            font-size: 14px;
        }
        
        .file-list a:hover {
            text-decoration: underline;
        }
        
        .checkbox-list {
            list-style: none;
        }
        
        .checkbox-list li {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 4px 0;
        }
        
        .checkbox-list input[type="checkbox"] {
            margin: 0;
        }
        
        .btn {
            display: inline-block;
            padding: 5px 16px;
            background-color: #f6f8fa;
            border: 1px solid #d0d7de;
            border-radius: 6px;
            color: #24292f;
            font-size: 14px;
            font-weight: 500;
            text-decoration: none;
            cursor: pointer;
            transition: background-color 0.2s;
        }
        
        .btn:hover {
            background-color: #f3f4f6;
        }
        
        .btn-primary {
            background-color: #2da44e;
            color: white;
            border-color: #2da44e;
        }
        
        .btn-primary:hover {
            background-color: #2c974b;
        }
        
        .commit {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 8px 0;
            border-bottom: 1px solid #f6f8fa;
        }
        
        .commit:last-child {
            border-bottom: none;
        }
        
        .commit-avatar {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: #8b949e;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 10px;
            font-weight: bold;
        }
        
        .commit-info {
            flex: 1;
            font-size: 12px;
        }
        
        .commit-message {
            color: #24292f;
            font-weight: 600;
        }
        
        .commit-meta {
            co
