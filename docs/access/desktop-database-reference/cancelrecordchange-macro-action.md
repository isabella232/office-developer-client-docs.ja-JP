---
title: "'CancelRecordChange/レコードの変更の取り消し' マクロ アクション"
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddf6a6eb71d60fb98d92a9ce18bfd871f298f702
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864208"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="9547d-102">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="9547d-102">CancelRecordChange Macro Action</span></span>


<span data-ttu-id="9547d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9547d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9547d-104">" **CancelRecordChange/レコードの変更の取り消し** " アクションを使用して、変更を確定する前に **[CreateRecord](createrecord-data-block.md)** または **[EditRecord](editrecord-data-block.md)** データ ブロック内でレコードに適用した変更を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="9547d-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="9547d-105">[!メモ] " **CancelRecordChange/レコードの変更の取り消し** " アクションは、データ マクロ内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9547d-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="9547d-106">備考</span><span class="sxs-lookup"><span data-stu-id="9547d-106">Remarks</span></span>

<span data-ttu-id="9547d-107">" **CancelRecordChange/レコードの変更の取り消し** " アクションを呼び出すと、 **CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。</span><span class="sxs-lookup"><span data-stu-id="9547d-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

