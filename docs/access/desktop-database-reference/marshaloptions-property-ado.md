---
title: MarshalOptions プロパティ (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704596"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

どのレコードがサーバーにマーシャリングされるかを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。

## <a name="remarks"></a>解説

クライアント側の[Recordset](recordset-object-ado.md)を使用すると、クライアント上で変更されたレコードに書き込まれます戻る、中間層またはマーシャ リングをパッケージ化し、スレッド間でインターフェイス メソッドのパラメーターを送信するという手法を使用して web サーバーまたはプロセス境界という考え方です。 **スレッド**を設定すると、リモート データが変更されたが、中間層または web サーバーに更新するためにマーシャ リングするときにパフォーマンスが向上することができます。

**リモート データ サービスの使用法**このプロパティはクライアント側の**Recordset**でのみ使用します。

