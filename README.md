<script>
/*
  Simple bilingual toggle (EN/SO) using data-i18n keys.
  Your HTML elements should have: data-i18n="keyName"
  Your language buttons should have IDs: lang-en and lang-so
  Your year span should have ID: year
*/

const dict = {
  en: {
    tagline: "Unity • Justice • Dignity",
    orgName: "Milwaukee Somali Bantu Community Organization",
    orgType: "Nonprofit • Milwaukee, Wisconsin",
    navAbout: "About",
    navPrograms: "Programs",
    navBoard: "Board",
    navContact: "Contact",
    pill: "Serving the Somali Bantu community in Milwaukee",
    heroTitle: "Human rights advocacy and trusted community services — built with dignity.",
    heroDesc: "We support families through resettlement help, youth sports, referrals, case support, and community programs. We also advocate for civil rights, fair access, and respect for every person.",
    btnGetHelp: "Get Help",
    btnExplore: "Explore Programs",
    trust1: "Community-based nonprofit",
    trust2Num: "Support",
    trust2: "Resettlement & services",
    trust3Num: "Advocacy",
    trust3: "Human rights & protection",

    impactTitle: "Community Impact",
    impactSub: "Practical support. Strong advocacy. Real results.",
    stat1Num: "Advocacy",
    stat1Label: "Human rights support & referrals",
    stat2Num: "Resettlement",
    stat2Label: "Guidance for families and newcomers",
    stat3Num: "Youth",
    stat3Label: "Sports, mentorship, and leadership",
    impact1Title: "Services that meet real needs",
    impact1Desc: "Support for forms, referrals, and community navigation.",
    impact2Title: "Advocacy with dignity",
    impact2Desc: "Helping protect rights and promote fair access.",
    impact3Title: "Community-led leadership",
    impact3Desc: "Transparent leadership serving Milwaukee.",
    impactBtn: "See Programs",

    aboutTitle: "About Us",
    aboutDesc: "We are a Milwaukee-based nonprofit dedicated to serving the Somali Bantu community through practical support, protection of rights, and community-led programs.",
    missionTitle: "Mission",
    missionDesc: "To strengthen and empower the Somali Bantu community in Milwaukee through human rights advocacy, social services, and programs that build opportunity.",
    visionTitle: "Vision",
    visionDesc: "A safe, thriving, and respected community where families have access, dignity, and a strong voice.",
    valuesTitle: "Values",
    valuesDesc: "Integrity, service, unity, accountability, and respect for every person.",

    programsTitle: "Programs & Services",
    programsDesc: "We provide support across multiple areas. If you need help, contact us and we will guide you to the right service.",
    prog1Title: "Human Rights Advocacy",
    prog1Desc: "Support, reporting help, referrals, and community education to protect civil rights and dignity.",
    prog2Title: "Resettlement Support",
    prog2Desc: "Guidance with resources, interpretation support, local referrals, and community navigation.",
    prog3Title: "Community Services",
    prog3Desc: "Case support, transportation resource guidance, forms help, and local service connections.",
    prog4Title: "Youth Sports",
    prog4Desc: "Sports programs and mentorship that promote health, leadership, teamwork, and confidence.",
    prog5Title: "Family & Children Support",
    prog5Desc: "Family-focused services, children support referrals, and youth wellbeing assistance.",
    prog6Title: "Community Engagement",
    prog6Desc: "Meetings, workshops, outreach, and partnerships that strengthen community voice.",

    boardTitle: "Board & Leadership",
    boardDesc: "Our leadership team serves the community with transparency, service, and accountability.",
    presRole: "President",
    vpRole: "Vice President",
    secRole: "Secretary",
    edRole: "Executive Director",
    aedRole: "Assistant Executive Director",
    treRole: "Treasury",
    pcRole: "Program Coordinator",
    apcRole: "Assistant Program Coordinator",
    fcRole: "Family & Children Coordinator",
    spRole: "Spokesperson",

    contactTitle: "Contact",
    contactDesc: "Tell us what you need help with. We will respond as soon as possible.",
    contactInfoTitle: "Organization Info",
    locationLabel: "Location:",
    locationValue: "Milwaukee, Wisconsin",
    emailLabel: "Email:",
    phoneLabel: "Phone:",
    contactNote: "Replace the email/phone with your real nonprofit contact info.",
    formName: "Name",
    formEmail: "Email",
    formMessage: "Message",
    formBtn: "Send Message",
    formHint: "This demo form doesn’t send yet. If you want, I’ll connect it to Formspree or your email.",
    footerSub: "Nonprofit • Milwaukee, Wisconsin"
  },

  so: {
    tagline: "Midnimo • Cadaalad • Karaamo",
    orgName: "Ururka Bulshada Soomaali Bantu ee Milwaukee",
    orgType: "Hay’ad Samafal • Milwaukee, Wisconsin",
    navAbout: "Ku Saabsan",
    navPrograms: "Barnaamijyada",
    navBoard: "Hoggaanka",
    navContact: "Xiriir",
    pill: "U adeegidda bulshada Soomaali Bantu ee Milwaukee",
    heroTitle: "Difaaca xuquuqda aadanaha iyo adeegyo bulsho oo lagu kalsoon yahay — si sharaf leh.",
    heroDesc: "Waxaan taageernaa qoysaska anagoo bixinayna caawinta dib-u-dejinta, ciyaaraha dhalinyarada, gudbinta adeegyada, taageerada kiisaska, iyo barnaamijyada bulshada. Sidoo kale waxaan u doodnaa xuquuqda madaniga, helitaanka caddaaladda, iyo ixtiraamka qof walba.",
    btnGetHelp: "Hel Caawimaad",
    btnExplore: "Eeg Barnaamijyada",
    trust1: "Hay’ad bulsho ku dhisan",
    trust2Num: "Taageero",
    trust2: "Dib-u-dejin & adeegyo",
    trust3Num: "U-doodid",
    trust3: "Xuquuqda aadanaha & ilaalin",

    impactTitle: "Saameynta Bulshada",
    impactSub: "Taageero dhab ah. U-doodid xooggan. Natiijo la taaban karo.",
    stat1Num: "U-doodid",
    stat1Label: "Taageero xuquuq & gudbin adeegyo",
    stat2Num: "Dib-u-dejin",
    stat2Label: "Hagid qoysas & dadka cusub",
    stat3Num: "Dhalinyaro",
    stat3Label: "Ciyaaro, hagid, & hoggaan",
    impact1Title: "Adeegyo la jaanqaada baahida",
    impact1Desc: "Caawin foomam, gudbin, iyo hagid adeegyada deegaanka.",
    impact2Title: "U-doodid si karaamo leh",
    impact2Desc: "Ka caawinta ilaalinta xuquuqda iyo helitaanka caddaaladda.",
    impact3Title: "Hoggaan bulshadu hoggaamiso",
    impact3Desc: "Hoggaan daahfuran oo u adeegaya Milwaukee.",
    impactBtn: "Eeg Barnaamijyada",

    aboutTitle: "Ku Saabsan",
    aboutDesc: "Waxaan nahay hay’ad samafal oo fadhigeedu yahay Milwaukee oo u heellan taageerada bulshada Soomaali Bantu anagoo bixinna caawimo wax ku ool ah, ilaalinta xuquuqda, iyo barnaamijyo bulsho hoggaaminayaan.",
    missionTitle: "Himiladeenna",
    missionDesc: "Inaan xoojino oo awood-siino bulshada Soomaali Bantu ee Milwaukee annagoo u marayna u-doodista xuquuqda aadanaha, adeegyada bulshada, iyo barnaamijyo fura fursado.",
    visionTitle: "Aragtideenna",
    visionDesc: "Bulsho ammaan ah, kobcaysa, oo la ixtiraamo—qoysaskuna helaan adeeg, karaamo, iyo cod xooggan.",
    valuesTitle: "Qiyamkeenna",
    valuesDesc: "Daacadnimo, adeeg, midnimo, isla-xisaabtan, iyo ixtiraam qof walba.",

    programsTitle: "Barnaamijyada & Adeegyada",
    programsDesc: "Waxaan bixinnaa taageero dhinacyo badan. Haddii aad u baahan tahay caawimo, nala soo xiriir—waan ku hagaynaa adeegga ku habboon.",
    prog1Title: "U-doodista Xuquuqda Aadanaha",
    prog1Desc: "Taageero, caawin warbixin, gudbin, iyo wacyigelin si loo ilaaliyo xuquuqda iyo karaamada.",
    prog2Title: "Taageerada Dib-u-dejinta",
    prog2Desc: "Hagid kheyraad, turjumaad/taageero luqadeed, gudbin, iyo hagitaan deegaanka.",
    prog3Title: "Adeegyada Bulshada",
    prog3Desc: "Taageero kiis, hagid gaadiid/kheyraad, caawin foomam, iyo isku-xir adeegyo.",
    prog4Title: "Ciyaaraha Dhalinyarada",
    prog4Desc: "Barnaamijyo ciyaareed iyo hagid dhalinyaro si loo dhiso caafimaad, hoggaan, iyo kalsooni.",
    prog5Title: "Taageerada Qoyska & Carruurta",
    prog5Desc: "Taageero qoys, gudbin carruurta, iyo caawin daryeelka dhalinyarada.",
    prog6Title: "Ka-Qaybgalka Bulshada",
    prog6Desc: "Kulan, aqoon-is-weydaarsi, wacyigelin, iyo iskaashi lagu xoojinayo codka bulshada.",

    boardTitle: "Hoggaanka & Guddiga",
    boardDesc: "Hoggaankeenna wuxuu u adeegaa bulshada si daahfurnaan, adeeg, iyo isla-xisaabtan leh.",
    presRole: "Guddoomiye",
    vpRole: "Guddoomiye Ku-xigeen",
    secRole: "Xoghayn",
    edRole: "Agaasimaha Fulinta",
    aedRole: "Ku-xigeenka Agaasimaha Fulinta",
    treRole: "Khasnajiga",
    pcRole: "Isku-duwaha Barnaamijyada",
    apcRole: "Kaaliyaha Isku-duwaha Barnaamijyada",
    fcRole: "Isku-duwaha Qoyska & Carruurta",
    spRole: "Afhayeen",

    contactTitle: "Xiriir",
    contactDesc: "Noo sheeg caawimada aad u baahan tahay. Waxaan kuu soo jawaabi doonnaa sida ugu dhakhsaha badan.",
    contactInfoTitle: "Macluumaadka Hay’adda",
    locationLabel: "Goobta:",
    locationValue: "Milwaukee, Wisconsin",
    emailLabel: "Iimayl:",
    phoneLabel: "Telefoon:",
    contactNote: "Beddel iimaylka/telefoonka si ay u noqdaan kuwa rasmiga ah ee hay’adda.",
    formName: "Magaca",
    formEmail: "Iimayl",
    formMessage: "Fariin",
    formBtn: "Dir Fariinta",
    formHint: "Foomkan demo ma dirayo hadda. Haddii aad rabto, waan ku xirin karaa Formspree ama iimaylkaaga.",
    footerSub: "Hay’ad Samafal • Milwaukee, Wisconsin"
  }
};

function setLang(lang){
  document.querySelectorAll("[data-i18n]").forEach(el=>{
    const key = el.getAttribute("data-i18n");
    if(dict[lang] && dict[lang][key]) el.textContent = dict[lang][key];
  });

  const enBtn = document.getElementById("lang-en");
  const soBtn = document.getElementById("lang-so");

  if(enBtn && soBtn){
    enBtn.classList.toggle("active", lang === "en");
    soBtn.classList.toggle("active", lang === "so");
  }

  localStorage.setItem("msbc_lang", lang);
  document.documentElement.lang = (lang === "so") ? "so" : "en";
}

(function init(){
  const yearEl = document.getElementById("year");
  if(yearEl) yearEl.textContent = new Date().getFullYear();

  const enBtn = document.getElementById("lang-en");
  const soBtn = document.getElementById("lang-so");

  if(enBtn) enBtn.addEventListener("click", ()=>setLang("en"));
  if(soBtn) soBtn.addEventListener("click", ()=>setLang("so"));

  setLang(localStorage.getItem("msbc_lang") || "en");
})();
</script>
