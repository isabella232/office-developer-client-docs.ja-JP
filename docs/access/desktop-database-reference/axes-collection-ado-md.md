---
title: Axes コレクション (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2681eacae56368d8b0f9f31a590da0b8bb9b3ac4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602956"
---
# <a name="axes-collection-ado-md"></a>Axes コレクション (ADO MD)


**適用先**: Access 2013、Office 2013

セルセットを定義する [Axis](axis-object-ado-md.md) オブジェクトを含みます。

## <a name="remarks"></a>注釈

[Cellset](cellset-object-ado-md.md) オブジェクトは、 **Axes** コレクションを含みます。 **Cellset** を開くと、このコレクションには少なくとも 1 つの **Axis** が含まれます。 [Axis](axis-object-ado-md.md) のオブジェクトの使い方の詳細については、 **Axis** オブジェクトを参照してください。


> [!NOTE]
> [!メモ] **Cellset** のフィルター軸は、 **Axes** コレクションには含まれません。詳細については、 [FilterAxis](filteraxis-property-ado-md.md) プロパティを参照してください。



**Axes** は、標準の ADO コレクションです。このコレクションのプロパティとメソッドを使用すると、次の操作を実行できます。

- [Count](count-property-ado.md) プロパティを使用して、コレクションのオブジェクトの数を取得します。

- 既定の [Item](item-property-ado.md) プロパティを使用して、コレクションからオブジェクトを返します。

- [Refresh](refresh-method-ado.md) メソッドを使用して、プロバイダーからコレクションのオブジェクトを更新します。

