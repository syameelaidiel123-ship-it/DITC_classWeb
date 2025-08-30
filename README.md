/* DIT3C Class Website - Colourful & Complex Theme */

body {
    font-family: 'Montserrat', Arial, sans-serif;
    margin: 0;
    min-height: 100vh;
    background: radial-gradient(circle at 20% 20%, #fbc2eb 0%, #a6c1ee 40%, #fcb69f 100%);
    opacity: 0;
    animation: fadeInBody 1s ease-in forwards;
}
@keyframes fadeInBody {
    from { opacity: 0; }
    to { opacity: 1; }
}
header {
    text-align: center;
    padding: 40px;
    color: #fff;
    background: linear-gradient(90deg, #ff6a88 0%, #0078D7 100%);
    box-shadow: 0 8px 32px rgba(0,0,0,0.12);
    border-bottom-left-radius: 40px;
    border-bottom-right-radius: 40px;
    position: relative;
    opacity: 0;
    transform: translateY(-40px);
    animation: slideDownHeader 1s 0.2s cubic-bezier(.42,0,.58,1) forwards;
}
@keyframes slideDownHeader {
    from { opacity: 0; transform: translateY(-40px);}
    to { opacity: 1; transform: translateY(0);}
}
header h1 {
    font-size: 2.8em;
    letter-spacing: 2px;
    text-shadow: 0 2px 8px #0078D7;
}
header p {
    font-size: 1.2em;
    margin: 10px 0;
}
section {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 24px;
    padding: 32px;
}
.card {
    background: linear-gradient(135deg, #fff 60%, #fbc2eb 100%);
    padding: 24px;
    border-radius: 22px;
    box-shadow: 0 6px 24px rgba(0,0,0,0.13);
    opacity: 0;
    transform: scale(0.96) translateY(30px);
    animation: cardPopIn 0.7s cubic-bezier(.42,0,.58,1) forwards;
    border: 2px solid #a6c1ee;
    position: relative;
}
.card:nth-child(1) { animation-delay: 0.4s; }
.card:nth-child(2) { animation-delay: 0.6s; }
.card:nth-child(3) { animation-delay: 0.8s; }
.card:nth-child(4) { animation-delay: 1s; }
@keyframes cardPopIn {
    from { opacity: 0; transform: scale(0.96) translateY(30px);}
    to { opacity: 1; transform: scale(1) translateY(0);}
}
h2 {
    color: #ff6a88;
    text-shadow: 0 2px 8px #a6c1ee;
    font-size: 1.5em;
    margin-bottom: 12px;
}
.card ul li {
    margin-bottom: 8px;
    font-size: 1.1em;
}
.gallery-section {
    padding: 32px;
    background: linear-gradient(90deg, #fcb69f 0%, #a6c1ee 100%);
    border-radius: 0 0 40px 40px;
    box-shadow: 0 -4px 24px #0078D744;
    animation: gradientMove 8s linear infinite;
}
@keyframes gradientMove {
    0% { background-position: 0% 50%; }
    100% { background-position: 100% 50%; }
}
.gallery-section h2 {
    color: #0078D7;
    font-size: 1.6em;
    margin-bottom: 18px;
    text-shadow: 0 2px 8px #ff6a88;
}
.gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 18px;
    justify-content: center;
}
.gallery-item {
    position: relative;
    transition: transform 0.2s;
    background: linear-gradient(135deg, #fff 60%, #fbc2eb 100%);
    border-radius: 12px;
    box-shadow: 0 2px 12px #0078D722;
    padding: 8px;
}
.gallery-item:hover {
    transform: scale(1.12) rotate(-2deg);
    z-index: 2;
    box-shadow: 0 4px 24px #ff6a88;
}
.gallery-item img {
    max-width: 160px;
    border-radius: 10px;
    box-shadow: 0 2px 8px #0078D722;
    border: 2px solid #ff6a88;
    background: #fff;
}
.delete-btn {
    position: absolute;
    top: 8px; right: 8px;
    background: linear-gradient(135deg, #ff6a88 60%, #0078D7 100%);
    color: #fff;
    border: none; border-radius: 50%;
    width: 28px; height: 28px;
    cursor: pointer;
    font-size: 1.3em;
    box-shadow: 0 2px 6px rgba(0,0,0,0.12);
    transition: background 0.2s;
}
.delete-btn:hover {
    background: linear-gradient(90deg, #0078D7 60%, #ff6a88 100%);
}
.view-modal {
    display: none;
    position: fixed; top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.85);
    justify-content: center; align-items: center;
    z-index: 9999;
}
.view-modal-content {
    background: linear-gradient(135deg, #fff 60%, #fbc2eb 100%);
    padding: 28px;
    border-radius: 18px;
    text-align: center;
    animation: popin 0.3s;
    box-shadow: 0 4px 32px #0078D744;
}
@keyframes popin {
    0% { transform: scale(0.7); opacity: 0; }
    100% { transform: scale(1); opacity: 1; }
}
.view-modal-content img {
    max-width: 80vw;
    max-height: 80vh;
    border-radius: 14px;
    border: 3px solid #ff6a88;
    background: #fff;
    box-shadow: 0 2px 12px #0078D722;
}
.close-modal-btn {
    margin-top: 14px;
    background: linear-gradient(90deg, #ff6a88 60%, #0078D7 100%);
    color: white;
    border: none;
    border-radius: 10px;
    padding: 10px 22px;
    font-size: 1.1em;
    cursor: pointer;
    font-weight: bold;
    transition: background 0.2s;
    box-shadow: 0 2px 8px #0078D744;
}
.close-modal-btn:hover {
    background: linear-gradient(90deg, #0078D7 60%, #ff6a88 100%);
}
.popup-page {
    max-width: 700px;
    margin: 40px auto;
    background: linear-gradient(135deg, #fff 60%, #fbc2eb 100%);
    border-radius: 22px;
    box-shadow: 0 4px 24px #0078D722;
    padding: 36px;
    animation: popupFadeIn 0.5s;
}
@keyframes popupFadeIn {
    from { opacity: 0; transform: scale(0.95);}
    to { opacity: 1; transform: scale(1);}
}
.popup-page h1 {
    color: #ff6a88;
    text-shadow: 0 2px 8px #a6c1ee;
}
.popup-page ul { margin-top: 18px; }
.popup-page a { color: #0078D7; text-decoration: none; }
.chat-link { color: #ff6a88; font-weight: bold; }
.fun-btn {
    animation: bounceBtn 1.2s infinite alternate;
    background: linear-gradient(90deg, #fbc2eb 60%, #0078D7 100%);
    color: #fff;
    border: none;
    border-radius: 10px;
    padding: 8px 18px;
    font-size: 1em;
    font-weight: bold;
    box-shadow: 0 2px 8px #0078D744;
    cursor: pointer;
    transition: background 0.2s;
}
.fun-btn:hover {
    background: linear-gradient(90deg, #0078D7 60%, #ff6a88 100%);
}
@keyframes bounceBtn {
    0% { transform: translateY(0);}
    100% { transform: translateY(-8px);}
}
.confetti {
    position: fixed;
    pointer-events: none;
    z-index: 99999;
    left: 0; top: 0; width: 100vw; height: 100vh;
}
/* Rainbow border for upload section */
.upload-section {
    border: 3px solid;
    border-image: linear-gradient(90deg, #ff6a88, #fbc2eb, #a6c1ee, #fcb69f) 1;
    box-shadow: 0 2px 12px #ff6a88;
}
