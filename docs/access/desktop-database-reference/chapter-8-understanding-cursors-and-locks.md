---
title: '第 8 章: カーソルとロックについて'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3075c0c9bd8267f6b30773a846523172eb2ef603
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726093"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="d322e-102">第 8 章: カーソルとロックについて</span><span class="sxs-lookup"><span data-stu-id="d322e-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="d322e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d322e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d322e-p101">アプリケーションのデータ アクセス要件に最も適した、最も効率的な種類のカーソルを選択するには、カーソルの動作を理解することが大切です。カーソルの構成が最適でない場合、データ アクセス操作の速度が極端に低下することがあります。</span><span class="sxs-lookup"><span data-stu-id="d322e-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="d322e-106">ADO **Recordset** オブジェクトの機能の多くは、カーソルの種類と位置、さらにはロックの種類に左右されます。</span><span class="sxs-lookup"><span data-stu-id="d322e-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="d322e-107">この章では、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d322e-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="d322e-108">カーソルとは何ですか。</span><span class="sxs-lookup"><span data-stu-id="d322e-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="d322e-109">カーソル位置の重要性</span><span class="sxs-lookup"><span data-stu-id="d322e-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="d322e-110">OLE DB 用 Microsoft Cursor Service</span><span class="sxs-lookup"><span data-stu-id="d322e-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="d322e-111">CacheSize を使用する</span><span class="sxs-lookup"><span data-stu-id="d322e-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="d322e-112">カーソルとロックの特徴</span><span class="sxs-lookup"><span data-stu-id="d322e-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="d322e-113">(ADO) のカーソルの種類</span><span class="sxs-lookup"><span data-stu-id="d322e-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="d322e-114">ロックとは何ですか。(ADO)</span><span class="sxs-lookup"><span data-stu-id="d322e-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

