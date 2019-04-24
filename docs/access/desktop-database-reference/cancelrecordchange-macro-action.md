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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296655"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="637c6-102">CancelRecordChange マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="637c6-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="637c6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="637c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="637c6-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span><span class="sxs-lookup"><span data-stu-id="637c6-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="637c6-105">The **CancelRecordChange** action is available only in Data Macros.</span><span class="sxs-lookup"><span data-stu-id="637c6-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="637c6-106">注釈</span><span class="sxs-lookup"><span data-stu-id="637c6-106">Remarks</span></span>

<span data-ttu-id="637c6-107">"**CancelRecordChange/レコードの変更の取り消し**" アクションを呼び出すと、**CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。</span><span class="sxs-lookup"><span data-stu-id="637c6-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

