# learn-ondoku

## 📝 概要・説明 / Overview and Description

### 🇯🇵 日本語
「ろうどく チャレンジ！」は、小学生向けの朗読練習ウェブアプリケーションです。教科書の写真を撮ってAIに読み取らせ、その文章をマイクに向かって元気よく朗読すると、AI先生が優しく採点・フィードバックをしてくれます。子どもたちの音読の宿題を楽しく、そしてモチベーションを上げるためにサポートするツールです。ポップなUIとひらがな中心の優しい言葉遣いで、子どもが一人でも楽しみながら学習できます。

### 🇬🇧 English
"Reading Challenge!" is a web application designed for elementary school students to practice reading aloud. Kids can take a picture of their textbook, let the AI extract the text, and then read it out loud into the microphone. An "AI Teacher" will gently grade their reading and provide encouraging feedback. This tool is built to make reading homework fun and boost children's motivation. With a colorful UI and simple, gentle language, kids can enjoy learning independently.

---

## ✨ 主な機能一覧 / Key Features

### 🇯🇵 日本語
- **📷 教科書のテキスト読み取り (OCR)**: スマホのカメラやPCから画像をアップロードし、Gemini APIを利用して画像からテキストを高精度で抽出します。
- **🎤 音声認識による録音**: ブラウザ標準のWeb Speech APIを使用して、子どもの朗読音声をリアルタイムにテキスト化します。
- **👩‍🏫 AI先生の採点とアドバイス**: 抽出した元の文章と朗読した文章をAIが比較。「正確さ」「スムーズさ」「表現力」「丁寧さ」の4項目で100点満点の採点を行い、とにかく褒めて伸ばす優しいフィードバックを提供します。
- **⚙️ カスタムAPIキー設定 (大人向け)**: 画面右上の設定メニューから、自身のGemini APIキーを安全にローカル保存して利用できます（設定がない場合はフォールバック用のWorker APIを利用）。

### 🇬🇧 English
- **📷 Textbook Text Extraction (OCR)**: Upload an image or take a photo with a smartphone camera. The app uses the Gemini API to extract text with high accuracy.
- **🎤 Voice Recording via Speech Recognition**: Utilizes the browser's native Web Speech API to transcribe the child's reading out loud in real-time.
- **👩‍🏫 AI Teacher's Grading & Advice**: The AI compares the original text with the spoken text. It calculates a score out of 100 based on "Accuracy," "Fluency," "Expression," and "Politeness," providing super encouraging and gentle feedback.
- **⚙️ Custom API Key Configuration (For Adults)**: Through the settings menu, parents can securely save their own Gemini API key to local storage (falls back to a shared Worker API if not set).

---

## 🛠 使用技術・ライブラリ / Technologies & Libraries

- **Frontend**: HTML5, Vanilla JavaScript
- **Styling**: Tailwind CSS (via CDN)
- **Typography**: Google Fonts (Zen Maru Gothic)
- **Speech Recognition**: Web Speech API (`SpeechRecognition` / `webkitSpeechRecognition`)
- **Generative AI / OCR**: Google Gemini API (`gemini-2.5-flash`)
- **Backend (Fallback)**: Cloudflare Workers (used as a proxy when a custom API key is not configured)

---

## 🚀 セットアップ・使い方 / Setup & Usage

### 🇯🇵 日本語
1. **アプリを開く**: 本リポジトリのHTMLファイルをブラウザで開きます。※音声認識機能を使用するため、**Google Chrome** または **Microsoft Edge** を推奨します。
2. **APIキーの設定（任意）**: 画面右上の「⚙️（設定ボタン）」をクリックし、保護者の方がご自身のGemini APIキーを入力して「ほぞんする」を押してください。
3. **ステップ 1（写真撮影）**: 「ここをおして しゃしんを えらぶ」ボタンを押し、読みたい教科書のページを撮影するか画像を選択します。AIが文字を読み取ります。
4. **ステップ 2（朗読する）**: 読み取られた文章を確認したら、「ろくおん スタート」を押して、マイクに向かって元気よく文章を読み上げます。読み終わったら終了ボタンを押します。
5. **ステップ 3（採点結果）**: 「AIせんせいに さいてんしてもらう」ボタンを押すと、AI先生が点数と4つのポイントで優しいアドバイスを返してくれます！

### 🇬🇧 English
1. **Open the App**: Open the HTML file in a web browser. *Note: **Google Chrome** or **Microsoft Edge** is highly recommended for the Web Speech API to work properly.*
2. **Configure API Key (Optional)**: Click the "⚙️ (Settings)" button in the top right corner. Parents can enter their Gemini API key and save it.
3. **Step 1 (Take a Photo)**: Click the camera button to take a picture or upload an image of the textbook page. The AI will extract the text.
4. **Step 2 (Read Aloud)**: Once the text is displayed, click "Start Recording" and read the text aloud into the microphone. Click the stop button when finished.
5. **Step 3 (Get Results)**: Click the "Ask AI Teacher to Grade" button. The AI teacher will analyze the audio and provide a score along with gentle feedback across four categories!

---

## 📸 スクリーンショット / Screenshots

*(ここに実際のスクリーンショット画像を配置してください / Place your actual screenshots here)*

![ステップ1：教科書読み取り / Step 1: OCR Extraction](https://via.placeholder.com/600x400?text=Step+1:+Textbook+OCR)

![ステップ2：朗読録音 / Step 2: Voice Recording](https://via.placeholder.com/600x400?text=Step+2:+Voice+Recording)

![ステップ3：採点結果 / Step 3: Grading Results](https://via.placeholder.com/600x400?text=Step+3:+AI+Grading+Results)

---

## 📄 ライセンス / License

### 🇯🇵 日本語
このプロジェクトは **MIT ライセンス** の下で公開されています。自由に利用、改変、配布することが可能です。詳細については、リポジトリ内の `LICENSE` ファイルをご参照ください。

### 🇬🇧 English
This project is licensed under the **MIT License**. You are free to use, modify, and distribute it. See the `LICENSE` file in the repository for more details.