---
title: 階層レコードセットの永続化
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1964d207f2b35eaeaf51b409adc12a41eac6438f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287581"
---
# <a name="persisting-hierarchical-recordsets"></a><span data-ttu-id="d2be4-102">階層レコードセットの永続化</span><span class="sxs-lookup"><span data-stu-id="d2be4-102">Persisting hierarchical Recordsets</span></span>

<span data-ttu-id="d2be4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2be4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2be4-p101">[Save](save-method-ado.md) メソッドを呼び出すことにより、階層 **Recordset** を ADTG 形式または XML 形式のファイルに保存できます。ただし、XML 形式で階層 **Recordset** を保存する場合には、保留中の更新を含んでいる **Recordset** は保存できない、および、パラメーター化された階層 **Recordset** は保存できないという 2 つの制限事項があります。</span><span class="sxs-lookup"><span data-stu-id="d2be4-p101">You can save a hierarchical **Recordset** to a file in either ADTG or XML format by calling the [Save](save-method-ado.md) method. However, two limitations apply when saving hierarchical **Recordset**s in XML format: You cannot save in XML if the hierarchical **Recordset** contains pending updates, and you cannot save a parameterized hierarchical **Recordset**.</span></span>

<span data-ttu-id="d2be4-106">データ シェイプ プロバイダーの詳細については、「[Microsoft Data Shaping Service for OLE DB (ADO サービス コンポーネント)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)」および「Microsoft Data Shaping Service for OLE DB」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2be4-106">For more information about the Data Shaping provider, see [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) and The Data Shaping Service for OLE DB(OLE DB).</span></span>

