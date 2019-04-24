---
title: ConnectPromptEnum (Access デスクトップデータベースリファレンス)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295668"
---
# <a name="connectpromptenum"></a><span data-ttu-id="6f80c-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="6f80c-102">ConnectPromptEnum</span></span>

<span data-ttu-id="6f80c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f80c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f80c-104">データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="6f80c-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f80c-105">定数</span><span class="sxs-lookup"><span data-stu-id="6f80c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6f80c-106">値</span><span class="sxs-lookup"><span data-stu-id="6f80c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6f80c-107">説明</span><span class="sxs-lookup"><span data-stu-id="6f80c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f80c-108"><strong>adpromptalways</strong></span><span class="sxs-lookup"><span data-stu-id="6f80c-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="6f80c-109">1-d</span><span class="sxs-lookup"><span data-stu-id="6f80c-109">1</span></span></p></td>
<td><p><span data-ttu-id="6f80c-110">常に要求します。</span><span class="sxs-lookup"><span data-stu-id="6f80c-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f80c-111"><strong>adpromptcomplete</strong></span><span class="sxs-lookup"><span data-stu-id="6f80c-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="6f80c-112">pbm-2</span><span class="sxs-lookup"><span data-stu-id="6f80c-112">2</span></span></p></td>
<td><p><span data-ttu-id="6f80c-113">さらに情報が必要な場合に要求します。</span><span class="sxs-lookup"><span data-stu-id="6f80c-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f80c-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="6f80c-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="6f80c-115">1/3</span><span class="sxs-lookup"><span data-stu-id="6f80c-115">3</span></span></p></td>
<td><p><span data-ttu-id="6f80c-116">さらに情報が必要だが、任意のパラメーターが禁止されている場合に要求します。</span><span class="sxs-lookup"><span data-stu-id="6f80c-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f80c-117"><strong>adpromptnever</strong></span><span class="sxs-lookup"><span data-stu-id="6f80c-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="6f80c-118">2/4</span><span class="sxs-lookup"><span data-stu-id="6f80c-118">4</span></span></p></td>
<td><p><span data-ttu-id="6f80c-119">要求しません。</span><span class="sxs-lookup"><span data-stu-id="6f80c-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6f80c-120">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="6f80c-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="6f80c-121">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6f80c-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f80c-122">定数</span><span class="sxs-lookup"><span data-stu-id="6f80c-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f80c-123">AdoEnums。常に</span><span class="sxs-lookup"><span data-stu-id="6f80c-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f80c-124">AdoEnums の完全なメッセージ</span><span class="sxs-lookup"><span data-stu-id="6f80c-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f80c-125">AdoEnums COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="6f80c-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f80c-126">AdoEnums のメッセージを表示しない</span><span class="sxs-lookup"><span data-stu-id="6f80c-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

