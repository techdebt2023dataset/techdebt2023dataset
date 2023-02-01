## Forest Structure

Based on the maintainability model defined by ISO/IEC 25010, we construct a forest structure as a knowledge base, combing widely-adopted code-level metrics from the developer side. All the collected metrics correspond to the nodes in the forest structure, where each link between nodes denotes their relation.

![metrics](C:\Users\zyy\Desktop\techdebt2023dataset\Knowledge Base\img\metrics.png)

## Metrics

The forest Structure contains four granularity maintainability metrics, and the number of metrics provided by each granularity is as follows:

| granularity | number |
| ----------- | ------ |
| project     | 11     |
| module      | 12     |
| class       | 42     |
| method      | 12     |

The metrics of all granularity are explained as follows.

- project

  | metric | full name                    | description                                                  | source |
  | ------ | ---------------------------- | ------------------------------------------------------------ | ------ |
  | score  | -                            | 对模块级指标进行融合得到模块可维护性的综合评分               |        |
  | CHM    |                              | 项目中所有模块在消息层内聚程度的均值。                       |        |
  | CHD    |                              | 项目中所有模块在领域层内聚程度的均值。                       |        |
  | SMQ    | structural modularity        | 结构模块化程度。SMQ 值越大,说明模块的模块化程度越高。        |        |
  | SPREAD | -                            | 度量模块中的实体在演化过程中横切协同变化集群的个数。SPREAD越小，总体模块性越好。 |        |
  | FOCUS  | -                            | 度量模块化良好的程度。FOCUS越大，总体模块性越好。            |        |
  | ICF    | intra co-change frequency    | 所有模块演化内部共变频率的平均值。ICF越高，总体模块内的实体更有可能一起演化。 |        |
  | ECF    | external co-change frequency | 所有模块演化外部共变频率的平均值。ECF越低，总体跨模块边界的实体更有可能独立演化。 |        |
  | REI    | ratio of ecf to icf          | 所有模块演化外部共变频率与内部共变频率的比值的平均值。REI越低，说明总体不同模块一起修改的可能性越低，各模块更有可能会独立演化、独立维护。 |        |
  | ODD    | out-degree dependence        | ODD越大，总体耦合其他模块的程度越高，模块之间的动态交互度越高。 |        |
  | IDD    | in-degree dependence         | IDD越大，总体被耦合的程度越高，模块间的动态交互程度越高。    |        |

- module

  | metric | description                                                  |
  | ------ | ------------------------------------------------------------ |
  | scoh   | scoh越大，模块内的结构内聚程度越大。                         |
  | scop   | scop越大，模块间的结构耦合程度越大。                         |
  | odd    | odd越大，该模块耦合其他模块的程度越高，模块之间的动态交互度越高。 |
  | idd    | idd越大，该模块被耦合的程度越高，模块间的动态交互程度越高。  |
  | spread | 度量模块中的实体在演化过程中接触的共变集群个数。spread越小，模块性越好。 |
  | focus  | 度量模块中的实体在演化过程中专注自身演进的程度。focus越大，模块性越好。 |
  | icf    | icf越高，模块内的实体更有可能一起演化。                      |
  | ecf    | ecf越低，跨模块边界的实体更有可能独立演化。                  |
  | rei    | rei越低，说明不同模块一起修改的可能性越低，模块更有可能会独立演化、独立维护。 |
  | DSM    | DSM越大，模块越复杂，与外部耦合的可能性越高。                |
  | chm    | chm越大，模块在消息层内聚程度越高。                          |
  | chd    | chd越大，模块在领域层内聚程度越高。                          |

- class

  | metric                 | description                                 |
  | ---------------------- | ------------------------------------------- |
  | CIS                    | 类中公共接口数                              |
  | NOM                    | 类中方法总数                                |
  | NOP                    | 多态方法数量                                |
  | NAC                    | 类继承树深度                                |
  | NDC                    | 派生类个数                                  |
  | NOI                    | 类导入依赖的个数                            |
  | NOID                   | 类被导入依赖的个数                          |
  | CTM                    | 调用方法个数(除自身类中方法)                |
  | IDCC                   | 模块内耦合类数量                            |
  | IODD                   | 模块内耦合其他类的数量                      |
  | IIDD                   | 模块内被其他类耦合的数量                    |
  | EDCC                   | 模块外耦合类数量                            |
  | c_FAN_IN               | 类扇入                                      |
  | c_FAN_OUT              | 类扇出                                      |
  | CBC                    | 类依赖的数量(包含被依赖)                    |
  | c_chm                  | 类在消息层的功能内聚度                      |
  | c_chd                  | 类在领域层的功能内聚度                      |
  | c_variablesQty         | 类中变量数量                                |
  | privateMethodsQty      | 私有方法数量                                |
  | protectedMethodsQty    | 保护方法数量                                |
  | staticMethodsQty       | 静态方法数量                                |
  | defaultMethodsQty      | 缺省方法数量                                |
  | abstractMethodsQty     | 抽象方法数量                                |
  | finalMethodsQty        | final方法数量                               |
  | synchronizedMethodsQty | synchronized方法数量                        |
  | publicFieldsQty        | 公有字段数量                                |
  | privateFieldsQty       | 私有字段数量                                |
  | protectedFieldsQty     | 保护字段数量                                |
  | staticFieldsQty        | 静态字段数量                                |
  | defaultFieldsQty       | 缺省字段数量                                |
  | finalFieldsQty         | final字段数量                               |
  | synchronizedFieldsQty  | synchronized字段数量                        |
  | RFC                    | 类的响应数量(本地方法数量+调用外部方法数量) |
  | NOF                    | 字段数量                                    |
  | NOVM                   | 可见方法数量                                |
  | NOSI                   | 静态方法调用数量                            |
  | TCC                    | 紧类内聚(仅考虑可见方法的直接调用)          |
  | LCC                    | 松类内聚(考虑可见方法的直接调用和间接调用)  |
  | LCOM                   | 方法内聚性缺失                              |
  | LOCM*                  | 方法内聚性缺失(标准化结果)                  |
  | WMC                    | 类方法复杂度之和                            |
  | c_modifiers            | 类中修饰符                                  |

- method

  | metric                         | description                   |
  | ------------------------------ | ----------------------------- |
  | startLine                      | 方法开始位置                  |
  | CBM                            | 方法依赖的数量(call/override) |
  | m_FAN_IN                       | 方法扇入                      |
  | m_FAN_OUT                      | 方法扇出                      |
  | IDMC                           | 模块内耦合方法的数量          |
  | EDMC                           | 模块外耦合方法的数量          |
  | methodsInvokedQty              | 调用方法的数量                |
  | methodsInvokedLocalQty         | 调用本地方法的数量            |
  | methodsInvokedIndirectLocalQty | 间接调用本地方法的数量        |
  | m_variablesQty                 | 方法中变量数量                |
  | parametersQty                  | 方法参数数量                  |
  | m_modifier                     | 方法修饰符                    |

## Module-level Metrics Detail

### functionality

- chm
- chd

### coupling

- scop
- scoh
- odd
- idd

### cohesion

- scoh

### evolution

- rei
- ecf
- icf
- spread
- focus

### complexity

- DSM