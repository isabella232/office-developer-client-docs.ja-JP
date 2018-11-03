---
title: 階層レコード セットを永続化します。
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55f005818ef8fa44a2ee59542aa220f4d71eb687
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944985"
---
# <a name="persisting-hierarchical-recordsets"></a>階層レコード セットを永続化します。

**適用されます**Access 2013、Office 2013。

[Save](save-method-ado.md) メソッドを呼び出すことにより、階層 **Recordset** を ADTG 形式または XML 形式のファイルに保存できます。ただし、XML 形式で階層 **Recordset** を保存する場合には、保留中の更新を含んでいる **Recordset** は保存できない、および、パラメーター化された階層 **Recordset** は保存できないという 2 つの制限事項があります。

データ シェイプ プロバイダーの詳細については、「[Microsoft Data Shaping Service for OLE DB (ADO サービス コンポーネント)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)」および「Microsoft Data Shaping Service for OLE DB」を参照してください。

