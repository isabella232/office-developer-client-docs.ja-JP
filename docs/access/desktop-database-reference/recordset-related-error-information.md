---
title: レコードセット関連のエラー情報
TOCTitle: Recordset-Related Error Information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62f9a6d235b6c06ad8e7fa49d7b89960fd1ad2b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478513"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="1853e-102">レコードセット関連のエラー情報</span><span class="sxs-lookup"><span data-stu-id="1853e-102">Recordset-Related Error Information</span></span>


<span data-ttu-id="1853e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1853e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1853e-104">バッチ処理中に、 **Recordset** オブジェクトの **Status** プロパティにより、 **Recordset** 内の個別のレコードに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1853e-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="1853e-105">バッチ更新が行われる前に、 **Recordset** の **Status** プロパティには、追加、変更、および削除されるレコードに関する情報が反映されます。</span><span class="sxs-lookup"><span data-stu-id="1853e-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="1853e-106">**UpdateBatch** が呼び出された後、 **Status** プロパティは、操作の成功または失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="1853e-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="1853e-107">**Recordset** 内のレコード間を移動すると、 **Status** プロパティの値が現在のレコードのステータスを示す値に変わります。</span><span class="sxs-lookup"><span data-stu-id="1853e-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

