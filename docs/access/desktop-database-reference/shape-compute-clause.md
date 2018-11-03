---
title: Shape Compute 句
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f8dbeb97a4afdc068d635411d6035f68ba1168b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946399"
---
# <a name="shape-compute-clause"></a>Shape Compute 句

**適用されます**Access 2013、Office 2013。

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
    
    - 子の {} オブジェクトを返すクエリ コマンドを波かっこ ("****") で囲んだもの。このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。
    
    - シェイプされた既存の **Recordset** の名前。
    
    - 別の shape コマンド。
    
    - TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。

- *child-alias*

  - **レコード セット**を参照するエイリアスが返される、*子コマンドです*。 *子エイリアス*では、COMPUTE 句の列の一覧で必要なし、親と子の**レコード セット**オブジェクトの間の関係を定義します。

- *appended-column-list*

  - 生成される親の列を定義する要素の一覧。各要素には、チャプター列、新規列、演算列、または子 **Recordset** に対する集計関数の結果の値が含まれます。

- *grp-field-list*

  - 子において行をグループ化する方法を指定する親と子の**Recordset**オブジェクト内の列の一覧です。 *グループのフィールドのリスト*内の各列には子と親の**Recordset**オブジェクトに対応する列があります。 親**レコード セット**内の各行の*グループ]* 列は、一意の値であるし、**レコード セット**の親テーブルの行によって参照されているのみで構成される子の子の行*グループのフィールドのリスト*を持つ列があると、同じ値、親の行です。

BY 句が含まれる場合、子 **Recordset** の行は COMPUTE 句の列に基づいてグループ化されます。親の **Recordset** には、子 **Recordset** の行グループごとに 1 行が含まれます。

BY 句を省略すると、子 **Recordset** 全体が単一のグループとして扱われ、親 **Recordset** にはただ 1 行だけが含まれます。この行は、子 **Recordset** 全体を参照します。BY 句を省略すると、子 **Recordset** 全体に対する "総合計" を計算できます。

次に例を示します。

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

親 **Recordset** には、その構成方法 (COMPUTE を使用するか APPEND を使用するか) に関係なく、子 **Recordset** との関連付けに使用されるチャプター列が含まれます。必要な場合は、親 **Recordset** に、子の行に対する集計 (SUM、MIN、MAX など) が格納された列を含めることもできます。親および子の **Recordset** はいずれも、 **Recordset** の行に対する式が格納された列、および初期状態が空の新しい列を持つことができます。

## <a name="operation"></a>操作

*子コマンド*は、子**レコード セット**を返すと、プロバイダーに発行されます。

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
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200,000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Portland</p></td>
<td><p>400,000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>Los Angeles</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="odd">
<td><p>CA</p></td>
<td><p>San Diego</p></td>
<td><p>600,000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Tacoma</p></td>
<td><p>500,000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
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

このコマンドは、シェイプされた **Recordset** を 2 つのレベルで開きます。 親レベルは、集計の列 (SUM(rs.population))、子**レコード セット**、(rs) を参照する列および列子**レコード セット**(状態) をグループ化するために生成された**レコード セット**です。 子レベルは、クエリ コマンド ()、子**レコード セット**、(rs) を参照している列、および子**レコード セット**(状態) をグループ化するための列によって返される**レコード セット**です。 子レベルでは、クエリによって返される**レコード セット**(選択\*人口統計から)。

状態によってグループ化されたが、特定の順序でそれ以外の場合に、子**Recordset**の詳細行になります。 グループはアルファベット順または数値順ではできません。 親**レコード セット**を注文する場合は、親**レコード セット**を注文するのには、**レコード セット**の**並べ替え**方法を使用できます。

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
<th><p>rs</p></th>
<th><p>State</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>子 1 への参照</p></td>
<td><p>CA</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>子 2 への参照</p></td>
<td><p>WA</p></td>
</tr>
<tr class="odd">
<td><p>1,100,000</p></td>
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
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CA</p></td>
<td><p>Los Angeles</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>San Diego</p></td>
<td><p>600,000</p></td>
</tr>
</tbody>
</table>


**子 2**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Tacoma</p></td>
<td><p>500,000</p></td>
</tr>
</tbody>
</table>


**子 3**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Population</p></th>
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
<td><p>Portland</p></td>
<td><p>400,000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>

