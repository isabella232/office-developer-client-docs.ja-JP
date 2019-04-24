---
title: Shape COMPUTE 句
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306455"
---
# <a name="shape-compute-clause"></a>Shape COMPUTE 句

**適用先:** Access 2013、Office 2013

shape の COMPUTE 句は、親 **Recordset** を生成します。その列は、子 **Recordset** に対する参照、省略可能な列 (その内容はチャプター列、新規列、演算列、および子 **Recordset** や既にシェイプされている **Recordset** に対して集計関数を実行した結果など)、および省略可能な BY 句で指定される一連の子 **Recordset** の任意の列で構成されます。

## <a name="syntax"></a>構文

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a>説明

この句の要素は以下のとおりです。

- *child-command*

  - 以下のいずれかで構成されます。
    
    - 子 Recordset オブジェクトを返すクエリコマンドを{}波かっこ ("") **** で囲んで指定します。 このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。 ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。
    
    - シェイプされた既存の **Recordset** の名前。
    
    - 別の shape コマンド。
    
    - TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。

- *child-alias*

  - *child-command* によって返される **Recordset** を参照するために使用される別名。*child-alias* は、COMPUTE 句の列の一覧で必要であり、親と子の **Recordset** オブジェクト間の関係を定義します。

- *appended-column-list*

  - 生成される親の列を定義する要素の一覧。各要素には、チャプター列、新規列、演算列、または子 **Recordset** に対する集計関数の結果の値が含まれます。

- *grp-field-list*

  - 子で行をグループ化する方法を指定する、親と子の**Recordset**オブジェクト内の列のリスト。 *"grp-フィールドリスト"* の各列には、子および親**Recordset**オブジェクトに対応する列があります。 親**recordset**の各行に対して、 *grp フィールドリスト*列に一意の値があり、親行によって参照される子**Recordset**は、親の行** だけで構成されます。親の行

BY 句が含まれる場合、子 **Recordset** の行は COMPUTE 句の列に基づいてグループ化されます。親の **Recordset** には、子 **Recordset** の行グループごとに 1 行が含まれます。

BY 句を省略すると、子 **Recordset** 全体が単一のグループとして扱われ、親 **Recordset** にはただ 1 行だけが含まれます。この行は、子 **Recordset** 全体を参照します。BY 句を省略すると、子 **Recordset** 全体に対する "総合計" を計算できます。

次に例を示します。

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

親 **Recordset** には、その構成方法 (COMPUTE を使用するか APPEND を使用するか) に関係なく、子 **Recordset** との関連付けに使用されるチャプター列が含まれます。必要な場合は、親 **Recordset** に、子の行に対する集計 (SUM、MIN、MAX など) が格納された列を含めることもできます。親および子の **Recordset** はいずれも、 **Recordset** の行に対する式が格納された列、および初期状態が空の新しい列を持つことができます。

## <a name="operation"></a>Operation

*child-command* はプロバイダーに対して発行され、プロバイダーは子の **Recordset** を返します。

COMPUTE 句では、親 **Recordset** の列を指定します。この列としては、子 **Recordset** に対する参照、1 つまたは複数の集計、演算式、または新規列を使用できます。BY 句がある場合は、BY 句で定義されている列も親 **Recordset** に追加されます。BY 句では、子 **Recordset** の行をグループ化する方法を指定します。

たとえば、State (州)、City (都市)、Population (人口) のフィールドで構成される Demographics テーブルを想定します (人口の値は一例です)。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>状態</p></th>
<th><p>市区町村</p></th>
<th><p>人口</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ワ</p></td>
<td><p>Seattle</p></td>
<td><p>70万</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200,000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>支店</p></td>
<td><p>400,000</p></td>
</tr>
<tr class="even">
<td><p>コンテンツ</p></td>
<td><p>Los Angeles</p></td>
<td><p>80万</p></td>
</tr>
<tr class="odd">
<td><p>コンテンツ</p></td>
<td><p>San Diego</p></td>
<td><p>600,000</p></td>
</tr>
<tr class="even">
<td><p>ワ</p></td>
<td><p>Tacoma</p></td>
<td><p>500,000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>corvallis</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>


このテーブルに対し、次のような shape コマンドを発行します。

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

このコマンドは、シェイプされた **Recordset** を 2 つのレベルで開きます。 親レベルは、集約列 (SUM (rs)) を使用した生成された**recordset** 、子**recordset** (rs) を参照する列、および子**recordset** (state) をグループ化する列です。 子レベルは、クエリコマンド () によって返される**recordset** 、子**recordset** (rs) を参照する列、および子**recordset** (state) をグループ化する列です。 子レベルは、クエリコマンドによって返される**Recordset**です\* ([デモグラフィックス] から選択します)。

The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.

これにより、開いている親 **Recordset** 内を移動して、子の詳細な **Recordset** オブジェクトにアクセスできるようになります。詳細については、「 [階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。

**親および子の詳細 Recordset の結果**

**親**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>SUM (rs.Population)</p></th>
<th><p>clr</p></th>
<th><p>状態</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>130万</p></td>
<td><p>子 1 への参照</p></td>
<td><p>コンテンツ</p></td>
</tr>
<tr class="even">
<td><p>120万</p></td>
<td><p>子 2 への参照</p></td>
<td><p>ワ</p></td>
</tr>
<tr class="odd">
<td><p>110万</p></td>
<td><p>子 3 への参照</p></td>
<td><p>OR</p></td>
</tr>
</tbody>
</table>


**Child1**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>状態</p></th>
<th><p>市区町村</p></th>
<th><p>人口</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>コンテンツ</p></td>
<td><p>Los Angeles</p></td>
<td><p>80万</p></td>
</tr>
<tr class="even">
<td><p>コンテンツ</p></td>
<td><p>San Diego</p></td>
<td><p>600,000</p></td>
</tr>
</tbody>
</table>


**Child2**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>状態</p></th>
<th><p>市区町村</p></th>
<th><p>人口</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ワ</p></td>
<td><p>Seattle</p></td>
<td><p>70万</p></td>
</tr>
<tr class="even">
<td><p>ワ</p></td>
<td><p>Tacoma</p></td>
<td><p>500,000</p></td>
</tr>
</tbody>
</table>


**Child3**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>状態</p></th>
<th><p>市区町村</p></th>
<th><p>人口</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200,000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>支店</p></td>
<td><p>400,000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>corvallis</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>

