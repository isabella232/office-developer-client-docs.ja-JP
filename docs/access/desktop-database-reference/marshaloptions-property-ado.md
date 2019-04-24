---
title: marshaloptions プロパティ (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289771"
---
# <a name="marshaloptions-property-ado"></a>marshaloptions プロパティ (ADO)


**適用先:** Access 2013、Office 2013

どのレコードがサーバーにマーシャリングされるかを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。

## <a name="remarks"></a>注釈

クライアント側の[Recordset](recordset-object-ado.md)を使用する場合、クライアント上で変更されたレコードは、マーシャリングと呼ばれる手法を使用して中間層または web サーバーに書き戻されます。これは、スレッド間でインターフェイスメソッドのパラメーターをパッケージ化して送信するプロセスです。プロセス境界。 **marshaloptions**プロパティを設定すると、変更されたリモートデータを中央層または web サーバーに戻すためにマーシャリングするときのパフォーマンスを向上させることができます。

**リモートデータサービスの使用状況**このプロパティは、クライアント側の**Recordset**でのみ使用されます。

