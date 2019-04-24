---
title: Item プロパティ (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290794"
---
# <a name="item-property-ado"></a>Item プロパティ (ADO)

**適用先:** Access 2013、Office 2013

コレクションの特定のメンバーをその名前または序数で示します。

## <a name="syntax"></a>構文

*オブジェクト* = の*コレクション*を設定します。Item (Index)

## <a name="return-value"></a>戻り値

オブジェクトへの参照を返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Index* |コレクション内のオブジェクトの名前または序数に評価されるバリアント型 ( **Variant** ) の式を指定します。|

## <a name="remarks"></a>注釈

**Item** プロパティは、コレクション内の特定のオブジェクトを返すために使います。コレクション内で **Item** が *Index* 引数に対応するオブジェクトを見つけられない場合は、エラーが発生します。また、コレクションの中には名前付きオブジェクトをサポートしていないものもあります。このようなコレクションでは、序数参照を使う必要があります。

**Item** プロパティはすべてのコレクションの既定プロパティなので、次のいずれの構文形式でも同じ結果が得られます。

```vb
    collection.Item (Index)
    collection (Index)
```
