# 1 Metrics
<html>
<body>
<!--StartFragment--><!DOCTYPE html><p cid="n24" mdtype="paragraph" class="md-end-block md-p" style="box-sizing: border-box; line-height: inherit; orphans: 4; margin: 0.8em 0px; white-space: pre-wrap; position: relative; color: rgb(51, 51, 51); font-family: &quot;Open Sans&quot;, &quot;Clear Sans&quot;, &quot;Helvetica Neue&quot;, Helvetica, Arial, &quot;Segoe UI Emoji&quot;, sans-serif; font-size: 16px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; text-align: start; text-indent: 0px; text-transform: none; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;"><span md-inline="plain" class="md-plain" style="box-sizing: border-box;">本度量工具共提供4个粒度的项目可维护性度量，每个粒度提供的指标数量统计如下：</span></p><figure class="md-table-fig" cid="n604" mdtype="table" style="box-sizing: border-box; margin: 1.2em 0px; overflow-x: auto; max-width: calc(100% + 16px); padding: 0px; cursor: default; color: rgb(51, 51, 51); font-family: &quot;Open Sans&quot;, &quot;Clear Sans&quot;, &quot;Helvetica Neue&quot;, Helvetica, Arial, &quot;Segoe UI Emoji&quot;, sans-serif; font-size: 16px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;">

| 粒度    | 指标数量 |
| ------- | -------- |
| project | 11       |
| module  | 12       |
| class   | 42       |
| method  | 12       |

</figure><h2 cid="n298" mdtype="heading" class="md-end-block md-heading" style="box-sizing: border-box; break-after: avoid-page; break-inside: avoid; orphans: 4; font-size: 1.75em; margin-top: 1rem; margin-bottom: 1rem; position: relative; font-weight: bold; line-height: 1.225; cursor: text; border-bottom: 1px solid rgb(238, 238, 238); white-space: pre-wrap; color: rgb(51, 51, 51); font-family: &quot;Open Sans&quot;, &quot;Clear Sans&quot;, &quot;Helvetica Neue&quot;, Helvetica, Arial, &quot;Segoe UI Emoji&quot;, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; letter-spacing: normal; text-align: start; text-indent: 0px; text-transform: none; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;"><span md-inline="plain" class="md-plain" style="box-sizing: border-box;">输出结果说明</span></h2><!--EndFragment-->
</body>
</html>
本度量工具共提供4个粒度的项目可维护性度量，每个粒度提供的指标数量统计如下：
<html>
<body>
<!--StartFragment--><!DOCTYPE html>

| 粒度    | 指标数量 |
| ------- | -------- |
| project | 11       |
| module  | 12       |
| class   | 42       |
| method  | 12       |
## 1.1 project
| 指标                              | 说明                                                         |
| --------------------------------- | ------------------------------------------------------------ |
| score                             | 对模块级指标进行融合得到模块可维护性的综合评分               |
| CHM                               | 项目中所有模块在消息层内聚程度的均值。                       |
| CHD                               | 项目中所有模块在领域层内聚程度的均值。                       |
| SMQ(structural modularity)        | 结构模块化程度。SMQ 值越大,说明模块的模块化程度越高。        |
| SPREAD                            | 度量模块中的实体在演化过程中横切协同变化集群的个数。SPREAD越小，总体模块性越好。 |
| FOCUS                             | 度量模块化良好的程度。FOCUS越大，总体模块性越好。            |
| ICF(intra co-change frequency)    | 所有模块演化内部共变频率的平均值。ICF越高，总体模块内的实体更有可能一起演化。 |
| ECF(external co-change frequency) | 所有模块演化外部共变频率的平均值。ECF越低，总体跨模块边界的实体更有可能独立演化。 |
| REI(ratio of ecf to icf)          | 所有模块演化外部共变频率与内部共变频率的比值的平均值。REI越低，说明总体不同模块一起修改的可能性越低，各模块更有可能会独立演化、独立维护。 |
| ODD(out-degree dependence)        | ODD越大，总体耦合其他模块的程度越高，模块之间的动态交互度越高。 |
| IDD(in-degree dependence)         | IDD越大，总体被耦合的程度越高，模块间的动态交互程度越高。    |

<!--EndFragment-->
## 1.2 module
<html>
<body>
<!--StartFragment--><!DOCTYPE html>

| 指标   | 说明                                                         |
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

<!--EndFragment-->
</body>
</html>
## 1.3 class
<html>
<body>
<!--StartFragment--><!DOCTYPE html>

| 指标                   | 说明                                        |
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

<!--EndFragment-->
</body>
</html>
## 1.4 method
<html>
<body>
<!--StartFragment--><!DOCTYPE html>

| 指标                           | 说明                          |
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

<!--EndFragment-->
</body>
</html>
</body>
</html>