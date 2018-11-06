---
title: Requery メソッド (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0105fb67c095355e607c6c73fc73fc4c6b1050ed
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998195"
---
# <a name="requery-method-ado"></a><span data-ttu-id="27916-102">Requery メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="27916-102">Requery method (ADO)</span></span>

<span data-ttu-id="27916-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="27916-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27916-104">オブジェクトの基になるクエリを再実行して、[Recordset](recordset-object-ado.md) オブジェクトのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="27916-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="27916-105">構文</span><span class="sxs-lookup"><span data-stu-id="27916-105">Syntax</span></span>

<span data-ttu-id="27916-106">*レコード セット*です。*オプション*のクエリを再実行します。</span><span class="sxs-lookup"><span data-stu-id="27916-106">*recordset*.Requery *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="27916-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="27916-107">Parameters</span></span>

|<span data-ttu-id="27916-108">名前</span><span class="sxs-lookup"><span data-stu-id="27916-108">Name</span></span> |<span data-ttu-id="27916-109">説明</span><span class="sxs-lookup"><span data-stu-id="27916-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="27916-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="27916-110">*Options*</span></span> |<span data-ttu-id="27916-p101">省略可能です。この操作に対する [ExecuteOptionEnum](executeoptionenum.md) 値と [CommandTypeEnum](commandtypeenum.md) 値を含む、ビットマスクを指定します。</span><span class="sxs-lookup"><span data-stu-id="27916-p101">Optional. A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>|

> [!NOTE]
> <span data-ttu-id="27916-113">*オプション*は、 **adAsyncExecute**に設定されている場合、この操作を非同期に実行され、 [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md)イベントが終了するときに発行されます。</span><span class="sxs-lookup"><span data-stu-id="27916-113">If *Options* is set to **adAsyncExecute**, this operation will execute asynchronously and a [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) event will be issued when it concludes.</span></span>

<span data-ttu-id="27916-114">**Requery** では、 **ExecuteOpenEnum** の値 **adExecuteNoRecords** または **adExecuteStream** は使用できません。</span><span class="sxs-lookup"><span data-stu-id="27916-114">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="27916-115">解説</span><span class="sxs-lookup"><span data-stu-id="27916-115">Remarks</span></span>

<span data-ttu-id="27916-p102">**Requery** メソッドは、元のコマンドを再実行してデータをもう一度取得することにより、データ ソースで **Recordset** オブジェクトの内容全体を更新する場合に使用します。このメソッドの呼び出しは、 [Close](close-method-ado.md) メソッドと [Open](open-method-ado-recordset.md) メソッドを連続して呼び出すことと同じです。カレント レコードを編集しているとき、または新規レコードを追加しているときにこのメソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="27916-p102">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time. Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession. If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="27916-p103">**Recordset** オブジェクトを開いている間は、カーソルの属性を定義するプロパティ ([CursorType](cursortype-property-ado.md)、[LockType](locktype-property-ado.md)、[MaxRecords](maxrecords-property-ado.md) など) は、読み取り専用になります。したがって、**Requery** メソッドでは、現在のカーソルの更新のみを行うことができます。カーソルのプロパティを変更して結果を確認するには、[Close](close-method-ado.md) メソッドを使用して、プロパティを再度読み取り/書き込み可能にする必要があります。その後、目的のプロパティの設定を変更し、[Open](open-method-ado-recordset.md) メソッドを呼び出してカーソルを再度開きます。</span><span class="sxs-lookup"><span data-stu-id="27916-p103">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only. Thus, the **Requery** method can only refresh the current cursor. To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again. You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

