# Reading Notes for `refs.bib`

Tai lieu nay tong hop ghi chu doc paper cho toan bo danh sach trong `content/refs.bib`.

Ghi chu ve cach doc:
- Uu tien nguon goc chinh thong: arXiv, OpenReview, ACL Anthology, CVPR/TheCVF, NeurIPS Proceedings, project page chinh thuc, technical report chinh thuc.
- Cac paper sat de tai cua ban (grounded VideoQA, video temporal grounding, long-video reasoning) duoc doc ky hon.
- Mot vai entry ma trong phien lam viec nay toi khong mo duoc full primary page thi toi van tom tat o muc best-effort dua tren abstract / project page / doi / venue; nhung toi danh dau ro.
- Noi dung ben duoi la paraphrase, khong copy nguyen van abstract.

---

## 1. `wu2025survey_vtg_mllm`
**Title:** A Survey on Video Temporal Grounding with Multimodal Large Language Model  
**Source:** https://arxiv.org/abs/2508.10922

- Day la survey rat trung tam voi de tai cua ban vi no nhin toan bo bai toan video temporal grounding (VTG) trong boi canh MLLM.
- Diem manh cua bai la mot taxonomy 3 chieu: vai tro cua MLLM trong pipeline, training paradigm, va cach xu ly video feature.
- Bai khong chi gom moment retrieval thong thuong ma con dat grounded VideoQA, highlight detection, dense captioning vao cung mot buc tranh nghien cuu.
- Gia tri thuc te voi paper cua ban: no giup dat bai toan cua ban vao dung vi tri "multiple-choice grounded VideoQA can retrieval-friendly queries", tu do lam noi bat dong gop cua Refiner va Selector.
- Neu ban can viet Related Work rat chat, day la paper nen de trich y "VTG-MLLM dang vuot len nho generalization, zero-shot, multi-task, multi-domain".

## 2. `tang2025video`
**Title:** Video Understanding with Large Language Models: A Survey  
**Source:** https://arxiv.org/abs/2312.17432

- Survey nay rong hon paper tren: no bao quat toan canh Vid-LLM thay vi chi VTG.
- Y tuong trung tam la xem LLM nhu thanh phan hop nhat cho suy luan video, gom cac kieu ket hop analyzer, embedder, va LLM.
- Bai nhan manh cac muc reasoning tu tong quat den temporal va spatiotemporal, dong thoi ban ve benchmark, hallucination, va kha nang mo rong sang ung dung thuc te.
- Relevance voi bai cua ban: no cho phep ban dat Grounding Time nhu mot he thong nam trong lan song "language-centric video understanding", nhung dong thoi cho thay bai cua ban khac o cho no can evidence grounding ro rang.

## 3. `xiao2025videoqa`
**Title:** VideoQA in the Era of LLMs: An Empirical Study  
**Source:** https://arxiv.org/abs/2408.04223

- Bai nay khong de xuat mot model cu the; no la bai phan tich hanh vi cua Video-LLMs tren VideoQA.
- Muc tieu la chi ra success mode va failure mode thay vi chi so sanh leaderboard.
- Tu abstract va cac thong tin benchmark, bai nghien cuu tren nhieu bo du lieu MCQA va open-ended QA, trong do co NExT-GQA, EgoSchema, Perception Test, MSVD-QA, ActivityNet-QA.
- Gia tri cua bai la thong diep: Video-LLMs da manh, nhung diem yeu van tap trung o temporal reasoning, grounding faithfulness, va kha nang tranh reliance vao language bias.
- Voi paper cua ban, day la mot nguon rat hop ly de backing cho motivation "answer accuracy alone is not enough".

---

## 4. `qin2025question_answering_dense_video_events`
**Title:** Question-Answering Dense Video Events  
**Source:** https://arxiv.org/abs/2409.04388

- Bai nay mo ra mot setting kho hon VideoQA thong thuong: long video co nhieu su kien dam dac, nhieu event xen nhau, va model phai vua answer vua grounding.
- Dong gop du lieu la **DeVE-QA**, gom 78K cau hoi, 26K events, tren 10.6K long videos.
- Dong gop phuong phap la **DeVi**, mot huong training-free gom hierarchical captioning, temporal event memory, va self-consistency checking.
- Thong diep quan trong: model manh o single-event video chua chac xu ly tot dense-event long video.
- Relevance voi bai cua ban: no ung ho y tuong tach bo phan "lay bang chung" va "suy luan tren bang chung", dac biet trong setting nhieu event va temporal complexity cao.

## 5. `yan2025tpo`
**Title:** Task Preference Optimization: Improving Multimodal Large Language Models with Vision Task Alignment  
**Source:** https://arxiv.org/abs/2412.19326

- Bai nay tap trung vao van de rat thuc dung: MLLM tong quat thuong yeu o cac tac vu visual fine-grained.
- TPO dua vao **learnable task tokens** de noi MLLM voi nhieu task-specific heads, va huan luyen multi-task de task skills bo sung lan nhau.
- Diem hay cua bai la no co gang cai thien visual precision ma khong lam mat nang luc multimodal tong quat.
- Voi bai cua ban, TPO giai thich vi sao mot backbone duoc "align task-wise" co the co grounding tot hon khi lam retriever/selector/generator.

## 6. `zhao2025videoexpert`
**Title:** VideoExpert: Augmented LLM for Temporal-Sensitive Video Understanding  
**Source:** https://arxiv.org/abs/2504.07519  
**Confidence:** best-effort; source URL duoc suy ra tu primary-link snippet trong qua trinh tim kiem.

- Huong chinh cua bai la lam cho MLLM nhay cam hon voi dong hoc theo thoi gian, thay vi chi nhin video nhu mot tap frame text-friendly.
- Theo project/review signal da doc, bai su dung kieu thiet ke song song giua **temporal expert** va **spatial expert**, kem theo dau ra localization.
- Gia tri cua bai nam o thong diep: temporal sensitivity can mot inductive bias rieng, khong nen chi dua vao general captioning ability.
- Relevance voi bai cua ban: rat gan voi nhan dinh cua ban rang retriever/selector nen duoc toi uu theo vai tro rieng, thay vi de mot model tong quat lam tat ca.

## 7. `wang2025grounded_videollm`
**Title:** Grounded-VideoLLM: Sharpening Fine-grained Temporal Grounding in Video Large Language Models  
**Source:** https://aclanthology.org/2025.findings-emnlp.50/

- Muc tieu la sua diem yeu cua Video-LLM o **fine-grained temporal grounding**.
- Dong gop ky thuat chinh:
- Two-stream encoder de vua model quan he lien frame, vua giu chi tiet ben trong tung frame.
- Discrete temporal tokens co enrich bang structured time knowledge.
- Multi-stage training tu caption task den grounding task de hoc temporal alignment dan dan.
- Bai con tao grounded VideoQA data bang automatic annotation pipeline de tang temporal reasoning.
- Voi paper cua ban, Grounded-VideoLLM la baseline/related work rat sat: no manh o temporal grounding, nhung chua giai quyet truc dien bai toan raw answer option khong phai retrieval-friendly query.

## 8. `yu2023sevila`
**Title:** Self-Chained Image-Language Model for Video Localization and Question Answering  
**Source:** https://arxiv.org/abs/2305.06988

- SeViLA la mot paper rat quan trong vi no som dua ra y tuong **tach localization va answering**.
- No dung mot image-language model duy nhat (BLIP-2) nhung self-chain qua nhieu buoc de tim keyframes / localize roi moi QA.
- Bai cho thay parameter-efficient adaptation van co the dat ket qua manh neu decomposition hop ly.
- Relevance: paper cua ban cung theo tinh than decomposition, nhung di xa hon bang cach them Refiner va Selector thay vi chi localization-answering.

## 9. `huang2024vtimellm`
**Title:** VTimeLLM: Empower LLM to Grasp Video Moments  
**Source:** https://openaccess.thecvf.com/content/CVPR2024/html/Huang_VTimeLLM_Empower_LLM_to_Grasp_Video_Moments_CVPR_2024_paper.html

- Van de bai nham toi la Video LLM chi mo ta dai y video, nhung khong nam duoc **ranh gioi start-end** cua su kien.
- Giai phap la **boundary-aware three-stage training**:
- Alignment voi image-text.
- Multiple-event videos de hoc boundary awareness.
- High-quality video instruction tuning de nang kha nang temporal understanding va instruction following.
- Ket qua cua bai nhan manh rang temporal comprehension tot hon giup ca temporal grounding lan video dialogue.
- Relevance: retriever trong bai cua ban thuc chat dang can chinh loai moment understanding ma VTimeLLM muon giai quyet.

## 10. `huang2024lita`
**Title:** LITA: Language Instructed Temporal-Localization Assistant  
**Source:** https://arxiv.org/abs/2403.19046

- LITA bat dau tu mot nhan xet cuc ky dung: video-LLM biet "what" nhung yeu o "when".
- Bai chi ra 3 nut that: time representation, architecture, va data.
- De giai quyet, no dua vao:
- **time tokens** ma hoa thoi gian tuong doi trong video.
- **SlowFast tokens** de giu thong tin temporal o nhieu resolution.
- training emphasis vao temporal localization data.
- Bai con de xuat task/dataset **Reasoning Temporal Localization (RTL)** va ActivityNet-RTL.
- Relevance: phan Refiner cua ban xu ly query, con LITA xu ly representation/time-awareness; hai huong nay bo sung cho nhau.

## 11. `liu2025videomind`
**Title:** VideoMind: A Chain-of-LoRA Agent for Temporal-Grounded Video Reasoning  
**Source:** https://videomind.github.io/

- Day la work gan nhat voi bai cua ban ve mat triet ly.
- Bai xac dinh 4 nang luc can co cho grounded video reasoning: planner, grounder, verifier, answerer.
- Dong gop dac sac la **Chain-of-LoRA**: mot base model chung, nhieu LoRA adapters cho role switching; vua hieu qua, vua giu duoc role specialization.
- Phan **verifier** cua VideoMind la nguon cam hung truc tiep cho Selector cua ban.
- Relevance: paper cua ban co the duoc xem nhu mot agentic-style pipeline duoc don gian hoa va dieu chinh theo bai toan multiple-choice grounded VideoQA, trong do Refiner la diem khac biet rat ro.

## 12. `wang2024hawkeye`
**Title:** HawkEye: Training Video-Text LLMs for Grounding Text in Videos  
**Source:** https://arxiv.org/abs/2403.10228

- HawkEye la mot trong cac bai dau tien dat trong tam vao grounding text query vao video theo kieu text-to-text.
- Dong gop chinh:
- InternVid-G, mot corpus quy mo lon co segment-level captions va negative spans.
- Time-aware training objectives.
- Cach bieu dien doan video coarse-grained de LLM hoc timestamp de hon.
- Bai nay quan trong vi no cho thay muon grounding tot thi can data va objective phu hop, khong the chi dua vao generic instruction tuning.

## 13. `ren2024timechat`
**Title:** TimeChat: A Time-Sensitive Multimodal Large Language Model for Long Video Understanding  
**Source:** https://arxiv.org/abs/2312.02051

- Bai nham toi long video understanding va temporal sensitivity.
- Hai thanh phan noi bat:
- **timestamp-aware frame encoder** de gan visual content voi moc thoi gian cua frame.
- **sliding video Q-Former** de sinh chuoi video tokens co do dai phu hop voi video do dai khac nhau.
- Bai con tao instruction-tuning set 125K mau, 6 tasks.
- Ket qua khang dinh zero-shot temporal localization va reasoning tot tren dense captioning, grounding, highlight detection.
- Relevance: no cung logic voi bai cua ban la "muon answer dung phai temporalize du thong tin vao".

## 14. `yang2022zero`
**Title:** Zero-Shot Video Question Answering via Frozen Bidirectional Language Models  
**Source:** https://proceedings.neurips.cc/paper_files/paper/2022/hash/00d1f03b87a401b1c7957e0cc785d0bc-Abstract-Conference.html

- FrozenBiLM la baseline quan trong trong VideoQA.
- Idea la khong fine-tune toan bo LLM ma giu frozen bidirectional LM, them it trainable modules de ket noi visual input.
- Luc inference, bai giai VideoQA bang **masked language modeling**: phan can doan la answer text.
- Bai cho thay frozen BiLM co the la lua chon manh va re hon cac framework dua tren autoregressive LM.
- Relevance: ve mat lich su, no la mot moc quan trong truoc khi cong dong chuyen manh sang grounded VideoQA va temporal reasoning.

---

## 15. `kahatapitiya2025language`
**Title:** Language Repository for Long Video Understanding  
**Source:** https://aclanthology.org/2025.findings-acl.294/

- LangRepo la huong tiep can text-centric cho long video.
- Bai quan sat rang LLM co context dai nhung chat luong xu ly thong tin giam dan khi input qua dai.
- Giai phap la mot **repository bang ngon ngu** duoc cap nhat lap di lap lai tren multi-scale video chunks.
- He thong co read/write operations de cat bo trung lap va trich xuat thong tin theo nhieu thang thoi gian.
- Relevance: neu bai cua ban sau nay mo rong sang long-form video, LangRepo la mot huong rat hop cho memory / external textual evidence bank.

## 16. `qian2024streaming`
**Title:** Streaming Long Video Understanding with Large Language Models  
**Source:** https://arxiv.org/abs/2405.16009

- VideoStreaming nham den bai toan engineering rat kho: lam sao xu ly video rat dai ma khong no token cost.
- Bai dua vao streaming encoding va co che chon memory thich nghi de giu so luong video tokens gan nhu hang so.
- Huong nay dac biet quan trong cho deployment hoac cho cac bai toan long-form.
- Relevance: voi bai cua ban, no la huong bo tro o lop ha tang. Ban giai quyet quality / grounding, con VideoStreaming giai quyet scalability.

## 17. `zhang2024simple`
**Title:** A Simple LLM Framework for Long-Range Video Question-Answering  
**Source:** https://aclanthology.org/2024.emnlp-main.1209/

- LLoVi la paper rat hay vi rat "pragmatic": dung short-term visual captioner de cat video thanh nhieu mo ta ngan, roi de LLM suy luan o lop ngon ngu.
- Bai co them **multi-round summarization prompt**: tom tat captions nhieu vong truoc khi answer.
- Ket qua rat tot tren EgoSchema, NExT-QA, IntentQA, va ca NExT-GQA.
- Thong diep lon cua bai: khong nhat thiet phai dung architecture phuc tap; neu decomposition va prompt design tot, LLM co the xu ly long-range reasoning hieu qua.
- Relevance: rat gan tư duy bai cua ban, nhung bai cua ban them hard grounding components (Retriever, Selector) thay vi chi caption -> summarize -> answer.

---

## 18. `xu2024vtg`
**Title:** VTG-GPT: Tuning-Free Zero-Shot Video Temporal Grounding with GPT  
**Source:** https://www.mdpi.com/2076-3417/14/5/1894

- Bai nay theo duong **training-free / zero-shot VTG**.
- Pipeline chinh:
- Query debiasing bang Baichuan2.
- Image captioning bang MiniGPT-v2 de bien visual thanh text sach hon.
- Proposal generator + post-processing de tim temporal span.
- Diem rat dang chu y voi bai cua ban: no cung dung y tuong **rewrite query** truoc khi grounding, nhung cho truy van text query thong thuong; bai cua ban chuyen y tuong do sang **answer-aware query refinement**.
- Day la related work quan trong de bao ve phan Refiner.

## 19. `chen2024timemarker`
**Title:** TimeMarker: A Versatile Video-LLM for Long and Short Video Understanding with Superior Temporal Localization Ability  
**Source:** https://arxiv.org/abs/2411.18211

- Muc tieu cua TimeMarker la dung mot Video-LLM cho ca short va long video ma van giu localization manh.
- Bai de xuat:
- **Temporal Separator Tokens** de danh dau thong tin temporal ro hon.
- **AnyLength mechanism** de dynamic sampling va token merging theo do dai video.
- Su dung tap du lieu temporal phong phu, chuyen doi them tu action detection / segmentation / grounding sang QA dang temporal.
- Relevance: paper nay la minh hoa ro cho xu huong "temporal localization capability must be built into both architecture and data recipe".

## 20. `xu2025zero`
**Title:** Zero-shot Video Moment Retrieval via Off-the-shelf Multimodal Large Language Models  
**Source:** AAAI 2025; trong phien nay toi chi thu thap duoc thong tin tu abstract-duoc-trich-dan qua secondary signal, khong mo duoc primary venue page.  
**Confidence:** best-effort

- Theo thong tin truy xuat duoc, bai de xuat mot pipeline zero-shot cho video moment retrieval bang MLLM off-the-shelf.
- Tin hieu abstract cho thay bai khai thac **query rewriting / correction**, **candidate span generation**, va **span scoring / selection** bang nhieu model co san.
- Gia tri cua bai la cho thay even khong fine-tune, MLLM da co prior temporal reasoning du de xay dung mot retrieval pipeline.
- Relevance: y tuong "query phai duoc viet lai cho retrieval than thien hon" rat gan voi Refiner trong bai cua ban.

## 21. `qu2024chatvtg`
**Title:** ChatVTG: Video Temporal Grounding via Chat with Video Dialogue Large Language Models  
**Source:** https://openaccess.thecvf.com/content/CVPR2024W/PVUW/html/Qu_ChatVTG_Video_Temporal_Grounding_via_Chat_with_Video_Dialogue_Large_CVPRW_2024_paper.html

- ChatVTG de xuat zero-shot VTG bang video dialogue LLM.
- He thong tao **multi-granularity segment captions**, so khop voi query de coarse grounding, roi dung **moment refinement** de fine grounding.
- Diem hay la no khong phu thuoc annotation paired data cho chinh bai toan VTG.
- Relevance: giong bai cua ban o cho retrieval khoang thoi gian duoc xem la mot bai toan su dung language-mediated evidence rather than end-to-end direct classification.

## 22. `zeng2024timesuite`
**Title:** TimeSuite: Improving MLLMs for Long Video Understanding via Grounded Tuning  
**Source:** https://proceedings.iclr.cc/paper_files/paper/2025/hash/5e8309c9ca683e11672e3dbcd4b87776-Abstract-Conference.html

- TimeSuite nham den bai toan adapt MLLM tu short-form sang long-form.
- Bai de xuat **VideoChat-T** voi token shuffling de nen long video tokens va **TAPE** (Temporal Adaptive Position Encoding) de tang temporal awareness.
- Dong gop data la **TimePro**, gom 9 tasks va 349K grounded annotations.
- Dong gop instruction tuning la **Temporal Grounded Caption**: sinh mo ta chi tiet cung timestamp, qua do ep model attend dung temporal evidence va giam hallucination.
- Relevance: no cung co triet ly rat gan bai cua ban la muon answer tot thi phai explicit grounding supervision.

## 23. `li2025llava`
**Title:** LLaVA-ST: A Multimodal Large Language Model for Fine-Grained Spatial-Temporal Understanding  
**Source:** https://arxiv.org/abs/2501.08282

- Khac voi cac bai chi lam temporal grounding, LLaVA-ST giai quyet ca spatial, temporal, va spatial-temporal interleaving.
- Hai dong gop architecture chinh:
- **Language-Aligned Positional Embedding** de canh hang token toa do van ban voi khong gian visual.
- **Spatial-Temporal Packer** de tach nen temporal va spatial.
- Bai con gioi thieu **ST-Align** dataset 4.3M samples va benchmark rieng cho fine-grained ST understanding.
- Relevance: paper nay cho thay neu bai cua ban sau nay mo rong sang evidence co object-level support, spatial grounding se la buoc tiep theo hop ly.

## 24. `wang2025timer1`
**Title:** Time-R1: Post-Training Large Vision Language Model for Temporal Video Grounding  
**Source:** https://openreview.net/forum?id=gJ05Gm5VxQ  
**Confidence:** best-effort; trong phien nay toi khong doc sau full page.

- Tu tieu de, venue, va cach paper nay duoc cac bai sau nhac den, Time-R1 tap trung vao **post-training** de nang temporal grounding cho LVLM.
- Diem can giu lai la su chuyen dich tu chi fine-tune task-specific sang **grounding-specific post-training / reinforcement-style optimization**.
- Relevance rat cao voi bai cua ban vi retriever cua ban dung GRPO/RLVR-style huan luyen; Time-R1 la mot minh chung cho gia tri cua post-training dac tri temporal grounding.

## 25. `zhang2026timelens`
**Title:** TimeLens: Rethinking Video Temporal Grounding with Multimodal LLMs  
**Source:** https://arxiv.org/abs/2512.14698

- Day la paper cuc ky quan trong voi bai cua ban vi retriever cua ban duoc noi la fine-tune tren **TimeLens-100K**.
- Bai khong tap trung "invent model moi" ma re-think toan bo recipe cho VTG.
- Hai truc lon:
- **Data quality**: chi ra benchmark cu co nhieu noisy annotation; de xuat **TimeLens-Bench** va **TimeLens-100K**.
- **Algorithmic design**: interleaved textual timestamp encoding, thinking-free RLVR, va recipe huan luyen hieu qua.
- Thong diep chinh: data sach + recipe dung co the thay doi rank model mot cach lon, thang chi ca proprietary models trong mot so setting.
- Relevance: day la tru cot cho phan Retriever trong paper cua ban.

## 26. `guo2024trace`
**Title:** TRACE: Temporal Grounding Video LLM via Causal Event Modeling  
**Source:** https://arxiv.org/abs/2410.05643

- TRACE xuat phat tu nhan xet rang video co cau truc su kien va quan he nhan-qua, nhung Video LLM thuong chua model phan nay tot.
- Bai de xuat mot task-interleaved Video LLM va modeling video nhu chuoi su kien co cau truc nhan-qua.
- Gia tri cua bai la dua **event structure** vao grounding thay vi chi frame-token alignment.
- Relevance: neu sau nay bai cua ban muon lam manh hon cho causal questions trong ReXTime, TRACE la mot related work can nghien cuu ky.

## 27. `zheng2024training`
**Title:** Training-free Video Temporal Grounding Using Large-Scale Pre-trained Models  
**Source:** https://arxiv.org/abs/2408.16219

- Bai nay nhao vao mot bai toan quan trong: supervised VTG dat ket qua cao nhung generalization kem duoi across-dataset va OOD.
- Huong giai quyet la training-free, tan dung tri thuc cua large-scale pre-trained vision-language / language models thay vi fine-tune task-specific.
- Thong diep lon: neu pipeline alignment duoc thiet ke hop ly, pre-trained models da co kha nang ground query vao video ma khong can huan luyen them.
- Relevance: giong bai cua ban o cho "off-the-shelf module + role specialization" co the rat manh, nhat la voi Refiner va Generator.

---

## 28. `hu2022lora`
**Title:** LoRA: Low-Rank Adaptation of Large Language Models  
**Source:** https://openreview.net/forum?id=nZeVKeeFYf9

- LoRA la PEFT kinh dien: dong bang trong so pre-trained, chi chen cac ma tran rank thap co the hoc.
- Loi ich chinh:
- Giam cuc manh so tham so can train.
- Giam nho GPU memory.
- Giup giu base model, de dang thay / xep nhieu adapters.
- Relevance truc tiep voi bai cua ban qua VideoMind-style role switching va Selector LoRA fine-tuning.

## 29. `shao2024deepseekmath`
**Title:** DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models  
**Source:** https://arxiv.org/abs/2402.03300

- Paper nay khong ve video, nhung rat lien quan vi no la nguon noi tieng cho **GRPO**.
- Hai dong gop lon:
- Data curation quy mo lon cho domain math.
- **Group Relative Policy Optimization (GRPO)**, mot bien the PPO tiet kiem bo nho hon.
- Relevance: paper cua ban su dung GRPO / RLVR cho retriever; vi vay can cite paper nay nhu nguon goc / inspiration cho reward-based post-training.

---

## 30. `xiao2024can`
**Title:** Can I Trust Your Answer? Visually Grounded Video Question Answering  
**Source:** https://openaccess.thecvf.com/content/CVPR2024/html/Xiao_Can_I_Trust_Your_Answer_Visually_Grounded_Video_Question_Answering_CVPR_2024_paper.html

- Day la paper dataset/benchmark trung tam nhat cho bai cua ban.
- Dong gop dataset la **NExT-GQA**, mo rong tu NExT-QA voi **10.5K temporal grounding labels** cho QA pairs.
- Thong diep rat manh: model co the answer dung nhung khong that su "substantiated" bang visual evidence.
- Bai con de xuat grounded-QA mechanism dua tren Gaussian mask optimization va cross-modal learning de cai thien ca grounding lan QA.
- Relevance: hieu don gian, paper cua ban dang tiep tuc duong huong do, nhung thay Gaussian-mask grounding bang pipeline Refiner -> Retriever -> Selector -> Generator.

## 31. `chen2024rextime`
**Title:** ReXTime: A Benchmark Suite for Reasoning-Across-Time in Videos  
**Source:** https://proceedings.neurips.cc/paper_files/paper/2024/hash/32683193e1d0e7a5795b073acecb3549-Abstract-Datasets_and_Benchmarks_Track.html

- ReXTime la benchmark rat hop voi bai cua ban vi no ep model phai suy luan khi question context va answer evidence nam o **nhung doan thoi gian khac nhau**.
- Dataset stats tu abstract:
- 921 validation samples.
- 2,143 test samples.
- 9,695 machine-generated training samples.
- Ket qua benchmark cho thay frontier LLM co tot hon academic models nhung van thua human 14.3% accuracy.
- Relevance: day la benchmark ly tuong de chung minh gia tri cua Refiner, vi answer option cho causal/across-time question thuong rat kho dung truc tiep lam retrieval query.

## 32. `anne2017localizing`
**Title:** Localizing Moments in Video with Natural Language  
**Source:** https://arxiv.org/abs/1708.01641

- Day la paper co y nghia lich su cho moment retrieval.
- Bai gioi thieu **DiDeMo** va model **Moment Context Network (MCN)**.
- Diem ky thuat quan trong la ket hop thong tin local cua khoanh khac va global context cua toan video.
- Dataset DiDeMo cung cap pairs giua video moments va referring expressions, tao nen mot benchmark som cho language-to-moment grounding.
- Relevance: la mot trong nhung bo du lieu co the duoc dung de train verifier / selector theo huong event grounding.

## 33. `lei2021detecting`
**Title:** Detecting Moments and Highlights in Videos via Natural Language Queries  
**Source:** https://arxiv.org/abs/2107.09609

- Paper nay gioi thieu **QVHighlights**, mot dataset query-based moment + highlight detection tren hon 10K YouTube videos.
- Annotation gom natural-language query, relevant moments, va saliency scores 5 muc cho cac clip lien quan.
- Baseline **Moment-DETR** xem bai toan nhu direct set prediction: predict coordinates va saliency end-to-end.
- Relevance: rat hop voi bai cua ban neu can selector/verifier hoc cach danh gia "muc do saliency / evidence-worthiness" cua candidate span.

## 34. `regneri-etal-2013-grounding`
**Title:** Grounding Action Descriptions in Videos  
**Source:** https://aclanthology.org/Q13-1003/

- Day la paper rat som, dat nen cho y tuong grounding mo ta hanh dong vao video.
- Dong gop chinh:
- Tao mot corpus multimodal canh hang mo ta ngôn ngu voi high-quality videos.
- Co them annotation do tuong dong giua cac action descriptions.
- Chung minh visual information tu video lam tot hon semantic similarity model cho action/event text.
- Relevance: ve lich su hoc thuat, paper nay giup dat bai toan cua ban vao dong lon "grounding language in video"; dong thoi TACoS co goc tu nhung dong du lieu kieu nay.

---

## 35. `bai2025qwen3`
**Title:** Qwen3-VL Technical Report  
**Source:** https://arxiv.org/abs/2511.21631

- Qwen3-VL la backbone rat quan trong voi bai cua ban vi retriever duoc mo ta la khoi tao tu Qwen3-VL-8B.
- Dong gop lon:
- Interleaved multimodal context **256K** tokens.
- Dong thoi manh o text understanding, long-context retention, va multimodal reasoning.
- Architecture co **enhanced interleaved-MRoPE**, **DeepStack** cho multi-level ViT features, va **text-based time alignment** cho video.
- Family gom ca dense va MoE variants.
- Relevance: neu can giai thich vi sao chon Qwen3-VL lam retriever backbone, paper nay chinh la co so ky thuat.

## 36. `wang2024qwen2`
**Title:** Qwen2-VL: Enhancing Vision-Language Model's Perception of the World at Any Resolution  
**Source:** https://arxiv.org/abs/2409.12191

- Qwen2-VL la nguon backbone hop ly cho Generator / Selector vi no rat manh o image-video-text unified understanding.
- Diem ky thuat chinh:
- **Naive Dynamic Resolution** de xu ly anh / frame o nhieu resolution.
- **M-RoPE** de hop nhat positional information cua text, image, video.
- Unified image-video paradigm va scaling study tren 2B / 8B / 72B.
- Relevance: paper nay backing cho lua chon Qwen2-VL lam generator vi no cung cap khung suy luan multimodal tong quat kha manh.

## 37. `qwen2.5-vl`
**Title:** Qwen2.5-VL Technical Report  
**Source:** https://arxiv.org/abs/2502.13923

- Qwen2.5-VL nang cap tu Qwen2-VL theo huong practical capabilities manh hon.
- Diem noi bat:
- Enhanced visual recognition va localization.
- Manh o document parsing, chart/layout understanding.
- Long-video comprehension voi **absolute time encoding** va second-level event localization.
- Native dynamic-resolution ViT va Window Attention de giam chi phi tinh toan.
- Relevance: du bai cua ban hien tai dung Qwen2-VL va Qwen3-VL, Qwen2.5-VL la mot lua chon thay the / ablation dang can nhac cho generator hoac selector.

## 38. `comanici2025gemini`
**Title:** Gemini 2.5: Pushing the Frontier with Advanced Reasoning, Multimodality, Long Context, and Next Generation Agentic Capabilities  
**Source:** https://arxiv.org/abs/2507.06261

- Day la technical report cho Gemini 2.5 Pro / Flash.
- Bai nhan manh 3 cot lon:
- reasoning co "thinking".
- native multimodality.
- long context / agentic workflows.
- Tu abstract, Gemini 2.5 Pro co kha nang xu ly video toi 3 gio, va family 2.X trai rong tradeoff capability-cost.
- Relevance: trong bai cua ban, Gemini 2.5 Flash duoc dung lam **Refiner**. Technical report nay giup hop thuc hoa lua chon do: Gemini rat manh o rewriting, reasoning, va xu ly multimodal long context, du khong can fine-tune them.

---

## Tong hop nhanh theo cum de tai

### A. Bai quan trong nhat de bao ve motivation
- `xiao2024can`: answer dung chua chac grounded.
- `chen2024rextime`: reasoning-across-time rat kho.
- `xiao2025videoqa`: empirical study cho thay VideoQA van con nhieu failure mode.

### B. Bai quan trong nhat cho phan pipeline cua ban
- `xu2024vtg`: query rewriting truoc grounding.
- `zhang2026timelens`: training recipe va du lieu cho retriever.
- `liu2025videomind`: verifier / role specialization.
- `wang2025grounded_videollm`, `huang2024vtimellm`, `huang2024lita`, `ren2024timechat`: temporal-aware backbones va training ideas.

### C. Bai de doi chieu khi viet related work
- `yu2023sevila`, `zhang2024simple`, `kahatapitiya2025language`, `qian2024streaming`.

### D. Bai nen cho implementation choices
- `hu2022lora` cho Selector / role adapters.
- `shao2024deepseekmath` cho GRPO.
- `bai2025qwen3`, `wang2024qwen2`, `qwen2.5-vl`, `comanici2025gemini` cho backbone justification.

---

## Nhan xet tong quan sau khi doc ca bo ref

- Cum ref cua ban co mot logic rat ro: motivation di tu "VideoQA khong du dang tin neu thieu grounding", sang "temporal evidence retrieval can module chuyen biet", roi sang "long video / across-time reasoning can evidence tot hon answer priors".
- Dong gop khac biet nhat cua bai ban so voi line of work hien tai la **Refiner**. Nhieu bai cai thien temporal representation, training recipe, hay verifier; it bai giai quyet truc dien viec **answer option** trong multiple-choice grounded VideoQA la query retrieval rat kem.
- Phan **Selector** cua ban dat rat dung xu huong hien tai, dac biet khi dat canh VideoMind verifier va cac bai nhan manh faithful evidence.
- Lua chon **TimeLens-trained retriever + VideoMind-style verification + Qwen2-VL generator + Gemini refiner** tao thanh mot story kha chinh: moi module duoc chon vi manh o dung vai tro cua no.

---

## Gap / follow-up goi y sau khi doc ref

- Nen bo sung mot hinh tong quan pipeline som trong Method; project hien co `figures/selector.svg` nhung chua duoc dua vao paper.
- Related Work nen nhan manh hon su khac nhau giua:
- temporal grounding thong thuong,
- grounded VideoQA,
- multiple-choice grounded VideoQA.
- Trong Introduction va Method, nen nhac ro hon rang Refiner khong chi "rewrite" ma la **convert discrimination-oriented answer text into evidence-oriented retrieval query**; day la cum y rat doc.
- Neu can phan han che / future work, cac ref goi y 3 huong hop ly:
- multi-span evidence,
- causal event modeling,
- long-form memory / repository / streaming.

