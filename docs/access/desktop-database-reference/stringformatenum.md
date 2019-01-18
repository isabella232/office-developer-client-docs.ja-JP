---
title: StringFormatEnum (デスクトップ データベース参照のアクセス)
TOCTitle: StringFormatEnum
ms:assetid: ab069d67-d983-f390-5d45-876a9f9d9691
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249794(v=office.15)
ms:contentKeyID: 48546964
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89eb3e9c972b19bc9908f29ce5ec5e42c8974d54
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712275"
---
# <a name="stringformatenum"></a><span data-ttu-id="33c8f-102">StringFormatEnum</span><span class="sxs-lookup"><span data-stu-id="33c8f-102">StringFormatEnum</span></span>

<span data-ttu-id="33c8f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="33c8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33c8f-104">文字列として [Recordset](recordset-object-ado.md) を取得するときの形式を表します。</span><span class="sxs-lookup"><span data-stu-id="33c8f-104">Specifies the format when retrieving a [Recordset](recordset-object-ado.md) as a string.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33c8f-105">定数</span><span class="sxs-lookup"><span data-stu-id="33c8f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="33c8f-106">値</span><span class="sxs-lookup"><span data-stu-id="33c8f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="33c8f-107">説明</span><span class="sxs-lookup"><span data-stu-id="33c8f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33c8f-108"><strong>adClipString</strong></span><span class="sxs-lookup"><span data-stu-id="33c8f-108"><strong>adClipString</strong></span></span></p></td>
<td><p><span data-ttu-id="33c8f-109">2</span><span class="sxs-lookup"><span data-stu-id="33c8f-109">2</span></span></p></td>
<td><p><span data-ttu-id="33c8f-p101">行が <em>RowDelimiter</em> によって、列が <em>ColumnDelimiter</em> によって、null 値が <em>NullExpr</em> によって区切られます。<a href="getstring-method-ado.md">GetString</a> メソッドのこれらの 3 つのパラメーターは、<strong>adClipString</strong> の <em>StringFormat</em> とのみ併用できます。</span><span class="sxs-lookup"><span data-stu-id="33c8f-p101">Delimits rows by <em>RowDelimiter</em>, columns by <em>ColumnDelimiter</em>, and null values by <em>NullExpr</em>. These three parameters of the <a href="getstring-method-ado.md">GetString</a> method are valid only with a <em>StringFormat</em> of <strong>adClipString</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="33c8f-112">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="33c8f-112">ADO/WFC equivalent</span></span>

<span data-ttu-id="33c8f-113">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="33c8f-113">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33c8f-114">定数</span><span class="sxs-lookup"><span data-stu-id="33c8f-114">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33c8f-115">AdoEnums.StringFormat.CLIPSTRING</span><span class="sxs-lookup"><span data-stu-id="33c8f-115">AdoEnums.StringFormat.CLIPSTRING</span></span></p></td>
</tr>
</tbody>
</table>

