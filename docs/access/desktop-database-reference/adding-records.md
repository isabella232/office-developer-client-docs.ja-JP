---
title: (デスクトップ データベース参照のアクセス) のレコードを追加します。
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 177eeb0499f3ba3376237c4773e776f8c7c7583f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946511"
---
# <a name="adding-records"></a><span data-ttu-id="c81db-102">レコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c81db-102">Adding records</span></span>

<span data-ttu-id="c81db-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c81db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c81db-p101">既存の **Recordset** 内に新しいレコードを作成し、これを初期化するには、 **AddNew** メソッドを使用します。 **Supports** メソッドで **CursorOptionEnum** 値の **adAddNew** を指定すると、現在の **Recordset** オブジェクトにレコードを追加できるかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c81db-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="c81db-p102">**AddNew** メソッドを呼び出した後は、新しいレコードが現在のレコードとなり、 **Update** メソッドを呼び出した後もそのままの状態です。 **Recordset** オブジェクトがブックマークをサポートしていない場合は、他のレコードに移動すると新しいレコードにアクセスできなくなる可能性があります。このため、カーソルの種類によっては、新しいレコードにアクセスできるようにするために、 **Requery** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c81db-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="c81db-109">現在のレコードの編集中、または新しいレコードの追加中に **AddNew** を呼び出すと、 **Update** メソッドが自動的に呼び出され、変更を保存してから新しいレコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c81db-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="c81db-110">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c81db-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="c81db-111">複数のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="c81db-111">Adding multiple fields</span></span>](adding-multiple-fields.md)
- [<span data-ttu-id="c81db-112">編集モードを決定します。</span><span class="sxs-lookup"><span data-stu-id="c81db-112">Determining Edit mode</span></span>](determining-edit-mode.md)
- [<span data-ttu-id="c81db-113">イミディ エイトとバッチ モードで AddNew を使用します。</span><span class="sxs-lookup"><span data-stu-id="c81db-113">Using AddNew in Immediate and Batch modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

