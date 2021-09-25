---
title: StayInSync プロパティ (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d5e9782fa9ff94c8fe40f10ed4a73aa1362d5c03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568363"
---
# <a name="stayinsync-property-ado"></a>StayInSync プロパティ (ADO)


**適用先:** Access 2013、Office 2013

階層的な [Recordset](recordset-object-ado.md) オブジェクトで、親行の位置が変更された場合に基になる子レコード (つまり *チャプター)* への参照が変更されるかどうかを示します。

## <a name="settings-and-return-values"></a>設定および戻り値

ブール型 (**Boolean**) の値を設定または取得します。既定値は **True** です。**True** の場合は、親の **Recordset** オブジェクトの行位置が変更されるとチャプターが更新されます。**False** の場合は、親の **Recordset** オブジェクトの行位置が変更されても、チャプターは以前のチャプターのデータを参照し続けます。

## <a name="remarks"></a>注釈

このプロパティは、[Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) によってサポートされるような階層 Recordset に適用され、子の **Recordset** を取得する前に親の **Recordset** を設定しておく必要があります。このプロパティによって、階層レコードセット内の移動が容易になります。

