---
title: "'CancelRecordChange/レコードの変更の取り消し' マクロ アクション"
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fe474f9ba7250e3225bc73460c6d192800c861b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477735"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="a8dbc-102">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a8dbc-102">CancelRecordChange Macro Action</span></span>


<span data-ttu-id="a8dbc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8dbc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a8dbc-104">" **CancelRecordChange/レコードの変更の取り消し** " アクションを使用して、変更を確定する前に **[CreateRecord](createrecord-data-block.md)** または **[EditRecord](editrecord-data-block.md)** データ ブロック内でレコードに適用した変更を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="a8dbc-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a8dbc-105">[!メモ] " <STRONG>CancelRecordChange/レコードの変更の取り消し</STRONG> " アクションは、データ マクロ内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="a8dbc-105">The <STRONG>CancelRecordChange</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="a8dbc-106">備考</span><span class="sxs-lookup"><span data-stu-id="a8dbc-106">Remarks</span></span>

<span data-ttu-id="a8dbc-107">" **CancelRecordChange/レコードの変更の取り消し** " アクションを呼び出すと、 **CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。</span><span class="sxs-lookup"><span data-stu-id="a8dbc-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

