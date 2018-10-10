---
title: ConnectOptionEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e2e8439099732cd3e1e9aa7531f5ae3be25d7ebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476548"
---
# <a name="connectoptionenum"></a><span data-ttu-id="1d593-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="1d593-102">ConnectOptionEnum</span></span>


<span data-ttu-id="1d593-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d593-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1d593-104">[Connection](open-method-ado-connection.md) オブジェクトの [Open](connection-object-ado.md) メソッドから制御が戻るのが、接続確立の後 (同期) か前 (非同期) かを表します。</span><span class="sxs-lookup"><span data-stu-id="1d593-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d593-105">定数</span><span class="sxs-lookup"><span data-stu-id="1d593-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1d593-106">値</span><span class="sxs-lookup"><span data-stu-id="1d593-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1d593-107">説明</span><span class="sxs-lookup"><span data-stu-id="1d593-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d593-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="1d593-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="1d593-109">16</span><span class="sxs-lookup"><span data-stu-id="1d593-109">16</span></span></p></td>
<td><p><span data-ttu-id="1d593-p101">接続を非同期で開きます。接続可能かをどうかを判別するために、<a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> イベントが使用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="1d593-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d593-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="1d593-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="1d593-113">-1</span><span class="sxs-lookup"><span data-stu-id="1d593-113">-1</span></span></p></td>
<td><p><span data-ttu-id="1d593-p102">既定値。接続を同期で開きます。</span><span class="sxs-lookup"><span data-stu-id="1d593-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1d593-116">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="1d593-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="1d593-117">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1d593-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d593-118">定数</span><span class="sxs-lookup"><span data-stu-id="1d593-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d593-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="1d593-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d593-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="1d593-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

