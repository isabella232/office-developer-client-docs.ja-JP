---
title: ConnectPromptEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 387e9a853a306b2375034359ce26db50685afcc4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887909"
---
# <a name="connectpromptenum"></a><span data-ttu-id="7f608-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="7f608-102">ConnectPromptEnum</span></span>

<span data-ttu-id="7f608-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7f608-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f608-104">データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="7f608-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f608-105">定数</span><span class="sxs-lookup"><span data-stu-id="7f608-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7f608-106">値</span><span class="sxs-lookup"><span data-stu-id="7f608-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7f608-107">説明</span><span class="sxs-lookup"><span data-stu-id="7f608-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f608-108"><strong>される</strong></span><span class="sxs-lookup"><span data-stu-id="7f608-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="7f608-109">1</span><span class="sxs-lookup"><span data-stu-id="7f608-109">1</span></span></p></td>
<td><p><span data-ttu-id="7f608-110">常に要求します。</span><span class="sxs-lookup"><span data-stu-id="7f608-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f608-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="7f608-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="7f608-112">2</span><span class="sxs-lookup"><span data-stu-id="7f608-112">2</span></span></p></td>
<td><p><span data-ttu-id="7f608-113">さらに情報が必要な場合に要求します。</span><span class="sxs-lookup"><span data-stu-id="7f608-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f608-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="7f608-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="7f608-115">3</span><span class="sxs-lookup"><span data-stu-id="7f608-115">3</span></span></p></td>
<td><p><span data-ttu-id="7f608-116">さらに情報が必要だが、任意のパラメーターが禁止されている場合に要求します。</span><span class="sxs-lookup"><span data-stu-id="7f608-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f608-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="7f608-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="7f608-118">4</span><span class="sxs-lookup"><span data-stu-id="7f608-118">4</span></span></p></td>
<td><p><span data-ttu-id="7f608-119">要求しません。</span><span class="sxs-lookup"><span data-stu-id="7f608-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="7f608-120">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="7f608-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="7f608-121">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7f608-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f608-122">定数</span><span class="sxs-lookup"><span data-stu-id="7f608-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f608-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="7f608-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f608-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="7f608-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f608-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="7f608-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f608-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="7f608-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

