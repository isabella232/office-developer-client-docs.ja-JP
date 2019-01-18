---
title: SaveOptionsEnum (デスクトップ データベース参照のアクセス)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705996"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="e6918-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="e6918-102">SaveOptionsEnum</span></span>

<span data-ttu-id="e6918-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e6918-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6918-p101">[Stream](stream-object-ado.md) オブジェクトからファイルに保存するときに、ファイルを作成するか、上書きするかを表します。これらの値は AND 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="e6918-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6918-106">定数</span><span class="sxs-lookup"><span data-stu-id="e6918-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="e6918-107">値</span><span class="sxs-lookup"><span data-stu-id="e6918-107">Value</span></span></p></th>
<th><p><span data-ttu-id="e6918-108">説明</span><span class="sxs-lookup"><span data-stu-id="e6918-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6918-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="e6918-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="e6918-110">1</span><span class="sxs-lookup"><span data-stu-id="e6918-110">1</span></span></p></td>
<td><p><span data-ttu-id="e6918-p102">既定値。<em>FileName</em> パラメーターで指定したファイルがない場合は新しいファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e6918-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6918-113"><strong>adSaveCreateOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="e6918-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="e6918-114">2</span><span class="sxs-lookup"><span data-stu-id="e6918-114">2</span></span></p></td>
<td><p><span data-ttu-id="e6918-115"><em>Filename</em> パラメーターで指定したファイルがある場合は、現在開かれている <strong>Stream</strong> オブジェクトのデータでファイルが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="e6918-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e6918-116">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="e6918-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="e6918-117">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="e6918-117">These constants do not have ADO/WFC equivalents.</span></span>

