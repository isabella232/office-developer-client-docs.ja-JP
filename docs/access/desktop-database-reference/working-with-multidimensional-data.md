---
title: 多次元データを処理する
TOCTitle: Working with Multidimensional Data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2210799fe46a0993a917a85a0e06a1a806b04548
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945825"
---
# <a name="working-with-multidimensional-data"></a>マルチ ディメンション データの操作


**適用されます**Access 2013、Office 2013。

*セルセット*は、多次元データのクエリの結果です。 軸、通常 4 つ以内の軸と通常 2 つまたは 3 つのコレクションで構成されています。 *軸*は、検索またはキューブ内の特定の値をフィルター処理に使用される 1 つまたは複数のディメンションのメンバーのコレクションです。

*位置*は、軸に沿ったポイントです。 1 つのディメンションで構成される軸の位置は、ディメンション メンバーのサブセットです。 軸は、複数のディメンションから構成されている場合、各位置は*その軸に沿った方向の次元の数が* *n*の部分から構成される複合エンティティには、 位置の各部分は、1 つの構成要素であるディメンションのメンバーです。

たとえば、売上データを含むキューブの Geography 次元と Product 次元がセルセットの x 軸に沿っている場合、この軸上の位置には、"USA" メンバーと "Computers" メンバーが含まれます。この例で、x 軸に沿った位置を決定するには、各次元のメンバーが軸に沿っている必要があります。

*セル*は、軸座標の交点にあるオブジェクトです。 各セルには、データ自体、フォーマット済み文字列 (表示可能形式のセル データ)、セルの序数値などの複数の関連情報が含まれます。 各セルは、セルセットで一意の序数値です。 セルセットの最初のセルの序数値はゼロで、8 列あるセルセットの 2 行目の一番左のセルの序数値は 8 です。

たとえば、キューブに以下の 6 つの次元があるとします。このキューブのスキーマは、「[多次元スキーマおよびデータの概要](overview-of-multidimensional-schemas-and-data.md)」の例と多少異なることに注意してください。

  - Salesperson

  - Geography (地理的な階層) - Continents、Countries、States など

  - Quarters - Quarters、Months、Days

  - Years

  - Measures - Sales、PercentChange、BudgetedSales

  - Products


> [!NOTE]
> <P>[!メモ] この例のセル値は軸位置の序数の整列されたペアとして表示でき、最初の桁は x 軸の位置を表し、2 桁目が Y 軸の位置を表します。</P>



このセルセットの特性は次のとおりです。

  - 軸の次元: Quarters、Salesperson、Geography

  - フィルター次元: Measures、Years、Products

  - 2 つの軸: COLUMN (x または Axis 0) と ROW (y または Axis 1)

  - x 軸: ネストされた 2 つの次元 (Salesperson と Geography)

  - y 軸: Quarters 次元

x 軸には、Salesperson と Geography という 2 つの次元があります。Geography からは、Seattle、Boston、USA-South、および Japan の 4 つのメンバーが選択されます。Salesperson からは、Valentine と Nash という 2 つのメンバーが選択されます。これによって、この軸には合計 8 つの位置が生成されます (8 = 4 \*2)。

各座標は、Salesperson 次元と Geography 次元から 1 つずつの 2 つのメンバーを持つ位置として表されます。

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

Y 軸の次元は 1 つだけで、以下の 8 つの位置があります。

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

セルセット、セル、軸、および位置は、すべて ADO MD の対応するオブジェクトによって表されます ([Cellset](cellset-object-ado-md.md)、[Cell](cell-object-ado-md.md)、[Axis](axis-object-ado-md.md)、および [Position](position-object-ado-md.md))。

