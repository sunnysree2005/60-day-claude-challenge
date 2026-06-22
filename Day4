from reportlab.lib.pagesizes import A4
from reportlab.lib import colors
from reportlab.lib.units import mm
from reportlab.platypus import SimpleDocTemplate, Paragraph, Spacer, Table, TableStyle, HRFlowable
from reportlab.lib.styles import ParagraphStyle
from reportlab.lib.enums import TA_CENTER, TA_LEFT, TA_RIGHT
from reportlab.platypus import KeepTogether

W, H = A4

# ── Palette ──────────────────────────────────────────────────────────────
NAVY      = colors.HexColor("#0F172A")
INDIGO    = colors.HexColor("#4F46E5")
INDIGO_LT = colors.HexColor("#EEF2FF")
SLATE     = colors.HexColor("#475569")
SLATE_LT  = colors.HexColor("#F8FAFC")
BORDER    = colors.HexColor("#E2E8F0")
WHITE     = colors.white
GREEN     = colors.HexColor("#059669")
AMBER     = colors.HexColor("#D97706")
RED       = colors.HexColor("#DC2626")
TEAL      = colors.HexColor("#0891B2")
TEAL_LT   = colors.HexColor("#E0F2FE")

# ── Styles ────────────────────────────────────────────────────────────────
def S(name, **kw):
    base = dict(fontName="Helvetica", fontSize=9, leading=13,
                textColor=NAVY, spaceAfter=0, spaceBefore=0)
    base.update(kw)
    return ParagraphStyle(name, **base)

sTitle    = S("title", fontSize=18, fontName="Helvetica-Bold", textColor=WHITE,
              alignment=TA_CENTER, leading=22)
sSub      = S("sub",   fontSize=9,  textColor=colors.HexColor("#C7D2FE"),
              alignment=TA_CENTER, leading=13)
sSecHdr   = S("sechdr", fontSize=8, fontName="Helvetica-Bold", textColor=WHITE,
              alignment=TA_LEFT, leading=10)
sBody     = S("body",  fontSize=7.5, textColor=SLATE, leading=11)
sBold     = S("bold",  fontSize=7.5, fontName="Helvetica-Bold", textColor=NAVY, leading=11)
sSmall    = S("small", fontSize=6.8, textColor=SLATE, leading=10)
sLabel    = S("label", fontSize=6.5, fontName="Helvetica-Bold", textColor=INDIGO, leading=9)
sGreen    = S("green", fontSize=7.5, fontName="Helvetica-Bold", textColor=GREEN, leading=11)
sAmber    = S("amber", fontSize=7.5, fontName="Helvetica-Bold", textColor=AMBER, leading=11)
sRed      = S("red",   fontSize=7.5, fontName="Helvetica-Bold", textColor=RED, leading=11)
sFooter   = S("footer",fontSize=6.5, textColor=colors.HexColor("#94A3B8"),
              alignment=TA_CENTER, leading=9)
sCenter   = S("center",fontSize=7.5, textColor=SLATE, alignment=TA_CENTER, leading=11)

def sec_header(emoji, text):
    return Table(
        [[Paragraph(f"{emoji}  {text}", sSecHdr)]],
        colWidths=[175*mm],
        style=TableStyle([
            ("BACKGROUND", (0,0), (-1,-1), INDIGO),
            ("TOPPADDING",  (0,0), (-1,-1), 4),
            ("BOTTOMPADDING",(0,0),(-1,-1), 4),
            ("LEFTPADDING", (0,0), (-1,-1), 8),
            ("ROUNDEDCORNERS", [4]),
        ])
    )

def card(content_rows, col_widths, bg=SLATE_LT, inner_style=None):
    base = [
        ("BACKGROUND",    (0,0),(-1,-1), bg),
        ("GRID",          (0,0),(-1,-1), 0.4, BORDER),
        ("TOPPADDING",    (0,0),(-1,-1), 4),
        ("BOTTOMPADDING", (0,0),(-1,-1), 4),
        ("LEFTPADDING",   (0,0),(-1,-1), 6),
        ("RIGHTPADDING",  (0,0),(-1,-1), 6),
        ("VALIGN",        (0,0),(-1,-1), "TOP"),
        ("ROWBACKGROUNDS",(0,0),(-1,-1), [WHITE, SLATE_LT]),
    ]
    if inner_style:
        base += inner_style
    return Table(content_rows, colWidths=col_widths,
                 style=TableStyle(base))

# ── Document ──────────────────────────────────────────────────────────────
doc = SimpleDocTemplate(
    "/mnt/user-data/outputs/AI_Engineer_Roadmap.pdf",
    pagesize=A4,
    leftMargin=12*mm, rightMargin=12*mm,
    topMargin=10*mm,  bottomMargin=8*mm,
)

story = []
full = 186*mm   # usable width

# ═══════════════════════════════════════════════════════════════════
# HEADER BANNER
# ═══════════════════════════════════════════════════════════════════
header_data = [[
    Paragraph("🚀  AI Engineer Career Roadmap", sTitle),
    Paragraph("Student  ·  Python / JS / ML / Web Dev  ·  3-Month Sprint", sSub),
]]
header = Table(
    [[Paragraph("🚀  AI Engineer Career Roadmap", sTitle)],
     [Paragraph("Student  ·  Python / JS / ML / Web Dev  ·  3-Month Sprint", sSub)]],
    colWidths=[full],
    style=TableStyle([
        ("BACKGROUND",    (0,0),(-1,-1), NAVY),
        ("TOPPADDING",    (0,0),(-1,-1), 8),
        ("BOTTOMPADDING", (0,0),(-1,-1), 8),
        ("LEFTPADDING",   (0,0),(-1,-1), 10),
        ("ROUNDEDCORNERS",[6]),
    ])
)
story.append(header)
story.append(Spacer(1, 3*mm))

# ═══════════════════════════════════════════════════════════════════
# ROW 1 — Current Position  |  Target Goal
# ═══════════════════════════════════════════════════════════════════
pos_data = [
    [Paragraph("🎯  CURRENT POSITION", sLabel)],
    [Paragraph("<b>Student</b> with strong technical foundations", sBold)],
    [Paragraph("✅ Python  ✅ JavaScript  ✅ ML basics  ✅ Web Dev", sBody)],
    [Paragraph("Strong: coding fundamentals, data intuition, frontend skills", sSmall)],
]
goal_data = [
    [Paragraph("⚡  TARGET GOAL", sLabel)],
    [Paragraph("<b>AI Engineer</b> — employed or freelancing", sBold)],
    [Paragraph("Build & deploy production-grade AI applications", sBody)],
    [Paragraph("Timeline: <b>3 months</b>  ·  Deadline: ~Sep 22, 2026", sSmall)],
]

col2 = full / 2 - 1.5*mm
row1 = Table(
    [[
        Table(pos_data, colWidths=[col2], style=TableStyle([
            ("BACKGROUND",   (0,0),(-1,-1), INDIGO_LT),
            ("TOPPADDING",   (0,0),(-1,-1), 4),
            ("BOTTOMPADDING",(0,0),(-1,-1), 3),
            ("LEFTPADDING",  (0,0),(-1,-1), 7),
            ("RIGHTPADDING", (0,0),(-1,-1), 7),
            ("GRID",         (0,0),(-1,-1), 0, colors.transparent),
            ("LINEBEFORE",   (0,0),(0,-1), 2.5, INDIGO),
        ])),
        Table(goal_data, colWidths=[col2], style=TableStyle([
            ("BACKGROUND",   (0,0),(-1,-1), colors.HexColor("#ECFDF5")),
            ("TOPPADDING",   (0,0),(-1,-1), 4),
            ("BOTTOMPADDING",(0,0),(-1,-1), 3),
            ("LEFTPADDING",  (0,0),(-1,-1), 7),
            ("RIGHTPADDING", (0,0),(-1,-1), 7),
            ("GRID",         (0,0),(-1,-1), 0, colors.transparent),
            ("LINEBEFORE",   (0,0),(0,-1), 2.5, GREEN),
        ])),
    ]],
    colWidths=[col2+1.5*mm, col2+1.5*mm],
    style=TableStyle([
        ("TOPPADDING",   (0,0),(-1,-1), 0),
        ("BOTTOMPADDING",(0,0),(-1,-1), 0),
        ("LEFTPADDING",  (0,0),(-1,-1), 0),
        ("RIGHTPADDING", (0,0),(-1,-1), 0),
        ("COLPADDING",   (0,0),(-1,-1), 1.5),
    ])
)
story.append(row1)
story.append(Spacer(1, 2.5*mm))

# ═══════════════════════════════════════════════════════════════════
# SKILL GAP ANALYSIS
# ═══════════════════════════════════════════════════════════════════
story.append(sec_header("📈", "SKILL GAP ANALYSIS"))
story.append(Spacer(1, 1.5*mm))

gap_rows = [
    [Paragraph("Skill Area", sBold), Paragraph("Current Level", sBold),
     Paragraph("Required Level", sBold), Paragraph("Gap", sBold), Paragraph("Priority", sBold)],
    [Paragraph("LLM APIs (OpenAI, Anthropic)", sBody), Paragraph("None", sRed),
     Paragraph("Proficient", sBody), Paragraph("HIGH", sRed), Paragraph("Week 1", sGreen)],
    [Paragraph("LangChain / LlamaIndex", sBody), Paragraph("None", sRed),
     Paragraph("Working knowledge", sBody), Paragraph("HIGH", sRed), Paragraph("Week 2", sGreen)],
    [Paragraph("Vector DBs (Pinecone, Chroma)", sBody), Paragraph("None", sRed),
     Paragraph("Basic usage", sBody), Paragraph("HIGH", sRed), Paragraph("Week 2", sGreen)],
    [Paragraph("FastAPI / API deployment", sBody), Paragraph("Beginner", sAmber),
     Paragraph("Intermediate", sBody), Paragraph("MED", sAmber), Paragraph("Week 3", sGreen)],
    [Paragraph("Prompt Engineering", sBody), Paragraph("None", sRed),
     Paragraph("Proficient", sBody), Paragraph("HIGH", sRed), Paragraph("Week 1", sGreen)],
    [Paragraph("Docker / Cloud (AWS/GCP)", sBody), Paragraph("Beginner", sAmber),
     Paragraph("Basic deploy", sBody), Paragraph("MED", sAmber), Paragraph("Month 2", sGreen)],
    [Paragraph("RAG Architecture", sBody), Paragraph("None", sRed),
     Paragraph("Implement from scratch", sBody), Paragraph("HIGH", sRed), Paragraph("Month 2", sGreen)],
    [Paragraph("Python (ML/AI libs)", sBody), Paragraph("Good ✅", sGreen),
     Paragraph("Strong", sBody), Paragraph("LOW", sGreen), Paragraph("Ongoing", sBody)],
]
gap_cols = [52*mm, 28*mm, 36*mm, 18*mm, 22*mm]
gap_table = Table(gap_rows, colWidths=gap_cols, style=TableStyle([
    ("BACKGROUND",   (0,0),(-1,0), NAVY),
    ("TEXTCOLOR",    (0,0),(-1,0), WHITE),
    ("FONTNAME",     (0,0),(-1,0), "Helvetica-Bold"),
    ("FONTSIZE",     (0,0),(-1,-1), 7.5),
    ("GRID",         (0,0),(-1,-1), 0.3, BORDER),
    ("ROWBACKGROUNDS",(0,1),(-1,-1), [WHITE, SLATE_LT]),
    ("TOPPADDING",   (0,0),(-1,-1), 3),
    ("BOTTOMPADDING",(0,0),(-1,-1), 3),
    ("LEFTPADDING",  (0,0),(-1,-1), 5),
    ("VALIGN",       (0,0),(-1,-1), "MIDDLE"),
]))
story.append(gap_table)
story.append(Spacer(1, 2.5*mm))

# ═══════════════════════════════════════════════════════════════════
# LEARNING PLAN  |  PROJECTS
# ═══════════════════════════════════════════════════════════════════
story.append(sec_header("🛠", "RECOMMENDED LEARNING PLAN  +  💼 SUGGESTED PROJECTS"))
story.append(Spacer(1, 1.5*mm))

learn_rows = [
    [Paragraph("Phase", sBold), Paragraph("Focus", sBold), Paragraph("Resources", sBold)],
    [Paragraph("Month 1\nWeeks 1–2", sSmall),
     Paragraph("<b>LLM Foundations</b>\nPrompt engineering, OpenAI/Anthropic APIs,\ntoken costs, function calling", sBody),
     Paragraph("fast.ai Practical LLMs\nAnthropicDocs / OpenAI Cookbook\nDeepLearning.AI short courses", sSmall)],
    [Paragraph("Month 1\nWeeks 3–4", sSmall),
     Paragraph("<b>AI App Stack</b>\nLangChain, LlamaIndex,\nChroma/Pinecone, RAG basics", sBody),
     Paragraph("LangChain docs + tutorials\nYT: Greg Kamradt RAG series\nPinecone learning center", sSmall)],
    [Paragraph("Month 2", sSmall),
     Paragraph("<b>Build & Deploy</b>\nFastAPI backends, Docker,\nVercel/Railway, Streamlit UIs", sBody),
     Paragraph("Full Stack FastAPI template\nDocker in 100 Seconds\nStreamlit docs", sSmall)],
    [Paragraph("Month 3", sSmall),
     Paragraph("<b>Polish & Ship</b>\nPortfolio projects, OSS contributions,\nLinkedIn content, job applications", sBody),
     Paragraph("GitHub open issues (good-first-issue)\nLinkedIn Creator Mode\nLinkedin AI job alerts", sSmall)],
]
learn_cols = [22*mm, 65*mm, 50*mm]
learn_table = Table(learn_rows, colWidths=learn_cols, style=TableStyle([
    ("BACKGROUND",   (0,0),(-1,0), colors.HexColor("#1E293B")),
    ("TEXTCOLOR",    (0,0),(-1,0), WHITE),
    ("FONTNAME",     (0,0),(-1,0), "Helvetica-Bold"),
    ("FONTSIZE",     (0,0),(-1,-1), 7.5),
    ("GRID",         (0,0),(-1,-1), 0.3, BORDER),
    ("ROWBACKGROUNDS",(0,1),(-1,-1), [WHITE, SLATE_LT]),
    ("TOPPADDING",   (0,0),(-1,-1), 4),
    ("BOTTOMPADDING",(0,0),(-1,-1), 4),
    ("LEFTPADDING",  (0,0),(-1,-1), 5),
    ("VALIGN",       (0,0),(-1,-1), "TOP"),
    ("LINEBEFORE",   (0,1),(0,-1), 2.5, INDIGO),
]))

proj_rows = [
    [Paragraph("Project", sBold), Paragraph("Stack & Impact", sBold)],
    [Paragraph("AI Chat Assistant", sBody),
     Paragraph("OpenAI API + LangChain + Streamlit. Shows LLM API mastery.", sSmall)],
    [Paragraph("RAG Doc Q&A App", sBody),
     Paragraph("LlamaIndex + Chroma + FastAPI. Upload PDF, ask questions.", sSmall)],
    [Paragraph("AI Image Caption Bot", sBody),
     Paragraph("Vision API + Python + deployed on Railway. Multimodal AI.", sSmall)],
    [Paragraph("Personal AI Agent", sBody),
     Paragraph("LangChain agents + tools + memory. Autonomous task runner.", sSmall)],
]
proj_cols = [full - 137*mm - 1*mm]   # we'll do it as a side-by-side below

# Two-column: learning (left) + projects (right)
proj_right = [22*mm, 25*mm]
proj_table = Table(proj_rows, colWidths=[28*mm, 18*mm], style=TableStyle([
    ("BACKGROUND",   (0,0),(-1,0), colors.HexColor("#1E293B")),
    ("TEXTCOLOR",    (0,0),(-1,0), WHITE),
    ("FONTNAME",     (0,0),(-1,0), "Helvetica-Bold"),
    ("FONTSIZE",     (0,0),(-1,-1), 7.5),
    ("GRID",         (0,0),(-1,-1), 0.3, BORDER),
    ("ROWBACKGROUNDS",(0,1),(-1,-1), [WHITE, SLATE_LT]),
    ("TOPPADDING",   (0,0),(-1,-1), 3),
    ("BOTTOMPADDING",(0,0),(-1,-1), 3),
    ("LEFTPADDING",  (0,0),(-1,-1), 5),
    ("VALIGN",       (0,0),(-1,-1), "TOP"),
    ("LINEBEFORE",   (0,1),(0,-1), 2.5, TEAL),
]))

lp_width = 140*mm
pj_width = full - lp_width - 2*mm

learn_proj = Table([[learn_table, proj_table]],
    colWidths=[lp_width+1*mm, pj_width+1*mm],
    style=TableStyle([
        ("TOPPADDING",   (0,0),(-1,-1), 0),
        ("BOTTOMPADDING",(0,0),(-1,-1), 0),
        ("LEFTPADDING",  (0,0),(-1,-1), 0),
        ("RIGHTPADDING", (0,0),(-1,-1), 0),
        ("COLPADDING",   (0,0),(-1,-1), 1),
    ]))
story.append(learn_proj)
story.append(Spacer(1, 2.5*mm))

# ═══════════════════════════════════════════════════════════════════
# NETWORKING  |  NEXT ACTIONS
# ═══════════════════════════════════════════════════════════════════
story.append(sec_header("🌐", "NETWORKING STRATEGY  +  ⚡ IMMEDIATE NEXT ACTIONS"))
story.append(Spacer(1, 1.5*mm))

net_rows = [
    [Paragraph("Channel", sBold), Paragraph("Action", sBold)],
    [Paragraph("LinkedIn", sBody), Paragraph("Post 1 project update/week. Connect with AI engineers. Comment on AI leader posts daily.", sSmall)],
    [Paragraph("GitHub", sBody), Paragraph("Daily commits. Star/fork trending AI repos. Open issues & submit small PRs.", sSmall)],
    [Paragraph("Discord/Slack", sBody), Paragraph("Join Hugging Face, LangChain, OpenAI communities. Answer newbie questions.", sSmall)],
    [Paragraph("Twitter/X", sBody), Paragraph("Share build-in-public progress. Tag creators when using their tutorials.", sSmall)],
    [Paragraph("Cold Outreach", sBody), Paragraph("DM 3 AI engineers/week on LinkedIn with a specific, genuine question.", sSmall)],
]
net_cols = [25*mm, 62*mm]
net_table = Table(net_rows, colWidths=net_cols, style=TableStyle([
    ("BACKGROUND",   (0,0),(-1,0), colors.HexColor("#1E293B")),
    ("TEXTCOLOR",    (0,0),(-1,0), WHITE),
    ("FONTNAME",     (0,0),(-1,0), "Helvetica-Bold"),
    ("FONTSIZE",     (0,0),(-1,-1), 7.5),
    ("GRID",         (0,0),(-1,-1), 0.3, BORDER),
    ("ROWBACKGROUNDS",(0,1),(-1,-1), [WHITE, SLATE_LT]),
    ("TOPPADDING",   (0,0),(-1,-1), 3),
    ("BOTTOMPADDING",(0,0),(-1,-1), 3),
    ("LEFTPADDING",  (0,0),(-1,-1), 5),
    ("VALIGN",       (0,0),(-1,-1), "TOP"),
    ("LINEBEFORE",   (0,1),(0,-1), 2.5, TEAL),
]))

action_items = [
    "Get an OpenAI API key & run your first completion call today",
    "Complete DeepLearning.AI 'ChatGPT Prompt Engineering' (free, 1hr)",
    "Set up a GitHub repo: 'ai-engineer-journey' — document everything",
    "Activate LinkedIn Creator Mode + write a 'starting my AI journey' post",
    "Join the LangChain Discord server",
    "Build 'Hello World' chatbot with Streamlit by end of Week 1",
]
act_rows = [[Paragraph(f"{'0'+str(i+1) if i<9 else str(i+1)}.", S('n', fontSize=7.5, fontName='Helvetica-Bold', textColor=INDIGO, leading=11)),
             Paragraph(a, sBody)] for i,a in enumerate(action_items)]
act_table = Table(act_rows, colWidths=[8*mm, 85*mm], style=TableStyle([
    ("TOPPADDING",   (0,0),(-1,-1), 2),
    ("BOTTOMPADDING",(0,0),(-1,-1), 2),
    ("LEFTPADDING",  (0,0),(-1,-1), 3),
    ("RIGHTPADDING", (0,0),(-1,-1), 3),
    ("ROWBACKGROUNDS",(0,0),(-1,-1), [WHITE, INDIGO_LT]),
    ("GRID",         (0,0),(-1,-1), 0.3, BORDER),
    ("VALIGN",       (0,0),(-1,-1), "TOP"),
]))

net_act_width = 90*mm
act_width = full - net_act_width - 2*mm
net_act = Table([[net_table, act_table]],
    colWidths=[net_act_width+1*mm, act_width+1*mm],
    style=TableStyle([
        ("TOPPADDING",   (0,0),(-1,-1), 0),
        ("BOTTOMPADDING",(0,0),(-1,-1), 0),
        ("LEFTPADDING",  (0,0),(-1,-1), 0),
        ("RIGHTPADDING", (0,0),(-1,-1), 0),
        ("COLPADDING",   (0,0),(-1,-1), 1),
    ]))
story.append(net_act)
story.append(Spacer(1, 2.5*mm))

# ═══════════════════════════════════════════════════════════════════
# MONTHLY MILESTONES
# ═══════════════════════════════════════════════════════════════════
story.append(sec_header("📅", "MONTHLY MILESTONES"))
story.append(Spacer(1, 1.5*mm))

col3 = full / 3 - 1*mm

def milestone_card(month, color, items):
    rows = [[Paragraph(month, S('mh', fontSize=8, fontName='Helvetica-Bold', textColor=WHITE, leading=10, alignment=TA_CENTER))]]
    for item in items:
        rows.append([Paragraph(f"▸  {item}", S('mi', fontSize=7, textColor=SLATE, leading=10))])
    return Table(rows, colWidths=[col3], style=TableStyle([
        ("BACKGROUND",   (0,0),(-1,0), color),
        ("BACKGROUND",   (0,1),(-1,-1), WHITE),
        ("GRID",         (0,0),(-1,-1), 0.3, BORDER),
        ("TOPPADDING",   (0,0),(-1,-1), 4),
        ("BOTTOMPADDING",(0,0),(-1,-1), 3),
        ("LEFTPADDING",  (0,0),(-1,-1), 6),
        ("ROWBACKGROUNDS",(0,1),(-1,-1), [WHITE, SLATE_LT]),
    ]))

m1 = milestone_card("Month 1  —  Foundation Sprint", INDIGO, [
    "Finish 2 DeepLearning.AI AI courses",
    "Call OpenAI, Anthropic & Google APIs",
    "Build & deploy a basic chatbot (Streamlit)",
    "Push all code to GitHub with READMEs",
    "Post 4 LinkedIn updates about progress",
])
m2 = milestone_card("Month 2  —  Build & Deploy", TEAL, [
    "Complete a RAG app (PDF Q&A)",
    "Deploy one project on Railway or Vercel",
    "Learn Docker basics; containerize one app",
    "Contribute to 1 open-source AI repo",
    "Resume draft with 2 AI projects listed",
])
m3 = milestone_card("Month 3  —  Hired Mode", GREEN, [
    "Portfolio site live with 3+ AI projects",
    "Apply to 20+ AI Engineer roles/internships",
    "Complete 5 technical interviews",
    "LinkedIn: 500+ connections in AI space",
    "Land offer / freelance client by Month 3",
])

milestones = Table([[m1, m2, m3]],
    colWidths=[col3+1*mm, col3+1*mm, col3+1*mm],
    style=TableStyle([
        ("TOPPADDING",   (0,0),(-1,-1), 0),
        ("BOTTOMPADDING",(0,0),(-1,-1), 0),
        ("LEFTPADDING",  (0,0),(-1,-1), 0),
        ("RIGHTPADDING", (0,0),(-1,-1), 0),
        ("COLPADDING",   (0,0),(-1,-1), 1),
    ]))
story.append(milestones)
story.append(Spacer(1, 3*mm))

# ═══════════════════════════════════════════════════════════════════
# FOOTER
# ═══════════════════════════════════════════════════════════════════
story.append(HRFlowable(width=full, thickness=0.5, color=BORDER))
story.append(Spacer(1, 1.5*mm))
story.append(Paragraph(
    "Generated using Chain-of-Thought Reasoning  ·  AI Career Strategist  ·  Claude by Anthropic  ·  June 2026",
    sFooter
))

doc.build(story)
print("Done!")
