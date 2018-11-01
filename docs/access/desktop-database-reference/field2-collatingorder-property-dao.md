---
title: Field2.CollatingOrder プロパティ (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 508f7f758d682dec0f1557f8a3f4dc2845e20a39
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870768"
---
# <a name="field2collatingorder-property-dao"></a><span data-ttu-id="de446-102">Field2.CollatingOrder プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="de446-102">Field2.CollatingOrder Property (DAO)</span></span>


<span data-ttu-id="de446-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="de446-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de446-p101">文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="de446-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="de446-106">構文</span><span class="sxs-lookup"><span data-stu-id="de446-106">Syntax</span></span>

<span data-ttu-id="de446-107">*式*です。照合順序</span><span class="sxs-lookup"><span data-stu-id="de446-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="de446-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="de446-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de446-109">注釈</span><span class="sxs-lookup"><span data-stu-id="de446-109">Remarks</span></span>

<span data-ttu-id="de446-110">戻り値は、長整数型 ( **Long**) の値、または次のいずれかの値の定数です。</span><span class="sxs-lookup"><span data-stu-id="de446-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de446-111">定数</span><span class="sxs-lookup"><span data-stu-id="de446-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="de446-112">並べ替え順</span><span class="sxs-lookup"><span data-stu-id="de446-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de446-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="de446-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-114">標準 (英語、フランス語、ドイツ語、ポルトガル語、イタリア語、および現代スペイン語)</span><span class="sxs-lookup"><span data-stu-id="de446-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="de446-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-116">アラビア語</span><span class="sxs-lookup"><span data-stu-id="de446-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="de446-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-118">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="de446-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="de446-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-120">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="de446-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="de446-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-122">ロシア語</span><span class="sxs-lookup"><span data-stu-id="de446-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="de446-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-124">チェコ語</span><span class="sxs-lookup"><span data-stu-id="de446-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="de446-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-126">オランダ語</span><span class="sxs-lookup"><span data-stu-id="de446-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="de446-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-128">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="de446-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="de446-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-130">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="de446-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="de446-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-132">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="de446-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="de446-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-134">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="de446-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="de446-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-136">日本語</span><span class="sxs-lookup"><span data-stu-id="de446-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="de446-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-138">韓国語</span><span class="sxs-lookup"><span data-stu-id="de446-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="de446-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-140">ニュートラル</span><span class="sxs-lookup"><span data-stu-id="de446-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="de446-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-142">ノルウェー語またはデンマーク語</span><span class="sxs-lookup"><span data-stu-id="de446-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="de446-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-144">Paradox インターナショナル版</span><span class="sxs-lookup"><span data-stu-id="de446-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="de446-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-146">Paradox ノルウェー語版または Paradox デンマーク語版</span><span class="sxs-lookup"><span data-stu-id="de446-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="de446-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-148">Paradox スウェーデン語版または Paradox フィンランド語版</span><span class="sxs-lookup"><span data-stu-id="de446-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="de446-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-150">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="de446-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="de446-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-152">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="de446-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="de446-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-154">スペイン語</span><span class="sxs-lookup"><span data-stu-id="de446-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="de446-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-156">スウェーデン語またはフィンランド語</span><span class="sxs-lookup"><span data-stu-id="de446-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="de446-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-158">タイ語</span><span class="sxs-lookup"><span data-stu-id="de446-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="de446-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-160">トルコ語</span><span class="sxs-lookup"><span data-stu-id="de446-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="de446-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="de446-162">未定義または不明</span><span class="sxs-lookup"><span data-stu-id="de446-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="de446-163">**CollatingOrder** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="de446-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de446-164">Fields コレクションの所属先</span><span class="sxs-lookup"><span data-stu-id="de446-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="de446-165">CollatingOrder プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="de446-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de446-166"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="de446-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="de446-167">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="de446-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-168"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="de446-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="de446-169">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="de446-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-170"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="de446-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="de446-171">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="de446-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de446-172"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="de446-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="de446-173">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="de446-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de446-174"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="de446-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="de446-175">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="de446-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="de446-176">**照合順序**プロパティの設定は、データベースの最適化を最後に、 **CompactDatabase**メソッド、データベースの作成時に、 **CreateDatabase**メソッドの locale 引数に対応します。</span><span class="sxs-lookup"><span data-stu-id="de446-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="de446-p102">**Index** オブジェクトの **Fields** コレクションに含まれる **Field2** オブジェクトの **CollatingOrder** プロパティと **Attributes** プロパティの設定値の組み合わせにより、インデックスの並べ替えの順序と方向が決まります。ただし、照合順序を設定できるのは、個別のインデックスに対してではなく、テーブル全体に対してのみです。</span><span class="sxs-lookup"><span data-stu-id="de446-p102">The **CollatingOrder** and **Attributes** property settings of a **Field2** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

