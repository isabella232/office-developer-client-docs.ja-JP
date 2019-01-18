---
title: StreamWriteEnum (デスクトップ データベース参照のアクセス)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87144e5409fb54cf0cb8f59ad4d593ab05d694a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706171"
---
# <a name="streamwriteenum"></a><span data-ttu-id="946f2-102">StreamWriteEnum</span><span class="sxs-lookup"><span data-stu-id="946f2-102">StreamWriteEnum</span></span>

<span data-ttu-id="946f2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="946f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="946f2-104">[Stream](stream-object-ado.md) オブジェクトに書き込む文字列に、行区切り記号を追加するかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="946f2-104">Specifies whether a line separator is appended to the string written to a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="946f2-105">定数</span><span class="sxs-lookup"><span data-stu-id="946f2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="946f2-106">値</span><span class="sxs-lookup"><span data-stu-id="946f2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="946f2-107">説明</span><span class="sxs-lookup"><span data-stu-id="946f2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="946f2-108"><strong>adWriteChar</strong></span><span class="sxs-lookup"><span data-stu-id="946f2-108"><strong>adWriteChar</strong></span></span></p></td>
<td><p><span data-ttu-id="946f2-109">0</span><span class="sxs-lookup"><span data-stu-id="946f2-109">0</span></span></p></td>
<td><p><span data-ttu-id="946f2-p101">既定値。<strong>Stream</strong> オブジェクトに、<em>Data</em> パラメーターで指定したテキスト文字列を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="946f2-p101">Default. Writes the specified text string (specified by the <em>Data</em> parameter) to the <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946f2-112"><strong>adWriteLine</strong></span><span class="sxs-lookup"><span data-stu-id="946f2-112"><strong>adWriteLine</strong></span></span></p></td>
<td><p><span data-ttu-id="946f2-113">1</span><span class="sxs-lookup"><span data-stu-id="946f2-113">1</span></span></p></td>
<td><p><span data-ttu-id="946f2-p102"><strong>Stream</strong> オブジェクトに、テキスト文字列と行区切り記号を書き込みます。<a href="lineseparator-property-ado.md">LineSeparator</a> プロパティが定義されていない場合は、実行時エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="946f2-p102">Writes a text string and a line separator character to a <strong>Stream</strong> object. If the <a href="lineseparator-property-ado.md">LineSeparator</a> property is not defined, then this returns a run-time error.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="946f2-116">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="946f2-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="946f2-117">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="946f2-117">These constants do not have ADO/WFC equivalents.</span></span>

