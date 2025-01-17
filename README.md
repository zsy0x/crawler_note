# 项目

## 1，项目简介

在“双碳”和可持续发展背景下，骑行旅游因其绿色、健康、灵活和自主的特点，成为旅游领域的“新宠”。骑行旅游不仅促进区域经济，还作为传统旅游的补充，推动旅游业可持续发展。正如Han等人所说：“自行车具有巨大可持续效益，无疑是现在旅游业的一个新兴趋势，无疑是一个光明的新未来。

游客运动分析是了解旅游者行为的关键，与以往注重心理情感的旅游研究不同，它主要分析游客在旅行中的时空行为及体验信息。研究游客的时空行为，首先需要获取他们的运动轨迹，过去常用问卷调查、访谈等方法收集数据，现在GPS技术因其多元、低成本、易获取的特点，成为研究微观行为模式的重要方法。西安作为西部旅游中心，拥有丰富旅游资源和骑行条件，骑行旅游发展成熟，**项目利用两步路平台的GPS数据，研究西安骑行游客的时空行为，探究这些行为背后的规律以及游客出行偏好，对骑行旅游发展具有重要借鉴意义**。

## 2，特征数据feature_liangbulu.json

![image](https://github.com/user-attachments/assets/b0eafd98-6991-49f1-bb78-09fea26f442e)

## 3，轨迹数据data_liangbulu

项目使用python编写脚本，将约束条件定义为2022年及以前，西安市，骑行，长度大于50KM，以此来收集西安市骑行的GPS轨迹数据。

从网站上获取骑行游客自愿分享的3947条轨迹，并从kml格式转换为csv格式，每一条轨迹包含时间戳，经纬度以及海拔数据。

![image](https://github.com/user-attachments/assets/2779073d-84cd-469f-9f90-2b6f9bafefeb)

由于开放式GPS轨迹数据经常存在信息错误导致用户轨迹不完整，因此对轨迹数据进行处理，去除以下两种类型的问题轨迹：1. 从同一用户复制的轨迹，即重复轨迹；2. 缺乏基本信息（例如，日期时间、海拔、经度、纬度）的轨迹。在进行上述清洗过后对轨迹进行粗粒度的研究时，发现仍存在很多异常数据，如海拔过大或过小，起始时间大于终止时间等，在对这些异常轨迹进行处理后，获得最终数据集，包括3310条有效轨迹，总共18171893个轨迹点。

## 4，图片数据graph_liangbulu

从网站上获取730名骑行游客上传到平台的16767张地理标记照片，包括骑行者的骑行记录、风景照、路面标识等，其中每张照片附带有游客的骑行距离，可以反映出游客的旅行足迹。通过检测照片中的内容可以说明游客在骑行中最喜欢拍摄什么东西，进而探究哪些因素可以吸引骑行的游客。

![image](https://github.com/user-attachments/assets/3712c2e1-2dd8-4cfe-8d2d-3d7cbbcf2683)

## 5，结论与建议

### 5.1，结论

了解骑行游客的时空行为，为政府和相关旅游组织对规划骑行路线和发展骑行旅游POI提供关键信息。传统上，这种努力必须依赖于官方的统计数据或调查数据，但技术的发展使研究人员能够试验新的数据源，允许实时数据的可用性。GPS轨迹数据是这些新数据源的一个例子，它具有独特的优势：（1）连续实时记录骑行游客的位置，（2）可以可视化为易于解释的“信息图”，指导旅游管理。以西安为例，探讨了以下的时空行为：

(1) 轨迹数据的逐年增加表明近年来骑行旅游得到迅速发展，越来越多的游客投身于骑行旅游当中。

(2) 西安市骑行游客大多集中在3-10月份，受季节影响较大；大部分骑行游客会选择在周末出行，周内出行的每日骑行量大致相同，体现了骑行休闲旅游的特征；大部分骑行游客选择在上午6-10点出发，而还有少部分的游客选择在夜晚或凌晨出发，这些人将更值得被关注。

(3) 西安市海拔差异较大，大部分的轨迹最高海拔与最低海拔之间的海拔差集中在0-250米，少部分的轨迹海拔差在250-1000米之间，而更少部分轨迹的海拔差在1000米以上。

(4) 受气候影响，骑行轨迹的数量具有明显的季节性波动特征，与中国旅游业和经济周期吻合较长。

(5) 市内和市外轨迹的数量都呈现逐年递增的趋势，大部分停留点所处的位置都集中在西安市的市中心地区，因为市中心通常是商业、文化和旅游活动的中心，吸引了大量的骑行游客，还有一部分停留点分布在西安市南部的秦岭地区，秦岭地区以其壮丽的自然风光和独特的生态环境而闻名，吸引了许多骑行爱好者。

(6) 大部分的骑行者都会选择往返路程，也映证了西安市骑行的特点为城市运动骑行，而非长路段的旅游骑行。

(7) 山地骑行出发时间相对集中，而城区骑行出发时间相对分散。山地骑行者常在早上7至10点出发，前往较远的秦岭峪口，早上气温凉爽，避开高温，骑行更舒适。城区骑行出发时间较分散，但上午9至10点为高峰，此时交通缓和，便于城市骑行。山地骑行停留时间大多在0-3个小时，城区骑行停留时间峰值大多在0-1小时。

(8) 骑行中出现频率最高的对象类别是car，这是由于骑行轨迹大都经过城市道路或者国道等车流量、人流量比较大的环境；对于城市骑行来说，大多数为单人骑行，但对于山地骑行来说，组团骑行是更多人的选择；出现频率较高的对象类别还有bowl、bottle、bench、chair、potted plant等，这些类别更倾向于休息和补充体力，说明骑行者停下拍照的地点环境比较好，比较适宜中途休息，补充体力。

(9) 检测出bowl和chair的轨迹90%都是山地骑行轨迹，这可能是因为山地骑行中更需要中途进餐和补充体力。

(10) 最受骑行游客欢迎的“热点”集中在风景名胜区，这些地点通常位于城市历史文化区、自然保护区等，环境优美，资源丰富，吸引大量游客骑行观光。

### 5.2，建议

从学术角度来看，本研究中应用的方法被证明是一个合适的工具来调查研究骑行时空行为，这些研究结果也提出了当地政府和相关旅游组织可能遵循的一些潜在的发展路径，以提高西安骑行旅游的吸引力，以造福该地区的经济。虽然本文提出的研究结果涉及到一个特定的区域，但本文的主要目的是介绍应用GPS轨迹数据的方法，以有利于旅游管理。如果存在合适的社交媒体数据源，本文提出的可视化和方法可以相对容易和低成本地应用于其他地区。

对于骑行者，可以参考上述的结论选择合适的骑行时间与骑行地点，如考虑在春季和秋季骑行，这时温度较为宜人，适合进行长时间的骑行活动。由于早晚温差较大，可以选择在温暖的白天骑行，避免高温和寒冷时段。

对于旅游管理部门，对轨迹数量的月度分布进行分析可以帮助旅游管理部门或者道路规划部门进行资源分配，以满足不同月份的需求。例如，在高峰期，相关管理部门可以做好骑行道路周边的基础设施建设，以提升骑行游客的满意度。同时，对轨迹数量的月度分布进行监测还可以帮助相关管理部门及时发现业务异常和风险事件。例如，如果某个月份的轨迹数量明显偏离原分布，这可能意味着面临着某种风险或发生了某些事件，需要及时采取措施来降低风险。

## 6，参考文献

[1] 张朝枝,张鑫.流动性的旅游体验模型建构——基于骑行入藏者的研究[J].地理研究, 2017, 36(12): 2332-2342.

[2] 王汝辉,马志新.客观本真与存在本真的互动:川藏线骑行旅游研究[J].四川师范大学学报(社会科学版), 2020, 47(6):64-73.

[3] 吕旭涛, 洪鹏飞. 基于网络文本分析的自行车骑行行为与空间特征研究[J]. 北京体育大学学报, 2018 (5):32-39.

[4] 邓冰,陈玲玲,张翾.国外自行车旅游研究综述[J].旅游学刊,2015,30(3):116-126.

[5] https://www.baidu.com/s?ie=UTF-8&wd=西安市区域图.

[6] 王坤,雷振仙.山地骑行旅游的时空特征及形成机理——以贵州省为例[J].旅游科学,2023,37(02):133-154.

[7] 张强,白征东,辛浩浩,等.基于共享单车时空大数据的细粒度聚类[J].测绘通报,2021,(05):15-19+29.

[8] Han H, Lho L H, Al-Ansi A, et al. Cycling tourism: a perspective article[J]. Tourism review, 2020, 75(1): 162-164.

[9] Mou N, Liu Z, Zheng Y, Makkonen T, Yang T, Zhang L. Cycling in Tibet: An analysis of tourists’ spatiotemporal behavior and infrastructure[J]. Tourism Management, 2022, 88: 104418.

[10] Majumdar B B, Mitra S. Analysis of bicycle route-related improvement strategies for two Indian cities using a stated preference survey[J]. Transport policy, 2018, 63: 176-188.

[11] Simonsen P S, Jorgenson B, Robbins D. Cycling Tourism [M].Bornholm: Unit of Tourism Research at Research Centre of Bornholm, 1998.

[12] Yeh C C, Lin C J Y, Hsiao J P H, et al. The effect of improving cycleway environment on the recreational benefits of bicycle tourism[J]. International journal of environmental research and public health, 2019, 16(18): 3460.

[13] Hagen S, Boyes M. Affective ride experiences on mountain bike terrain[J]. Journal of outdoor recreation and tourism, 2016, 15: 89-98.

[14] Nugraha M H, Chahyati D. Tourism object detection around monumen nasional (monas) using YOLO and retinanet[C]//2020 International Conference on Advanced Computer Science and Information Systems (ICACSIS). IEEE, 2020: 317-322.
