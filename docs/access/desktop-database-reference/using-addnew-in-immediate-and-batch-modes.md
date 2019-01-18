---
title: イミディエイト モードとバッチ モードで AddNew を使用する
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 929c01032924182d8db1bd5b06b573fb5d0171ae
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701579"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a><span data-ttu-id="d7fb3-102">イミディ エイトとバッチ モードで AddNew を使用します。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-102">Using AddNew in Immediate and Batch modes</span></span>


<span data-ttu-id="d7fb3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7fb3-104">**AddNew**メソッドの動作は、**レコード セット**オブジェクトと、 *FieldList*と*値*の引数を渡すかどうかの更新モードに依存します。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-104">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *FieldList* and *Values* arguments.</span></span>

<span data-ttu-id="d7fb3-p101">**Update** メソッドを呼び出すとプロバイダーによって基になるデータ ソースに変更が書き込まれるイミディエイト更新モードでは、引数を指定せずに **AddNew** メソッドを呼び出すと、**EditMode** プロパティが **adEditAdd** に設定されます。プロバイダーは、フィールドの値に変更があった場合、それをローカルにキャッシュします。**Update** メソッドを呼び出すと、新しいレコードがデータベースに保存され、**EditMode** プロパティが **adEditNone** にリセットされます。*FieldList* 引数と *Values* 引数を指定した場合は、直ちに新しいレコードが自動的にデータベースに保存されます (**Update** を呼び出す必要はありません)。この場合、**EditMode** プロパティの値は **adEditNone** のまま変化しません。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-p101">In immediate update mode (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd.** The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone**. If you pass the *FieldList* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="d7fb3-109">バッチ更新モードでは、引数を指定しないで**AddNew**メソッドを呼び出すと、 **EditMode**プロパティ**adEditAdd**に設定します。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-109">In batch update mode, calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="d7fb3-110">プロバイダーは、ローカルでのフィールド値の変更をキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-110">The provider caches any field value changes locally.</span></span> <span data-ttu-id="d7fb3-111">**UpdateBatch が呼び出されるまで、プロバイダーは基になるデータベースへの変更 post しないですが、現在の**レコード セット**に新しいレコードを追加します。 **Update**メソッドを呼び出すと、 **EditMode**プロパティが**adEditNone**にリセット**メソッドです。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-111">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="d7fb3-112">ADO がプロバイダーをキャッシュに格納するために新しいレコードを送信する、 *FieldList*と*値*の引数を渡す場合**UpdateBatch**メソッドを呼び出して基になるデータベースに新しいレコードを転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-112">If you pass the *FieldList* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span> <span data-ttu-id="d7fb3-113">**および**UpdateBatch\*\*\*\* の詳細についてを参照してください[第 5 章: データを更新し保存する](chapter-5-updating-and-persisting-data.md)です。</span><span class="sxs-lookup"><span data-stu-id="d7fb3-113">For more information about **Update** and **UpdateBatch**, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

