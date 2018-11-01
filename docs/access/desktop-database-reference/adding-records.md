---
title: (デスクトップ データベース参照のアクセス) のレコードを追加します。
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 760c9b2915b84457d64325c97c5118fb5debc925
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880594"
---
# <a name="adding-records"></a><span data-ttu-id="84381-102">レコードの追加</span><span class="sxs-lookup"><span data-stu-id="84381-102">Adding Records</span></span>


<span data-ttu-id="84381-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="84381-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84381-p101">既存の **Recordset** 内に新しいレコードを作成し、これを初期化するには、 **AddNew** メソッドを使用します。 **Supports** メソッドで **CursorOptionEnum** 値の **adAddNew** を指定すると、現在の **Recordset** オブジェクトにレコードを追加できるかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="84381-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="84381-p102">**AddNew** メソッドを呼び出した後は、新しいレコードが現在のレコードとなり、 **Update** メソッドを呼び出した後もそのままの状態です。 **Recordset** オブジェクトがブックマークをサポートしていない場合は、他のレコードに移動すると新しいレコードにアクセスできなくなる可能性があります。このため、カーソルの種類によっては、新しいレコードにアクセスできるようにするために、 **Requery** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="84381-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="84381-109">現在のレコードの編集中、または新しいレコードの追加中に **AddNew** を呼び出すと、 **Update** メソッドが自動的に呼び出され、変更を保存してから新しいレコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="84381-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="84381-110">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="84381-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="84381-111">複数のフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="84381-111">Adding Multiple Fields</span></span>](adding-multiple-fields.md)

- [<span data-ttu-id="84381-112">編集モードを判断する</span><span class="sxs-lookup"><span data-stu-id="84381-112">Determining Edit Mode</span></span>](determining-edit-mode.md)

- [<span data-ttu-id="84381-113">イミディエイト モードとバッチ モードで AddNew を使用する</span><span class="sxs-lookup"><span data-stu-id="84381-113">Using AddNew in Immediate and Batch Modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

