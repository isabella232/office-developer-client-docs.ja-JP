---
title: CursorLocationEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 63b4ae569ce76c480725853e119b4807dd121758
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882820"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="fb58d-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="fb58d-102">CursorLocationEnum</span></span>

<span data-ttu-id="fb58d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fb58d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb58d-104">カーソル サービスの場所を表します。</span><span class="sxs-lookup"><span data-stu-id="fb58d-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb58d-105">定数</span><span class="sxs-lookup"><span data-stu-id="fb58d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fb58d-106">値</span><span class="sxs-lookup"><span data-stu-id="fb58d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fb58d-107">説明</span><span class="sxs-lookup"><span data-stu-id="fb58d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb58d-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="fb58d-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="fb58d-109">3</span><span class="sxs-lookup"><span data-stu-id="fb58d-109">3</span></span></p></td>
<td><p><span data-ttu-id="fb58d-110">ローカル カーソル ライブラリによって提供されたクライアント側カーソルを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb58d-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="fb58d-111">ローカル カーソル サービス多くの場合と、ドライバーによって提供されるカーソルよりも多くの機能に対して有効になる機能の利点を提供することがありますこの設定を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="fb58d-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="fb58d-112">下位互換性のための類義語<strong>adUseClientBatch</strong>もサポートされます。</span><span class="sxs-lookup"><span data-stu-id="fb58d-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb58d-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="fb58d-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="fb58d-114">1</span><span class="sxs-lookup"><span data-stu-id="fb58d-114">1</span></span></p></td>
<td><p><span data-ttu-id="fb58d-p102">カーソル サービスを使用しません。(この定数は現在使用されておらず、以前のバージョンとの互換性を保つために装備されています。)</span><span class="sxs-lookup"><span data-stu-id="fb58d-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb58d-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="fb58d-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="fb58d-118">2</span><span class="sxs-lookup"><span data-stu-id="fb58d-118">2</span></span></p></td>
<td><p><span data-ttu-id="fb58d-119">既定値です。</span><span class="sxs-lookup"><span data-stu-id="fb58d-119">Default.</span></span> <span data-ttu-id="fb58d-120">データ プロバイダーまたはドライバーによって提供されるカーソルを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb58d-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="fb58d-121">これらのカーソルは、非常に柔軟性のある場合があり、データ ソースに加える他のユーザーの変更を検出できるようにします。</span><span class="sxs-lookup"><span data-stu-id="fb58d-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="fb58d-122">ただし、サーバー側カーソル (<a href="recordset-object-ado.md">レコード セット</a>オブジェクトを作り出す) などの<a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">OLE DB のカーソル サービスをマイクロソフト</a>の一部の機能をシミュレートすることはできませんし、これらの機能はこの設定では利用できません。</span><span class="sxs-lookup"><span data-stu-id="fb58d-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fb58d-123">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="fb58d-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="fb58d-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fb58d-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb58d-125">定数</span><span class="sxs-lookup"><span data-stu-id="fb58d-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb58d-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="fb58d-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb58d-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="fb58d-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb58d-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="fb58d-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

