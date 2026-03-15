**SAR星群泛在协同辐射定标方法研究**

**国内外相关工作（详细版）**

### 2. 国内外相关工作

以下分别从**SAR辐射定标参考目标、遥感载荷协同辐射定标、遥感载荷时间序列辐射定标**三个维度，系统分析国内外研究现状、发展脉络与技术趋势。

#### 2.1 SAR辐射定标参考目标国内外现状与发展趋势

SAR辐射定标的精度核心取决于参考目标的可靠性，该领域正经历**从依赖人工专用设备，到广域自然地物挖掘，再到数字化基准场构建**的三代技术演进，是当前SAR定标领域的核心发展方向。

![](./image1.emf)

图2  遥感载荷辐射定标参考目标发展脉络图

##### 2.1.1 人工定标器与定标场------经典高精度基准，受限于时空覆盖能力

人工定标器（角反射器CR、有源定标器ARC）具有理论可精确计算的雷达散射截面（RCS），是目前SAR辐射定标的基准源头，也是各国星载SAR卫星官方定标的核心手段，其发展历程与全球定标场网建设同步推进。

国际上，德国宇航中心（DLR）在Oberpfaffenhofen建设的定标场，部署了6个永久角反射器、24个临时安置点与高精度有源定标器，支撑了TerraSAR-X卫星优于0.3dB的定标精度；美国NASA喷气推进实验室（JPL）在Rosamond干湖床建设的定标场，布设16组多波段兼容角反射器，是UAVSAR、NISAR等卫星的核心定标基准；澳大利亚在昆士兰建设的定标场，部署40组航空级钛合金三面角反射器，形成了覆盖Sentinel-1、TerraSAR-X等卫星的定标验证能力。美国德尔塔章克申定标场位于阿拉斯加州，南北向75km、东西向65km。该定标场目前提供4个2.5m永久角反射器、6个3m永久角反射器。

国内方面，我国先后建设了包头国家高分辨遥感综合定标场、嵩山遥感卫星定标场、中卫遥感卫星定标场、内蒙苏尼特右旗定标场、新疆哈密定标场、内蒙古鄂托克旗定标场等国家级设施。其中包头定标场东西向布设10座角反射器基座，南北向4座基座，配备100余台全波段适配的固定式、可移动式角反射器，支撑了高分三号系列卫星优于0.5dB的定标精度，相关靶标已纳入CEOS全球SAR目标库；中卫定标场配备3台星载SAR有源定标器与20组自动角反射器，实现了SAR二维天线方向图反演与辐射质量自动化评估。
然而，人工定标器与定标场的核心瓶颈日益凸显：一是定标器的研制、运输、布设、维护需耗费巨大人力物力，数量规模化提升难度极大，无法匹配百星级SAR星群的组网发展节奏；二是定标场空间覆盖范围有限，卫星重访周期长，无法实现高频次、全域化的定标需求；三是角反射器窄波束宽度要求与星载SAR大入射角变化范围存在天然矛盾，需人工频繁调整仰角，定标时效性严重不足。

##### 2.1.2 自然稳定目标定标场------广域覆盖新方向，受限于真值不确定性

为解决人工定标器时空覆盖的核心瓶颈，国内外学界开始探索利用自然界广泛存在的稳定地物作为定标参考目标，主要分为**自然稳定点目标**与**自然分布式均匀目标**两类，是当前SAR定标领域的研究热点。

**（1）自然稳定点目标**

自然稳定点目标是指具有类似人工定标器强散射、时序稳定特性的地物，包括通讯塔、输电塔、海上石油平台、抛物面天线、海上风车等。1999年，Usai等^\[1\]^研究发现，SAR图像中裸露岩石、人工建筑(如道路、房屋)在长时间序列上一直保持较高的相干性，并且可反演出时间序列的地表形变。1999年，Ferretti等^\[2\]^在此基础上提出了永久散射体技术，其基本思想是筛选出时序SAR图像上受去相干影响较小的点，提取并解算这些点的差分相位模型，提取形变相位。其后十余年，PS-InSAR技术逐步成熟应用。2010年，D\'Aria等^\[3\]^提出人工定标器与永久散射体（PS）结合的SAR辐射定标方法，利用PS点实现了卫星全任务周期的辐射稳定性监测，克服了人工定标器的成本瓶颈；2014年，Guarnieri等^\[4\]^从自然界永久散射体中提取点目标，并应用到SAR长期相对辐射定标与天线指向测试中，获得了1dB以内的精度。2018年，Guarnieri等^\[5\]^进一步将稳定点目标用于L/P波段SAR辐射定标和天线方向图估计中。2019年，Du等^\[6,7\]^通过FEKO电磁仿真计算抛物面天线的理论RCS，验证了抛物面天线作为星载SAR定标参考目标的可行性；2021年，李佳楠等^\[8\]^通过通讯塔RCS建模实现了SAR影像绝对辐射定标；2023年，Ying等^\[9,10\]^提出基于海上风电场的SAR绝对辐射定标方法，将海上风车作为稳定参考目标；Zakharov等^\[11,12\]^对里海石油平台的长时序观测表明，其L波段RCS稳定性极高，可作为定标参考目标。

但现有自然点目标定标方法仍存在显著局限：Biancardi等^\[13\]^指出，点目标的各向散射异性对成像角度、极化方式等条件要求严苛，微小的成像参数差异就会导致散射强度显著变化，定标精度难以保障；同时，自然点目标多分布不均，背景杂波对定标结果的干扰难以完全消除，仅能作为人工定标器的补充，无法成为星群定标的核心基准。

**（2）自然分布式均匀目标**

自然分布式均匀目标是指大面积、地表类型单一、后向散射特性时序稳定的自然场景，其广域分布特性可完美匹配SAR宽幅成像需求。亚马逊热带雨林是最早用于SAR定标的分布式目标，1985年Moore^\[14\]^首次提出利用亚马逊雨林进行星载SAR天线方向图估算，后续大量研究验证了其体散射特性导致后向散射系数几乎不随入射角变化，时序稳定性可达0.2dB/年以内，是Sentinel-1、ALOS
PALSAR、TerraSAR-X等多颗卫星的核心天然定标区。

为进一步扩展分布式目标的适用范围，国内外学界对其他场景展开了大量研究：2018年，中科院空天院Yang等^\[15\]^发现城区SAR影像的后向散射系数中值重心具有优异的时序稳定性，经神经网络筛选后定标精度可达0.21dB；Shangguan等^\[16\]^通过城区超像素点的辐射特性监测，进一步验证了城区目标的定标适用性；Zakharov等^\[17\]^发现智利阿塔卡马沙漠、亚马逊雨林、南极洲永久冰盖等分布式均匀目标的稳定性与人工角反射器的稳定性相当，南极沃斯托克湖甚至达到了3.5年内0.19dB的辐射稳定度。南美洲阿塔卡马沙漠3.5年内稳定度达0.52dB，均具备作为定标参考目标的潜力。

与此同时，国际上开始推动分布式目标的标准化与网络化建设。2021年，CEOS提出构建全球SAR辐射定标场网SARCalNet，旨在形成类似光学RadCalNet的全球标准化定标基准网络，目前已完成亚马逊雨林、包头条状靶标、澳大利亚昆士兰角反射器阵列等数十个目标的收录，推动分布式目标从零散研究走向标准化应用。

但现有自然分布式目标的应用仍存在核心瓶颈：一是除亚马逊雨林外，绝大多数分布式目标的后向散射系数随入射角、频段、极化方式的变化显著，在异星交叉定标中，成像参数差异会导致散射系数偏差超过2dB，无法直接作为定标基准；二是现有目标筛选多依赖均值、方差等统计特征，缺乏对地物电磁散射机理的物理反演与参数化表征，目标"真值"的不确定性限制了其从"相对校正"走向"绝对定标"；三是全球可用的标准化分布式目标数量仍严重不足，无法满足百星级SAR星群高频次、全域化的定标需求。

##### 2.1.3 数字定标场------物理驱动的数字孪生新趋势，尚处于起步探索阶段

数字定标场的概念最早源于光学几何定标，研究人员通过高分辨率DOM、DEM构建数字定标场，实现了遥感影像无场地几何定标；在光学辐射定标领域，稳定场定标技术(如敦煌戈壁场、青海湖场)通过长期监测地表反射率为卫星提供辐射基准^\[18\]^，中国科学院合肥物质科学研究院发展了动态辐射参数监测系统，并提出了多涂层结构的数字靶标场系统^\[19\]^，构建了覆盖103个定标场的全球定标场网数据库，通过多源数据融合为高分辨率卫星提供定标基准；国际上，CEOS构建的RadCalNet^\[20\]^、LANDNET等定标场网，通过多场地联合验证实现了光学卫星的常态化交叉定标。

而在SAR辐射定标领域，数字定标场的建设鲜有系统性研究，目前仅处于概念提出与初步探索阶段。现有研究中，Li等^\[8,21\]^通过电磁仿真软件构建通讯塔的散射模型，尝试将仿真结果作为定标参考真值，但仿真环境的理想性限制了实际定标精度；Zhou等^\[22,23\]^构建了包含57个伪不变分布目标的全球SAR-PICS库，为数字定标场的目标库建设奠定了基础；申请人前期研究中^\[24,25\]^，通过Oh模型、场景评估模型实现了分布式目标散射特性的入射角校正，为目标特性的数字化建模提供了可行路径。

在干涉SAR定标领域，也有利用数字高程模型开展定标的工作。北京大学遥感与地理信息系统研究所^\[26\]^基于参考数字高程模型发展了无人工靶标的机载InSAR动态定标技术，利用已知精度的参考DEM模拟SAR图像，并与InSAR生成的DEM进行对比，有效解决了传统方法中因初始值偏差导致的迭代发散问题。

随着数字孪生技术的发展，2023年中国科学院空天信息创新研究院提出"遥感实验场数字孪生体"概念，通过场景三维重建、模型耦合与动态演进、数据同化与模型优化，实现动态模拟的物理遥感实验场的协同观测技术。

总体来看，SAR辐射定标参考目标的发展呈现三大明确趋势：一是从人工专用设备向广域自然地物拓展，突破时空覆盖限制；二是从单一场地统计特征向物理驱动的全参数建模升级，解决真值不确定性问题；三是从离散场地向全球网络化、可动态调用的数字孪生基准场演进，匹配星群化发展需求。而当前SAR数字定标场的系统性研究仍属空白，是本项目的核心研究方向之一。

#### 2.2 遥感载荷协同辐射定标国内外发展趋势分析

协同辐射定标通过辐射基准的跨载荷、跨场地传递，解决多星观测的一致性问题，是星座化遥感发展的核心支撑技术，目前已形成**星间交叉定标**与**多场地网络化定标**两大核心技术路径，在光学领域已实现成熟业务化应用，在SAR领域正处于快速发展阶段。

##### 2.2.1 星间交叉辐射定标

星间交叉定标是通过已定标高精度传感器的观测值作为参考，实现待定标传感器的定标，核心是解决辐射基准的跨载荷传递问题，其技术成熟度与遥感载荷的星座化进程高度同步。

在光学遥感领域，交叉定标技术已形成完整的理论体系与业务化流程。从早期的光线匹配法，到光谱匹配法，再到辐射传输模型、瑞利散射校正法，光学交叉定标技术不断迭代升级；国际上，WMO和CGMS建立了全球星载交叉定标系统（GSICS），以MODIS、AIRS、IASI等高精度载荷为参考，实现了全球气象卫星的常态化交叉定标；国内针对HJ-CCD、GF1-WFV、ZY3-MSS等国产光学卫星，构建了完善的交叉辐射定标方法体系，实现了国产卫星定标频次从年级到月级的跨越。

在SAR遥感领域，交叉定标技术仍处于起步阶段，经历了从机载双星定标到星载分布式目标定标的技术演进。1993年，德国宇航中心Zink等在Oberpfaffenhofen定标场，通过多个人工定标器完成了两个机载SAR系统的交叉定标实验，首次验证了SAR交叉定标的可行性，定标精度达2dB；2001年，Wakabayashi等^\[27\]^完成了机载L波段SAR的交叉定标实验，从串扰、增益平衡等维度完成了定标精度评估；2004年，Zakharov等^\[28\]^通过抛物面天线完成了两个SAR系统的辐射稳定性交叉研究，但该方法对飞行路径、天气条件要求严苛，难以规模化应用。

上述早期研究均依赖人工定标器，无法突破定标频次的核心限制。直到2022年，Zhou等^\[24\]^首次提出基于自然分布式目标的星载SAR辐射交叉定标方法，通过筛选时序稳定的自然界面目标，基于Oh模型校正交叉双星的入射角差异，实现了Sentinel-1系列卫星的高精度交叉定标，定标精度控制在1dB以内，彻底摆脱了对人工定标器的依赖；2024年，Zhou等^\[25\]^进一步提出基于场景评估的入射角差异校正方法与加权回归定标系数求解方法，将交叉定标精度提升至0.5dB以内；同年，湘潭大学邓明军等^\[29\]^分析了建筑区域的SAR成像机制，构建了基于城区目标的SAR辐射交叉定标方案，不同卫星间的定标精度达0.36dB。

但现有SAR交叉定标方法仍存在核心瓶颈：一是本质上仍属于"点对点"的基准传递，仅能实现两颗卫星间的成对定标，面对百星级异构SAR星群，存在误差累积、链路不闭合的核心问题，无法实现星群全局辐射基准的统一；二是仅解决了入射角差异的校正问题，对异星间频段、极化方式、分辨率等成像参数差异的校正能力不足，异构载荷间的基准传递精度难以保障；三是未形成标准化的目标筛选与定标流程，无法实现业务化、自动化的高频次定标。

##### 2.2.2 多场地网络化协同定标

多场地网络化协同定标，是利用全球分布的定标场网作为中间媒介，通过多场地联合平差实现辐射基准的全局统一，是解决单一场地定标不确定性、实现星座级载荷定标的核心手段。

在光学领域，该技术已实现成熟应用。国际上，CEOS牵头建设的RadCalNet全球自动辐射定标网，已建成包头、La
Crau、Railroad Valley
Playa等5个核心站点，可提供可溯源的大气层顶反射率数据，Bouvet等验证了该网络可显著降低单点定标的不确定性；国内科研人员通过敦煌、塔克拉玛干、巴丹吉林等多个沙漠场地的联合定标，实现了国产光学卫星的宽动态辐射定标，解决了单一场地定标动态范围受限的核心问题。

在SAR领域，多场地网络化协同定标仍处于初步探索阶段。目前研究多局限于单星对多场的独立监测，2025年，Zhou等^\[22,23\]^首次提出基于多伪不变定标场的SAR宽动态辐射交叉定标方法，通过多个具有不同后向散射系数的稳定目标，扩展了定标动态范围，解决了单一场地定标误差易传递至全动态范围的问题；CEOS主导的SARCalNet网络，也正在推动全球定标场地的标准化与数据共享，为多场地协同定标奠定了基础。

但现有研究仍存在显著空白：缺乏类似光学领域的"星-地-星"联合平差机制，未建立统一的辐射归一化模型，无法将不同自然场景的观测数据映射到同一基准面，多场数据无法有效融合；同时，未考虑不同场地的质量差异与不确定度，定标权重分配缺乏理论依据，全局优化的鲁棒性不足。

总体来看，协同辐射定标的发展呈现两大核心趋势：一是从双星成对交叉定标，向百星级星群多场全局协同定标升级；二是从单一场地独立定标，向全球网络化多场联合平差演进。而现有SAR协同定标技术，仍未突破成对定标的局限，无法适配SAR星群的发展需求，这是本项目的核心解决方向。

#### 2.3 遥感载荷时间序列辐射定标国内外发展趋势分析

时间序列辐射定标，旨在通过多时相数据的协同分析，监测载荷全生命周期的辐射性能演变，实现定标系数的动态优化，核心是解决跨时相定标误差与载荷本征衰变的解耦问题，是保障长时序遥感数据一致性的核心技术，在光学领域已形成完善体系，在SAR领域仍处于空白探索阶段。时间序列辐射定标的发展脉络如图3所示。

![](./image2.emf)

图3  遥感载荷时间序列辐射定标发展脉络图

##### 2.3.1 光学领域时间序列辐射定标已形成成熟技术体系

光学遥感领域的时间序列辐射定标，已发展出三类核心技术路径，形成了从载荷衰变监测到定标系数动态优化的完整业务化流程。

一是基于自然稳定场景的时间序列定标。1993年，Henry等^\[30\]^首次通过稳定沙漠场景的长时序观测，实现了SPOT-1/2卫星HRV载荷的辐射稳定性监测；后续Cosnefroy^\[31\]^、Rao^\[32\]^、Heidinger等^\[33\]^学者，利用全球多个沙漠稳定场景，实现了AVHRR传感器全生命周期的时间序列定标，建立了载荷衰变的量化模型；Fougnie等^\[34\]^也通过沙漠场进行了POLDER的在轨测量，发现了POLDER性能的非线性并提出了校正模型。Tahnk等^\[35\]^利用极地场景获得了NOAA-14不同时期的时间序列定标系数，有效地反映了传感器辐射性能的变化情况；Angal等^\[36\]^、谢玉娟^\[37\]^分别基于沙漠场景完成了Landsat-7/ETM+、MODIS以及HJ-1
CCD的长时序性能监测任务。2015年，王玲等^\[38\]^利用沙漠、盐湖等多种亮度稳定目标，结合MODIS地表和大气参数产品以及大气辐射传输模型，进行了FY-3C/MERSI的时间序列定标。2016年，Wu等^\[39\]^分别采用与Aqua/MODIS同步过境、沙漠场景、雪场景三种方法来衡量Suomi-NPP/VIIRS传感器的辐射稳定性，为VIIRS发射后的校准稳定性和一致性提供了有效信息。

二是基于定标场的时间序列定标。2012年，孙凌等^\[40\]^以敦煌定标场为参考，获取了FY-3A/MERSI载荷各通道的衰变曲线，完成了载荷在轨响应变化的量化分析；邱刚刚^\[41\]^、韦玮等^\[42\]^提出基于全球广泛分布的辐射校正场，实现了MODIS、GF1/WFV载荷的高频次时间序列定标，定标结果与官方发布系数具有良好一致性。

三是基于交叉定标的时间序列定标。2000年，Cabot等^\[43\]^以POLDER为参考卫星，完成了Vegetation、AVHRR、SeaWiFS三个传感器的时间序列定标；国内李小英等^\[44\]^在2005年以MODIS为参考，实现了CBERS-02卫星CCD相机的时间序列交叉定标；随后2006年^\[45\]^在考虑地物BRDF特性的基础上，再次利用交叉定标实现该卫星的时间序列定标。邵雯^\[46\]^、胡新凯^\[47\]^等利用交叉定标方法，选取适当地物目标和已高精度定标的卫星为参考，实现了GF1-WFV的时间序列定标。Wang^\[48\]^、Liu^\[49\]^等分别以Sentinel-2/MSI、Terra/MODIS为参考，实现了GF-6/WFV、HJ-1A/CCD1载荷的长时序交叉定标。高海亮等^\[50\]^分别采用上述三种方法对CBERS02B星的CCD相机开展时间序列定标，分别得到CCD相机2007---2008年期间三种方法对应的定标系数，分析比较了三种方法的优缺点。

针对传统时序定标中定标误差与载荷衰变混叠的核心问题，豆新格等提出基于卡尔曼滤波的光学时间序列定标方法，利用不同时相定标结果的相关性，对定标系数进行动态优化，有效降低了单时相定标的不确定性，实现了定标随机误差与载荷缓变衰变的初步解耦。

##### 2.3.2 SAR领域时间序列辐射定标仍处于性能监测阶段，核心技术存在空白

相较于光学领域的成熟应用，SAR领域的时间序列辐射定标相关研究极少，目前仍停留在载荷辐射性能的长时序监测层面，未形成真正的时序定标理论与方法体系。

2013年，Miranda等^\[51\]^通过荷兰定标场角反射器的时序后向散射系数，监测了ENVISAT
ASAR卫星的辐射性能变化；2016年，EI
Hajj等^\[52\]^通过分析来自不变目标的后向散射系数的时序变化，对Sentinel-1A传感器的辐射稳定性进行了评估。2018年，Schwerdt等^\[53\]^以德国DLR定标场角反射器为参考，持续监测了TerraSAR-X、TanDEM-X卫星超过10年的辐射稳定性与性能变化；2024年，史磊等^\[54\]^以亚马逊热带雨林为观测对象，分析了我国LT-1A卫星全极化SAR辐射与极化系统误差的时序稳定性。

上述研究仅实现了SAR载荷辐射性能的定性监测，并未真正涉及星载SAR时间序列定标方法与载荷衰变模型的构建，核心技术空白包括：一是未建立多时相定标结果的协同优化机制，传统单时相独立定标模式，无法分离定标随机误差与载荷本征衰变，定标结果的时序一致性差；二是未构建SAR载荷全生命周期的辐射衰变特征模型，无法实现载荷性能异常突变的自动识别与定标系数的动态订正；三是未形成时序定标精度的量化评估与不确定性分析体系，定标结果的可靠性无法保障。

总体来看，时间序列辐射定标的发展趋势十分明确：从单时相独立定标，向多时相协同递归优化升级；从载荷性能定性监测，向衰变特征定量建模与动态解耦演进。而SAR领域在该方向的系统性研究仍属空白，是本项目的核心突破点。

### 2.4 国内外研究现状小结

综合以上分析，可总结出SAR辐射定标领域的三大核心发展趋势，以及现有研究的核心瓶颈与空白：

第一，定标参考目标正从人工专用定标器，向广域自然稳定目标、数字化孪生定标场演进。人工定标器虽精度可控，但成本高、数量少、时空覆盖能力不足，无法匹配SAR星群的发展需求；自然稳定目标虽广域分布，但真值不确定性、成像参数敏感性问题尚未解决；SAR数字定标场是未来的核心发展方向，但目前仍缺乏系统性的理论与方法研究。

第二，定标模式正从单星单场独立定标、双星成对交叉定标，向百星级星群多场全局协同定标发展。光学领域已形成成熟的全球协同定标体系与业务化流程，而SAR领域仍停留在成对交叉定标阶段，缺乏星群辐射基准全局传递与优化的理论模型，无法实现异构星群的辐射一致性统一。

第三，定标维度正从单时相静态定标，向全生命周期时序动态定标升级。光学领域已实现载荷衰变与定标误差的有效解耦，而SAR领域仍停留在载荷性能定性监测层面，缺乏顾及时间相关性的时序定标优化方法，无法保障长时序SAR数据的辐射一致性。

本项目正是顺应上述三大发展趋势，针对现有研究的核心空白，开展基于数字基准场的SAR星群泛在协同辐射定标方法研究，突破自然稳定目标散射特性跨参数泛化建模、异构星群辐射基准全局协同优化、跨时相定标误差与载荷衰变动态解耦三大关键科学问题，为我国百星级SAR星群的高频次、高精度辐射定标提供理论与方法支撑。

\[1\] Usai S, Klees R. SAR interferometry on a very long time scale: a
study of the interferometric characteristics of man-made features\[J\].
IEEE Transactions on Geoscience and Remote Sensing, 1999, 37(4):
2118-2123.

\[2\] Ferretti A, Prati C, Rocca F. Permanent scatterers in SAR
interferometry\[C\]//IEEE International Geoscience and Remote Sensing
Symposium: 卷 3. IEEE, 1999: 1528-1530.

\[3\] D\'Aria D, Ferretti A, Guarnieri A M, et al. SAR calibration aided
by permanent scatterers\[J\]. IEEE Transactions on Geoscience and Remote
Sensing, 2010, 48(4): 2076-2086.

\[4\] Guccione P, Guarnieri A M, Zonno M. Azimuth antenna maximum
likelihood estimation by persistent point scatterers in SAR images\[J\].
IEEE Transactions on Geoscience and Remote Sensing, 2014, 52(2):
947-955.

\[5\] Guccione P, Scagliola M, Giudici D. Low-frequency SAR radiometric
calibration and antenna pattern estimation by using stable point
targets\[J\]. IEEE Transactions on Geoscience and Remote Sensing, 2018,
56(2): 635-646.

\[6\] Du S, Hong J, Wang Y, et al. Analysis of Using the Parabolic
Antenna as the Passive Calibrator for P-Band Spaceborne SAR Radiometric
Calibration\[J\]. Remote Sens., 2021, 13(21): 4300.

\[7\] Du S, Hong J, Wang Y, 等. Investigation of Parabolic Antennas As
Potential Calibrators For Spaceborne P-band POLSAR
Calibration\[C\]//2019 6th Asia-Pacific Conference on Synthetic Aperture
Radar (APSAR). 2019: 1-4.

\[8\] 李佳楠, 李玉, 赵泉华, 等.
基于通讯信号塔RCS建模的SAR影像绝对辐射定标\[J\].
武汉大学学报(信息科学版), 2021, 46(11): 1746-1755.

\[9\] Ying Q, Zhou Y, Yin Q, et al. SAR absolute radiometric calibration
method based on offshore wind farm\[C\]//IET Conference Proceedings:
Vol. 2023. 2023: 3507-3512.

\[10\] Zhou Y, Ying Q, Yin Q, et al. SAR absolute radiometric
calibration utilizing offshore wind farms with mask-based response
energy extraction approach\[J\]. IEEE Journal of Selected Topics in
Applied Earth Observations and Remote Sensing, 2025, 18: 16816-16830.

\[11\] Zakharov A, Zakharova L, Sorochinsky M, et al. Oil Platforms as
SAR calibration Targets in C and L bands\[C\]//Eur. Conf. Synth.
Aperture Radar. 2018: 1-4.

\[12\] Zakharov A, Zakharova L, Sorochinsky M, et al. Oil platforms in
Caspian Sea as stable distributed radar scatterers for PALSAR
calibration\[C\]//IEEE Int. Geosci. Remote Sens. Symp. 2016: 3859-3862.

\[13\] Biancardi P, Iannini L, d'Alessandro M, et al. Performances and
limitations of persistent scatterers-based SAR calibration\[C\]//2010
IEEE Radar Conference. IEEE, 2010: 762-766.

\[14\] Moore R, Westmoreland V, Frank D, et al. Determining the vertical
antenna pattern of a spaceborne SAR by observation of uniform
targets\[C\]//IEEE International Geoscience and Remote Sensing
Symposium: Vol. 1. IEEE, 1986: 469-472.

\[15\] Yang J, Qiu X, Ding C, et al. Identification of stable
backscattering features, suitable for maintaining absolute synthetic
aperture radar (SAR) radiometric calibration of sentinel-1\[J\]. Remote
Sensing, 2018, 10(7): 1010.

\[16\] Shangguan S, Qiu X, Fu K. Research on A Special Hyper-Pixel for
SAR Radiometric Monitoring\[J\]. Remote Sensing, 2023, 15(8): 2175.

\[17\] Zakharov A, Zakharova L. Palsar calibration with distributed
targets\[C\]//2019 IEEE International Geoscience and Remote Sensing
Symposium. IEEE, 2019: 8328-8331.

\[18\] 徐文斌, 史剑民, 郑小兵, 等. 全球定标场网数据库的设计与应用\[J\].
光学学报, 2014, 34(11): 9-19.

\[19\] Qiao Y, Zheng X, Wang X, 等. Whole-process radiometric
calibration of optical remote sensors\[J\]. Journal of Remote Sensing,
2006, 10(5): 616-623.

\[20\] Bouvet M, Thome K, Berthelot B, et al. RadCalNet: a radiometric
calibration network for Earth observing imagers operating in the visible
to shortwave infrared spectral range\[J\]. Remote Sensing, 2019, 11(20):
2401.

\[21\] Li J, Li Y, Zhao Q, et al. SAR Image Absolute Radiometric
Calibration Based on RCS Modeling of Communication Tower\[J\]. Geomat.
Inf. Sci. Wuhan Univ., 2021, 46(11): 1746-1755.

\[22\] Chen X, Zhou Y, Ma F, et al. Optimized Selection of
Pseudo-Invariant Calibration Sites for Radiometric Cross-Calibration of
Spaceborne Sar Sensors\[C\]//2023 SAR in Big Data Era (BIGSARDATA).
Beijing, China: IEEE, 2023: 1-4.

\[23\] Zhou Y, Chen X, Yin Q, et al. SAR Radiometric Cross-Calibration
Based on Multiple Pseudoinvariant Calibration Sites With Extensive
Backscattering Coefficient Range\[J\]. IEEE Journal of Selected Topics
in Applied Earth Observations and Remote Sensing, 2025, 18: 4836-4849.

\[24\] Zhou Y, Zhuang L, Duan J, 等. Synthetic Aperture Radar
Radiometric Cross Calibration Based on Distributed Targets\[J\]. IEEE
Journal of Selected Topics in Applied Earth Observations and Remote
Sensing, 2022, 15: 9599-9612.

\[25\] Zhou Y, Yang B, Yin Q, et al. Improved SAR Radiometric
Cross-Calibration Method Based on Scene-Driven Incidence Angle
Difference Correction and Weighted Regression\[J\]. IEEE Transactions on
Geoscience and Remote Sensing, 2024, 62: 1-16.

\[26\] 云烨, 曾琪明, 焦健, 等. 基于参考DEM的机载InSAR定标方法\[J\].
测绘学报, 2014, 43(01): 74-82.

\[27\] Wakabayashi H, Tadono T, Matsuoka M, et al. Cross-calibration
experiment of airborne L-band polarimetric SAR\[C\]//IEEE 2001
International Geoscience and Remote Sensing Symposium (IGARSS): Vol. 1.
IEEE, 2001: 423-425.

\[28\] Zakharov A, Zherdev P, Sokolov A. Intercalibration of ERS AMI and
envisat ASAR with ground-based parabolic antennas\[C\]//2004 Envisat &
ERS Symposium. Salzburg, Austria, 2004.

\[29\] Deng M, Chen R, Chen Z, et al. Spaceborne SAR radiometric
cross-calibration considering typical scattering effects in building
areas\[J\]. IEEE Transactions on Geoscience and Remote Sensing, 2024,
62: 1-11.

\[30\] Henry P, Dinguirard M, Bodilis M. SPOT multitemporal calibration
over stable desert areas\[J\]. Recent Advances in Sensors, Radiometric
Calibration, and Processing of Remotely Sensed Data, 1993, 1938: 67-76.

\[31\] Cosnefroy H, Leroy M, Briottet X. Selection and characterization
of saharan and arabian desert sites for the calibration of optical
satellite sensors\[J\]. Remote Sensing of Environment, 1996, 58(1):
101-114.

\[32\] Rao C N, Chen J. Revised post-launch calibration of the visible
and near-infrared channels of the advanced very high resolution
radiometer (AVHRR) on the NOAA-14 spacecraft\[J\]. International Journal
of Remote Sensing, 1999, 20(18): 3485-3491.

\[33\] Heidinger A K, Sullivan J T, Rao C R N. Calibration of visible
and near-infrared channels of the NOAA-12 AVHRR using time series of
observations over deserts\[J\]. International Journal of Remote Sensing,
2003, 24(18): 3635-3649.

\[34\] Fougnie B, Hagolle O, Cabot F. In-flight measurement and
correction of nonlinearity of the POLDER-1's sensitivity\[C\]//8th
Symposium of the International Society for Photogrammetry and Remote
Sensing. Aussois, France, 2001: 8-12.

\[35\] Tahnk W, Coakley Jr J. Improved calibration coefficients for
NOAA-14 AVHRR visible and near-infrared channels\[J\]. International
Journal of Remote Sensing, 2001, 22(7): 1269-1283.

\[36\] Angal A, Xiong X, Choi T, 等. Using the Sonoran and Libyan Desert
test sites to monitor the temporal stability of reflective solar bands
for Landsat 7 enhanced thematic mapper plus and Terra moderate
resolution imaging spectroradiometer sensors\[J\]. Journal of Applied
Remote Sensing, 2010, 4(1): 043525.

\[37\] 谢玉娟. 基于沙漠场景的HJ-1CCD相机在轨辐射定标研究\[D\]. 焦作:
河南理工大学, 2011.

\[38\] 王玲, 胡秀清, 陈林.
基于多种亮度稳定目标的FY-3C/中分辨率光谱成像仪的反射太阳波段辐射定标\[J\].
光学精密工程, 2015, 23(7): 1911-1920.

\[39\] Wu A, Xiong X, Cao C, 等. Assessment of SNPP VIIRS VIS/NIR
radiometric calibration stability using Aqua MODIS and invariant surface
targets\[J\]. IEEE Transactions on Geoscience and Remote Sensing, 2016,
54(5): 2918-2924.

\[40\] 孙凌, 郭茂华, 徐娜, 等. 基于敦煌场地定标的FY-3
MERSI反射太阳波段在轨响应变化分析\[J\]. 光谱学与光谱分析, 2012, 32(7):
1869-1877.

\[41\] 邱刚刚. 卫星辐射校正场自动化观测系统的研制与定标应用\[D\]. 合肥:
中国科学技术大学, 2017.

\[42\] 韦玮, 张艳娜, 张孟, 等.
高分一号宽视场成像仪多场地高频次辐射定标\[J\]. 光子学报, 2018, 47(2):
0228001.

\[43\] Cabot F, Hagolle O, Henry P. Relative and multitemporal
calibration of AVHRR, SeaWiFS, and VEGETATION using POLDER
characterization of desert sites\[C\]//IEEE International Geoscience and
Remote Sensing Symposium (IGARSS): Vol. 5. IEEE, 2000: 2188-2190.

\[44\] 李小英, 顾行发, 余涛, 等.
考虑地物BRDF特性改进后的CBERS-02卫星CCD相机的辐射定标系数\[J\].
遥感学报, 2006, 10(5): 636-643.

\[45\] 李小英, 顾行发, 余涛, 等.
考虑地物BRDF特性改进后的CBERS-02卫星CCD相机的辐射定标系数\[J\].
遥感学报, 2021, 25(5): 636-643.

\[46\] 邵雯, 谢勇, 宦海, 等. "高分一号"宽幅多光谱相机时间序列定标\[J\].
现代电子技术, 2020, 43(10): 33-37.

\[47\] 胡新凯. 基于稳定目标场的高分一号卫星时间序列交叉定标研究\[D\].
桂林: 桂林理工大学, 2020.

\[48\] Wang Y, Liu Y, Zhao W, 等. Time-series cross radiometric
calibration and validation of GF-6/WFV using multi-site\[J\]. Remote
Sensing, 2024, 16(7): 1287.

\[49\] Liu L, Shi T, Gao H, 等. Long-term cross calibration of HJ-1A
CCD1 and Terra MODIS reflective solar bands\[J\]. Scientific Reports,
2021, 11(1): 7386.

\[50\] 高海亮, 顾行发, 余涛, 等.
CCD卫星相机时间序列定标--以CBERS02B为例\[J\]. 测绘学报, 2011, 40(2):
180.

\[51\] Miranda N, Meadows P, Piantanida R, 等. Sentinel-1A/B SAR
Calibration and Performance Status\[C\]//13th European Conference on
Synthetic Aperture Radar. 2021: 1-4.

\[52\] El Hajj M, Baghdadi N, Zribi M, 等. Analysis of Sentinel-1
radiometric stability and quality for land surface applications\[J\].
Remote Sensing, 2016, 8(5): 406.

\[53\] Schwerdt M, Schmidt K, Klenk P, et al. Radiometric performance of
the TerraSAR-X mission over more than ten years of operation\[J\].
Remote Sensing, 2018, 10(5): 754.

\[54\] 史磊, 孙维东, 杨乐, 等. LT-1A
卫星全极化SAR辐射与极化系统误差稳定性分析: 以热带雨林场景为例\[J\].
雷达学报, 2024, 13: 1-19.
