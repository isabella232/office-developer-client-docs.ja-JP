---
title: レコードセットに関連するエラー情報
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 12a67657d5543aac22a49690256b0410a2b901bd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708901"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="37339-102">レコードセットに関連するエラー情報</span><span class="sxs-lookup"><span data-stu-id="37339-102">Recordset-related error information</span></span>

<span data-ttu-id="37339-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="37339-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37339-104">バッチ処理中に、 **Recordset** オブジェクトの **Status** プロパティにより、 **Recordset** 内の個別のレコードに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="37339-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="37339-105">バッチ更新が行われる前に、 **Recordset** の **Status** プロパティには、追加、変更、および削除されるレコードに関する情報が反映されます。</span><span class="sxs-lookup"><span data-stu-id="37339-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="37339-106">**UpdateBatch** が呼び出された後、 **Status** プロパティは、操作の成功または失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="37339-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="37339-107">**Recordset** 内のレコード間を移動すると、 **Status** プロパティの値が現在のレコードのステータスを示す値に変わります。</span><span class="sxs-lookup"><span data-stu-id="37339-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

