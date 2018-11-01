---
title: MarshalOptions プロパティ (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5983b7794677b5cc584c541289069acf282d9f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883212"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

どのレコードがサーバーにマーシャリングされるかを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。

## <a name="remarks"></a>解説

クライアント側の[Recordset](recordset-object-ado.md)を使用すると、クライアント上で変更されたレコードに書き込まれます戻る、中間層またはマーシャ リングをパッケージ化し、スレッド間でインターフェイス メソッドのパラメーターを送信するという手法を使用して web サーバーまたはプロセス境界という考え方です。 **スレッド**を設定すると、リモート データが変更されたが、中間層または web サーバーに更新するためにマーシャ リングするときにパフォーマンスが向上することができます。

**リモート データ サービスの使用法**このプロパティはクライアント側の**Recordset**でのみ使用します。

