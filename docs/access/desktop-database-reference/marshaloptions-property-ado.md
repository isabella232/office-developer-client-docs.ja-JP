---
title: MarshalOptions プロパティ (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8fff5f725df8c53e3990ed1aacd519a0bfdf6f4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594000"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions プロパティ (ADO)


**適用先**: Access 2013、Office 2013

どのレコードがサーバーにマーシャリングされるかを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。

## <a name="remarks"></a>注釈

クライアント側の [Recordset](recordset-object-ado.md)を使用する場合、クライアントで変更されたレコードは、マーシャリング、スレッドまたはプロセスの境界を越えてインターフェイス メソッド パラメーターをパッケージ化して送信するプロセスと呼ばれる手法を使用して、ミドル 層または Web サーバーに書き戻されます。 **MarshalOptions** プロパティを設定すると、ミドル 層または Web サーバーに更新するために変更されたリモート データをマーシャリングすると、パフォーマンスが向上します。

**リモート データ サービスの使用状況** このプロパティは、クライアント側の Recordset でのみ使用 **されます**。

