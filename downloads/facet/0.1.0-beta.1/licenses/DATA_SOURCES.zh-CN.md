[English](DATA_SOURCES.md) | **简体中文**

# 科学数据来源

Facet 0.1.0-beta.1 · 2026-11-08

## 目录

1. [结论](#findings)
2. [共价半径](#covalent)
3. [范德华半径](#vdw)
4. [电子组态](#configurations)
5. [原子量与示例](#masses)
6. [配色与参考样式](#palettes)
7. [兼容性与未决项](#compatibility)
8. [文献](#references)

<a id="findings"></a>
## 结论

当前结果见 [beta1-data-review.json](beta1-data-review.json)；[historical-data-audit.json](historical-data-audit.json) 是修正前快照。本轮未跑自动化测试。数值匹配只证明与指定参考相符，不证明历史复制路径，也不表示适用于全部配位、自旋或氧化态。

<a id="covalent"></a>
## 共价半径

前端与 Rust 共用一份 Cordero 2008 表 2 的 H–Cm 共 96 项数据。C 使用 sp3 的 0.76 Å，Mn/Fe/Co 使用低自旋 1.39/1.32/1.26 Å，程序不随环境自动改变选择。原有 84 项数值不变；新增 12 项如下，其中 10 项数值改变，At/Rn 数值不变但由兜底改为文献来源。

| 元素 | 参考值 (Å) | 旧值 (Å) |
| --- | ---: | ---: |
| Pm | 1.99 | 1.50 |
| Po | 1.40 | 1.50 |
| At | 1.50 | 1.50 |
| Rn | 1.50 | 1.50 |
| Fr | 2.60 | 1.50 |
| Ra | 2.21 | 1.50 |
| Ac | 2.15 | 1.50 |
| Pa | 2.00 | 1.50 |
| Np | 1.90 | 1.50 |
| Pu | 1.87 | 1.50 |
| Am | 1.80 | 1.50 |
| Cm | 1.69 | 1.50 |

Bk–Og 共 22 项保留 1.50 Å 兜底，不归于 Cordero。修订号 `cordero2008-20261108` 加入共价自动键指纹。将来重建的 Rust 消费者也会读取新表；公开 ftkit 旧包本次未重建。

<a id="vdw"></a>
## 范德华半径

保留原有 95 个显式数值和 2.00 Å 默认值。这是混合参考集合，不能称为统一 Alvarez 表；文献参考也不等于直接实验测量。118 个元素分为 73 项参考、3 项估算、13 项汇编、29 项兜底。

| 来源 | 数量 | 说明 |
| --- | ---: | --- |
| Mantina 2009，表 12 | 41 | 主族推荐/理论参考。 |
| Batsanov 2001，表 9 上行 | 26 | 晶体统计参考。 |
| Bondi 1964，表 I/XIV | 6 | H、Li、Br、Ni、Cu、Zn。 |
| Batsanov 2001，表 2 | 1 | Fe 2.00 Å，估算；不是表 9 的 2.05 Å。 |
| Hu 2003；Hu 2009 对照列 | 1 | Ag 2.03 Å 估算，未换成 2009 推荐的 2.11 Å。 |
| Hu 2009，表 1 脚注 c | 1 | Cd 2.18 Å，Cd(II)–O 键价估算。 |
| BODR 固定版本 | 13 | Ce、Pr、Nd、Sm、Eu、Gd、Tb、Dy、Ho、Er、Tm、Yb、Lu。 |
| 程序兜底 | 29 | Pm、Ac、Pa、Np、Pu、Am、Cm、Bk–Og，均为 2.00 Å。 |

六个原有显式 2.00 Å 重分类为兜底，不改变数值，也不倒推历史填写意图。BODR 固定为 `c22a200776984388564ef90536d8af24ae09d21e`；仓库 CC0 与 XML 旧 MIT 元数据差异在 sources.json 保留。状态栏直接标记估算/汇编/兜底，提示与可访问说明给出来源。

<a id="configurations"></a>
## 电子组态

H–Hs 共 108 项逐项核对 NIST 中性原子基态；Mt–Og 共 10 项核对 Smits 等（2023）表 2，第 34 页，展开 [No]/[Cn] 核并合并相对论子壳层记法。仅 Lr 从 `[Rn] 5f14 6d1 7s2` 改为 `[Rn] 5f14 7s2 7p1`，采用 NIST，而不是该综述的旧 Lr 行。Rf–Og 标记理论预测；其余参考项也不宣称全部实测。

本地价电子显示约定保留 f 区的 f 壳层，所以 Lr 显示 `5f14 7s2 7p1`；这不是完整组态或唯一价电子定义。保留 NIST 非 SRD 完整条款，不笼统称全球公有领域；Smits 采用 CC BY 4.0，附署名、链接、全文和改编说明。未继续以未核实 LANL 链接作为当前许可依据。

<a id="masses"></a>
## 原子量与示例

83 项 ABACUS 质量原经 ASE 转录，本轮与 Meija 等 IUPAC 2013 评估报告（2016 发表）独立核对：69 项对应表 1，12 项为表 3 约定值；Tc=97.90721、Pm=144.91276 对应表 4 的 98Tc、145Pm 同位素质量，不是标准原子量。旧注释“最稳定同位素”改为明确质量数；数值不变。没有分发 ASE 运行代码。

APNS 仅内置 83 个元素的文件名和质量，不附带伪势/轨道二进制。保留 v1 efficiency 归档身份与 SHA-256 `869ba0765194c4c699153d8856078f5a1d7330b146dfe4b07235d13d3541d68f`，本轮未重下整套输入，也不重新授权它。内置结构是演示模型，不是认证实验结构；本轮未完整审计所有外部样例。

<a id="palettes"></a>
## 配色与参考样式

newVESTA 作者于 2026-11-08 确认自写。五套 NV_* 旧配色展开继承后各 25 项均匹配前身，归属确认不替代单独引入数据的来源核对。84 项基础颜色、全部命名配色及 ID 保持不变。

- JMOL 30/30 匹配 Jmol 12.1.15 / revision 14469，保守保留 LGPL-2.1-or-later 原文及版权，无 Jmol 运行库，也不为 Facet 自有代码声明 LGPL。
- NV_MATERIAL_STUDIO 25 项中 23 项同 Jmol，Mo/Te 不同；变量名不能证明商业 Materials Studio 来源。
- 旧 VESTA 表与官方 3.5.8 elements.ini 比较，27 项中 9 同、18 不同，不是精确默认副本。官方文件仅本地核对，没有再分发。
- Studio 118 项有本地补齐/调色历史（617e3956），没有完整官方版本/取得记录；与 Jmol 不同不能证明独立来源。CPK 名称同样不是具体许可。
- Matplotlib 3.10.7 的 magma/inferno/plasma/viridis/cividis/turbo 各 256 节点，共 1536 项，8 位取整颜色与位置匹配；不分发 Python 运行库。
- Pretty Lattice 固定 `7980a9a2e7c7ed21f4b5ef534ed0cc264a4db3c7`：vesta-soft 97 项（含 D/XX）一致；metalness 0.1、roughness 0.6、环境光 0.8、方向光 2.2、偏移 [0.3,0.2,0]、键半径 0.1 Å、框色 #444444 一致；MIT 原文一致。之后的本地调整不等于相同渲染。
- ColorBrewer BrBG 五节点由三色方案与十一色端点组合，不是原版五类表；固定 `7d135fc4e19eda73f2eb1bf55fcdf4a04fe4881f`，保留 Apache-2.0、作者与插值改编说明。旧 coolwarm/grayscale/稀疏 viridis 和八套截图近似 reference 色图不冒称完整 Matplotlib 或其他官方原表。

<a id="compatibility"></a>
## 兼容性与未决项

旧项目继续使用保存的比例乘当前半径，受影响十种元素的尺寸、共价键及相关视图/导出可能变化。共价缓存因修订号重算，绝对距离输入不变；坐标、晶胞、手动键、删除覆盖、颜色、比例、项目和撤销/恢复格式不变。重要旧项目可另存副本。

旧 VESTA/Studio/CPK 最初取得记录仍不完整，不能从数值匹配推导完整权利链；已去除“精确官方默认色”等不成立表述。320 项声明和 215 份原文不是所有历史问题的自动权利结论。原始文献、NIST 响应和本地核查材料不分发。

<a id="references"></a>
## 文献

| 文献 | 核对信息 |
| --- | --- |
| Meija et al., Atomic weights of the elements 2013 | Pure Appl. Chem. 88, 265–291 (2016), [DOI](https://doi.org/10.1515/pac-2015-0305); Tables 1, 3, 4. |
| Cordero et al., Covalent radii revisited | Dalton Trans., 2832–2838 (2008), [DOI](https://doi.org/10.1039/B801115J); Table 2, p. 2836. |
| Bondi, van der Waals Volumes and Radii | J. Phys. Chem. 68, 441–451 (1964), [DOI](https://doi.org/10.1021/j100785a001); Tables I and XIV, pp. 443, 449. |
| Mantina et al., Consistent van der Waals Radii for the Whole Main Group | J. Phys. Chem. A 113, 5806–5812 (2009), [Table 12](https://pmc.ncbi.nlm.nih.gov/articles/PMC3658832/#T12), [DOI](https://doi.org/10.1021/jp8111556). |
| Batsanov, Van der Waals Radii of Elements | Inorganic Materials 37, 871–885 (2001), [DOI](https://doi.org/10.1023/A:1011625728803); Tables 2 and 9, pp. 873, 879. |
| Hu, Zhou, Tsai, Average van der Waals Radii of Atoms in Crystals | Acta Phys.-Chim. Sin. 19, 1073–1077 (2003), [DOI](https://doi.org/10.3866/PKU.WHXB20031118); Ag correspondence also explicit in Hu 2009. |
| Hu, Zhou, Robertson, Consistent approaches to van der Waals radii for the metallic elements | Z. Kristallogr. 224, 375–383 (2009), [DOI](https://doi.org/10.1524/zkri.2009.1158); Table 1, p. 378. |
| Smits, Indelicato, Nazarewicz, Piibeleht, Schwerdtfeger, Pushing the limits of the periodic table — A review on atomic relativistic electronic structure theory and calculations for the superheavy elements | Physics Reports 1035, 1–57 (2023), [DOI](https://doi.org/10.1016/j.physrep.2023.09.004); Table 2, p. 34; CC BY 4.0. |
| NIST Periodic Table of the Elements | [Official compilation](https://www.nist.gov/pml/periodic-table-elements), [terms](https://www.nist.gov/open/license); 108 records retrieved 2026-11-08. |
| Blue Obelisk Data Repository | [Pinned source](https://github.com/BlueObelisk/bodr/tree/c22a200776984388564ef90536d8af24ae09d21e); repository COPYING/README: CC0 1.0. |

[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) · [supplemental/](supplemental/)
