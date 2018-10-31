---
title: ConnectOptionEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 76203f1406a3152488f6404b1a9eb47e541c3351
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864187"
---
# <a name="connectoptionenum"></a><span data-ttu-id="57c58-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="57c58-102">ConnectOptionEnum</span></span>

<span data-ttu-id="57c58-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="57c58-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="57c58-104">[Connection](open-method-ado-connection.md) オブジェクトの [Open](connection-object-ado.md) メソッドから制御が戻るのが、接続確立の後 (同期) か前 (非同期) かを表します。</span><span class="sxs-lookup"><span data-stu-id="57c58-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57c58-105">定数</span><span class="sxs-lookup"><span data-stu-id="57c58-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="57c58-106">値</span><span class="sxs-lookup"><span data-stu-id="57c58-106">Value</span></span></p></th>
<th><p><span data-ttu-id="57c58-107">説明</span><span class="sxs-lookup"><span data-stu-id="57c58-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57c58-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="57c58-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="57c58-109">16</span><span class="sxs-lookup"><span data-stu-id="57c58-109">16</span></span></p></td>
<td><p><span data-ttu-id="57c58-p101">接続を非同期で開きます。接続可能かをどうかを判別するために、<a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> イベントが使用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="57c58-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57c58-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="57c58-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="57c58-113">-1</span><span class="sxs-lookup"><span data-stu-id="57c58-113">-1</span></span></p></td>
<td><p><span data-ttu-id="57c58-p102">既定値。接続を同期で開きます。</span><span class="sxs-lookup"><span data-stu-id="57c58-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="57c58-116">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="57c58-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="57c58-117">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="57c58-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57c58-118">定数</span><span class="sxs-lookup"><span data-stu-id="57c58-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57c58-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="57c58-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57c58-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="57c58-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

