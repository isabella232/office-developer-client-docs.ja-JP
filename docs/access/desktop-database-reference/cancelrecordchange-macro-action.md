---
title: CancelRecordChange マクロ アクション
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d19e7adcdd3bb60f24d90e75942fcc0b4e16e2e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718544"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="cac71-102">CancelRecordChange マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="cac71-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="cac71-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cac71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cac71-104">" **CancelRecordChange/レコードの変更の取り消し** " アクションを使用して、変更を確定する前に **[CreateRecord](createrecord-data-block.md)** または **[EditRecord](editrecord-data-block.md)** データ ブロック内でレコードに適用した変更を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="cac71-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="cac71-105">[!メモ] " **CancelRecordChange/レコードの変更の取り消し** " アクションは、データ マクロ内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cac71-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="cac71-106">解説</span><span class="sxs-lookup"><span data-stu-id="cac71-106">Remarks</span></span>

<span data-ttu-id="cac71-107">" **CancelRecordChange/レコードの変更の取り消し** " アクションを呼び出すと、 **CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。</span><span class="sxs-lookup"><span data-stu-id="cac71-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

