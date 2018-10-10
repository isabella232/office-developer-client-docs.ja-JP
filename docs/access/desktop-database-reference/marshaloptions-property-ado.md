---
title: MarshalOptions プロパティ (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478758"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

どのレコードがサーバーにマーシャリングされるかを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。

## <a name="remarks"></a>解説

クライアント側の [Recordset](recordset-object-ado.md) を使用する場合、クライアントで修正されたレコードは、マーシャリングという技術により、中間層または Web サーバーに書き戻されます。マーシャリングとは、スレッドまたはプロセスの境界を越えてインターフェイス メソッドのパラメーターをパッケージ化して送信するプロセスです。 **MarshalOptions** プロパティを設定すると、修正されたリモート データをマーシャリングして中間層や Web サーバーを更新するときのパフォーマンスが向上します。

**リモート データ サービスの使用法**このプロパティはクライアント側の**Recordset**でのみ使用します。

