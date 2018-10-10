---
title: Axes コレクション (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2b078f2d8f1ea6562d6f82f90943923c7d92a07
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478742"
---
# <a name="axes-collection-ado-md"></a>Axes コレクション (ADO MD)


**適用されます**Access 2013 |。Office 2013

セルセットを定義する [Axis](axis-object-ado-md.md) オブジェクトを含みます。

## <a name="remarks"></a>解説

[Cellset](cellset-object-ado-md.md) オブジェクトは、 **Axes** コレクションを含みます。 **Cellset** を開くと、このコレクションには少なくとも 1 つの **Axis** が含まれます。 [Axis](axis-object-ado-md.md) のオブジェクトの使い方の詳細については、 **Axis** オブジェクトを参照してください。


> [!NOTE]
> <P>[!メモ] <STRONG>Cellset</STRONG> のフィルター軸は、 <STRONG>Axes</STRONG> コレクションには含まれません。詳細については、 <A href="filteraxis-property-ado-md.md">FilterAxis</A> プロパティを参照してください。</P>



**Axes** は、標準の ADO コレクションです。このコレクションのプロパティとメソッドを使用すると、次の操作を実行できます。

  - [Count](count-property-ado.md) プロパティを使用して、コレクションのオブジェクトの数を取得します。

  - 既定の [Item](item-property-ado.md) プロパティを使用して、コレクションからオブジェクトを返します。

  - [Refresh](refresh-method-ado.md) メソッドを使用して、プロバイダーからコレクションのオブジェクトを更新します。

