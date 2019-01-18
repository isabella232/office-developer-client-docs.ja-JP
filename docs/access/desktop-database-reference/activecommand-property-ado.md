---
title: ActiveCommand プロパティ (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705296"
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

