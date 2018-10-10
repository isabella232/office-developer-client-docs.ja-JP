---
title: ActiveCommand プロパティ (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479082"
---
# <a name="activecommand-property-ado"></a>ActiveCommand プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

関連付けられた [Recordset](command-object-ado.md) オブジェクトを作成した [Command](recordset-object-ado.md) オブジェクトを示します。

## <a name="return-value"></a>戻り値

**Command** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を返します。既定は、Null オブジェクト参照です。

## <a name="remarks"></a>解説

**ActiveCommand** プロパティは、値の取得のみ可能です。

現在の **Recordset** の作成に **Command** オブジェクトが使用されていない場合は、 **Null** オブジェクト参照が返されます。

このプロパティは、作成された **Recordset** オブジェクトのみが与えられていて、関連付けられている **Command** オブジェクトを取得したい場合に使用します。

