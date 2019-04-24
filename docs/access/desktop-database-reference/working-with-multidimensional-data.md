---
title: 多次元データの使用
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 67b22219fdbbec8bf518b7be0fabd9a6adfbcf7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306042"
---
# <a name="working-with-multidimensional-data"></a>多次元データの使用

**適用先:** Access 2013、Office 2013

*セルセット*は、多次元データのクエリの結果で、通常は 4 つ以内の軸および 2 つまたは 3 だけのコレクションで構成されます。*軸*は、1 つ以上の次元のメンバーのコレクションで、キューブ内で特定の値を検索またはフィルターするために使用します。

*位置*は、軸に沿ったポイントです。単一の次元で構成される軸の位置は、次元メンバーのサブセットです。複数の次元で構成される軸の各位置は、*n* 個の部分で構成される合成エンティティです。ここで、*n* は、軸に沿った次元の数です。位置の各部は、構成されている次元の 1 つのメンバーです。

たとえば、売上データを含むキューブの Geography 次元と Product 次元がセルセットの x 軸に沿っている場合、この軸上の位置には、"USA" メンバーと "Computers" メンバーが含まれます。この例で、x 軸に沿った位置を決定するには、各次元のメンバーが軸に沿っている必要があります。

*セル*は、軸座標の交点にあるオブジェクトです。各セルには、データ自体、フォーマット済み文字列 (表示可能形式のセル データ)、セルの序数値などの複数の関連情報が含まれます。各セルは、セルセットで一意の序数値です。セルセットの最初のセルの序数値はゼロで、8 列あるセルセットの 2 行目の一番左のセルの序数値は 8 です。

たとえば、キューブに以下の 6 つの次元があるとします。このキューブのスキーマは、「[多次元スキーマおよびデータの概要](overview-of-multidimensional-schemas-and-data.md)」の例と多少異なることに注意してください。

- Salesperson
- Geography (地理的な階層) - Continents、Countries、States など
- Quarters - Quarters、Months、Days
- Years
- Measures - Sales、PercentChange、BudgetedSales
- Products

> [!NOTE]
> [!メモ] この例のセル値は軸位置の序数の整列されたペアとして表示でき、最初の桁は x 軸の位置を表し、2 桁目が Y 軸の位置を表します。

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

