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
ms.openlocfilehash: 3258e19c7e167927cf341089ed99e5525ebb0f8d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868134"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="ef1c3-102">Field.CollatingOrder プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="ef1c3-102">Field.CollatingOrder Property (DAO)</span></span>


<span data-ttu-id="ef1c3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef1c3-p101">文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1c3-106">構文</span><span class="sxs-lookup"><span data-stu-id="ef1c3-106">Syntax</span></span>

<span data-ttu-id="ef1c3-107">*式*です。照合順序</span><span class="sxs-lookup"><span data-stu-id="ef1c3-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="ef1c3-108">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1c3-109">注釈</span><span class="sxs-lookup"><span data-stu-id="ef1c3-109">Remarks</span></span>

<span data-ttu-id="ef1c3-110">戻り値は、長整数型 ( **Long**) の値、または次のいずれかの値の定数です。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef1c3-111">定数</span><span class="sxs-lookup"><span data-stu-id="ef1c3-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="ef1c3-112">並べ替え順</span><span class="sxs-lookup"><span data-stu-id="ef1c3-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-114">標準 (英語、フランス語、ドイツ語、ポルトガル語、イタリア語、および現代スペイン語)</span><span class="sxs-lookup"><span data-stu-id="ef1c3-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-116">アラビア語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-118">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-120">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-122">ロシア語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-124">チェコ語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-126">オランダ語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-128">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-130">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-132">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-134">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-136">日本語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-138">韓国語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-140">ニュートラル</span><span class="sxs-lookup"><span data-stu-id="ef1c3-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-142">ノルウェー語またはデンマーク語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-144">Paradox インターナショナル版</span><span class="sxs-lookup"><span data-stu-id="ef1c3-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-146">Paradox ノルウェー語版または Paradox デンマーク語版</span><span class="sxs-lookup"><span data-stu-id="ef1c3-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-148">Paradox スウェーデン語版または Paradox フィンランド語版</span><span class="sxs-lookup"><span data-stu-id="ef1c3-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-150">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-152">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-154">スペイン語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-156">スウェーデン語またはフィンランド語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-158">タイ語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-160">トルコ語</span><span class="sxs-lookup"><span data-stu-id="ef1c3-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="ef1c3-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="ef1c3-162">未定義または不明</span><span class="sxs-lookup"><span data-stu-id="ef1c3-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef1c3-163">**CollatingOrder** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef1c3-164">Fields コレクションの所属先</span><span class="sxs-lookup"><span data-stu-id="ef1c3-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="ef1c3-165">CollatingOrder プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="ef1c3-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-166"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ef1c3-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ef1c3-167">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-168"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ef1c3-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ef1c3-169">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ef1c3-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-170"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ef1c3-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ef1c3-171">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ef1c3-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef1c3-172"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ef1c3-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ef1c3-173">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef1c3-174"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ef1c3-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ef1c3-175">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ef1c3-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef1c3-176">**照合順序**プロパティの設定は、データベースの最適化を最後に、 **CompactDatabase**メソッド、データベースの作成時に、 **CreateDatabase**メソッドの locale 引数に対応します。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="ef1c3-p102">**Index** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **CollatingOrder** プロパティと **Attributes** プロパティの設定値は、インデックス内の並べ替え順の順番と方向によって決まります。ただし、それぞれのインデックスの照合順序は設定できないため、テーブル全体に対して順序を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef1c3-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

