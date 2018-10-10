---
title: CacheSize (デスクトップ データベース参照のアクセス) を使用します。
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e4937ee83251f9e4114827860da2ea571887ad8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478246"
---
# <a name="using-cachesize"></a><span data-ttu-id="27c81-102">CacheSize を使用する</span><span class="sxs-lookup"><span data-stu-id="27c81-102">Using CacheSize</span></span>


<span data-ttu-id="27c81-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="27c81-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="27c81-p101">**CacheSize** プロパティを使用すると、プロバイダーからローカル メモリに一度に取り込むレコード数を制御できます。たとえば、 **CacheSize** が 10 の場合、 **Recordset** オブジェクトが初めて開かれた後に、最初の 10 のレコードがプロバイダーによってローカル メモリに取り込まれます。 **Recordset** オブジェクト内を移動すると、プロバイダーはローカル メモリのバッファーからデータを返します。キャッシュ内の最後のレコードより後ろのレコードに移動すると、プロバイダーはすぐに次の 10 のレコードをデータ ソースからキャッシュに取り込みます。</span><span class="sxs-lookup"><span data-stu-id="27c81-p101">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>


> [!NOTE]
> <P><span data-ttu-id="27c81-p102">[!メモ] <STRONG>CacheSize</STRONG> は、 <STRONG>Recordset</STRONG> オブジェクトの <STRONG>Properties</STRONG> コレクションに含まれる <STRONG>Maximum Open Rows</STRONG> というプロバイダー固有のプロパティを基にしています。 <STRONG>CacheSize</STRONG> は、 <STRONG>Maximum Open Rows</STRONG> よりも大きい値には設定できません。プロバイダーが開くことのできる行数を変更するには、 <STRONG>Maximum Open Rows</STRONG> を設定します。</span><span class="sxs-lookup"><span data-stu-id="27c81-p102"><STRONG>CacheSize</STRONG> is based on the <STRONG>Maximum Open Rows</STRONG> provider-specific property (in the <STRONG>Properties</STRONG> collection of the <STRONG>Recordset</STRONG> object). You cannot set <STRONG>CacheSize</STRONG> to a value greater than <STRONG>Maximum Open Rows</STRONG>. To modify the number of rows that can be opened by the provider, set <STRONG>Maximum Open Rows</STRONG>.</span></span></P>



<span data-ttu-id="27c81-p103">**CacheSize** の値は、 **Recordset** オブジェクトの存続中に調整できますが、この値を変更しても、データ ソースから次にデータが取り込まれるまで、キャッシュ内のレコード数は変化しません。プロパティ値を変更しただけでは、キャッシュの現在の内容は変更されません。</span><span class="sxs-lookup"><span data-stu-id="27c81-p103">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="27c81-113">取り込まれるレコード数が **CacheSize** で指定された数よりも少ない場合は、残りのレコードが返され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="27c81-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="27c81-114">**CacheSize** を 0 に設定することはできません。これを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="27c81-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="27c81-p104">キャッシュから取り込まれたレコードには、他のユーザーがソース データに対して同時に加えた変更が反映されません。キャッシュされたすべてのデータの更新を強制実行するには、[Resync](resync-method-ado.md) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="27c81-p104">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="27c81-p105">**CacheSize** が 1 よりも大きい値に設定されている場合、レコードの取得後に削除操作が行われると、移動メソッド ([Move](move-method-ado.md)、[MoveFirst、MoveLast、MoveNext、および MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) によって、削除されたレコードに移動してしまう場合があります。最初のフェッチよりも後に実行された削除操作は、削除された行からデータ値にアクセスしようとしない限り、データ キャッシュに反映されません。ただし、**CacheSize** を 1 に設定すると、削除された行はフェッチできないため、この問題は発生しません。</span><span class="sxs-lookup"><span data-stu-id="27c81-p105">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

