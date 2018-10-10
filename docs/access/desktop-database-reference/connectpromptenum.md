---
title: ConnectPromptEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e405b1eb3a1326d56a32c432fb212de417cf3469
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479353"
---
# <a name="connectpromptenum"></a><span data-ttu-id="db5e7-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="db5e7-102">ConnectPromptEnum</span></span>


<span data-ttu-id="db5e7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="db5e7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="db5e7-104">データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="db5e7-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db5e7-105">定数</span><span class="sxs-lookup"><span data-stu-id="db5e7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="db5e7-106">値</span><span class="sxs-lookup"><span data-stu-id="db5e7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="db5e7-107">説明</span><span class="sxs-lookup"><span data-stu-id="db5e7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db5e7-108"><strong>される</strong></span><span class="sxs-lookup"><span data-stu-id="db5e7-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="db5e7-109">1</span><span class="sxs-lookup"><span data-stu-id="db5e7-109">1</span></span></p></td>
<td><p><span data-ttu-id="db5e7-110">常に要求します。</span><span class="sxs-lookup"><span data-stu-id="db5e7-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db5e7-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="db5e7-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="db5e7-112">2</span><span class="sxs-lookup"><span data-stu-id="db5e7-112">2</span></span></p></td>
<td><p><span data-ttu-id="db5e7-113">さらに情報が必要な場合に要求します。</span><span class="sxs-lookup"><span data-stu-id="db5e7-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db5e7-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="db5e7-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="db5e7-115">3</span><span class="sxs-lookup"><span data-stu-id="db5e7-115">3</span></span></p></td>
<td><p><span data-ttu-id="db5e7-116">さらに情報が必要だが、任意のパラメーターが禁止されている場合に要求します。</span><span class="sxs-lookup"><span data-stu-id="db5e7-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db5e7-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="db5e7-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="db5e7-118">4</span><span class="sxs-lookup"><span data-stu-id="db5e7-118">4</span></span></p></td>
<td><p><span data-ttu-id="db5e7-119">要求しません。</span><span class="sxs-lookup"><span data-stu-id="db5e7-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db5e7-120">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="db5e7-120">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="db5e7-121">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="db5e7-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db5e7-122">定数</span><span class="sxs-lookup"><span data-stu-id="db5e7-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db5e7-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="db5e7-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db5e7-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="db5e7-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db5e7-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="db5e7-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db5e7-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="db5e7-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

