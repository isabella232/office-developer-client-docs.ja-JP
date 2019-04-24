---
title: カーソルの場所列挙 (Access デスクトップデータベースリファレンス)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295213"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="5fe4f-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="5fe4f-102">CursorLocationEnum</span></span>

<span data-ttu-id="5fe4f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fe4f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5fe4f-104">カーソル サービスの場所を表します。</span><span class="sxs-lookup"><span data-stu-id="5fe4f-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fe4f-105">定数</span><span class="sxs-lookup"><span data-stu-id="5fe4f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5fe4f-106">値</span><span class="sxs-lookup"><span data-stu-id="5fe4f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5fe4f-107">説明</span><span class="sxs-lookup"><span data-stu-id="5fe4f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fe4f-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="5fe4f-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe4f-109">1/3</span><span class="sxs-lookup"><span data-stu-id="5fe4f-109">3</span></span></p></td>
<td><p><span data-ttu-id="5fe4f-110">ローカルカーソルライブラリによって提供されるクライアント側カーソルを使用します。</span><span class="sxs-lookup"><span data-stu-id="5fe4f-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="5fe4f-111">多くの場合、ローカル カーソル サービスにはドライバーによって提供されるカーソルよりも多くのカーソル機能があるので、この設定を利用すると、より高度な機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="5fe4f-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="5fe4f-112">以前のバージョンとの互換性を保つために、同じ意味を持つ <strong>adUseClientBatch</strong> もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5fe4f-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe4f-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="5fe4f-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe4f-114">1-d</span><span class="sxs-lookup"><span data-stu-id="5fe4f-114">1</span></span></p></td>
<td><p><span data-ttu-id="5fe4f-p102">カーソル サービスを使用しません。(この定数は現在使用されておらず、以前のバージョンとの互換性を保つために装備されています。)</span><span class="sxs-lookup"><span data-stu-id="5fe4f-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe4f-117"><strong>が aduseserver</strong></span><span class="sxs-lookup"><span data-stu-id="5fe4f-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe4f-118">pbm-2</span><span class="sxs-lookup"><span data-stu-id="5fe4f-118">2</span></span></p></td>
<td><p><span data-ttu-id="5fe4f-119">既定値。</span><span class="sxs-lookup"><span data-stu-id="5fe4f-119">Default.</span></span> <span data-ttu-id="5fe4f-120">データ プロバイダー カーソルまたはドライバーによって提供されるカーソルを使用します。</span><span class="sxs-lookup"><span data-stu-id="5fe4f-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="5fe4f-121">これらのカーソルは、多くの場合柔軟性が高く、他のユーザーが行うデータ ソースへの変更を検出できます。</span><span class="sxs-lookup"><span data-stu-id="5fe4f-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="5fe4f-122">ただし、 <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (関連付けられていない<a href="recordset-object-ado.md">Recordset</a>オブジェクトなど) の一部の機能は、サーバー側カーソルを使用してシミュレートすることはできません。この設定では、これらの機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="5fe4f-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="5fe4f-123">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="5fe4f-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="5fe4f-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="5fe4f-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fe4f-125">定数</span><span class="sxs-lookup"><span data-stu-id="5fe4f-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fe4f-126">AdoEnums (クライアントの場所)</span><span class="sxs-lookup"><span data-stu-id="5fe4f-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe4f-127">AdoEnums。なし</span><span class="sxs-lookup"><span data-stu-id="5fe4f-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe4f-128">AdoEnums (サーバーの場所)</span><span class="sxs-lookup"><span data-stu-id="5fe4f-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

