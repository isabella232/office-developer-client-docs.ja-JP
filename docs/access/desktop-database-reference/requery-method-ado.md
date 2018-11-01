---
title: Requery メソッド (ADO)
TOCTitle: Requery Method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be8cbda9e185b3e0b28717e7216f3ff6bea5238c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876128"
---
# <a name="requery-method-ado"></a><span data-ttu-id="5e820-102">Requery メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="5e820-102">Requery Method (ADO)</span></span>


<span data-ttu-id="5e820-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5e820-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="5e820-104">オブジェクトの基になるクエリを再実行して、[Recordset](recordset-object-ado.md) オブジェクトのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="5e820-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e820-105">構文</span><span class="sxs-lookup"><span data-stu-id="5e820-105">Syntax</span></span>

<span data-ttu-id="5e820-106">*レコード セット*です。*オプション*のクエリを再実行します。</span><span class="sxs-lookup"><span data-stu-id="5e820-106">*recordset*.Requery *Options*</span></span>

## <a name="parameter"></a><span data-ttu-id="5e820-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e820-107">Parameter</span></span>

  - <span data-ttu-id="5e820-108">*Options*</span><span class="sxs-lookup"><span data-stu-id="5e820-108">*Options*</span></span>

  - <span data-ttu-id="5e820-p101">省略可能です。この操作に対する [ExecuteOptionEnum](executeoptionenum.md) 値と [CommandTypeEnum](commandtypeenum.md) 値を含む、ビットマスクを指定します。</span><span class="sxs-lookup"><span data-stu-id="5e820-p101">Optional. A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5e820-111"><EM>オプション</EM>は、 <STRONG>adAsyncExecute</STRONG>に設定されている場合、この操作を非同期に実行され、 <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A>イベントが終了するときに発行されます。</span><span class="sxs-lookup"><span data-stu-id="5e820-111">If <EM>Options</EM> is set to <STRONG>adAsyncExecute</STRONG>, this operation will execute asynchronously and a <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> event will be issued when it concludes.</span></span></P>



<span data-ttu-id="5e820-112">**Requery** では、 **ExecuteOpenEnum** の値 **adExecuteNoRecords** または **adExecuteStream** は使用できません。</span><span class="sxs-lookup"><span data-stu-id="5e820-112">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e820-113">解説</span><span class="sxs-lookup"><span data-stu-id="5e820-113">Remarks</span></span>

<span data-ttu-id="5e820-p102">**Requery** メソッドは、元のコマンドを再実行してデータをもう一度取得することにより、データ ソースで **Recordset** オブジェクトの内容全体を更新する場合に使用します。このメソッドの呼び出しは、 [Close](close-method-ado.md) メソッドと [Open](open-method-ado-recordset.md) メソッドを連続して呼び出すことと同じです。カレント レコードを編集しているとき、または新規レコードを追加しているときにこのメソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5e820-p102">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time. Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession. If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="5e820-p103">**Recordset** オブジェクトを開いている間は、カーソルの属性を定義するプロパティ ([CursorType](cursortype-property-ado.md)、[LockType](locktype-property-ado.md)、[MaxRecords](maxrecords-property-ado.md) など) は、読み取り専用になります。したがって、**Requery** メソッドでは、現在のカーソルの更新のみを行うことができます。カーソルのプロパティを変更して結果を確認するには、[Close](close-method-ado.md) メソッドを使用して、プロパティを再度読み取り/書き込み可能にする必要があります。その後、目的のプロパティの設定を変更し、[Open](open-method-ado-recordset.md) メソッドを呼び出してカーソルを再度開きます。</span><span class="sxs-lookup"><span data-stu-id="5e820-p103">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only. Thus, the **Requery** method can only refresh the current cursor. To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again. You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

