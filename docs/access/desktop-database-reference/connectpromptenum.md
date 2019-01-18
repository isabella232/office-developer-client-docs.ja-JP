---
title: ConnectPromptEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701110"
---
# <a name="connectpromptenum"></a><span data-ttu-id="73c65-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="73c65-102">ConnectPromptEnum</span></span>

<span data-ttu-id="73c65-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="73c65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73c65-104">データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="73c65-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73c65-105">定数</span><span class="sxs-lookup"><span data-stu-id="73c65-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="73c65-106">値</span><span class="sxs-lookup"><span data-stu-id="73c65-106">Value</span></span></p></th>
<th><p><span data-ttu-id="73c65-107">説明</span><span class="sxs-lookup"><span data-stu-id="73c65-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73c65-108"><strong>される</strong></span><span class="sxs-lookup"><span data-stu-id="73c65-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="73c65-109">1</span><span class="sxs-lookup"><span data-stu-id="73c65-109">1</span></span></p></td>
<td><p><span data-ttu-id="73c65-110">常に要求します。</span><span class="sxs-lookup"><span data-stu-id="73c65-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73c65-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="73c65-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="73c65-112">2</span><span class="sxs-lookup"><span data-stu-id="73c65-112">2</span></span></p></td>
<td><p><span data-ttu-id="73c65-113">さらに情報が必要な場合に要求します。</span><span class="sxs-lookup"><span data-stu-id="73c65-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73c65-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="73c65-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="73c65-115">3</span><span class="sxs-lookup"><span data-stu-id="73c65-115">3</span></span></p></td>
<td><p><span data-ttu-id="73c65-116">さらに情報が必要だが、任意のパラメーターが禁止されている場合に要求します。</span><span class="sxs-lookup"><span data-stu-id="73c65-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73c65-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="73c65-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="73c65-118">4</span><span class="sxs-lookup"><span data-stu-id="73c65-118">4</span></span></p></td>
<td><p><span data-ttu-id="73c65-119">要求しません。</span><span class="sxs-lookup"><span data-stu-id="73c65-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="73c65-120">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="73c65-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="73c65-121">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="73c65-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73c65-122">定数</span><span class="sxs-lookup"><span data-stu-id="73c65-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73c65-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="73c65-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73c65-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="73c65-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73c65-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="73c65-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73c65-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="73c65-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

