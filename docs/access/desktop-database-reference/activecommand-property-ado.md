---
title: ActiveCommand プロパティ (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 473a0b99310d2eb5e050ed50f1e331cb65174ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869562"
---
# <a name="activecommand-property-ado"></a>ActiveCommand プロパティ (ADO)

**適用されます**Access 2013、Office 2013。

関連付けられた [Recordset](command-object-ado.md) オブジェクトを作成した [Command](recordset-object-ado.md) オブジェクトを示します。

## <a name="return-value"></a>戻り値

**Command** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を返します。既定は、Null オブジェクト参照です。

## <a name="remarks"></a>解説

**ActiveCommand** プロパティは、値の取得のみ可能です。

以前に現在の**レコード セット**を作成する**コマンド**オブジェクトを使用しない場合は、 **Null**オブジェクト参照が返されます。

このプロパティは、作成された **Recordset** オブジェクトのみが与えられていて、関連付けられている **Command** オブジェクトを取得したい場合に使用します。

