---
title: GetString メソッド (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba235094aa7f491cbd86bf753713d50f01009d47
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605402"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="61567-102">GetString メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="61567-102">GetString Method (ADO)</span></span>


<span data-ttu-id="61567-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="61567-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="61567-104">[Recordset](recordset-object-ado.md) を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="61567-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="61567-105">構文</span><span class="sxs-lookup"><span data-stu-id="61567-105">Syntax</span></span>

<span data-ttu-id="61567-106">*バリアント* = *レコード セット*です。GetString (*StringFormat*、 *NumRows*、 *";"と*、 *RowDelimiter*、 *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="61567-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

<span data-ttu-id="61567-107"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="61567-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="61567-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="61567-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="61567-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="61567-109">Return value</span></span>
>>>>>>> <span data-ttu-id="61567-110">master</span><span class="sxs-lookup"><span data-stu-id="61567-110">master</span></span>

<span data-ttu-id="61567-111">**Recordset** を文字列値を持つバリアント型 ( **Variant** )、つまり、BSTR として返します。</span><span class="sxs-lookup"><span data-stu-id="61567-111">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="61567-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="61567-112">Parameters</span></span>

  - <span data-ttu-id="61567-113">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="61567-113">*StringFormat*</span></span>

  - <span data-ttu-id="61567-p101">**Recordset** を文字列に変換する方法を示す [StringFormatEnum](stringformatenum.md) 値を指定します。*RowDelimiter*、*ColumnDelimiter*、および *NullExpr* パラメーターは、*StringFormat* に **adClipString** を指定した場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="61567-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="61567-116">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="61567-116">*NumRows*</span></span>

  - <span data-ttu-id="61567-117">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="61567-117">Optional.</span></span> <span data-ttu-id="61567-118">**Recordset** から変換する行数を指定します。</span><span class="sxs-lookup"><span data-stu-id="61567-118">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="61567-119">*NumRows*を指定しない場合、または**レコード セット**内の行の合計数より大きい場合は、**レコード セット**内のすべての行は変換されます。</span><span class="sxs-lookup"><span data-stu-id="61567-119">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="61567-120">*";"と*</span><span class="sxs-lookup"><span data-stu-id="61567-120">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="61567-p103">省略可能です。列間に使用する区切り記号を指定し、指定しないとタブ文字が使用されます。</span><span class="sxs-lookup"><span data-stu-id="61567-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="61567-123">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="61567-123">*RowDelimiter*</span></span>

  - <span data-ttu-id="61567-p104">省略可能です。行間に使用する区切り記号を指定し、指定しないとキャリッジ リターン文字が使用されます。</span><span class="sxs-lookup"><span data-stu-id="61567-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="61567-126">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="61567-126">*NullExpr*</span></span>

  - <span data-ttu-id="61567-p105">省略可能です。Null 値の代わりに使用する表現を指定し、指定しないと空文字列が使用されます。</span><span class="sxs-lookup"><span data-stu-id="61567-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="61567-129">解説</span><span class="sxs-lookup"><span data-stu-id="61567-129">Remarks</span></span>

<span data-ttu-id="61567-p106">文字列には行データが保存され、スキーマ データは保存されません。したがって、この文字列を使用して **Recordset** を再度開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="61567-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="61567-132">このメソッドは、RDO の **GetClipString** メソッドと同等です。</span><span class="sxs-lookup"><span data-stu-id="61567-132">This method is equivalent to the RDO **GetClipString** method.</span></span>

