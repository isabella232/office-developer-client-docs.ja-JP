---
title: Field.CollatingOrder プロパティ (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: a2607ace-a660-899b-eae8-4612ce2f87f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820980(v=office.15)
ms:contentKeyID: 48546758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052897
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d64620ccf1c0d011c060ac829223041f49bde9d1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925290"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="0869c-102">Field.CollatingOrder プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="0869c-102">Field.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="0869c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0869c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0869c-p101">文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0869c-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0869c-106">構文</span><span class="sxs-lookup"><span data-stu-id="0869c-106">Syntax</span></span>

<span data-ttu-id="0869c-107">*式*です。照合順序</span><span class="sxs-lookup"><span data-stu-id="0869c-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="0869c-108">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="0869c-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0869c-109">注釈</span><span class="sxs-lookup"><span data-stu-id="0869c-109">Remarks</span></span>

<span data-ttu-id="0869c-110">戻り値は、長整数型 ( **Long**) の値、または次のいずれかの値の定数です。</span><span class="sxs-lookup"><span data-stu-id="0869c-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0869c-111">定数</span><span class="sxs-lookup"><span data-stu-id="0869c-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="0869c-112">並べ替え順</span><span class="sxs-lookup"><span data-stu-id="0869c-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0869c-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-114">標準 (英語、フランス語、ドイツ語、ポルトガル語、イタリア語、および現代スペイン語)</span><span class="sxs-lookup"><span data-stu-id="0869c-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-116">アラビア語</span><span class="sxs-lookup"><span data-stu-id="0869c-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-118">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="0869c-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-120">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="0869c-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-122">ロシア語</span><span class="sxs-lookup"><span data-stu-id="0869c-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-124">チェコ語</span><span class="sxs-lookup"><span data-stu-id="0869c-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-126">オランダ語</span><span class="sxs-lookup"><span data-stu-id="0869c-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-128">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="0869c-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-130">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="0869c-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-132">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="0869c-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-134">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="0869c-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-136">日本語</span><span class="sxs-lookup"><span data-stu-id="0869c-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-138">韓国語</span><span class="sxs-lookup"><span data-stu-id="0869c-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-140">ニュートラル</span><span class="sxs-lookup"><span data-stu-id="0869c-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-142">ノルウェー語またはデンマーク語</span><span class="sxs-lookup"><span data-stu-id="0869c-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-144">Paradox インターナショナル版</span><span class="sxs-lookup"><span data-stu-id="0869c-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-146">Paradox ノルウェー語版または Paradox デンマーク語版</span><span class="sxs-lookup"><span data-stu-id="0869c-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-148">Paradox スウェーデン語版または Paradox フィンランド語版</span><span class="sxs-lookup"><span data-stu-id="0869c-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-150">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="0869c-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-152">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="0869c-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-154">スペイン語</span><span class="sxs-lookup"><span data-stu-id="0869c-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-156">スウェーデン語またはフィンランド語</span><span class="sxs-lookup"><span data-stu-id="0869c-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-158">タイ語</span><span class="sxs-lookup"><span data-stu-id="0869c-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-160">トルコ語</span><span class="sxs-lookup"><span data-stu-id="0869c-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="0869c-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="0869c-162">未定義または不明</span><span class="sxs-lookup"><span data-stu-id="0869c-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0869c-163">**CollatingOrder** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="0869c-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0869c-164">Fields コレクションの所属先</span><span class="sxs-lookup"><span data-stu-id="0869c-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="0869c-165">CollatingOrder プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="0869c-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0869c-166"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0869c-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0869c-167">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="0869c-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-168"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0869c-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0869c-169">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="0869c-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-170"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0869c-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0869c-171">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="0869c-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0869c-172"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0869c-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0869c-173">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="0869c-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0869c-174"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0869c-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0869c-175">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="0869c-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0869c-176">**照合順序**プロパティの設定は、データベースの最適化を最後に、 **CompactDatabase**メソッド、データベースの作成時に、 **CreateDatabase**メソッドの locale 引数に対応します。</span><span class="sxs-lookup"><span data-stu-id="0869c-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="0869c-p102">**Index** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **CollatingOrder** プロパティと **Attributes** プロパティの設定値は、インデックス内の並べ替え順の順番と方向によって決まります。ただし、それぞれのインデックスの照合順序は設定できないため、テーブル全体に対して順序を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0869c-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

