---
title: ConnectOptionEnum (Access デスクトップデータベースリファレンス)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295682"
---
# <a name="connectoptionenum"></a><span data-ttu-id="2db4c-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="2db4c-102">ConnectOptionEnum</span></span>

<span data-ttu-id="2db4c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="2db4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2db4c-104">[Connection](connection-object-ado.md) オブジェクトの [Open](open-method-ado-connection.md) メソッドから制御が戻るのが、接続確立の後 (同期) か前 (非同期) かを表します。</span><span class="sxs-lookup"><span data-stu-id="2db4c-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2db4c-105">定数</span><span class="sxs-lookup"><span data-stu-id="2db4c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2db4c-106">値</span><span class="sxs-lookup"><span data-stu-id="2db4c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2db4c-107">説明</span><span class="sxs-lookup"><span data-stu-id="2db4c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2db4c-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="2db4c-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="2db4c-109">16</span><span class="sxs-lookup"><span data-stu-id="2db4c-109">16</span></span></p></td>
<td><p><span data-ttu-id="2db4c-p101">接続を非同期で開きます。接続可能かをどうかを判別するために、<a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> イベントが使用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="2db4c-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2db4c-112"><strong>adの指定</strong></span><span class="sxs-lookup"><span data-stu-id="2db4c-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="2db4c-113">-1</span><span class="sxs-lookup"><span data-stu-id="2db4c-113">-1</span></span></p></td>
<td><p><span data-ttu-id="2db4c-p102">既定値。接続を同期で開きます。</span><span class="sxs-lookup"><span data-stu-id="2db4c-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2db4c-116">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="2db4c-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="2db4c-117">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2db4c-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2db4c-118">定数</span><span class="sxs-lookup"><span data-stu-id="2db4c-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2db4c-119">ConnectOption 接続</span><span class="sxs-lookup"><span data-stu-id="2db4c-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2db4c-120">指定された ConnectOption AdoEnums</span><span class="sxs-lookup"><span data-stu-id="2db4c-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

