---
title: ActiveCommand プロパティ (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab0bee62d55b11ce9a35e08cecf814cb4d75d5a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586321"
---
# <a name="activecommand-property-ado"></a>ActiveCommand プロパティ (ADO)

**適用先**: Access 2013、Office 2013

関連付けられた [Recordset](command-object-ado.md) オブジェクトを作成した [Command](recordset-object-ado.md) オブジェクトを示します。

## <a name="return-value"></a>戻り値

**Command** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を返します。既定は、Null オブジェクト参照です。

## <a name="remarks"></a>注釈

**ActiveCommand** プロパティは、値の取得のみ可能です。

Command オブジェクト **を使用** して現在の **Recordset** を作成していない場合は **、Null** オブジェクト参照が返されます。

このプロパティは、作成された **Recordset** オブジェクトのみが与えられていて、関連付けられている **Command** オブジェクトを取得したい場合に使用します。

