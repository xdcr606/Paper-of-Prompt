# Paper-of-Prompt
## CVPR-prompt 2023
### prompt相关文章总览
1. VoP: Text-Video Co-operative Prompt Tuning for Cross-Modal Retrieval
https://arxiv.org/pdf/2211.12764.pdf  
   提出了VoP是一个端到端的框架，同时引入了视频和文本提示，它可以被视为一个强大的基线，只有0.1%的可训练参数。此外，基于视频的时空特征，我们开发了三种新的视频提示机制，以提高不同尺度的可训练参数的性能。VoP增强的基本思想是分别用特定的可训练提示对帧位置、帧上下文和层函数进行建模。***文本视频检索，联合提示*** 
2. Prompt, Generate, then Cache: Cascade of Foundation Models makes Strong Few-shot Learners 
https://arxiv.org/pdf/2303.02151.pdf、
    我们提出疑问，如果更多样化的预训练知识可以级联，以进一步帮助小样本表示学习。在本文中，我们提出了CaFo，这是一个层叠的基础模型，它结合了各种预训练范式的不同先验知识，以实现更好的小样本学习。***小样本学习，多层次模型*** 
3. Visual-Language Prompt Tuning With Knowledge-Guided Context Optimization
https://arxiv.org/pdf/2303.13283.pdf
    提示调优是利用任务相关文本标记使预训练的视觉语言模型适应下游任务的有效方法。典型的基于Clip的工作将可学习的文本标记与类标记结合起来，以获得特定的文本知识。但是，具体的文本知识由于忘记了具有较强泛化能力的基本的一般文本知识，对看不见的类泛化程度较差。为了解决这个问题，我们引入了一种新的知识引导上下文优化(Knowledge-guided Context Optimization, KgCoOp)来增强文本的泛化能力 ***知识引导上下文优化，视觉语言*** 
4. Prompting Large Language Models With Answer Heuristics for Knowledge-Based Visual Question Answering
https://arxiv.org/pdf/2303.01903.pdf
    在本文中，我们提出了Prophet——一个概念简单的框架，旨在为基于知识的VQA提供答案启发式提示GPT-3。具体来说，我们首先在没有外部知识的特定基于知识的VQA数据集上训练一个无特性VQA模型。之后，我们从模型中提取了两种互补的答案启发式:答案候选和答案感知示例（answer candidates and answer-aware examples）。最后，这两种类型的答案启发式被编码到提示中，使GPT-3能够更好地理解任务，从而提高其能力。***VQA，答案启发式提示，LLM*** 
5. PromptCAL: Contrastive Affinity Learning via Auxiliary Prompts for Generalized Novel Category Discovery https://arxiv.org/pdf/2212.05590.pdf
    尽管现有的半监督学习模型在无标注分布内数据的学习上取得了显著的成功，但由于其闭集假设（ in-distribution data），它们大多无法对从新语义类中采样的无标记数据进行学习。在这项工作中，我们的目标是一个实用但未被充分探索的广义新类别发现(Generalized Novel Category Discovery (GNCD))设置。GNCD设置的目的是利用部分标记的已知类的信息，对来自已知类和新类的未标记训练数据进行分类。我们提出了一种带有辅助视觉提示的两阶段对比亲和学习方法，称为PromptCAL，以解决这一具有挑战性的问题。我们的方法发现了可靠的成对样本匹配度，以便为类标记和视觉提示更好地学习已知类和新类的语义聚类。首先，我们提出了一种判别性的提示正则化损失，以增强提示适应的预训练视觉转换器对精炼亲和关系的语义判别性。此外，我们提出了基于迭代半监督亲和图生成方法的对比亲和学习来校准语义表示，以增强语义监督。***对比学习，半监督学习，判别性的提示正则化损失*** 
6. Position-guided Text Prompt for Vision-Language Pre-training https://arxiv.org/pdf/2212.09737.pdf 
   视觉语言预训练(VLP)已经显示出对齐图像和文本对的潜力，促进了各种各样的跨模式学习任务。然而，我们观察到VLP模型往往缺乏视觉基础（grounding）/定位能力，这对许多下游任务(如视觉推理)至关重要。在这项工作中，我们提出了一种新的位置引导文本提示(Position-guided Text Prompt)范式，以增强使用VLP训练的跨模态模型的视觉基础能力。具体来说，在VLP阶段，PTP将图像分成N*N个块，并通过VLP中广泛使用的目标检测器来识别每个块中的目标。然后，它通过鼓励模型预测给定块中的对象或回归给定对象的块，将视觉基础任务重新制定为给定PTP中的填空问题，例如在aPTP中填充“P”或“O”“块P有一个O”。这种机制提高了VLP模型的视觉基础能力，从而帮助它们更好地处理各种下游任务。 ***图像文本对齐，位置引导*** 
7. Diversity-Aware Meta Visual Prompting https://arxiv.org/pdf/2303.08138.pdf
   我们提出了多样性感知元视觉提示(DAM-VP)，这是一种将预训练模型转移到具有冻结主干的下游任务的高效提示方法。视觉提示中一个具有挑战性的问题是，图像数据集有时具有很大的数据多样性，而单个数据集的通用提示很难处理复杂的分布向原始预训练数据分布的转移。为了解决这个问题，我们提出了一种数据集多样性感知提示策略，该策略的初始化由元提示符实现。具体而言，我们以多样性自适应的方式将下游数据集聚为小的同质性子集，每个子集都有自己的单独优化提示。这种分而治之的设计大大降低了优化难度，显著提高了提示性能。此外，所有提示都是用元提示初始化的，这是跨多个数据集学习的。这是一个自举范例，关键的观察是，从以前的数据集中学习的提示知识可以帮助提示更快地收敛，并在新的数据集中表现得更好。在推理过程中，我们根据输入和每个子集之间的特征距离动态地为每个输入选择合适的提示符。 ***元提示，生成式提示，动态选择提示***
8. Open-set Fine-grained Retrieval via Prompting Vision-Language Evaluator https://openaccess.thecvf.com/content/CVPR2023/papers/Wang_Open-Set_Fine-Grained_Retrieval_via_Prompting_Vision-Language_Evaluator_CVPR_2023_paper.pdf
   开放集细粒度检索是一个新出现的挑战，它需要在评估期间检索未知子类别的额外功能。然而，目前的工作侧重于近集视觉概念，其中所有子类别都是预定义的，这使得很难从未知子类别中捕获判别性知识，因此无法处理开放世界场景中的未知子类别。在这项工作中，我们提出了一个新的提示视觉语言评估器(PLEor)框架，该框架基于最近引入的对比语言图像预训练(CLIP)模型，用于开放集细粒度检索。PLEor可以利用预训练的CLIP模型来推断包含预定义和未知子类别的差异，称为特定类别差异，并将其转移到在近集场景中训练的骨干网络。为了使预训练的CLIP模型对特定类别的差异敏感，我们设计了一种双提示方案来学习指定特定类别差异的视觉提示，并将文本提示中具有类别名称的随机向量转换为特定类别的差异描述。在此基础上，提出了一种基于CLIP模型的视觉语言评价器，对视觉提示和文本提示进行语义对齐，并相互增强。此外，我们提出了一种开放集知识转移方法，利用知识蒸馏机制将特定类别的差异转移到骨干网络中。***细粒度检索，差异描述文本提示，知识转移***
9. Multimodal Prompting with Missing Modalities for Visual Recognition https://arxiv.org/pdf/2303.03369.pdf
    在本文中，我们解决了视觉识别多模态学习中的两个挑战:1)在训练或测试中出现模态缺失;2)在计算资源有限的情况下对heavy tansformer模型进行微调。为此，我们建议利用提示学习，同时缓解上述两个挑战。具体来说，我们的模态缺失感知提示可以插入到多模态转换器中，以处理一般的模态缺失情况，而与训练整个模型相比，只需要不到1%的可学习参数。我们进一步探讨了不同提示配置的影响，并分析了对缺失模态的鲁棒性。***视觉识别，模态缺失感知提示***
10. Visual Prompt Tuning for Generative Transfer Learning https://arxiv.org/pdf/2210.00990.pdf
    从大数据集训练的图像合成模型中转移知识是有效学习各领域生成图像模型的一个有前途的方向。虽然以前的工作已经研究了GAN模型，但我们提出了一种通过生成知识转移学习视觉tansformer的方法。我们的框架基于最先进的生成视觉tansformer，它将图像表示为自回归或非自回归tansformer的视觉标记序列。为了适应新的领域，我们采用提示调优，将称为提示的可学习标记添加到图像标记序列中，并为我们的任务引入新的提示设计。***迁移学习，图像生成***
11. CORA: Adapting CLIP for Open-Vocabulary Detection with Region Prompting and Anchor Pre-Matching https://arxiv.org/pdf/2303.13076.pdf
    (Open-vocabulary detection, OVD)是一种目标检测任务，目的是在检测器训练的基本类别之外，从新的类别中检测对象。最近的OVD方法依赖于大规模的视觉语言预训练模型，如CLIP，来识别新物体。我们确定了将这些模型纳入检测器训练时需要解决的两个核心障碍:(1)将在整个图像上训练的vl模型应用于区域识别任务时发生的分布不匹配;(2)不可见类对象的定位困难。为了克服这些障碍，我们提出了CORA，这是一个DETR风格的框架，它通过区域提示和锚点预匹配来适应CLIP进行开放词汇检测。区域提示通过提示基于clip的区域分类器的区域特征来缓解整体到区域的分布差距。锚点预匹配通过类感知匹配机制帮助学习可泛化的对象定位。***Open-vocabulary detection，区域提示，锚点匹配***
12. Doubly Right Object Recognition: A Why Prompt for Visual Rationales https://arxiv.org/pdf/2212.06202.pdf
    许多视觉识别模型仅根据其分类精度进行评估，这是他们获得强大性能的度量。在本文中，我们研究计算机视觉模型是否也可以为他们的预测提供正确的依据。我们提出了一个“双重正确”的对象识别基准，其中度量要求模型同时产生正确的标签和正确的基本原理。我们发现，最先进的视觉模型，如CLIP，经常为其分类预测提供不正确的依据。然而，通过定制数据集将基本原理从语言模型转换为视觉表示，我们表明我们可以学习“为什么提示”，它适应大型视觉表示来产生正确的基本原理。可视化和经验实验表明，我们的提示显着提高了双重正确物体识别的性能，另外可以零样本迁移到不可见的任务和数据集。***双重正确识别基准，零样本迁移 ***
13. RIATIG: Reliable and Imperceptible Adversarial Text-to-Image Generation With Natural Prompts https://openaccess.thecvf.com/content/CVPR2023/papers/Liu_RIATIG_Reliable_and_Imperceptible_Adversarial_Text-to-Image_Generation_With_Natural_Prompts_CVPR_2023_paper.pdf
    文本到图像的生成领域在创造高保真度和逼真的图像方面取得了显著的进步。随着这项技术的普及，人们越来越担心其潜在的安全风险。然而，从对抗的角度对这些模型的鲁棒性进行了有限的探索。现有的研究主要集中在非目标设置上，缺乏对可靠性(攻击成功率)和隐身性(不可感知性)的整体考虑。在本文中，我们提出了RIATIG，这是一种通过不明显的例子对文本到图像模型进行可靠且难以察觉的对抗性攻击。通过将示例制作作为优化过程并使用基于遗传的方法进行求解，我们提出的攻击可以以可靠的方式为文本到图像生成模型生成难以察觉的提示。对六种流行的文本到图像生成模型的评估表明了我们的攻击在白盒和黑盒设置下的效率和隐蔽性。***文生图，不可见攻击***
14. Prompt-Guided Zero-Shot Anomaly Action Recognition using Pretrained Deep Skeleton Features https://arxiv.org/pdf/2303.15167.pdf
    本研究研究了无监督异常动作识别，该识别以无监督的方式在没有异常样本的情况下识别视频级别的异常人类行为事件，同时解决了传统基于骨架方法的三个局限性:目标域依赖的DNN训练，对骨架错误的鲁棒性以及缺乏正常样本。我们提出了一个统一的、用户提示引导的零样本学习框架，使用目标域无关的骨架特征提取器，该框架在大规模动作识别数据集上进行预训练。特别是，在使用正态样本的训练阶段，该方法对正态动作的骨架特征分布进行建模，同时冻结dnn的权重，并在推理阶段使用该分布估计异常分数。此外，为了增加对骨骼误差的鲁棒性，我们引入了一种受点云深度学习范式启发的DNN架构，该架构在关节之间稀疏传播特征。此外，为了防止未观察到的正常动作被误认为异常动作，我们将用户提示嵌入与在公共空间中对齐的骨架特征之间的相似性得分纳入异常得分，间接补充了正常动作。***无监督学习，异常动作识别，零样本学习***
15. Efficient Multimodal Fusion via Interactive Prompting https://arxiv.org/pdf/2304.06306.pdf
    大规模的预训练将计算机视觉和自然语言处理等单模态领域带入了一个新时代。在这种趋势下，多模态学习模型的规模不断增加，导致迫切需要减少为下游任务微调这些模型的大量计算成本。在本文中，我们提出了一种高效灵活的多模态融合方法，即PMF，专门用于融合单模预训练transformer。具体来说，我们首先提出了一个模块化的多模态融合框架，它具有高度的灵活性，并促进了不同模态之间的相互作用。此外，为了学习多模态学习的不同优化目标，我们将无特征提示分解为三种类型。同样值得注意的是，我们建议仅在单模transformer的深层上添加提示向量，从而显着减少训练内存的使用。***多模态融合，单模态深层提示***
16. CODA-Prompt: COntinual Decomposed Attention-based Prompting for Rehearsal-Free Continual Learning https://openaccess.thecvf.com/content/CVPR2023/papers/Smith_CODA-Prompt_COntinual_Decomposed_Attention-Based_Prompting_for_Rehearsal-Free_Continual_Learning_CVPR_2023_paper.pdf
    当计算机视觉模型从不断变化的训练数据中学习新概念时，会出现一种被称为灾难性遗忘的现象。这种持续学习问题的典型解决方案需要对以前看到的数据进行大量的排练，这增加了内存成本，并可能侵犯数据隐私。最近，大规模预训练视觉转换模型的出现使得提示方法成为数据排练的替代方法。这些方法依赖于一个键查询机制来生成提示，并被发现在建立良好的无预演持续学习环境中对灾难性遗忘具有高度的抵抗力。然而，这些方法的关键机制并不是端到端按照任务序列进行训练的。我们的实验表明，这会导致它们的可塑性降低，从而牺牲新任务的准确性，并且无法从扩展的参数容量中受益。相反，我们建议学习一组提示组件，这些组件与输入条件权重组合以产生输入条件提示，从而产生一种新的基于注意力的端到端键查询方案。***灾难性遗忘，条件提示，端到端键查询***
17. Zero-shot Generative Model Adaptation via Image-specific Prompt Learning https://arxiv.org/pdf/2304.03119.pdf
    最近，clip引导的图像合成在将预训练的源域生成器适应于看不见的目标域方面显示出了吸引人的性能。它不需要任何目标域样本，只需要文本域标签。训练效率很高，例如，几分钟。然而，现有的方法在生成图像的质量上仍然存在一定的局限性，并且可能存在模态崩溃问题。一个关键原因是对所有的跨域图像对采用固定的自适应方向，导致监督信号相同。为了解决这个问题，我们提出了一种图像特定提示学习( Image-specific Prompt Learning，IPL)方法，该方法为每个源域图像学习特定的提示向量。这为每个跨域图像对提供了更精确的自适应方向，大大增强了目标域生成器的灵活性。各领域的定性和定量评价表明，IPL有效地提高了合成图像的质量和多样性，缓解了模态崩溃。此外，IPL独立于生成模型的结构，如生成对抗网络或扩散模型。***图像特定提示，源域生成source-domain***
18. TranSG: Transformer-Based Skeleton Graph Prototype Contrastive Learning with Structure-Trajectory Prompted Reconstruction for Person Re-Identification https://arxiv.org/pdf/2303.06819.pdf
    基于三维骨骼数据的人体识别是一个新兴的研究课题，具有突出的优势。现有的方法通常是使用原始身体关节设计骨骼描述符或进行骨骼序列表示学习。然而，它们通常不能同时建模不同的身体-组件关系，并且很少从身体关节的细粒度表示中探索有用的语义。在本文中，我们提出了一种通用的基于transformer的骨架图原型对比学习(TranSG)方法，该方法具有结构-轨迹提示重建，可以从骨架图中充分捕获骨架关系和有价值的时空语义，用于人员重新识别。具体来说，我们首先设计了骨架图转换器(SGT)来同时学习骨架图中的身体和运动关系，从而将关键的相关节点特征聚合成图表示。然后，我们提出了图原型对比学习(GPC)来挖掘每个身份的最典型的图特征(图原型)，并从骨架和序列两个层次对比图表示与不同原型之间的内在相似性，从而学习判别图表示。最后，提出了一种图形结构-轨迹提示重构(STPR)机制，利用图节点的时空背景来提示骨架图重构，有利于捕获更有价值的模式和图形语义。实证评估表明，TranSG显著优于现有的最先进的方法。我们进一步展示了它在不同图建模、rgb估计骨架和无监督场景下的通用性。***三维骨骼人体识别，对比学习***
19. CLAMP: Prompt-Based Contrastive Learning for Connecting Language and Animal Pose https://arxiv.org/pdf/2206.11752.pdf
    由于训练数据有限，物种内和物种间差异大，现有的基于图像的动物姿态估计方法具有挑战性。受视觉语言研究进展的推动，我们提出预训练的语言模型(如CLIP)可以通过提供丰富的先验知识来描述文本中的动物关键点，从而促进动物姿态估计。然而，我们发现在预训练的语言模型和视觉动物关键点之间建立有效的联系是非常重要的，因为基于文本的描述和基于关键点的动物姿势视觉特征之间的差距可能是显著的。为了解决这个问题，我们引入了一种新的基于提示的对比学习方案来有效地连接语言和动物姿势(CLAMP)。CLAMP试图通过在网络训练期间调整文本提示以适应动物关键点来弥合这一差距。将自适应分解为空间感知和特征感知两个过程，并相应地设计了两种新的对比损失。在实践中，CLAMP实现了第一个跨模态动物姿态估计范式。***动物姿态估计，对比学习***
20. Hierarchical Prompt Learning for Multi-Task Learning https://openaccess.thecvf.com/content/CVPR2023/papers/Liu_Hierarchical_Prompt_Learning_for_Multi-Task_Learning_CVPR_2023_paper.pdf
    视觉语言模型可以通过快速学习有效地迁移到各种视觉任务中。现实世界的场景通常需要使模型适应多个相似但不同的任务。现有的方法侧重于学习每个任务的特定提示，限制了利用来自其他任务的潜在共享信息的能力。天真地使用所有任务的组合来训练任务共享提示会忽略细粒度的任务相关性。任务间的显著差异可能导致负迁移。考虑到这一点，我们提出了分层提示(HiPro)学习，这是一种简单有效的方法，可以使预训练的VLM共同适应多个下游任务。我们的方法量化了任务间的匹配度，并随后构建了一个分层任务树。由内部节点学习的任务共享提示探索相应任务组中的信息，而由叶节点学习的任务单独提示获取针对每个任务的细粒度信息。分层提示的组合提供了不同粒度的高质量内容。**分层提示。任务匹配度量化**
21. FashionSAP: Symbols and Attributes Prompt for Fine-Grained Fashion Vision-Language Pre-Training https://arxiv.org/pdf/2304.05051.pdf
    时尚视觉语言预训练模型已经显示出对一系列下游任务的有效性。然而，一般的视觉语言预训练模型对细粒度的领域特征关注较少，而这些特征对于区分特定的领域任务和一般任务非常重要。提出了一种基于时尚符号和属性提示符(FashionSAP)的细粒度时尚视觉语言预训练方法，对细粒度多模态时尚属性和特征进行建模。首先，我们提出了一种新颖的抽象时尚概念层——时尚符号，用来表示不同的时尚单品，概括各种细粒度的时尚特征，使细粒度属性的建模更加有效。其次，提出了属性提示方法，使模型明确地学习时尚单品的特定属性;我们根据时尚数据的格式设计合适的提示模板。在两个公共时尚基准，即fashionengen和FashionIQ上进行了综合实验，FashionSAP在四个流行的时尚任务上获得了SOTA的表现。本文还对所提出的抽象时尚符号进行了研究，并利用属性提示方法使模型能够有效地获取时尚领域的细粒度语义。从FashionSAP中获得的明显性能提升为未来的时尚任务研究提供了新的基准。**时尚任务，属性提示**
22. PIVOT: Prompting for Video Continual Learning https://openaccess.thecvf.com/content/CVPR2023/papers/Villa_PIVOT_Prompting_for_Video_Continual_Learning_CVPR_2023_paper.pdf
    由于数据可用性、存储配额、隐私法规和昂贵的注释过程，现代机器学习pipelines受到限制。这些约束使得在这种动态注释集上训练和更新大规模模型变得困难或不可能。持续学习直接解决了这个问题，其最终目标是设计一种方法，让深度神经网络有效地学习新的(看不见的)类的相关模式，而不会显著改变它在以前学习过的类上的表现。本文主要研究视频数据的持续学习问题。我们介绍了PIVOT，这是一种利用图像域预训练模型的广泛知识的新方法，从而减少了可训练参数的数量和相关的遗忘。与以前的方法不同，我们的方法是第一个有效地使用提示机制进行持续学习而不需要任何领域内预训练的方法。**持续学习+提示学习**
23. SmallCap: Lightweight Image Captioning Prompted With Retrieval Augmentation https://arxiv.org/pdf/2209.15323.pdf
    图像字幕的最新进展主要集中在缩放数据和模型大小上，这大大增加了预训练和微调的成本。作为大型模型的替代方案，我们提出了SmallCap，它根据输入图像和从数据存储中检索的相关标题生成标题。我们的模型重量轻，训练速度快，因为唯一学习的参数是在预训练的CLIP编码器和GPT-2解码器之间新引入的交叉注意层。SmallCap可以转移到新的领域，而无需额外的调优，并且可以以不需要训练的方式利用大规模数据，因为数据存储的内容可以很容易地替换。**图像字幕，预生成图文词典**
24. Learning Expressive Prompting With Residuals for Vision Transformers https://arxiv.org/pdf/2303.15591.pdf
    通过在预训练模型的输入和中间表示中插入一组可学习的参数，提示学习是一种有效的适应transformer的方法。在这项工作中，我们提出了带有残差的表达提示(express)，它修改了提示学习范式，专门用于有效适应视觉变形(ViT)。Out方法通过可学习的“输出”标记构建下游表示，这些标记类似于ViT的已学习类标记。为了更好地控制冻结transformer处理的下游表示，我们引入了残差可学习令牌，将其添加到各种计算的输出中。我们将express应用于图像分类、少数镜头学习和语义分割，并表明我们的方法能够在VTAB基准的3/3类别上实现最先进的提示调优。除了强大的性能之外，我们观察到我们的方法比现有的视觉提示基线的提示效率要高一个数量级。我们分析地展示了我们的方法比权重空间适应技术(如微调)的计算优势。最后，通过一系列烧蚀实验系统地验证了该方法的结构设计。**残差提示**
25. Generating Anomalies for Video Anomaly Detection With Prompt-Based Feature Mapping https://openaccess.thecvf.com/content/CVPR2023/papers/Liu_Generating_Anomalies_for_Video_Anomaly_Detection_With_Prompt-Based_Feature_Mapping_CVPR_2023_paper.pdf
    监控视频中的异常检测是一项具有挑战性的计算机视觉任务，在训练期间只有正常的视频可用。最近的工作发布了第一个虚拟异常检测数据集，以辅助现实世界的检测。然而，由于虚拟数据集中的异常是有界的，而现实数据集中的异常是无界的，因此存在异常间隙，从而降低了虚拟数据集的泛化能力。虚拟场景和真实场景之间也存在场景差距，包括场景特定的异常(在一个场景中异常但在另一个场景中正常的事件)和场景特定的属性，例如监控摄像机的视点。本文提出了一种基于提示的特征映射框架(PFMF)来解决异常间隙和场景间隙的问题。该模型包含一个以异常提示为导向的映射网络，用于生成真实场景中不可见且类型无界的异常，以及一个映射自适应分支，通过应用领域分类器和异常分类器来缩小场景差距。所提出的框架在三个基准数据集上优于最先进的框架。**视频异常检测，特征映射（Feature Mapping）**
26. Fusing Pre-Trained Language Models With Multimodal Prompts Through Reinforcement Learning https://openaccess.thecvf.com/content/CVPR2023/papers/Yu_Fusing_Pre-Trained_Language_Models_With_Multimodal_Prompts_Through_Reinforcement_Learning_CVPR_2023_paper.pdf
    语言模型能够进行常识推理:而特定领域的模型可以从明确的知识中学习，而像GPT-3这样的大型模型则表现出广泛的常识推理能力。他们的知识是否可以扩展到多模态输入，如图像和音频，而不需要配对的领域数据?在这项工作中，我们提出了ESPER(扩展感官知觉与强化学习)，它使纯文本预训练模型能够处理多模态任务，如视觉常识推理。我们的关键新颖之处在于使用强化学习在没有直接监督的情况下将多模态输入与语言模型代对齐:例如，我们的奖励优化仅依赖于源自CLIP的余弦相似性，并且不需要额外的配对(图像，文本)数据。实验表明，ESPER在从字幕到常识推理的各种多模态文本生成任务上优于基线和先前的工作;其中包括我们收集和发布的一个新基准，ESP数据集，它的任务是为每个图像生成几个不同域的文本。**强化学习，扩展感官知觉**
27. BlackVIP: Black-Box Visual Prompting for Robust Transfer Learning https://arxiv.org/pdf/2303.14773.pdf
    随着大规模预训练模型(ptm)的激增，对这些模型进行微调以适应众多下游任务成为一个关键问题。因此，大型模型的参数高效迁移学习(PETL)受到了广泛的关注。虽然最近的PETL方法展示了令人印象深刻的性能，但它们依赖于乐观的假设:1)PTM的整个参数集是可用的，2)为微调配备了足够大的内存容量。然而，在大多数现实世界的应用程序中，ptm被用作黑盒API或专有软件，没有明确的参数可访问性。此外，现代ptm很难满足大容量的内存需求。在这项工作中，我们提出了黑盒视觉提示(BlackVIP)，它可以在不了解模型体系结构和参数的情况下有效地适应ptm。BlackVIP有两个组成部分;1)协调器和2)梯度校正同步摄动随机逼近(SPSA-GC)。协调器设计了依赖于输入的图像形视觉提示，提高了对分布/位置移动的少镜头适应性和鲁棒性。SPSA-GC可以有效地估计目标模型的梯度来更新协调器。在16个数据集上进行的大量实验表明，BlackVIP能够在不访问PTMs参数的情况下对不同领域进行鲁棒适应，并且内存需求最小。**黑盒调优，零阶优化**
28. From Images to Textual Prompts: Zero-Shot Visual Question Answering With Frozen Large Language Models https://openaccess.thecvf.com/content/CVPR2023/papers/Guo_From_Images_to_Textual_Prompts_Zero-Shot_Visual_Question_Answering_With_CVPR_2023_paper.pdf
    大型语言模型(llm)已经证明了对新语言任务的出色的零样本泛化。然而，有效利用LLM进行零样本视觉问答(VQA)仍然具有挑战性，主要是由于LLM和VQA任务之间的模态脱节和任务脱节。对多模态数据的端到端训练可以弥合这种脱节，但不灵活且计算成本高。为了解决这个问题，我们提出了Img2LLM，这是一个即插即用模块，它提供LLM提示，使LLM能够在没有端到端培训的情况下执行零样本VQA任务。我们开发了与LLM无关的模型，将图像内容描述为示例问答对，这被证明是有效的LLM提示。**LLM，VQA，LLM提示**
29. Visual Prompt Multi-Modal Tracking https://arxiv.org/pdf/2303.10826.pdf
    可见模态目标跟踪产生了一系列下游多模态跟踪分支。为了继承基础模型的强大表示，多模态跟踪的自然操作方式是对基于rgb的参数进行全面微调。这种方式虽然有效，但由于下游数据的稀缺性和可移植性差等原因，并不是最优的。在本文中，受提示学习在语言模型中最近取得的成功的启发，我们开发了视觉提示多模态跟踪(ViPT)，它学习与模态相关的提示，使冻结的预训练基础模型适应各种下游多模态跟踪任务。ViPT找到了一种更好的方法来刺激基于rgb的模型的知识，该模型是在规模上预训练的，同时只引入了一些可训练的参数(不到模型参数的1%)。ViPT在多个下游跟踪任务(包括RGB+Depth, RGB+Thermal和RGB+Event跟踪)上优于全微调范式。**多模态追踪，视觉提示**
30. ProD: Prompting-To-Disentangle Domain Knowledge for Cross-Domain Few-Shot Image Classification https://openaccess.thecvf.com/content/CVPR2023/papers/Ma_ProD_Prompting-To-Disentangle_Domain_Knowledge_for_Cross-Domain_Few-Shot_Image_Classification_CVPR_2023_paper.pdf
    本文考虑了跨域场景下的小样本图像分类，训练与测试的域差距影响了分类的准确性。为了缓解区域间隙，我们通过对提示机制的新颖探索，提出了一种提示解耦(ProD)方法。ProD采用流行的多域训练方案，利用标准的卷积神经网络提取主干特征。基于这两种常见的做法，ProD的关键是利用transformer中的提示机制将主干特征中的领域通用(DG)和领域特定(DS)知识分离出来。具体来说，ProD将DG和DS提示连接到主干特性，并将它们馈送到轻量级transformer中。DG提示是可学习的，并由所有训练域共享，而DS提示是从感兴趣的领域动态生成的。因此，transformer输出DG和DS特征与两个提示并行，产生解耦效果。我们表明:1)简单地为所有训练域共享单个DG提示已经提高了对新测试域的泛化。2)通过使DG提示对训练域保持中立，可以进一步加强跨域泛化。3)推理时，从支持样本中生成DS提示，通过提示机制捕获测试领域知识。 **小样本分类，领域特定，领域通用提示**
31. A-La-Carte Prompt Tuning (APT): Combining Distinct Data via Composable Prompting https://openaccess.thecvf.com/content/CVPR2023/papers/Bowman_A-La-Carte_Prompt_Tuning_APT_Combining_Distinct_Data_via_Composable_Prompting_CVPR_2023_paper.pdf 
    我们介绍了A-la-carte Prompt Tuning(APT)，这是一种基于transformer的方案，用于调优不同数据上的提示，以便它们可以在推理时任意组合。可以在不同的设备、不同的时间、不同的发行版或域上隔离地训练单个提示。此外，每个提示符只包含有关训练期间暴露的数据子集的信息。在推理过程中，可以根据任意选择的数据源来组装模型，我们称之为单点学习。“单点学习”可以根据每个用户的个人访问权限和偏好构建定制模型。我们可以通过简单地添加或删除相应的提示来从模型中添加或删除信息，而无需从头开始重新训练。我们证明，在各自来源的联合上训练的模型的准确率在5%以内，在训练和推理时间方面的成本相当。对于持续学习基准Split CIFAR-100和CORe50，我们实现了最先进的性能.**单点学习，提示隔离定制**
32. Visual Exemplar Driven Task-Prompting for Unified Perception in Autonomous Driving https://arxiv.org/pdf/2303.01788.pdf
    多任务学习已经成为一种同时解决一系列任务的强大范例，在计算资源和推理时间上都有很好的效率。然而，这些算法大多是针对不同的任务而设计的，并不在自动驾驶的范围内，因此很难对自动驾驶中的多任务方法进行比较。为了全面评估当前自动驾驶中的多任务学习方法，我们广泛研究了流行的多任务学习方法在大规模驾驶数据集上的性能，该数据集涵盖了四种常见的感知任务，即目标检测、语义分割、可驾驶区域分割和车道检测。我们对目前不同常见设置下的多任务学习方法进行了深入分析，发现现有方法取得了进步，但与单任务基线相比仍有较大的性能差距。为了缓解自动驾驶中的这一困境，我们提出了一个有效的多任务框架，VE-Prompt，它通过特定任务的提示引入视觉范例，引导模型学习高质量的特定任务表示。具体来说，我们基于边界框和基于颜色的标记生成视觉范例，这提供了目标类别的准确视觉外观，并进一步缓解了性能差距。此外，我们在基于变压器的编码器和卷积层之间架起桥梁，以实现自动驾驶中高效准确的统一感知。在多种自动驾驶数据集BDD100K上的综合实验结果表明，VE-Prompt提高了多任务基线，进一步超越了单任务模型。**任务提示，视觉范例，多任务学习**
33. Decomposed Soft Prompt Guided Fusion Enhancing for Compositional Zero-Shot Learning https://arxiv.org/pdf/2211.10681.pdf
    组合零样本学习(CZSL)旨在识别在训练过程中由已知状态和对象形成的新概念。现有方法要么学习组合状态-对象表示，挑战未见组合的泛化，要么设计两个分类器从图像特征中单独识别状态和对象，忽略它们之间的内在关系。为了共同消除上述问题并构建一个更健壮的CZSL系统，我们提出了一个新的框架，称为分解融合与软提示(DFSP)1，通过使用视觉语言模型(VLMs)进行看不见的成分识别。具体来说，DFSP构建了一个由状态和对象组成的可学习软提示向量组合，建立了它们的联合表示。此外，在语言和图像分支之间设计了跨模态分解融合模块，将状态和对象分解为语言特征，而不是图像特征。值得注意的是，将图像特征与分解后的特征融合在一起，可以更好地表达图像特征与状态和对象之间的关系，从而提高对空间中未见组合的响应，从而缩小了未见集和见集之间的域差距。在三个具有挑战性的基准上的实验结果表明，我们的方法明显优于其他最先进的方法。**可学习软提示向量组合**
34. Text-Visual Prompting for Efficient 2D Temporal Video Grounding https://arxiv.org/pdf/2303.04995.pdf
    在本文中，我们研究了时间视频基础(TVG)问题，该问题旨在预测未经修剪的长视频中由文本句子描述的时刻的开始/结束时间点。TVG技术得益于细粒度的3D视觉特征，近年来取得了显著的进展。然而，三维卷积神经网络(cnn)的高复杂性使得提取密集的三维视觉特征非常耗时，这需要大量的内存和计算资源。为了提高TVG的效率，我们提出了一种新的文本-视觉提示(TVP)框架，该框架将优化的扰动模式(我们称之为“提示”)整合到TVG模型的视觉输入和文本特征中。与3D cnn形成鲜明对比的是，我们发现TVP允许我们在2D TVG模型中有效地共同训练视觉编码器和语言编码器，并且仅使用低复杂度的稀疏2D视觉特征就可以提高跨模态特征融合的性能。此外，我们提出了一个时间距离IoU (TDIoU)损失来有效地学习TVG。
35. Understanding and Improving Visual Prompting: A Label-Mapping Perspective https://arxiv.org/pdf/2211.11635.pdf
    我们回顾和推进视觉提示(VP)，一种用于视觉任务的输入提示技术。VP可以通过简单地将通用提示(根据输入扰动模式)合并到下游数据点中，对固定的、预训练的源模型进行重新编程，以完成目标域中的下游任务。然而，即使在源类和目标类之间给出无规则的标签映射(LM)，为什么VP仍然有效，这一点仍然难以理解。受以上启发，我们问:LM与VP是如何关联的?如何利用这种关系来提高它在目标任务上的准确性?我们探讨了语言管理对副总裁的影响，并提供了一个肯定的答案，即更好的语言管理“质量”(通过映射精度和解释来评估)可以持续提高VP的有效性。这与缺少LM因素的现有技术形成对比。为了优化LM，我们提出了一个新的VP框架，称为iterative label mapping-based visual prompting，ILM-VP(基于迭代标签映射的视觉提示)，该框架自动将源标签重新映射到目标标签，并逐步提高VP的目标任务精度。此外，在使用对比语言图像预训练(CLIP)模型时，我们建议集成LM过程来辅助CLIP的文本提示选择，提高目标任务的准确性。广泛的实验表明，我们的建议显着优于最先进的VP方法。**视觉提示，标签映射**
36. Language-Guided Music Recommendation for Video via Prompt Analogies https://openaccess.thecvf.com/content/CVPR2023/papers/McKee_Language-Guided_Music_Recommendation_for_Video_via_Prompt_Analogies_CVPR_2023_paper.pdf
    我们提出了一种为输入视频推荐音乐的方法，同时允许用户使用自由形式的自然语言指导音乐选择。这个问题设置的一个关键挑战是，现有的音乐视频数据集提供了所需的(视频、音乐)训练对，但缺乏音乐的文本描述。这项工作通过以下三个贡献来应对这一挑战。首先，我们提出了一种文本合成方法，该方法依赖于基于类比的提示过程，根据预先训练好的音乐标注器输出和少量人类文本描述，从大规模语言模型(BLOOM-176B)生成自然语言音乐描述。其次，我们使用这些合成的音乐描述来训练一个新的三模态模型，该模型融合了文本和视频输入表示来查询音乐样本。对于训练，我们引入了文本剔除正则化机制，我们认为这对模型性能至关重要。我们的模型设计允许检索到的音乐音频通过匹配视频中描述的视觉风格和自然语言查询中描述的音乐类型、情绪或乐器来与两种输入模式一致。第三，为了评估我们的方法，我们为我们的问题收集了一个测试数据集，通过使用我们公开提供的自然语言音乐描述来注释YT8M-MusicVideo数据集的4k片段子集。我们表明，我们的方法在使用文本引导时可以匹配或超过先前的视频到音乐检索方法的性能，同时显着提高检索精度。
37. LASP: Text-to-Text Optimization for Language-Aware Soft Prompting of Vision & Language Models https://arxiv.org/pdf/2210.01115.pdf
    软提示学习最近成为使用少量训练示例使V&L模型适应下游任务的选择方法之一。然而，目前的方法明显过拟合训练数据，当测试来自同一领域的未见过的类时，准确性下降很大。为此，在本文中，我们做出了以下4个贡献:(1)为了缓解基类过拟合，我们提出了一种新的语言感知软提示(LASP)学习方法，该方法通过文本到文本的交叉熵损失来最大化学习到的提示相对于预定义的手工文本提示被正确分类的概率。(2)为了增加提示的表示能力，我们提出了分组LASP，其中每组提示都针对单独的文本提示子集进行优化。(3)我们发现了由快速学习和LASP引入的视觉语言失调，更重要的是，提出了一种重新校准机制来解决它。(4)我们证明了LASP在训练过程中固有地适用于包括虚拟类，即没有视觉样本的类名，进一步增加了学习提示的鲁棒性。通过对11个数据集的评估，我们表明我们的方法(a)显著优于之前在软提示上的所有工作，并且(b)在11个测试数据集中的8个中，首次匹配并超过了手工制作提示和CLIP获得的新类别的准确性。**软提示，对齐**
38. Learning Federated Visual Prompt in Null Space for MRI Reconstruction https://arxiv.org/pdf/2303.16181.pdf
    联合磁共振成像(MRI)重建使多家医院能够在不聚合本地数据的情况下进行分布式协作，从而保护患者隐私。然而，由于核磁共振成像协议的不同、局部训练数据的不足以及通信带宽的限制，导致数据的异质性不可避免地影响了全局模型的收敛和更新。在本文中，我们提出了一种新的算法FedPR，用于在MRI重建的全局提示的零空间中学习联邦视觉提示。FedPR是一种新的联邦范式，它采用了一个强大的预训练模型，同时只学习和交流具有很少可学习参数的提示，从而大大降低了通信成本，并在有限的本地数据上取得了具有竞争力的性能。此外，为了处理数据异构导致的灾难性遗忘，FedPR还更新了高效的联邦视觉提示，将本地提示投影到全局提示的近似零空间中，从而抑制梯度对服务器性能的干扰。在联邦MRI上进行的大量实验表明，在给定有限的局部训练数据时，FedPR以6%的通信成本显著优于最先进的FL算法。
39. MaPLe: Multi-Modal Prompt Learning https://arxiv.org/pdf/2210.03117.pdf
    预训练的视觉语言(V-L)模型，如CLIP，在下游任务中显示出出色的泛化能力。但是，它们对输入文本提示的选择很敏感，需要仔细选择提示模板才能运行良好。受自然语言处理(NLP)文献的启发，最近的CLIP适应方法学习提示作为文本输入，以微调下游任务的CLIP。我们注意到，使用提示来适应CLIP(语言或视觉)的单个分支中的表示是次优的，因为它不允许在下游任务上动态调整两个表示空间的灵活性。在这项工作中，我们提出了针对视觉和语言分支的多模态提示学习(MaPLe)，以改善视觉和语言表征之间的一致性。我们的设计促进了视觉语言提示之间的强耦合，以确保相互协同，并阻止学习独立的单模态解决方案。此外，我们在不同的早期阶段学习单独的提示，逐步对阶段特征关系建模，以允许丰富的上下文学习。我们评估了我们的方法在三个代表性任务上的有效性:对新类别的泛化、新的目标数据集和未见过的域转移。与最先进的Co-CoOp方法相比，MaPLe表现出良好的性能，在11个不同的图像识别数据集上平均，MaPLe在新类别上实现了3.45%的绝对增益，在总谐波平均值上实现了2.72%的绝对增益。我们的代码和预训练模型可在此https URL。**多模态提示，两阶段学习**
40. Explicit Visual Prompting for Low-Level Structure Segmentations https://arxiv.org/pdf/2303.10883.pdf
    我们考虑了检测图像中底层结构的一般问题，包括分割被操纵部分、识别失焦像素、分离阴影区域和检测隐藏物体。虽然每个这样的主题通常都是用特定于领域的解决方案来解决的，但我们展示了统一的方法在所有这些问题上都能很好地执行。我们从NLP中广泛使用的预训练后提示调优协议中获得灵感，提出了一种新的视觉提示模型，称为显式视觉提示(Explicit visual prompt, EVP)。与之前的视觉提示不同，通常是数据集级别的隐式嵌入，我们的关键见解是将可调参数集中在每个单独图像的显式视觉内容上，即来自冻结补丁嵌入的特征和输入的高频成分。在相同数量的可调参数(每个任务额外5.7%的可训练参数)下，所提出的EVP显着优于其他参数高效调优协议。与特定于任务的解决方案相比，EVP在各种低级结构分割任务上也实现了最先进的性能。**显示视觉提示**
