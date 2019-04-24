---
title: GetRows メソッド (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f7ce441eb837b76e824b55393741e0cf821bb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292224"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="c772d-102">GetRows メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="c772d-102">GetRows method (ADO)</span></span>

<span data-ttu-id="c772d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c772d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c772d-104">[Recordset](recordset-object-ado.md) オブジェクトの複数のレコードを配列に取り込みます。</span><span class="sxs-lookup"><span data-stu-id="c772d-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="c772d-105">構文</span><span class="sxs-lookup"><span data-stu-id="c772d-105">Syntax</span></span>

<span data-ttu-id="c772d-106">*配列* = *recordset*。GetRows (*行*、*開始*、*フィールド*)</span><span class="sxs-lookup"><span data-stu-id="c772d-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="c772d-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="c772d-107">Return value</span></span>

<span data-ttu-id="c772d-108">2 次元配列の値を持つバリアント型 (**Variant**) を返します。</span><span class="sxs-lookup"><span data-stu-id="c772d-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="c772d-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c772d-109">Parameters</span></span>

|<span data-ttu-id="c772d-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c772d-110">Parameter</span></span>|<span data-ttu-id="c772d-111">説明</span><span class="sxs-lookup"><span data-stu-id="c772d-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c772d-112">*Rows*</span><span class="sxs-lookup"><span data-stu-id="c772d-112">*Rows*</span></span> |<span data-ttu-id="c772d-p101">省略可能です。取得するレコード数を示す [GetRowsOptionEnum](getrowsoptionenum.md) 値を指定します。既定値は **adGetRowsRest** です。</span><span class="sxs-lookup"><span data-stu-id="c772d-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="c772d-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="c772d-116">*Start*</span></span> |<span data-ttu-id="c772d-p102">省略可能です。 **GetRows** 操作を開始するレコードへのブックマークとして評価される文字列型 ( **String** ) の値またはバリアント型 ( **Variant** ) を指定します。 [BookmarkEnum](bookmarkenum.md) 値を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="c772d-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="c772d-120">*Fields*</span><span class="sxs-lookup"><span data-stu-id="c772d-120">*Fields*</span></span> |<span data-ttu-id="c772d-p103">省略可能です。単一のフィールド名または順序を表す、あるいは複数のフィールド名または順序番号の配列を表す、バリアント型 ( **Variant** ) を指定します。指定したフィールドのデータだけが返されます。</span><span class="sxs-lookup"><span data-stu-id="c772d-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c772d-124">注釈</span><span class="sxs-lookup"><span data-stu-id="c772d-124">Remarks</span></span>

<span data-ttu-id="c772d-p104">**GetRows** メソッドでは、**Recordset** のレコードを 2 次元配列にコピーします。1 番目の添え字でフィールドを指定し、2 番目の添え字でレコード番号を指定します。**GetRows** メソッドからデータが返されると、*array* 変数は自動的に適切なサイズに調整されます。</span><span class="sxs-lookup"><span data-stu-id="c772d-p104">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array. The first subscript identifies the field and the second identifies the record number. The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="c772d-p105">*Rows* 引数の値を指定しないと、**GetRows** メソッドは **Recordset** オブジェクトのすべてのレコードを自動的に取得します。要求したレコード数が使用可能なレコード数より多い場合、**GetRows** は使用可能なレコード数だけを返します。</span><span class="sxs-lookup"><span data-stu-id="c772d-p105">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object. If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="c772d-130">**Recordset** オブジェクトがブックマークをサポートしている場合は、*Start* 引数にレコードの [Bookmark](bookmark-property-ado.md) プロパティの値を渡して、**GetRows** メソッドの取得開始レコードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c772d-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="c772d-131">**GetRows** の呼び出しで返されるフィールドを制限するには、*Fields* 引数に単一のフィールド名または番号、あるいは複数のフィールド名または番号の配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="c772d-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="c772d-132">**GetRows** を呼び出すと、まだ読み込まれていない次のレコードがカレント レコードになるか、それ以上レコードがない場合は [EOF](bof-eof-properties-ado.md) プロパティが **True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c772d-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

