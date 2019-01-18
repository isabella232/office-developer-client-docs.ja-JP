---
title: 既存のレコードの編集
TOCTitle: Editing existing records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dae80ddb85709ccc668e80adad0cb0c723c79cd5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710861"
---
# <a name="editing-existing-records"></a><span data-ttu-id="5eb14-102">既存のレコードの編集</span><span class="sxs-lookup"><span data-stu-id="5eb14-102">Editing existing records</span></span>


<span data-ttu-id="5eb14-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5eb14-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5eb14-p101">既存のレコードを編集するには、編集対象の行に移動し、変更するフィールドの **Value** プロパティを変更します。 **Field** オブジェクトの **Value** プロパティの詳細については、「 [3 章: データを調べる](chapter-3-examining-data.md)」を参照してください。変更をデータ ソースに送り返すには、カーソルの種類に応じ、 **Update** または **UpdateBatch** を使用します。詳細については、「 [5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5eb14-p101">To edit existing records, move to the row you want to edit and change the **Value** property of the fields you want to change. For more information about the **Field** object's **Value** property, see [Chapter 3: Examining Data](chapter-3-examining-data.md). Depending on your cursor type, you will use **Update** or **UpdateBatch** to send changes back to the data source. For more information, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

<span data-ttu-id="5eb14-p102">通常、更新や、その他の操作を実行するときは、ストアド プロシージャをコマンド オブジェクトと共に使用すると、より効率的です。これは、ストアド プロシージャがカーソルの作成を必要としないからです。カーソルの詳細については、「[8 章: カーソルとロックの概要](chapter-8-understanding-cursors-and-locks.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5eb14-p102">It is usually more efficient to use a stored procedure with a command object to perform updates, as well as to perform other operations, because a stored procedure does not require the creation of a cursor. For more information about cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

