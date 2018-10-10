---
title: CursorLocationEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477573"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="6b2f6-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="6b2f6-102">CursorLocationEnum</span></span>


<span data-ttu-id="6b2f6-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b2f6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6b2f6-104">カーソル サービスの場所を表します。</span><span class="sxs-lookup"><span data-stu-id="6b2f6-104">Specifies the location of the cursor service.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b2f6-105">定数</span><span class="sxs-lookup"><span data-stu-id="6b2f6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6b2f6-106">値</span><span class="sxs-lookup"><span data-stu-id="6b2f6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6b2f6-107">説明</span><span class="sxs-lookup"><span data-stu-id="6b2f6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b2f6-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="6b2f6-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="6b2f6-109">3</span><span class="sxs-lookup"><span data-stu-id="6b2f6-109">3</span></span></p></td>
<td><p><span data-ttu-id="6b2f6-110">ローカル カーソル ライブラリによって提供されたクライアント側カーソルを使用します。</span><span class="sxs-lookup"><span data-stu-id="6b2f6-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="6b2f6-111">ローカル カーソル サービス多くの場合と、ドライバーによって提供されるカーソルよりも多くの機能に対して有効になる機能の利点を提供することがありますこの設定を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="6b2f6-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="6b2f6-112">下位互換性のための類義語<strong>adUseClientBatch</strong>もサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6b2f6-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2f6-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="6b2f6-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="6b2f6-114">1</span><span class="sxs-lookup"><span data-stu-id="6b2f6-114">1</span></span></p></td>
<td><p><span data-ttu-id="6b2f6-p102">カーソル サービスを使用しません。(この定数は現在使用されておらず、以前のバージョンとの互換性を保つために装備されています。)</span><span class="sxs-lookup"><span data-stu-id="6b2f6-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2f6-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="6b2f6-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6b2f6-118">2</span><span class="sxs-lookup"><span data-stu-id="6b2f6-118">2</span></span></p></td>
<td><p><span data-ttu-id="6b2f6-p103">既定値。データ プロバイダー カーソルまたはドライバーによって提供されるカーソルを使用します。これらのカーソルは、多くの場合柔軟性が高く、他のユーザーが行うデータ ソースへの変更を検出できます。ただし、<a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> にはサーバー側カーソルではシミュレートできない機能 (独立した <a href="recordset-object-ado.md">Recordset</a> オブジェクトなど) があり、そのような機能はこの設定では利用できません。</span><span class="sxs-lookup"><span data-stu-id="6b2f6-p103">Default. Uses data-provider or driver-supplied cursors. These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source. However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6b2f6-123">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="6b2f6-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="6b2f6-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6b2f6-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b2f6-125">定数</span><span class="sxs-lookup"><span data-stu-id="6b2f6-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b2f6-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="6b2f6-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2f6-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="6b2f6-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2f6-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="6b2f6-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

