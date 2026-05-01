import React, { useState, useMemo, useRef, useEffect } from "react";
import { Search, X, Sparkles, Send, Loader2, BookOpen, Volume2, VolumeX, Mic, MicOff, Play, Pause, Music, Settings, Edit3, Save, RotateCcw, Plus, Trash2, Check } from "lucide-react";

const defaultNames = [
  { n: 1, ar: "اللّٰه", tr: "Allah", ku: "ناوی تایبەت بە زاتی خودا" },
  { n: 2, ar: "الرَّحْمٰن", tr: "Ar-Rahman", ku: "یەکجار بەبەزەیی (بۆ هەمووان)" },
  { n: 3, ar: "الرَّحِيم", tr: "Ar-Rahim", ku: "میهرەبان (بۆ بڕواداران)" },
  { n: 4, ar: "الْمَلِك", tr: "Al-Malik", ku: "پاشا و خاوەن دەسەڵات" },
  { n: 5, ar: "الْقُدُّوس", tr: "Al-Quddus", ku: "زۆر پاک و بێگەرد" },
  { n: 6, ar: "السَّلَام", tr: "As-Salam", ku: "بڵاوکەرەوەی ئاشتی و سەلامەتی" },
  { n: 7, ar: "الْمُؤْمِن", tr: "Al-Mu’min", ku: "دڵنیاکەرەوە و پەناگەی بڕواداران" },
  { n: 8, ar: "الْمُهَيْمِن", tr: "Al-Muhaymin", ku: "چاودێر و پارێزەری هەموو شتێک" },
  { n: 9, ar: "الْعَزِيز", tr: "Al-Aziz", ku: "زۆر باڵادەست و بەهێز" },
  { n: 10, ar: "الْجَبَّار", tr: "Al-Jabbar", ku: "خاوەن شکۆ و جێبەجێکەر" },
  { n: 11, ar: "الْمُتَكَبِّر", tr: "Al-Mutakabbir", ku: "هەرە گەورە و باڵا" },
  { n: 12, ar: "الْخَالِق", tr: "Al-Khaliq", ku: "دروستکەر و بەدیهێنەر" },
  { n: 13, ar: "الْبَارِئ", tr: "Al-Bari’", ku: "داهێنەر و بێ کەمایەسی" },
  { n: 14, ar: "الْمُصَوِّر", tr: "Al-Musawwir", ku: "وێنەکێش و شێوەدەر" },
  { n: 15, ar: "الْغَفَّار", tr: "Al-Ghaffar", ku: "زۆر لێبوردە و پۆشەر" },
  { n: 16, ar: "الْقَهَّار", tr: "Al-Qahhar", ku: "هەرە زاڵ و باڵادەست" },
  { n: 17, ar: "الْوَهَّاب", tr: "Al-Wahhab", ku: "زۆر بەخشندە" },
  { n: 18, ar: "الرَّزَّاق", tr: "Ar-Razzaq", ku: "ڕۆزیدەر و بەخشەر" },
  { n: 19, ar: "الْفَتَّاح", tr: "Al-Fattah", ku: "کەرامەتکەر و گرێ کەرەوە" },
  { n: 20, ar: "الْعَلِيم", tr: "Al-‘Alim", ku: "زۆر زانا بە هەموو شتێک" },
  { n: 21, ar: "الْقَابِض", tr: "Al-Qabid", ku: "ڕۆزیبڕ و تەنگکەرەوە" },
  { n: 22, ar: "الْبَاسِط", tr: "Al-Basit", ku: "ڕۆزیبەخش و فراوانکەر" },
  { n: 23, ar: "الْخَافِض", tr: "Al-Khafid", ku: "نزمکەرەوە (بۆ ستەمکاران)" },
  { n: 24, ar: "الرَّافِع", tr: "Ar-Rafi’", ku: "بەرزکەرەوە (بۆ چاکەکاران)" },
  { n: 25, ar: "الْمُعِزّ", tr: "Al-Mu’izz", ku: "ڕێزدارکەر و سەرخەر" },
  { n: 26, ar: "الْمُذِلّ", tr: "Al-Mudhill", ku: "خوارکەرەوە و سەرشۆڕکەر" },
  { n: 27, ar: "السَّمِيع", tr: "As-Sami’", ku: "زۆر بیسەر بۆ هەموو دەنگێک" },
  { n: 28, ar: "الْبَصِير", tr: "Al-Basir", ku: "زۆر بینەر بۆ هەموو شتێک" },
  { n: 29, ar: "الْحَكَم", tr: "Al-Hakam", ku: "داوەری ڕەها و دادپەروەر" },
  { n: 30, ar: "الْعَدْل", tr: "Al-‘Adl", ku: "زۆر دادپەروەر" },
  { n: 31, ar: "اللَّطِيف", tr: "Al-Latif", ku: "میهرەبان و وردبین" },
  { n: 32, ar: "الْخَبِير", tr: "Al-Khabir", ku: "زۆر ئاگادار بە نهێنییەکان" },
  { n: 33, ar: "الْحَلِيم", tr: "Al-Halim", ku: "زۆر پشوودرێژ و لەسەرەخۆ" },
  { n: 34, ar: "الْعَظِيم", tr: "Al-‘Azim", ku: "زۆر گەورە و شکۆدار" },
  { n: 35, ar: "الْغَفُور", tr: "Al-Ghafur", ku: "زۆر لێبوردە و بەخشندە" },
  { n: 36, ar: "الشَّكُور", tr: "Ash-Shakur", ku: "پاداشتکەرەوەی چاکەکان" },
  { n: 37, ar: "الْعَلِيّ", tr: "Al-‘Aliyy", ku: "هەرە بەرز و باڵا" },
  { n: 38, ar: "الْكَبِير", tr: "Al-Kabir", ku: "زۆر گەورە و مەزن" },
  { n: 39, ar: "الْحَفِيظ", tr: "Al-Hafiz", ku: "پارێزەری هەموو دروستکراوەکان" },
  { n: 40, ar: "الْمُقِيت", tr: "Al-Muqit", ku: "بژێویدەر و توانادار" },
  { n: 41, ar: "الْحَسِيب", tr: "Al-Hasib", ku: "وردبین و ژمارەکار" },
  { n: 42, ar: "الْجَلِيل", tr: "Al-Jalil", ku: "خاوەن گەورەیی و پایەبەرز" },
  { n: 43, ar: "الْكَرِيم", tr: "Al-Karim", ku: "زۆر چاکەکار و بەخشندە" },
  { n: 44, ar: "الرَّقِيب", tr: "Ar-Raqib", ku: "چاودێر و ئاگادار" },
  { n: 45, ar: "الْمُجِيب", tr: "Al-Mujib", ku: "وەڵامدەرەوەی نزا و پاڕانەوە" },
  { n: 46, ar: "الْوَاسِع", tr: "Al-Wasi’", ku: "فراوان و گشتگیر" },
  { n: 47, ar: "الْحَكِيم", tr: "Al-Hakim", ku: "کاردروست و دانا" },
  { n: 48, ar: "الْوَدُود", tr: "Al-Wadud", ku: "زۆر خۆشەویست و دۆست" },
  { n: 49, ar: "الْمَجِيد", tr: "Al-Majid", ku: "شکۆدار و هەرە پایەبەرز" },
  { n: 50, ar: "الْبَاعِث", tr: "Al-Ba’ith", ku: "زیندووکەرەوەی دوای مردن" },
  { n: 51, ar: "الشَّهِيد", tr: "Ash-Shahid", ku: "شاهید و ئامادە لە هەموو کاتێک" },
  { n: 52, ar: "الْحَقّ", tr: "Al-Haqq", ku: "ڕاستی ڕەها و نەگۆڕ" },
  { n: 53, ar: "الْوَكِيل", tr: "Al-Wakil", ku: "پشت و پەنای بڕواداران" },
  { n: 54, ar: "الْقَوِيّ", tr: "Al-Qawiyy", ku: "زۆر بەهێز و توانادار" },
  { n: 55, ar: "الْمَتِين", tr: "Al-Matin", ku: "زۆر پتەو و جێگیر" },
  { n: 56, ar: "الْوَلِيّ", tr: "Al-Waliyy", ku: "دۆست و سەرپەرشتیار" },
  { n: 57, ar: "الْحَمِيد", tr: "Al-Hamid", ku: "شایستەی سوپاس و ستایش" },
  { n: 58, ar: "الْمُحْصِي", tr: "Al-Muhsi", ku: "ئامارکەر و ژمێریار" },
  { n: 59, ar: "الْمُبْدِئ", tr: "Al-Mubdi’", ku: "سەرەتاپێکەر و بەدیهێنەر" },
  { n: 60, ar: "الْمُعِيد", tr: "Al-Mu’id", ku: "گێڕەرەوە و دووبارەکەرەوە" },
  { n: 61, ar: "الْمُحْيِي", tr: "Al-Muhyi", ku: "ژیانبەخش و زیندووکەرەوە" },
  { n: 62, ar: "الْمُمِيت", tr: "Al-Mumit", ku: "مرێنەر و گیانکێش" },
  { n: 63, ar: "الْحَيّ", tr: "Al-Hayy", ku: "هەردەم زیندوو و نەمر" },
  { n: 64, ar: "الْقَيُّوم", tr: "Al-Qayyum", ku: "ڕاوەستاو بە زاتی خۆی" },
  { n: 65, ar: "الْوَاجِد", tr: "Al-Wajid", ku: "دەستکەوتوو و خاوەن شت" },
  { n: 66, ar: "الْمَاجِد", tr: "Al-Majid", ku: "شکۆدار و گەورە" },
  { n: 67, ar: "الْوَاحِد", tr: "Al-Wahid", ku: "تەنها و بێ هاوتا" },
  { n: 68, ar: "الصَّمَد", tr: "As-Samad", ku: "بێ پێویست و پەناگەی هەمووان" },
  { n: 69, ar: "الْقَادِر", tr: "Al-Qadir", ku: "توانادار بەسەر هەموو شتێکدا" },
  { n: 70, ar: "الْمُقْتَدِر", tr: "Al-Muqtadir", ku: "هەرە بەدەسەڵات و بەهێز" },
  { n: 71, ar: "الْمُقَدِّم", tr: "Al-Muqaddim", ku: "پێشخەر و گەیەنەر" },
  { n: 72, ar: "الْمُؤَخِّر", tr: "Al-Mu’akhkhir", ku: "پاشخەر و دوورخەرەوە" },
  { n: 73, ar: "الْأَوَّل", tr: "Al-Awwal", ku: "یەکەم و بێ سەرەتا" },
  { n: 74, ar: "الْآخِر", tr: "Al-Akhir", ku: "کۆتایی و بێ کۆتایی" },
  { n: 75, ar: "الظَّاهِر", tr: "Az-Zahir", ku: "ئاشکرا بە بەڵگەکان" },
  { n: 76, ar: "الْبَاطِن", tr: "Al-Batin", ku: "پەنهان و نادیار بە چاو" },
  { n: 77, ar: "الْوَالِي", tr: "Al-Wali", ku: "فەرمانڕەوا و پارێزەر" },
  { n: 78, ar: "الْمُتَعَالِي", tr: "Al-Muta’ali", ku: "هەرە بەرز و بڵند" },
  { n: 79, ar: "الْبَرّ", tr: "Al-Barr", ku: "زۆر چاکەکار و میهرەبان" },
  { n: 80, ar: "التَّوَّاب", tr: "At-Tawwab", ku: "تۆبەکەر و لێبوردە" },
  { n: 81, ar: "الْمُنْتَقِم", tr: "Al-Muntaqim", ku: "تۆڵەسێنەر (لە ستەمکاران)" },
  { n: 82, ar: "الْعَفُوّ", tr: "Al-‘Afuww", ku: "لێبوردەی گەورە" },
  { n: 83, ar: "الرَّؤُوف", tr: "Ar-Ra’uf", ku: "زۆر بەسۆز و بەڕەحم" },
  { n: 84, ar: "مَالِكُ الْمُلْك", tr: "Malik-ul-Mulk", ku: "خاوەنی هەموو موڵک و جیهان" },
  { n: 85, ar: "ذُو الْجَلَالِ وَالْإِكْرَام", tr: "Dhul-Jalali wal-Ikram", ku: "خاوەن گەورەیی و ڕێز" },
  { n: 86, ar: "الْمُقْسِط", tr: "Al-Muqsit", ku: "دادپەروەری ڕەها" },
  { n: 87, ar: "الْجَامِع", tr: "Al-Jami’", ku: "کۆکەرەوەی خەڵک لە ڕۆژی دوایی" },
  { n: 88, ar: "الْغَنِيّ", tr: "Al-Ghaniyy", ku: "دەوڵەمەندی بێ پێویست" },
  { n: 89, ar: "الْمُغْنِي", tr: "Al-Mughni", ku: "دەوڵەمەندکەر و بەخشەر" },
  { n: 90, ar: "الْمَانِع", tr: "Al-Mani’", ku: "ڕێگر لە خراپە و کێشە" },
  { n: 91, ar: "الضَّارّ", tr: "Ad-Darr", ku: "زیانبەخش (بە ویستی خۆی)" },
  { n: 92, ar: "النَّافِع", tr: "An-Nafi’", ku: "سودبەخش و خێرخواز" },
  { n: 93, ar: "النُّور", tr: "An-Nur", ku: "ڕووناککەرەوەی دڵ و جیهان" },
  { n: 94, ar: "الْهَادِي", tr: "Al-Hadi", ku: "ڕێ نیشاندەر بۆ ڕێگای ڕاست" },
  { n: 95, ar: "الْبَدِيع", tr: "Al-Badi’", ku: "داهێنەری بێ وێنە" },
  { n: 96, ar: "الْبَاقِي", tr: "Al-Baqi", ku: "هەرمان و جاویدان" },
  { n: 97, ar: "الْوَارِث", tr: "Al-Warith", ku: "خاوەنی کۆتایی هەموو شتێک" },
  { n: 98, ar: "الرَّشِيد", tr: "Ar-Rashid", ku: "شارەزا و ڕێنماییکەر" },
  { n: 99, ar: "الصَّبُور", tr: "As-Sabur", ku: "زۆر پشوودرێژ و ئارامگر" },
];

const DEFAULT_SYSTEM_PROMPT = `تۆ یاریدەدەرێکی شارەزایت لەسەر "ناوە جوانەکانی خودا" (الأسماء الحسنى) ـ ئەو ٩٩ ناوە پیرۆزەی خودا.

تەنها لەسەر ئەم بابەتانە وەڵام دەدەیتەوە:
- ماناکانی هەر یەک لە ٩٩ ناوەکە
- شیکردنەوەی واتای زمانەوانی و شەرعی ناوەکان
- ئاماژەکانی قورئان و فەرمودەکان دەربارەی ئەم ناوانە
- ئەخلاق و یادگار لە هەر ناوێک

ڕێنماییەکان:
- بە کوردی سۆرانی وەڵام بدەرەوە، زمانێکی ڕوون و ساکار بەکار بهێنە
- ئەگەر پێویست بوو، ناوی عەرەبی لەگەڵ نووسینی کوردی بنووسە
- ئەگەر پرسیار لە دەرەوەی بابەتی ٩٩ ناوەکە بوو، بە جوانی بڵێ:
  "ببورە، من تەنها شارەزام لەسەر ناوە جوانەکانی خودا. تکایە پرسیار لەسەر ئەم بابەتە بکە."
- وەڵامەکانت کورت و پڕ مانا بن (٢-٤ ڕستە)، نەوەک زۆر درێژ`;

// Persistent storage keys
const STORAGE_KEYS = {
  NAMES: "aih:names_v1",
  PROMPT: "aih:prompt_v1",
  KNOWLEDGE: "aih:knowledge_v1",
};

// Strip Arabic diacritics for cleaner TTS pronunciation
const cleanArabic = (s) => s.replace(/[\u064B-\u0652\u0670\u0640]/g, "");

// Detect if text is mostly Arabic/Kurdish script vs Latin
const detectLang = (text) => {
  if (!text) return "ar-SA";
  const arabicCount = (text.match(/[\u0600-\u06FF\u0750-\u077F]/g) || []).length;
  const latinCount = (text.match(/[a-zA-Z]/g) || []).length;
  return arabicCount > latinCount ? "ar-SA" : "en-US";
};

export default function App() {
  const [query, setQuery] = useState("");
  const [selected, setSelected] = useState(null);
  const [messages, setMessages] = useState([]);
  const [input, setInput] = useState("");
  const [loading, setLoading] = useState(false);
  const [showChat, setShowChat] = useState(false);
  const [speakingId, setSpeakingId] = useState(null);
  const [recording, setRecording] = useState(false);
  const [autoSpeak, setAutoSpeak] = useState(false);
  const [voicesReady, setVoicesReady] = useState(false);
  const [errorMsg, setErrorMsg] = useState("");
  const [recitationPlaying, setRecitationPlaying] = useState(false);
  const [recitationLoading, setRecitationLoading] = useState(false);
  const [recitationProgress, setRecitationProgress] = useState(0);

  // Admin / Update Panel state
  const [names, setNames] = useState(defaultNames);
  const [systemPrompt, setSystemPrompt] = useState(DEFAULT_SYSTEM_PROMPT);
  const [customKnowledge, setCustomKnowledge] = useState([]); // [{q, a}]
  const [showAdmin, setShowAdmin] = useState(false);
  const [adminTab, setAdminTab] = useState("ai"); // 'ai' | 'names' | 'knowledge'
  const [editingName, setEditingName] = useState(null); // name object being edited
  const [draftPrompt, setDraftPrompt] = useState("");
  const [newKnowledgeQ, setNewKnowledgeQ] = useState("");
  const [newKnowledgeA, setNewKnowledgeA] = useState("");
  const [savedFlash, setSavedFlash] = useState(false);
  const [storageReady, setStorageReady] = useState(false);

  const chatEndRef = useRef(null);
  const recognitionRef = useRef(null);
  const voicesRef = useRef([]);
  const audioRef = useRef(null);

  // Public domain full recitation of all 99 names from Internet Archive
  const FULL_RECITATION_URL =
    "https://archive.org/download/asma-ul-husna-99-names-of-allah/Asma-ul-Husna%20%2899%20Names%20of%20Allah%29.mp3";

  const filtered = useMemo(() => {
    if (!query.trim()) return names;
    const q = query.trim().toLowerCase();
    return names.filter(
      (n) =>
        n.ar.includes(query) ||
        n.tr.toLowerCase().includes(q) ||
        n.ku.includes(query) ||
        String(n.n).includes(q)
    );
  }, [query]);

  useEffect(() => {
    chatEndRef.current?.scrollIntoView({ behavior: "smooth" });
  }, [messages, loading]);

  // ===== Persistent Storage =====
  // Load saved data on mount
  useEffect(() => {
    const loadData = async () => {
      if (!window.storage) {
        setStorageReady(true);
        return;
      }
      try {
        const [nRes, pRes, kRes] = await Promise.all([
          window.storage.get(STORAGE_KEYS.NAMES).catch(() => null),
          window.storage.get(STORAGE_KEYS.PROMPT).catch(() => null),
          window.storage.get(STORAGE_KEYS.KNOWLEDGE).catch(() => null),
        ]);

        if (nRes?.value) {
          try {
            const parsed = JSON.parse(nRes.value);
            if (Array.isArray(parsed) && parsed.length > 0) setNames(parsed);
          } catch (e) {}
        }
        if (pRes?.value) {
          setSystemPrompt(pRes.value);
        }
        if (kRes?.value) {
          try {
            const parsed = JSON.parse(kRes.value);
            if (Array.isArray(parsed)) setCustomKnowledge(parsed);
          } catch (e) {}
        }
      } catch (e) {
        console.warn("Storage load error:", e);
      }
      setStorageReady(true);
    };
    loadData();
  }, []);

  // Helpers to save individual pieces
  const saveNames = async (newNames) => {
    setNames(newNames);
    if (window.storage) {
      try {
        await window.storage.set(STORAGE_KEYS.NAMES, JSON.stringify(newNames));
      } catch (e) { console.warn("Save names failed:", e); }
    }
  };

  const savePrompt = async (newPrompt) => {
    setSystemPrompt(newPrompt);
    if (window.storage) {
      try {
        await window.storage.set(STORAGE_KEYS.PROMPT, newPrompt);
      } catch (e) { console.warn("Save prompt failed:", e); }
    }
  };

  const saveKnowledge = async (newKnowledge) => {
    setCustomKnowledge(newKnowledge);
    if (window.storage) {
      try {
        await window.storage.set(STORAGE_KEYS.KNOWLEDGE, JSON.stringify(newKnowledge));
      } catch (e) { console.warn("Save knowledge failed:", e); }
    }
  };

  const flashSaved = () => {
    setSavedFlash(true);
    setTimeout(() => setSavedFlash(false), 1500);
  };

  // FIX: Load voices on mount - voices load async in most browsers
  useEffect(() => {
    if (typeof window === "undefined" || !window.speechSynthesis) return;

    const loadVoices = () => {
      const v = window.speechSynthesis.getVoices();
      if (v && v.length > 0) {
        voicesRef.current = v;
        setVoicesReady(true);
      }
    };

    loadVoices();
    window.speechSynthesis.onvoiceschanged = loadVoices;

    // Fallback: try again after 500ms (some browsers need this)
    const timer = setTimeout(loadVoices, 500);

    return () => {
      window.speechSynthesis.onvoiceschanged = null;
      clearTimeout(timer);
    };
  }, []);

  useEffect(() => {
    return () => {
      if (typeof window !== "undefined" && window.speechSynthesis) {
        window.speechSynthesis.cancel();
      }
      if (recognitionRef.current) {
        try { recognitionRef.current.stop(); } catch (e) {}
      }
      if (audioRef.current) {
        audioRef.current.pause();
        audioRef.current = null;
      }
    };
  }, []);

  // ===== Full Recitation Audio Player =====
  const toggleRecitation = () => {
    // Stop any TTS first
    if (window.speechSynthesis) window.speechSynthesis.cancel();
    setSpeakingId(null);

    if (audioRef.current && recitationPlaying) {
      audioRef.current.pause();
      setRecitationPlaying(false);
      return;
    }

    if (audioRef.current && !recitationPlaying) {
      audioRef.current.play().then(() => setRecitationPlaying(true)).catch(() => {});
      return;
    }

    // First time loading
    setRecitationLoading(true);
    const audio = new Audio(FULL_RECITATION_URL);
    audio.preload = "auto";

    audio.addEventListener("canplay", () => {
      setRecitationLoading(false);
    });
    audio.addEventListener("playing", () => {
      setRecitationPlaying(true);
      setRecitationLoading(false);
    });
    audio.addEventListener("pause", () => setRecitationPlaying(false));
    audio.addEventListener("ended", () => {
      setRecitationPlaying(false);
      setRecitationProgress(0);
    });
    audio.addEventListener("timeupdate", () => {
      if (audio.duration) {
        setRecitationProgress((audio.currentTime / audio.duration) * 100);
      }
    });
    audio.addEventListener("error", () => {
      setRecitationLoading(false);
      setRecitationPlaying(false);
      setErrorMsg("نەتوانرا دەنگەکە دابەزێنرێت. تکایە ئینتەرنێتەکەت پشکنە.");
      setTimeout(() => setErrorMsg(""), 4000);
    });

    audioRef.current = audio;
    audio.play().catch((err) => {
      setRecitationLoading(false);
      setErrorMsg("نەتوانرا لێدان دەست پێ بکات. دیسان هەوڵ بدە.");
      setTimeout(() => setErrorMsg(""), 4000);
    });
  };

  // ===== Text-to-Speech (FIXED) =====
  const speak = (text, id, lang = null) => {
    if (typeof window === "undefined" || !window.speechSynthesis) {
      setErrorMsg("ببورە، وێبگەڕەکەت پشتگیری قسەکردن ناکات.");
      return;
    }

    // If already speaking same item, stop
    if (speakingId === id) {
      window.speechSynthesis.cancel();
      setSpeakingId(null);
      return;
    }

    // Cancel any current speech
    window.speechSynthesis.cancel();

    // Auto-detect language if not specified
    const speechLang = lang || detectLang(text);

    // Use timeout to avoid race condition with cancel() (iOS/Safari fix)
    setTimeout(() => {
      const utter = new SpeechSynthesisUtterance(text);
      utter.lang = speechLang;
      utter.rate = speechLang.startsWith("ar") ? 0.75 : 0.9;
      utter.pitch = 1;
      utter.volume = 1;

      // Pick best voice from loaded voices
      const voices = voicesRef.current.length
        ? voicesRef.current
        : window.speechSynthesis.getVoices();

      if (voices && voices.length > 0) {
        let chosenVoice = null;
        if (speechLang.startsWith("ar")) {
          // Try to find Arabic voice
          chosenVoice =
            voices.find((v) => v.lang === "ar-SA") ||
            voices.find((v) => v.lang.startsWith("ar"));
        } else {
          chosenVoice =
            voices.find((v) => v.lang.startsWith("en")) || voices[0];
        }
        if (chosenVoice) utter.voice = chosenVoice;
      }

      utter.onend = () => setSpeakingId(null);
      utter.onerror = (e) => {
        setSpeakingId(null);
        if (e.error !== "interrupted" && e.error !== "canceled") {
          setErrorMsg("هەڵە لە قسەکردندا ڕوویدا. لەوانەیە دەنگی عەرەبی نەبێت.");
          setTimeout(() => setErrorMsg(""), 4000);
        }
      };

      setSpeakingId(id);
      window.speechSynthesis.speak(utter);
    }, 80);
  };

  const stopSpeaking = () => {
    if (typeof window !== "undefined" && window.speechSynthesis) {
      window.speechSynthesis.cancel();
    }
    setSpeakingId(null);
  };

  // ===== Speech-to-Text (FIXED) =====
  const startRecording = () => {
    const SR =
      typeof window !== "undefined" &&
      (window.SpeechRecognition || window.webkitSpeechRecognition);
    if (!SR) {
      setErrorMsg("وێبگەڕەکەت پشتگیری ناسینەوەی دەنگ ناکات. تکایە Chrome یان Edge بەکار بهێنە.");
      setTimeout(() => setErrorMsg(""), 4000);
      return;
    }

    try {
      const recognition = new SR();
      recognition.lang = "ar-SA";
      recognition.continuous = false;
      recognition.interimResults = false;
      recognition.maxAlternatives = 1;

      recognition.onstart = () => {
        setRecording(true);
        setErrorMsg("");
      };
      recognition.onend = () => setRecording(false);
      recognition.onerror = (event) => {
        setRecording(false);
        let msg = "هەڵە لە تۆمارکردندا.";
        if (event.error === "not-allowed" || event.error === "permission-denied") {
          msg = "ڕێگەی مایکرۆفۆن نەدراوە. تکایە لە دانانی وێبگەڕ ڕێگە بدە.";
        } else if (event.error === "no-speech") {
          msg = "هیچ دەنگێک نەهات. تکایە دیسان قسە بکە.";
        } else if (event.error === "network") {
          msg = "کێشەی ئینتەرنێت. تکایە پشکنین بکە.";
        }
        setErrorMsg(msg);
        setTimeout(() => setErrorMsg(""), 4000);
      };
      recognition.onresult = (event) => {
        const transcript = event.results[0][0].transcript;
        setInput((prev) => (prev ? prev + " " + transcript : transcript));
      };

      recognitionRef.current = recognition;
      recognition.start();
    } catch (e) {
      setRecording(false);
      setErrorMsg("نەتوانرا تۆمارکردن دەست پێ بکات.");
      setTimeout(() => setErrorMsg(""), 4000);
    }
  };

  const stopRecording = () => {
    if (recognitionRef.current) {
      try { recognitionRef.current.stop(); } catch (e) {}
    }
    setRecording(false);
  };

  // ===== AI Chat (FIXED) =====
  const askAI = async (userMsg, contextName = null) => {
    const newUser = { role: "user", content: userMsg };
    const updated = [...messages, newUser];
    setMessages(updated);
    setInput("");
    setLoading(true);
    setShowChat(true);
    setErrorMsg("");

    try {
      const contextNote = contextName
        ? `\n\nزانیاری دەربارەی ئەم ناوە: ${contextName.ar} (${contextName.tr}) ـ ${contextName.ku}`
        : "";

      // Inject custom knowledge if any exists
      const knowledgeNote = customKnowledge.length > 0
        ? "\n\n=== زانیاری زیادە لە کاربەر ===\n" +
          customKnowledge
            .map((k, i) => `${i + 1}. پرسیار: ${k.q}\n   وەڵام: ${k.a}`)
            .join("\n")
        : "";

      const res = await fetch("https://api.anthropic.com/v1/messages", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          model: "claude-sonnet-4-20250514",
          max_tokens: 1000,
          system: systemPrompt + contextNote + knowledgeNote,
          messages: updated.map((m) => ({ role: m.role, content: m.content })),
        }),
      });

      if (!res.ok) {
        let errorDetail = `هەڵە: ${res.status}`;
        try {
          const errData = await res.json();
          if (errData?.error?.message) errorDetail = errData.error.message;
        } catch (_) {}
        throw new Error(errorDetail);
      }

      const data = await res.json();
      const text = (data.content || [])
        .filter((b) => b.type === "text")
        .map((b) => b.text)
        .join("\n");
      const reply = text.trim() || "ببورە، وەڵامێک نەهاتەوە.";
      const newMessages = [...updated, { role: "assistant", content: reply }];
      setMessages(newMessages);

      if (autoSpeak && reply) {
        setTimeout(
          () => speak(reply, `msg-${newMessages.length - 1}`),
          300
        );
      }
    } catch (e) {
      console.error("API Error:", e);
      setMessages([
        ...updated,
        {
          role: "assistant",
          content: `ببورە، هەڵەیەک ڕوویدا: ${e.message || "نەزانراو"}. تکایە دیسان هەوڵ بدە.`,
        },
      ]);
    } finally {
      setLoading(false);
    }
  };

  const handleSend = () => {
    if (!input.trim() || loading) return;
    askAI(input.trim(), selected);
  };

  const askAboutName = (name) => {
    askAI(`زیاتر دەربارەی ناوی "${name.ar} (${name.tr})" بۆم ڕوون بکەرەوە.`, name);
  };

  return (
    <div
      dir="rtl"
      className="min-h-screen w-full"
      style={{
        background:
          "radial-gradient(ellipse at top, #f5efe1 0%, #ebe3cf 60%, #e0d6bc 100%)",
        fontFamily: "'Noto Naskh Arabic', 'Amiri', serif",
      }}
    >
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Scheherazade+New:wght@400;700&family=Noto+Naskh+Arabic:wght@400;500;700&family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&display=swap');
        .font-arabic { font-family: 'Amiri', 'Scheherazade New', serif; }
        .font-kurdish { font-family: 'Noto Naskh Arabic', serif; }
        .font-latin { font-family: 'Cormorant Garamond', serif; letter-spacing: 0.04em; }
        .ornament::before, .ornament::after {
          content: '✦';
          color: #b8954a;
          font-size: 0.7em;
          margin: 0 0.6em;
          opacity: 0.6;
        }
        .card-hover {
          transition: transform 0.4s cubic-bezier(0.2, 0.8, 0.2, 1), box-shadow 0.4s, background 0.4s;
        }
        .card-hover:hover {
          transform: translateY(-3px);
          background: rgba(255, 252, 244, 0.95);
          box-shadow: 0 12px 30px -10px rgba(45, 60, 45, 0.18);
        }
        .pattern-bg {
          background-image: 
            radial-gradient(circle at 1px 1px, rgba(45, 60, 45, 0.06) 1px, transparent 0);
          background-size: 24px 24px;
        }
        .scroll-fade::-webkit-scrollbar { width: 6px; }
        .scroll-fade::-webkit-scrollbar-thumb { background: rgba(45,60,45,0.2); border-radius: 3px; }
        .glow-gold {
          text-shadow: 0 0 30px rgba(184, 149, 74, 0.3);
        }
        @keyframes fadeUp {
          from { opacity: 0; transform: translateY(8px); }
          to { opacity: 1; transform: translateY(0); }
        }
        .fade-in { animation: fadeUp 0.4s ease forwards; }
        @keyframes pulse-rec {
          0%, 100% { box-shadow: 0 0 0 0 rgba(220, 38, 38, 0.5); }
          50% { box-shadow: 0 0 0 12px rgba(220, 38, 38, 0); }
        }
        .recording-pulse { animation: pulse-rec 1.5s infinite; }
        @keyframes pulse-speak {
          0%, 100% { transform: scale(1); }
          50% { transform: scale(1.1); }
        }
        .speaking-pulse { animation: pulse-speak 1s infinite; }
      `}</style>

      <div className="pattern-bg min-h-screen">
        {/* Settings Button (top-left) */}
        <button
          onClick={() => {
            setDraftPrompt(systemPrompt);
            setShowAdmin(true);
          }}
          className="fixed top-5 left-5 z-30 w-11 h-11 rounded-full flex items-center justify-center transition-all hover:rotate-45"
          style={{
            background: "rgba(255, 252, 244, 0.85)",
            border: "1px solid rgba(184, 149, 74, 0.4)",
            color: "#1a3024",
            backdropFilter: "blur(8px)",
            boxShadow: "0 4px 12px rgba(20, 30, 20, 0.08)",
          }}
          aria-label="ڕێکخستنەکان"
          title="نوێکردنەوەی AI"
        >
          <Settings size={18} />
        </button>

        {/* Error Toast */}
        {errorMsg && (
          <div
            className="fixed top-4 right-1/2 translate-x-1/2 z-50 px-5 py-3 rounded-full font-kurdish text-sm fade-in shadow-lg"
            style={{
              background: "linear-gradient(135deg, #dc2626, #b91c1c)",
              color: "#fff",
              maxWidth: "90vw",
            }}
            role="alert"
          >
            ⚠️ {errorMsg}
          </div>
        )}

        {/* Header */}
        <header className="max-w-5xl mx-auto px-6 pt-16 pb-10 text-center">
          <div className="flex justify-center mb-4">
            <div className="flex items-center gap-2 text-xs tracking-widest uppercase font-latin" style={{ color: "#8a7340" }}>
              <span>۹۹</span>
              <span>·</span>
              <span>الأسماء الحسنى</span>
            </div>
          </div>
          <h1
            className="font-arabic text-5xl md:text-6xl mb-3 glow-gold"
            style={{ color: "#1a3024", fontWeight: 700 }}
          >
            ناوە جوانەکانی خودا
          </h1>
          <p
            className="font-kurdish text-base md:text-lg ornament"
            style={{ color: "#5a4a2a" }}
          >
            ٩٩ ناوی پیرۆز و ماناکانیان
          </p>
        </header>

        {/* Full Recitation Player */}
        <div className="max-w-2xl mx-auto px-6 mb-8">
          <div
            className="rounded-2xl p-4 border relative overflow-hidden"
            style={{
              background: recitationPlaying
                ? "linear-gradient(135deg, #1a3024 0%, #2d4a36 100%)"
                : "linear-gradient(135deg, rgba(255, 252, 244, 0.9) 0%, rgba(245, 239, 225, 0.9) 100%)",
              borderColor: "rgba(184, 149, 74, 0.3)",
              transition: "background 0.5s",
            }}
          >
            {/* Progress bar background */}
            {recitationProgress > 0 && (
              <div
                className="absolute bottom-0 left-0 h-1 transition-all"
                style={{
                  width: `${recitationProgress}%`,
                  background: recitationPlaying
                    ? "linear-gradient(90deg, #d4b876, #b8954a)"
                    : "linear-gradient(90deg, #b8954a, #8a7340)",
                }}
              />
            )}

            <div className="flex items-center gap-4">
              <button
                onClick={toggleRecitation}
                disabled={recitationLoading}
                className="flex-shrink-0 w-14 h-14 rounded-full flex items-center justify-center transition-transform hover:scale-105 disabled:opacity-50"
                style={{
                  background: recitationPlaying
                    ? "rgba(212, 184, 118, 0.9)"
                    : "linear-gradient(135deg, #1a3024, #2d4a36)",
                  color: recitationPlaying ? "#1a3024" : "#d4b876",
                }}
                aria-label={recitationPlaying ? "وەستاندن" : "لێدان"}
              >
                {recitationLoading ? (
                  <Loader2 size={22} className="animate-spin" />
                ) : recitationPlaying ? (
                  <Pause size={22} />
                ) : (
                  <Play size={22} style={{ marginRight: "-3px" }} />
                )}
              </button>

              <div className="flex-1 text-right">
                <div className="flex items-center gap-2 justify-end mb-1">
                  <Music
                    size={14}
                    style={{
                      color: recitationPlaying ? "#d4b876" : "#8a7340",
                    }}
                    className={recitationPlaying ? "speaking-pulse" : ""}
                  />
                  <h3
                    className="font-kurdish text-sm font-bold"
                    style={{ color: recitationPlaying ? "#f5efe1" : "#1a3024" }}
                  >
                    خوێندنەوەی تەواوی ٩٩ ناو
                  </h3>
                </div>
                <p
                  className="text-xs font-kurdish"
                  style={{ color: recitationPlaying ? "rgba(245, 239, 225, 0.7)" : "#8a7340" }}
                >
                  {recitationLoading
                    ? "دادەبەزێنرێت..."
                    : recitationPlaying
                    ? `لێدان • ${Math.round(recitationProgress)}%`
                    : "گوێ بگرە لە دەنگی ڕاستی"}
                </p>
              </div>
            </div>
          </div>
        </div>

        {/* Search */}
        <div className="max-w-2xl mx-auto px-6 mb-10">
          <div
            className="flex items-center gap-3 px-5 py-3 rounded-full border"
            style={{
              background: "rgba(255, 252, 244, 0.7)",
              borderColor: "rgba(184, 149, 74, 0.3)",
              backdropFilter: "blur(8px)",
            }}
          >
            <Search size={18} style={{ color: "#8a7340" }} />
            <input
              value={query}
              onChange={(e) => setQuery(e.target.value)}
              placeholder="گەڕان لە ناوەکان... (عەرەبی، کوردی یان ژمارە)"
              className="flex-1 bg-transparent outline-none font-kurdish text-sm md:text-base"
              style={{ color: "#1a3024" }}
            />
            {query && (
              <button onClick={() => setQuery("")} aria-label="پاککردنەوە">
                <X size={16} style={{ color: "#8a7340" }} />
              </button>
            )}
          </div>
          <p className="text-center text-xs mt-3 font-kurdish" style={{ color: "#8a7340" }}>
            {filtered.length} لە {names.length} ناو
          </p>
        </div>

        {/* Names grid */}
        <main className="max-w-6xl mx-auto px-4 md:px-6 pb-32">
          <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
            {filtered.map((name, i) => {
              const isSpeaking = speakingId === `card-${name.n}`;
              return (
                <div
                  key={name.n}
                  className="card-hover fade-in relative p-5 rounded-2xl border"
                  style={{
                    background: "rgba(255, 252, 244, 0.6)",
                    borderColor: "rgba(184, 149, 74, 0.25)",
                    animationDelay: `${(i % 12) * 30}ms`,
                  }}
                >
                  <button
                    onClick={() => setSelected(name)}
                    className="w-full text-right"
                  >
                    <div className="flex items-start justify-between mb-3">
                      <span
                        className="font-latin text-xs"
                        style={{ color: "#8a7340", letterSpacing: "0.15em" }}
                      >
                        {String(name.n).padStart(2, "0")}
                      </span>
                      <Sparkles size={12} style={{ color: "#b8954a", opacity: 0.6 }} />
                    </div>
                    <div
                      className="font-arabic text-3xl md:text-4xl mb-2"
                      style={{ color: "#1a3024", lineHeight: 1.4 }}
                    >
                      {name.ar}
                    </div>
                    <div
                      className="font-latin text-sm mb-3"
                      style={{ color: "#8a7340" }}
                    >
                      {name.tr}
                    </div>
                    <div
                      className="font-kurdish text-sm leading-relaxed pl-10"
                      style={{ color: "#3a3020", fontWeight: 500 }}
                    >
                      {name.ku}
                    </div>
                  </button>

                  {/* Speak button */}
                  <button
                    onClick={(e) => {
                      e.stopPropagation();
                      speak(cleanArabic(name.ar), `card-${name.n}`, "ar-SA");
                    }}
                    className={`absolute bottom-4 left-4 w-9 h-9 rounded-full flex items-center justify-center transition-all ${isSpeaking ? "speaking-pulse" : ""}`}
                    style={{
                      background: isSpeaking
                        ? "linear-gradient(135deg, #1a3024, #2d4a36)"
                        : "rgba(184, 149, 74, 0.15)",
                      color: isSpeaking ? "#d4b876" : "#8a7340",
                    }}
                    aria-label="گوێگرتن"
                  >
                    {isSpeaking ? <VolumeX size={14} /> : <Volume2 size={14} />}
                  </button>
                </div>
              );
            })}
          </div>

          {filtered.length === 0 && (
            <div className="text-center py-20 font-kurdish" style={{ color: "#5a4a2a" }}>
              هیچ ناوێک نەدۆزرایەوە بۆ "{query}"
            </div>
          )}
        </main>

        {/* Detail Modal */}
        {selected && (
          <div
            className="fixed inset-0 z-40 flex items-center justify-center p-4"
            style={{ background: "rgba(20, 28, 22, 0.6)", backdropFilter: "blur(6px)" }}
            onClick={() => { stopSpeaking(); setSelected(null); }}
          >
            <div
              className="relative max-w-lg w-full rounded-3xl p-8 fade-in"
              style={{
                background: "linear-gradient(180deg, #fdfaf0 0%, #f5efe1 100%)",
                boxShadow: "0 25px 60px -15px rgba(20, 30, 20, 0.4)",
                border: "1px solid rgba(184, 149, 74, 0.3)",
              }}
              onClick={(e) => e.stopPropagation()}
            >
              <button
                onClick={() => { stopSpeaking(); setSelected(null); }}
                className="absolute top-4 left-4 p-2 rounded-full hover:bg-black/5"
                aria-label="داخستن"
              >
                <X size={18} style={{ color: "#5a4a2a" }} />
              </button>

              <div className="text-center mb-6">
                <div
                  className="font-latin text-xs mb-2"
                  style={{ color: "#8a7340", letterSpacing: "0.2em" }}
                >
                  ناوی ژمارە {selected.n}
                </div>
                <div
                  className="font-arabic text-6xl mb-3 glow-gold"
                  style={{ color: "#1a3024", fontWeight: 700 }}
                >
                  {selected.ar}
                </div>
                <div
                  className="font-latin text-base mb-4"
                  style={{ color: "#8a7340", letterSpacing: "0.05em" }}
                >
                  {selected.tr}
                </div>

                {/* Big speak button in modal */}
                <button
                  onClick={() => speak(cleanArabic(selected.ar), `modal-${selected.n}`, "ar-SA")}
                  className={`mx-auto w-14 h-14 rounded-full flex items-center justify-center transition-all ${speakingId === `modal-${selected.n}` ? "speaking-pulse" : ""}`}
                  style={{
                    background:
                      speakingId === `modal-${selected.n}`
                        ? "linear-gradient(135deg, #1a3024, #2d4a36)"
                        : "rgba(184, 149, 74, 0.2)",
                    color: speakingId === `modal-${selected.n}` ? "#d4b876" : "#1a3024",
                  }}
                  aria-label="گوێگرتن لە تەلەفز"
                >
                  {speakingId === `modal-${selected.n}` ? <VolumeX size={22} /> : <Volume2 size={22} />}
                </button>
                <p className="text-xs mt-2 font-kurdish" style={{ color: "#8a7340" }}>
                  گوێ بگرە لە تەلەفزی ڕاستی
                </p>
              </div>

              <div
                className="text-center mb-4 ornament font-kurdish"
                style={{ color: "#5a4a2a", fontSize: "0.9rem", letterSpacing: "0.05em" }}
              >
                واتا
              </div>

              <p
                className="text-center font-kurdish leading-loose mb-7 text-lg"
                style={{ color: "#1a3024" }}
              >
                {selected.ku}
              </p>

              <button
                onClick={() => {
                  stopSpeaking();
                  askAboutName(selected);
                  setSelected(null);
                }}
                className="w-full py-3 rounded-full font-kurdish text-sm flex items-center justify-center gap-2 transition-all"
                style={{
                  background: "linear-gradient(90deg, #1a3024, #2d4a36)",
                  color: "#f5efe1",
                  letterSpacing: "0.03em",
                }}
              >
                <Sparkles size={14} />
                زیاتر بزانە لە یاریدەدەرەکە
              </button>
            </div>
          </div>
        )}

        {/* ====== ADMIN / UPDATE PANEL ====== */}
        {showAdmin && (
          <div
            className="fixed inset-0 z-50 flex items-center justify-center p-3"
            style={{ background: "rgba(20, 28, 22, 0.7)", backdropFilter: "blur(8px)" }}
            onClick={() => { setShowAdmin(false); setEditingName(null); }}
          >
            <div
              className="relative w-full max-w-3xl rounded-3xl flex flex-col fade-in"
              style={{
                background: "linear-gradient(180deg, #fdfaf0 0%, #f5efe1 100%)",
                boxShadow: "0 25px 60px -15px rgba(20, 30, 20, 0.5)",
                border: "1px solid rgba(184, 149, 74, 0.3)",
                maxHeight: "90vh",
              }}
              onClick={(e) => e.stopPropagation()}
            >
              {/* Header */}
              <div
                className="flex items-center justify-between p-5 border-b"
                style={{ borderColor: "rgba(184, 149, 74, 0.2)" }}
              >
                <div className="flex items-center gap-3">
                  <div
                    className="w-10 h-10 rounded-full flex items-center justify-center"
                    style={{ background: "linear-gradient(135deg, #1a3024, #2d4a36)" }}
                  >
                    <Settings size={18} style={{ color: "#d4b876" }} />
                  </div>
                  <div className="text-right">
                    <h2 className="font-kurdish text-lg font-bold" style={{ color: "#1a3024" }}>
                      نوێکردنەوەی AI
                    </h2>
                    <p className="font-kurdish text-xs" style={{ color: "#8a7340" }}>
                      ڕێنماییەکان و ناوەکان دەستکاری بکە
                    </p>
                  </div>
                </div>
                <button
                  onClick={() => { setShowAdmin(false); setEditingName(null); }}
                  className="p-2 rounded-full hover:bg-black/5"
                  aria-label="داخستن"
                >
                  <X size={20} style={{ color: "#5a4a2a" }} />
                </button>
              </div>

              {/* Tabs */}
              <div
                className="flex gap-1 p-2 border-b"
                style={{ borderColor: "rgba(184, 149, 74, 0.2)", background: "rgba(245, 239, 225, 0.4)" }}
              >
                {[
                  { id: "ai", label: "ڕێنماییەکانی AI", icon: Edit3 },
                  { id: "names", label: "ناوەکان", icon: BookOpen },
                  { id: "knowledge", label: "زانیاری زیادە", icon: Plus },
                ].map((tab) => {
                  const Icon = tab.icon;
                  const active = adminTab === tab.id;
                  return (
                    <button
                      key={tab.id}
                      onClick={() => setAdminTab(tab.id)}
                      className="flex-1 flex items-center justify-center gap-2 py-2.5 px-3 rounded-xl font-kurdish text-sm transition-all"
                      style={{
                        background: active ? "linear-gradient(135deg, #1a3024, #2d4a36)" : "transparent",
                        color: active ? "#d4b876" : "#5a4a2a",
                        fontWeight: active ? 700 : 500,
                      }}
                    >
                      <Icon size={14} />
                      <span>{tab.label}</span>
                    </button>
                  );
                })}
              </div>

              {/* Content area */}
              <div className="overflow-y-auto scroll-fade flex-1 p-5">
                {/* TAB 1: AI System Prompt */}
                {adminTab === "ai" && (
                  <div className="space-y-4 fade-in">
                    <div>
                      <label
                        className="font-kurdish text-sm font-bold block mb-2"
                        style={{ color: "#1a3024" }}
                      >
                        ڕێنماییەکانی AI (System Prompt)
                      </label>
                      <p className="font-kurdish text-xs mb-3" style={{ color: "#8a7340" }}>
                        ئەم دەقە دیاری دەکات کە AI چۆن قسە بکات و چی بزانێت. تەنها ئەو شتانە دەزانێت کە تۆ پێی دەڵێیت.
                      </p>
                      <textarea
                        value={draftPrompt}
                        onChange={(e) => setDraftPrompt(e.target.value)}
                        rows={14}
                        dir="rtl"
                        className="w-full p-4 rounded-2xl outline-none font-kurdish text-sm leading-relaxed border resize-y"
                        style={{
                          background: "#fdfaf0",
                          borderColor: "rgba(184, 149, 74, 0.3)",
                          color: "#1a3024",
                          minHeight: "260px",
                        }}
                      />
                    </div>

                    <div className="flex gap-2">
                      <button
                        onClick={async () => {
                          await savePrompt(draftPrompt);
                          flashSaved();
                        }}
                        className="flex-1 py-3 rounded-full font-kurdish text-sm flex items-center justify-center gap-2"
                        style={{
                          background: "linear-gradient(90deg, #1a3024, #2d4a36)",
                          color: "#f5efe1",
                        }}
                      >
                        {savedFlash ? <Check size={14} /> : <Save size={14} />}
                        {savedFlash ? "هەڵگیرا!" : "هەڵگرتن"}
                      </button>
                      <button
                        onClick={() => {
                          if (confirm("دڵنیایت کە دەتەوێت بگەڕێیتەوە بۆ ڕاسپێردراوی سەرەتایی؟")) {
                            setDraftPrompt(DEFAULT_SYSTEM_PROMPT);
                            savePrompt(DEFAULT_SYSTEM_PROMPT);
                            flashSaved();
                          }
                        }}
                        className="px-4 py-3 rounded-full font-kurdish text-sm flex items-center gap-2 border"
                        style={{
                          borderColor: "rgba(184, 149, 74, 0.4)",
                          color: "#5a4a2a",
                        }}
                      >
                        <RotateCcw size={14} />
                        گەڕاندنەوە
                      </button>
                    </div>
                  </div>
                )}

                {/* TAB 2: Names Editor */}
                {adminTab === "names" && (
                  <div className="space-y-3 fade-in">
                    {editingName ? (
                      <div
                        className="p-5 rounded-2xl border"
                        style={{
                          background: "rgba(255, 252, 244, 0.7)",
                          borderColor: "rgba(184, 149, 74, 0.4)",
                        }}
                      >
                        <div className="text-center mb-4">
                          <div
                            className="font-arabic text-4xl mb-1"
                            style={{ color: "#1a3024" }}
                          >
                            {editingName.ar}
                          </div>
                          <div className="font-latin text-sm" style={{ color: "#8a7340" }}>
                            {editingName.tr} · ژمارە {editingName.n}
                          </div>
                        </div>

                        <label className="font-kurdish text-xs block mb-1" style={{ color: "#5a4a2a" }}>
                          ناوی عەرەبی
                        </label>
                        <input
                          value={editingName.ar}
                          onChange={(e) => setEditingName({ ...editingName, ar: e.target.value })}
                          className="w-full p-3 mb-3 rounded-xl outline-none font-arabic text-2xl border text-center"
                          style={{
                            background: "#fdfaf0",
                            borderColor: "rgba(184, 149, 74, 0.3)",
                            color: "#1a3024",
                          }}
                          dir="rtl"
                        />

                        <label className="font-kurdish text-xs block mb-1" style={{ color: "#5a4a2a" }}>
                          نووسینی لاتینی
                        </label>
                        <input
                          value={editingName.tr}
                          onChange={(e) => setEditingName({ ...editingName, tr: e.target.value })}
                          className="w-full p-3 mb-3 rounded-xl outline-none font-latin border"
                          style={{
                            background: "#fdfaf0",
                            borderColor: "rgba(184, 149, 74, 0.3)",
                            color: "#1a3024",
                          }}
                          dir="ltr"
                        />

                        <label className="font-kurdish text-xs block mb-1" style={{ color: "#5a4a2a" }}>
                          مانا بە کوردی
                        </label>
                        <textarea
                          value={editingName.ku}
                          onChange={(e) => setEditingName({ ...editingName, ku: e.target.value })}
                          rows={3}
                          className="w-full p-3 mb-4 rounded-xl outline-none font-kurdish text-sm border resize-y"
                          style={{
                            background: "#fdfaf0",
                            borderColor: "rgba(184, 149, 74, 0.3)",
                            color: "#1a3024",
                          }}
                          dir="rtl"
                        />

                        <div className="flex gap-2">
                          <button
                            onClick={async () => {
                              const updated = names.map((nm) =>
                                nm.n === editingName.n ? editingName : nm
                              );
                              await saveNames(updated);
                              flashSaved();
                              setEditingName(null);
                            }}
                            className="flex-1 py-2.5 rounded-full font-kurdish text-sm flex items-center justify-center gap-2"
                            style={{
                              background: "linear-gradient(90deg, #1a3024, #2d4a36)",
                              color: "#f5efe1",
                            }}
                          >
                            <Save size={13} /> هەڵگرتن
                          </button>
                          <button
                            onClick={() => setEditingName(null)}
                            className="px-4 py-2.5 rounded-full font-kurdish text-sm border"
                            style={{
                              borderColor: "rgba(184, 149, 74, 0.4)",
                              color: "#5a4a2a",
                            }}
                          >
                            هەڵوەشاندنەوە
                          </button>
                        </div>
                      </div>
                    ) : (
                      <>
                        <div className="flex items-center justify-between mb-3">
                          <p className="font-kurdish text-xs" style={{ color: "#8a7340" }}>
                            {names.length} ناو ـ کرتە بکە بۆ دەستکاری
                          </p>
                          <button
                            onClick={() => {
                              if (confirm("هەموو گۆڕانکاریەکان بسڕێتەوە؟")) {
                                saveNames(defaultNames);
                                flashSaved();
                              }
                            }}
                            className="text-xs font-kurdish px-3 py-1.5 rounded-full border flex items-center gap-1"
                            style={{
                              borderColor: "rgba(184, 149, 74, 0.4)",
                              color: "#5a4a2a",
                            }}
                          >
                            <RotateCcw size={11} /> گەڕاندنەوە
                          </button>
                        </div>

                        {names.map((nm) => (
                          <button
                            key={nm.n}
                            onClick={() => setEditingName({ ...nm })}
                            className="w-full p-3 rounded-xl border flex items-center gap-3 text-right hover:bg-white/40 transition-colors"
                            style={{
                              background: "rgba(255, 252, 244, 0.5)",
                              borderColor: "rgba(184, 149, 74, 0.2)",
                            }}
                          >
                            <span
                              className="font-latin text-xs flex-shrink-0 w-6"
                              style={{ color: "#8a7340" }}
                            >
                              {String(nm.n).padStart(2, "0")}
                            </span>
                            <span
                              className="font-arabic text-2xl flex-shrink-0"
                              style={{ color: "#1a3024" }}
                            >
                              {nm.ar}
                            </span>
                            <span className="flex-1 font-kurdish text-sm" style={{ color: "#3a3020" }}>
                              {nm.ku}
                            </span>
                            <Edit3 size={14} style={{ color: "#8a7340" }} />
                          </button>
                        ))}
                      </>
                    )}
                  </div>
                )}

                {/* TAB 3: Custom Knowledge */}
                {adminTab === "knowledge" && (
                  <div className="space-y-4 fade-in">
                    <p className="font-kurdish text-xs" style={{ color: "#8a7340" }}>
                      زانیاری زیادە بنووسە کە AI لەگەڵ ڕێنماییە سەرەکیەکان بەکار بهێنێت. وەک نموونە: ئایەتە قورئانیەکان، فەرمودەکان، یان زانیاری تایبەتی.
                    </p>

                    {/* Add new knowledge form */}
                    <div
                      className="p-4 rounded-2xl border"
                      style={{
                        background: "rgba(255, 252, 244, 0.7)",
                        borderColor: "rgba(184, 149, 74, 0.3)",
                      }}
                    >
                      <label className="font-kurdish text-xs block mb-1" style={{ color: "#5a4a2a" }}>
                        پرسیار / بابەت
                      </label>
                      <input
                        value={newKnowledgeQ}
                        onChange={(e) => setNewKnowledgeQ(e.target.value)}
                        placeholder="بۆ نموونە: ئایەتی الرحمن لە قورئاندا"
                        className="w-full p-3 mb-3 rounded-xl outline-none font-kurdish text-sm border"
                        style={{
                          background: "#fdfaf0",
                          borderColor: "rgba(184, 149, 74, 0.3)",
                          color: "#1a3024",
                        }}
                        dir="rtl"
                      />

                      <label className="font-kurdish text-xs block mb-1" style={{ color: "#5a4a2a" }}>
                        وەڵام / زانیاری
                      </label>
                      <textarea
                        value={newKnowledgeA}
                        onChange={(e) => setNewKnowledgeA(e.target.value)}
                        rows={3}
                        placeholder="زانیاریەکە لێرە بنووسە..."
                        className="w-full p-3 mb-3 rounded-xl outline-none font-kurdish text-sm border resize-y"
                        style={{
                          background: "#fdfaf0",
                          borderColor: "rgba(184, 149, 74, 0.3)",
                          color: "#1a3024",
                        }}
                        dir="rtl"
                      />

                      <button
                        onClick={async () => {
                          if (!newKnowledgeQ.trim() || !newKnowledgeA.trim()) return;
                          const updated = [
                            ...customKnowledge,
                            { q: newKnowledgeQ.trim(), a: newKnowledgeA.trim() },
                          ];
                          await saveKnowledge(updated);
                          setNewKnowledgeQ("");
                          setNewKnowledgeA("");
                          flashSaved();
                        }}
                        disabled={!newKnowledgeQ.trim() || !newKnowledgeA.trim()}
                        className="w-full py-2.5 rounded-full font-kurdish text-sm flex items-center justify-center gap-2 disabled:opacity-40"
                        style={{
                          background: "linear-gradient(90deg, #1a3024, #2d4a36)",
                          color: "#f5efe1",
                        }}
                      >
                        <Plus size={14} /> زیادکردن
                      </button>
                    </div>

                    {/* List existing knowledge */}
                    {customKnowledge.length === 0 ? (
                      <div
                        className="text-center py-8 font-kurdish text-sm"
                        style={{ color: "#8a7340" }}
                      >
                        هیچ زانیاری زیادە نییە. یەکەم زانیاری بنووسە لە سەرەوە.
                      </div>
                    ) : (
                      <div className="space-y-2">
                        <p className="font-kurdish text-xs" style={{ color: "#5a4a2a" }}>
                          {customKnowledge.length} زانیاری زیادە
                        </p>
                        {customKnowledge.map((k, i) => (
                          <div
                            key={i}
                            className="p-3 rounded-xl border flex items-start gap-2"
                            style={{
                              background: "rgba(255, 252, 244, 0.5)",
                              borderColor: "rgba(184, 149, 74, 0.2)",
                            }}
                          >
                            <div className="flex-1 text-right">
                              <div
                                className="font-kurdish text-sm font-bold mb-1"
                                style={{ color: "#1a3024" }}
                              >
                                {k.q}
                              </div>
                              <div
                                className="font-kurdish text-xs leading-relaxed"
                                style={{ color: "#3a3020" }}
                              >
                                {k.a}
                              </div>
                            </div>
                            <button
                              onClick={async () => {
                                const updated = customKnowledge.filter((_, idx) => idx !== i);
                                await saveKnowledge(updated);
                              }}
                              className="p-1.5 rounded-lg hover:bg-red-50"
                              aria-label="سڕینەوە"
                            >
                              <Trash2 size={14} style={{ color: "#dc2626" }} />
                            </button>
                          </div>
                        ))}
                      </div>
                    )}
                  </div>
                )}
              </div>

              {/* Footer */}
              <div
                className="px-5 py-3 border-t flex items-center justify-between text-xs font-kurdish"
                style={{
                  borderColor: "rgba(184, 149, 74, 0.2)",
                  color: "#8a7340",
                  background: "rgba(245, 239, 225, 0.5)",
                }}
              >
                <span>
                  {storageReady ? "✓ بیرگە چالاکە" : "⏳ بیرگە لۆد دەبێت..."}
                </span>
                {savedFlash && (
                  <span style={{ color: "#1a3024", fontWeight: 700 }} className="fade-in">
                    ✓ هەڵگیرا
                  </span>
                )}
              </div>
            </div>
          </div>
        )}

        {/* AI Chat Panel */}
        <div
          className="fixed bottom-0 left-0 right-0 z-30 transition-all duration-500"
          style={{
            transform: showChat ? "translateY(0)" : "translateY(calc(100% - 72px))",
          }}
        >
          <div
            className="max-w-2xl mx-auto rounded-t-3xl border-t border-x"
            style={{
              background: "linear-gradient(180deg, #fdfaf0 0%, #f5efe1 100%)",
              borderColor: "rgba(184, 149, 74, 0.3)",
              boxShadow: "0 -15px 40px -10px rgba(20, 30, 20, 0.2)",
            }}
          >
            {/* Toggle bar */}
            <div className="flex items-center justify-between px-6 py-4">
              <button
                onClick={() => setShowChat(!showChat)}
                className="flex items-center gap-3 font-kurdish flex-1 text-right"
                style={{ color: "#1a3024" }}
              >
                <div
                  className="w-9 h-9 rounded-full flex items-center justify-center"
                  style={{ background: "linear-gradient(135deg, #1a3024, #2d4a36)" }}
                >
                  <BookOpen size={16} style={{ color: "#d4b876" }} />
                </div>
                <div className="text-right">
                  <div className="text-sm font-bold">یاریدەدەری ناوەکان</div>
                  <div className="text-xs" style={{ color: "#8a7340" }}>
                    پرسیار بکە بە دەنگ یان نووسین
                  </div>
                </div>
              </button>
              <div className="flex items-center gap-2">
                <button
                  onClick={() => setAutoSpeak(!autoSpeak)}
                  className="text-xs font-kurdish px-3 py-1.5 rounded-full border"
                  style={{
                    background: autoSpeak ? "linear-gradient(135deg, #1a3024, #2d4a36)" : "transparent",
                    color: autoSpeak ? "#d4b876" : "#8a7340",
                    borderColor: "rgba(184, 149, 74, 0.3)",
                  }}
                  title="خوێندنەوەی خۆکار"
                >
                  {autoSpeak ? "🔊 چالاک" : "🔇 ناچالاک"}
                </button>
                <button
                  onClick={() => setShowChat(!showChat)}
                  className="text-2xl transition-transform px-2"
                  style={{
                    color: "#8a7340",
                    transform: showChat ? "rotate(180deg)" : "rotate(0deg)",
                  }}
                  aria-label="کردنەوە/داخستن"
                >
                  ⌃
                </button>
              </div>
            </div>

            {/* Messages */}
            <div
              className="scroll-fade overflow-y-auto px-6 pb-2"
              style={{ height: "320px" }}
            >
              {messages.length === 0 && (
                <div className="text-center py-10 font-kurdish text-sm" style={{ color: "#8a7340" }}>
                  <Sparkles size={20} className="mx-auto mb-3" style={{ color: "#b8954a" }} />
                  پرسیارت چییە دەربارەی ناوە جوانەکانی خودا؟
                  <div className="mt-4 flex flex-wrap gap-2 justify-center">
                    {[
                      "مانای ناوی الرحمن چییە؟",
                      "جیاوازی نێوان الرحمن و الرحیم چییە؟",
                      "کام ناوەکان دەربارەی بەخشندەییەکیەتین؟",
                    ].map((q) => (
                      <button
                        key={q}
                        onClick={() => askAI(q)}
                        className="px-3 py-1.5 rounded-full text-xs font-kurdish border"
                        style={{
                          background: "rgba(255, 252, 244, 0.8)",
                          borderColor: "rgba(184, 149, 74, 0.3)",
                          color: "#1a3024",
                        }}
                      >
                        {q}
                      </button>
                    ))}
                  </div>
                </div>
              )}

              {messages.map((m, i) => {
                const isSpeak = speakingId === `msg-${i}`;
                return (
                  <div
                    key={i}
                    className={`mb-3 flex ${m.role === "user" ? "justify-start" : "justify-end"} fade-in`}
                  >
                    <div className="max-w-[80%] flex flex-col gap-1">
                      <div
                        className="px-4 py-2.5 rounded-2xl font-kurdish text-sm leading-relaxed whitespace-pre-wrap"
                        style={{
                          background:
                            m.role === "user"
                              ? "linear-gradient(135deg, #1a3024, #2d4a36)"
                              : "rgba(255, 252, 244, 0.95)",
                          color: m.role === "user" ? "#f5efe1" : "#1a3024",
                          border: m.role === "user" ? "none" : "1px solid rgba(184, 149, 74, 0.25)",
                        }}
                      >
                        {m.content}
                      </div>
                      {m.role === "assistant" && (
                        <button
                          onClick={() => speak(m.content, `msg-${i}`)}
                          className="self-end text-xs flex items-center gap-1 px-2 py-1 rounded-full"
                          style={{ color: isSpeak ? "#1a3024" : "#8a7340" }}
                        >
                          {isSpeak ? <VolumeX size={11} /> : <Volume2 size={11} />}
                          <span className="font-kurdish">{isSpeak ? "وەستان" : "گوێگرتن"}</span>
                        </button>
                      )}
                    </div>
                  </div>
                );
              })}

              {loading && (
                <div className="flex justify-end mb-3">
                  <div
                    className="px-4 py-3 rounded-2xl flex items-center gap-2"
                    style={{
                      background: "rgba(255, 252, 244, 0.95)",
                      border: "1px solid rgba(184, 149, 74, 0.25)",
                    }}
                  >
                    <Loader2 size={14} className="animate-spin" style={{ color: "#8a7340" }} />
                    <span className="text-xs font-kurdish" style={{ color: "#5a4a2a" }}>
                      وەڵامدانەوە...
                    </span>
                  </div>
                </div>
              )}
              <div ref={chatEndRef} />
            </div>

            {/* Input with mic */}
            <div className="p-4 border-t" style={{ borderColor: "rgba(184, 149, 74, 0.2)" }}>
              <div className="flex items-center gap-2">
                <button
                  onClick={recording ? stopRecording : startRecording}
                  disabled={loading}
                  className={`p-3 rounded-full transition-all ${recording ? "recording-pulse" : ""}`}
                  style={{
                    background: recording
                      ? "linear-gradient(135deg, #dc2626, #b91c1c)"
                      : "rgba(184, 149, 74, 0.2)",
                    color: recording ? "#fff" : "#1a3024",
                  }}
                  aria-label={recording ? "وەستاندنی تۆمارکردن" : "تۆمارکردنی دەنگ"}
                  title={recording ? "وەستاندن" : "قسە بکە"}
                >
                  {recording ? <MicOff size={16} /> : <Mic size={16} />}
                </button>
                <input
                  value={input}
                  onChange={(e) => setInput(e.target.value)}
                  onKeyDown={(e) => e.key === "Enter" && handleSend()}
                  placeholder={recording ? "گوێ دەگرم..." : "پرسیارەکەت بنووسە یان قسە بکە..."}
                  className="flex-1 px-4 py-3 rounded-full outline-none font-kurdish text-sm border"
                  style={{
                    background: "#fdfaf0",
                    borderColor: recording ? "rgba(220, 38, 38, 0.5)" : "rgba(184, 149, 74, 0.3)",
                    color: "#1a3024",
                  }}
                  disabled={loading}
                />
                <button
                  onClick={handleSend}
                  disabled={loading || !input.trim()}
                  className="p-3 rounded-full disabled:opacity-40 transition-opacity"
                  style={{
                    background: "linear-gradient(135deg, #1a3024, #2d4a36)",
                    color: "#d4b876",
                  }}
                  aria-label="ناردن"
                >
                  <Send size={16} style={{ transform: "scaleX(-1)" }} />
                </button>
              </div>
            </div>
          </div>
        </div>

        <div className="h-20" />
      </div>
    </div>
  );
}
