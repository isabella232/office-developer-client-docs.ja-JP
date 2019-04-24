---
title: StayInSync プロパティ (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308492"
---
# <a name="stayinsync-property-ado"></a>StayInSync プロパティ (ADO)


**適用先:** Access 2013、Office 2013

親の行の位置が変更されたときに、基になる子のレコード (つまり、*チャプター*) への参照を変更するかどうかを、階層[Recordset](recordset-object-ado.md)オブジェクト内に示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

ブール型 (**Boolean**) の値を設定または取得します。既定値は **True** です。**True** の場合は、親の **Recordset** オブジェクトの行位置が変更されるとチャプターが更新されます。**False** の場合は、親の **Recordset** オブジェクトの行位置が変更されても、チャプターは以前のチャプターのデータを参照し続けます。

## <a name="remarks"></a>注釈

このプロパティは、[Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) によってサポートされるような階層 Recordset に適用され、子の **Recordset** を取得する前に親の **Recordset** を設定しておく必要があります。このプロパティによって、階層レコードセット内の移動が容易になります。

