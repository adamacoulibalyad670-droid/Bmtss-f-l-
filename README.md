# Bmtss-f-l-
a ka fisa. 
bmtts 

./start.sh
cd /data/user/0/com.vscodroid/files/home/projects/bamanankan-app
sh start.sh
pip install -r requirements.txt
python3 -m uvicorn app:app --host 0.0.0.0 --port 8000
http://127.0.0.1:8000
export GEMINI_API_KEY="مفتاحك"
sh start.sh
gemini tts kmankanw

import base64
from google import genai

# ==============================
# قائمة الأصوات الجاهزة (30 صوت)
# ==============================
VOICES = {
    "Zephyr": "Bright",
    "Puck": "Upbeat",
    "Charon": "Informative",
    "Kore": "Firm",
    "Fenrir": "Excitable",
    "Leda": "Youthful",
    "Orus": "Firm",
    "Aoede": "Breezy",
    "Callirrhoe": "Easy-going",
    "Autonoe": "Bright",
    "Enceladus": "Breathy",
    "Iapetus": "Clear",
    "Umbriel": "Easy-going",
    "Algieba": "Smooth",
    "Despina": "Smooth",
    "Erinome": "Clear",
    "Algenib": "Gravelly",
    "Rasalgethi": "Informative",
    "Laomedeia": "Upbeat",
    "Achernar": "Soft",
    "Alnilam": "Firm",
    "Schedar": "Even",
    "Gacrux": "Mature",
    "Pulcherrima": "Forward",
    "Achird": "Friendly",
    "Zubenelgenubi": "Casual",
    "Vindemiatrix": "Gentle",
    "Sadachbia": "Lively",
    "Sadaltager": "Knowledgeable",
    "Sulafat": "Warm",
}

# ==============================
# الإعدادات (غيّر هنا)
# ==============================
API_KEY = None          # أو ضع مفتاحك هنا، أو اتركه None ليستخدم GEMINI_API_KEY من البيئة
VOICE = "Kore"          # اختر أي صوت من القائمة أعلاه
TEXT = "مرحباً، كيف حالك اليوم؟ أتمنى لك يوماً سعيداً!"
STYLE = "cheerful and friendly"  # أسلوب الكلام
OUTPUT_FILE = "output.wav"

# ==============================
# الكود الرئيسي
# ==============================
client = genai.Client(api_key=API_KEY) if API_KEY else genai.Client()

interaction = client.interactions.create(
    model="gemini-3.8-flash-tts",
    input=[{
        "type": "user_input",
        "content": [{
            "type": "text",
            "text": TEXT,
            "annotations": [{
                "type": "speech_metadata",
                "style": STYLE,
            }],
        }],
    }],
    response_format={"type": "audio"},
    generation_config={
        "speech_config": [
            {"voice": VOICE},
        ]
    },
)

# حفظ الملف
with open(OUTPUT_FILE, "wb") as f:
    f.write(base64.b64decode(interaction.output_audio.data))

print(f"✅ تم إنشاء الصوت بنجاح!")
print(f"الصوت المستخدم: {VOICE} ({VOICES.get(VOICE, '')})")
print(f"الملف: {OUTPUT_FILE}")
لا تنقص منها شيء خالص منها تشوش والقرقرة في الصوت اجعلها نقية 
لا تنقص منها شيء اجعلها تطبيق ثابتة غير فاشلة 
لا تنقص منها شيء اجعلها تدعم قرأة النص كيفما كثرت وطالت 
لا تنقص منها شيء انه لا يقوم بقراءة بصوت الحقيقي 
لا تنقص منها شيء اجعلها تستطيع قراءة باللغة البامبارا الصحيح النص والارقام مثلا 7: wolonwula
اجعلها تطبيق تستطيع قراءة ارقام والنص باللغة البامبارا بصوت صحيحة بالوقار والثبات جدا نقية من القرقرة والتشوش الصوت لا تنقص منها شيء اجعلها تستطيع قراءة ارقام والنص باللغة البامبارا بصوت صحيحة قوية احترافيته بالوقار والثبات جدا نقية من القرقرة والتشوش الصوت مع استنساخ الصوت بصمة مع كل ميزتها. اجعلها تستطيع قراءة النص كيفما طالت وكثرت
