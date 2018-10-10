---
title: (デスクトップ データベース参照のアクセス) のデータを更新します。
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f507cb7d8939a4d4da65b570ae8e2db53cc8c7c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477121"
---
# <a name="updating-data"></a><span data-ttu-id="fdc88-102">データを更新する</span><span class="sxs-lookup"><span data-stu-id="fdc88-102">Updating Data</span></span>


<span data-ttu-id="fdc88-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdc88-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fdc88-104">更新動作および更新機能は、更新モード (ロックの種類)、カーソルの種類、およびカーソル位置に大きく依存します。</span><span class="sxs-lookup"><span data-stu-id="fdc88-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="fdc88-p101">**AddNew** メソッドを呼び出した後、または既存のレコードのフィールドを変更した後に行われた **Recordset** オブジェクトの現在のレコードへの変更内容を保存するには、 **Update** メソッドを使用します。 **Recordset** オブジェクトは、更新をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdc88-p101">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="fdc88-p102">**Recordset** オブジェクトがバッチ更新をサポートしている場合、 **UpdateBatch** メソッドを呼び出すまで、1 つ以上のレコードに対する複数の変更をローカルにキャッシュできます。現在のレコードの編集中、または新規レコードの追加中に **UpdateBatch** メソッドを呼び出すと、変更を一括してプロバイダーに送信する前に、 **Update** メソッドが自動的に呼び出され、現在のレコードの保留中の変更がすべて保存されます。</span><span class="sxs-lookup"><span data-stu-id="fdc88-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="fdc88-109">**Update** メソッドまたは **UpdateBatch** メソッドを呼び出した後も、現在のレコードは変わりません。</span><span class="sxs-lookup"><span data-stu-id="fdc88-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

