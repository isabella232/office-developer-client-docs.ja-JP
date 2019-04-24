---
title: GetString メソッド (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292189"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="41880-102">GetString メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="41880-102">GetString method (ADO)</span></span>

<span data-ttu-id="41880-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="41880-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41880-104">[Recordset](recordset-object-ado.md) を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="41880-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="41880-105">構文</span><span class="sxs-lookup"><span data-stu-id="41880-105">Syntax</span></span>

<span data-ttu-id="41880-106">*バリアント型 (Variant* = ) の*recordset*。GetString (*StringFormat*、 *numrows*、 *columndelimiter*、 *rowdelimiter*、 *nullexpr*)</span><span class="sxs-lookup"><span data-stu-id="41880-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="41880-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="41880-107">Return value</span></span>

<span data-ttu-id="41880-108">**Recordset** を文字列値を持つバリアント型 (**Variant**)、つまり、BSTR として返します。</span><span class="sxs-lookup"><span data-stu-id="41880-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="41880-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="41880-109">Parameters</span></span>

|<span data-ttu-id="41880-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="41880-110">Parameter</span></span>|<span data-ttu-id="41880-111">説明</span><span class="sxs-lookup"><span data-stu-id="41880-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="41880-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="41880-112">*StringFormat*</span></span> |<span data-ttu-id="41880-p101">**Recordset** を文字列に変換する方法を示す [StringFormatEnum](stringformatenum.md) 値を指定します。*RowDelimiter*、*ColumnDelimiter*、および *NullExpr* パラメーターは、*StringFormat* に **adClipString** を指定した場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="41880-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="41880-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="41880-115">*NumRows*</span></span> |<span data-ttu-id="41880-p102">省略可能です。**Recordset** から変換する行数を指定します。*NumRows* を指定しない場合、または **Recordset** の行の総数より大きい値を指定した場合は、**Recordset** のすべての行が変換されます。</span><span class="sxs-lookup"><span data-stu-id="41880-p102">Optional. The number of rows to be converted in the **Recordset**. If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="41880-119">*columndelimiter*</span><span class="sxs-lookup"><span data-stu-id="41880-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="41880-p103">省略可能です。列間に使用する区切り記号を指定し、指定しないとタブ文字が使用されます。</span><span class="sxs-lookup"><span data-stu-id="41880-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="41880-122">*rowdelimiter*</span><span class="sxs-lookup"><span data-stu-id="41880-122">*RowDelimiter*</span></span> |<span data-ttu-id="41880-p104">省略可能です。行間に使用する区切り記号を指定し、指定しないとキャリッジ リターン文字が使用されます。</span><span class="sxs-lookup"><span data-stu-id="41880-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="41880-125">*nullexpr*</span><span class="sxs-lookup"><span data-stu-id="41880-125">*NullExpr*</span></span> |<span data-ttu-id="41880-p105">省略可能です。Null 値の代わりに使用する表現を指定し、指定しないと空文字列が使用されます。</span><span class="sxs-lookup"><span data-stu-id="41880-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="41880-128">注釈</span><span class="sxs-lookup"><span data-stu-id="41880-128">Remarks</span></span>

<span data-ttu-id="41880-p106">文字列には行データが保存され、スキーマ データは保存されません。したがって、この文字列を使用して **Recordset** を再度開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="41880-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="41880-131">このメソッドは、RDO の **GetClipString** メソッドと同等です。</span><span class="sxs-lookup"><span data-stu-id="41880-131">This method is equivalent to the RDO **GetClipString** method.</span></span>

