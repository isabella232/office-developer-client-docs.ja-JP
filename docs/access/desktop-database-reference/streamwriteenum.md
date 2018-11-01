---
title: StreamWriteEnum (デスクトップ データベース参照のアクセス)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7ba09a0b741483713dfa019062309344eecdb139
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891122"
---
# <a name="streamwriteenum"></a><span data-ttu-id="04f54-102">StreamWriteEnum</span><span class="sxs-lookup"><span data-stu-id="04f54-102">StreamWriteEnum</span></span>

<span data-ttu-id="04f54-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="04f54-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04f54-104">[Stream](stream-object-ado.md) オブジェクトに書き込む文字列に、行区切り記号を追加するかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="04f54-104">Specifies whether a line separator is appended to the string written to a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04f54-105">定数</span><span class="sxs-lookup"><span data-stu-id="04f54-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="04f54-106">値</span><span class="sxs-lookup"><span data-stu-id="04f54-106">Value</span></span></p></th>
<th><p><span data-ttu-id="04f54-107">説明</span><span class="sxs-lookup"><span data-stu-id="04f54-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04f54-108"><strong>adWriteChar</strong></span><span class="sxs-lookup"><span data-stu-id="04f54-108"><strong>adWriteChar</strong></span></span></p></td>
<td><p><span data-ttu-id="04f54-109">0</span><span class="sxs-lookup"><span data-stu-id="04f54-109">0</span></span></p></td>
<td><p><span data-ttu-id="04f54-p101">既定値。<strong>Stream</strong> オブジェクトに、<em>Data</em> パラメーターで指定したテキスト文字列を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="04f54-p101">Default. Writes the specified text string (specified by the <em>Data</em> parameter) to the <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04f54-112"><strong>adWriteLine</strong></span><span class="sxs-lookup"><span data-stu-id="04f54-112"><strong>adWriteLine</strong></span></span></p></td>
<td><p><span data-ttu-id="04f54-113">1</span><span class="sxs-lookup"><span data-stu-id="04f54-113">1</span></span></p></td>
<td><p><span data-ttu-id="04f54-p102"><strong>Stream</strong> オブジェクトに、テキスト文字列と行区切り記号を書き込みます。<a href="lineseparator-property-ado.md">LineSeparator</a> プロパティが定義されていない場合は、実行時エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="04f54-p102">Writes a text string and a line separator character to a <strong>Stream</strong> object. If the <a href="lineseparator-property-ado.md">LineSeparator</a> property is not defined, then this returns a run-time error.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="04f54-116">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="04f54-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="04f54-117">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="04f54-117">These constants do not have ADO/WFC equivalents.</span></span>

