---
title: GetRows メソッド (ADO)
TOCTitle: GetRows Method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 99988383c40b84e1993582ad0d1c07491de82933
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879880"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="b4ca1-102">GetRows メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="b4ca1-102">GetRows Method (ADO)</span></span>


<span data-ttu-id="b4ca1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b4ca1-104">[Recordset](recordset-object-ado.md) オブジェクトの複数のレコードを配列に取り込みます。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ca1-105">構文</span><span class="sxs-lookup"><span data-stu-id="b4ca1-105">Syntax</span></span>

<span data-ttu-id="b4ca1-106">*配列* = *レコード セット*です。GetRows (*行*を*開始*する*フィールド*)</span><span class="sxs-lookup"><span data-stu-id="b4ca1-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="b4ca1-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="b4ca1-107">Return value</span></span>

<span data-ttu-id="b4ca1-108">2 次元配列の値を持つバリアント型 ( **Variant** ) を返します。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4ca1-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b4ca1-109">Parameters</span></span>

  - <span data-ttu-id="b4ca1-110">*Rows*</span><span class="sxs-lookup"><span data-stu-id="b4ca1-110">*Rows*</span></span>

  - <span data-ttu-id="b4ca1-p101">省略可能です。取得するレコード数を示す [GetRowsOptionEnum](getrowsoptionenum.md) 値を指定します。既定値は **adGetRowsRest** です。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>

  - <span data-ttu-id="b4ca1-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="b4ca1-114">*Start*</span></span>

  - <span data-ttu-id="b4ca1-p102">省略可能です。 **GetRows** 操作を開始するレコードへのブックマークとして評価される文字列型 ( **String** ) の値またはバリアント型 ( **Variant** ) を指定します。 [BookmarkEnum](bookmarkenum.md) 値を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

  - <span data-ttu-id="b4ca1-118">*Fields*</span><span class="sxs-lookup"><span data-stu-id="b4ca1-118">*Fields*</span></span>

  - <span data-ttu-id="b4ca1-p103">省略可能です。単一のフィールド名または順序を表す、あるいは複数のフィールド名または順序番号の配列を表す、バリアント型 ( **Variant** ) を指定します。指定したフィールドのデータだけが返されます。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ca1-122">解説</span><span class="sxs-lookup"><span data-stu-id="b4ca1-122">Remarks</span></span>

<span data-ttu-id="b4ca1-123">**GetRows** メソッドでは、 **Recordset** のレコードを 2 次元配列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-123">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="b4ca1-124">1 番目の添え字でフィールドを指定し、2 番目の添え字でレコード番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-124">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="b4ca1-125">**GetRows**メソッドにはデータが返されるときに、*配列*変数の次元は適切なサイズに自動的が。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-125">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="b4ca1-126">*行*の引数の値を指定しないと、 **GetRows**メソッドは、 **Recordset**オブジェクト内のすべてのレコードを自動的に取得します。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-126">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="b4ca1-127">要求したレコード数が使用可能なレコード数より多い場合、 **GetRows** は使用可能なレコード数だけを返します。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-127">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="b4ca1-128">**Recordset**オブジェクトはブックマークをサポートする場合は、どのレコードを**GetRows**メソッドを開始引数*Start*にレコードの[Bookmark](bookmark-property-ado.md)プロパティの値を渡すことによってデータを取得するを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-128">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="b4ca1-129">**GetRows**の呼び出しを返すフィールドを制限する場合は、 *Fields*引数に単一のフィールド名または番号またはフィールド名または番号の配列を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-129">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="b4ca1-130">**GetRows** を呼び出すと、まだ読み込まれていない次のレコードがカレント レコードになるか、それ以上レコードがない場合は [EOF](bof-eof-properties-ado.md) プロパティが **True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b4ca1-130">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

