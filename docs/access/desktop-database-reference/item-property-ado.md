---
title: Item プロパティ (ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476483"
---
# <a name="item-property-ado"></a>Item プロパティ (ADO)

**適用されます**Access 2013 |。Office 2013

コレクションの特定のメンバーをその名前または序数で示します。

## <a name="syntax"></a>構文

*オブジェクト*を設定する = *コレクション*です。項目 (インデックス)

## <a name="return-value"></a>戻り値

オブジェクトへの参照を返します。

## <a name="parameters"></a>パラメーター

- *Index*

- コレクション内のオブジェクトの名前または序数に評価されるバリアント型 ( **Variant** ) の式を指定します。

## <a name="remarks"></a>解説

コレクションから特定のオブジェクトを取得するのにには、 **Item**プロパティを使用します。 **項目**は、 *Index*引数に対応するコレクション内でオブジェクトを検索することはできません、エラーが発生します。 また、いくつかのコレクションをサポートしていない名前付きオブジェクトです。これらのコレクションでは、序数参照を使用する必要があります。

**Item** プロパティはすべてのコレクションの既定プロパティなので、次のいずれの構文形式でも同じ結果が得られます。

```vb
    collection.Item (Index)
    collection (Index)
```
