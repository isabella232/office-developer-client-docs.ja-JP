---
title: allownullsenum (Access デスクトップデータベースリファレンス)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c184253551fa3f974de1840d47654af597881cb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297167"
---
# <a name="allownullsenum"></a><span data-ttu-id="c3ba8-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="c3ba8-102">AllowNullsEnum</span></span>

<span data-ttu-id="c3ba8-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3ba8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3ba8-104">Null 値を含むレコードにインデックスを付けるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c3ba8-104">Specifies whether records with null values are indexed.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3ba8-105">定数</span><span class="sxs-lookup"><span data-stu-id="c3ba8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c3ba8-106">値</span><span class="sxs-lookup"><span data-stu-id="c3ba8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c3ba8-107">説明</span><span class="sxs-lookup"><span data-stu-id="c3ba8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3ba8-108"><strong>adindexnullsallow</strong></span><span class="sxs-lookup"><span data-stu-id="c3ba8-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="c3ba8-109">.0</span><span class="sxs-lookup"><span data-stu-id="c3ba8-109">0</span></span></p></td>
<td><p><span data-ttu-id="c3ba8-p101">インデックスは、キー列が Null 値のエントリを許可します。Null 値がキー列に入力された場合、そのエントリはインデックスに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="c3ba8-p101">The index does allow entries in which the key columns are null. If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3ba8-112"><strong>adindexnullsdisallow</strong></span><span class="sxs-lookup"><span data-stu-id="c3ba8-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="c3ba8-113">1-d</span><span class="sxs-lookup"><span data-stu-id="c3ba8-113">1</span></span></p></td>
<td><p><span data-ttu-id="c3ba8-p102">既定値です。インデックスは、キー列が Null 値のエントリを許可しません。Null 値がキー列に入力された場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c3ba8-p102">Default. The index does not allow entries in which the key columns are null. If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3ba8-117"><strong>adindexnullsignore</strong></span><span class="sxs-lookup"><span data-stu-id="c3ba8-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="c3ba8-118">pbm-2</span><span class="sxs-lookup"><span data-stu-id="c3ba8-118">2</span></span></p></td>
<td><p><span data-ttu-id="c3ba8-p103">インデックスは、Null 値のキーを含むエントリを挿入しません。Null 値がキー列に入力された場合、そのエントリは無視され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="c3ba8-p103">The index does not insert entries containing null keys. If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3ba8-121"><strong>adIndexNullsIgnoreAny</strong></span><span class="sxs-lookup"><span data-stu-id="c3ba8-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="c3ba8-122">2/4</span><span class="sxs-lookup"><span data-stu-id="c3ba8-122">4</span></span></p></td>
<td><p><span data-ttu-id="c3ba8-p104">インデックスは、キー列に Null 値を含むエントリを挿入しません。複数列キーを持つインデックスでは、Null 値が入力された列がある場合、そのエントリは無視され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="c3ba8-p104">The index does not insert entries where some key column has a null value. For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>

