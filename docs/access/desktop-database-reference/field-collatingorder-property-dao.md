---
title: フィールドの並べ替え順序プロパティ (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 3d016d779472ec9809d3ac5c77158c2c1d994f3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293127"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="d89d7-102">フィールドの並べ替え順序プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d89d7-102">Field.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="d89d7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d89d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d89d7-p101">文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d89d7-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89d7-106">構文</span><span class="sxs-lookup"><span data-stu-id="d89d7-106">Syntax</span></span>

<span data-ttu-id="d89d7-107">*式*。CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="d89d7-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="d89d7-108">\*式\***Field**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d89d7-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d89d7-109">注釈</span><span class="sxs-lookup"><span data-stu-id="d89d7-109">Remarks</span></span>

<span data-ttu-id="d89d7-110">戻り値は、長整数型 ( **Long**) の値、または次のいずれかの値の定数です。</span><span class="sxs-lookup"><span data-stu-id="d89d7-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d89d7-111">定数</span><span class="sxs-lookup"><span data-stu-id="d89d7-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="d89d7-112">並べ替え順</span><span class="sxs-lookup"><span data-stu-id="d89d7-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-113"><strong>dbsortgeneral</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-114">欧米標準 (英語、フランス語、ドイツ語、ポルトガル語、イタリア語、および現代スペイン語)</span><span class="sxs-lookup"><span data-stu-id="d89d7-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-115"><strong>dbsortarabic</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-116">アラビア語</span><span class="sxs-lookup"><span data-stu-id="d89d7-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-117"><strong>dbsortchinesesimplified</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-118">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="d89d7-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-119"><strong>dbsortchinesetraditional</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-120">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="d89d7-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-121"><strong>dbsortcyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-122">ロシア語</span><span class="sxs-lookup"><span data-stu-id="d89d7-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-123"><strong>dbsortczech</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-124">チェコ語</span><span class="sxs-lookup"><span data-stu-id="d89d7-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-125"><strong>dbsortdutch 語</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-126">オランダ語</span><span class="sxs-lookup"><span data-stu-id="d89d7-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-127"><strong>dbsortgreek 語</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-128">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="d89d7-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-130">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="d89d7-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-132">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="d89d7-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-133"><strong>dbsorticelandic</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-134">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="d89d7-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-135"><strong>dbsortjapanese</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-136">日本語</span><span class="sxs-lookup"><span data-stu-id="d89d7-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-137"><strong>dbsortkorean 語</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-138">韓国語</span><span class="sxs-lookup"><span data-stu-id="d89d7-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-139"><strong>dbsortneutral</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-140">中間</span><span class="sxs-lookup"><span data-stu-id="d89d7-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-141"><strong>dbsortnorwdan</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-142">ノルウェー語またはデンマーク語</span><span class="sxs-lookup"><span data-stu-id="d89d7-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-143"><strong>dbsortpdxintl</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-144">Paradox 国際</span><span class="sxs-lookup"><span data-stu-id="d89d7-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-145"><strong>dbsortpdxnor は</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-146">Paradox ノルウェー語またはデンマーク語</span><span class="sxs-lookup"><span data-stu-id="d89d7-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-147"><strong>dbsortpdxswe</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-148">Paradox スウェーデン語またはフィンランド語</span><span class="sxs-lookup"><span data-stu-id="d89d7-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-149"><strong>dbsortpolish</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-150">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="d89d7-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-151"><strong>dbsortsloベンダーの場合</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-152">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="d89d7-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-153"><strong>dbsortspanish 語</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-154">スペイン語</span><span class="sxs-lookup"><span data-stu-id="d89d7-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-155"><strong>dbsortswedfin</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-156">スウェーデン語またはフィンランド語</span><span class="sxs-lookup"><span data-stu-id="d89d7-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-157"><strong>dbsortthai 語</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-158">タイ語</span><span class="sxs-lookup"><span data-stu-id="d89d7-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-159"><strong>dbsortturkish</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-160">トルコ語</span><span class="sxs-lookup"><span data-stu-id="d89d7-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-161"><strong>dbsortundefined</strong></span><span class="sxs-lookup"><span data-stu-id="d89d7-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="d89d7-162">未定義または不明</span><span class="sxs-lookup"><span data-stu-id="d89d7-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d89d7-163">**CollatingOrder** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="d89d7-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d89d7-164">Fields コレクションの所属先</span><span class="sxs-lookup"><span data-stu-id="d89d7-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="d89d7-165">CollatingOrder の使用</span><span class="sxs-lookup"><span data-stu-id="d89d7-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-166"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d89d7-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d89d7-167">サポートされない</span><span class="sxs-lookup"><span data-stu-id="d89d7-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-168"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d89d7-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d89d7-169">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="d89d7-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-170"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d89d7-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d89d7-171">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="d89d7-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d89d7-172"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d89d7-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d89d7-173">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="d89d7-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d89d7-174"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d89d7-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d89d7-175">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="d89d7-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d89d7-176">" \*\*\*\* CreateDatabase/プロパティの設定" プロパティの設定値は、データベースが作成されたときの\*\*\*\* メソッドまたはデータベースが最後に最適化されたときの**CompactDatabase**メソッドの locale 引数に対応しています。</span><span class="sxs-lookup"><span data-stu-id="d89d7-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="d89d7-p102">**Index** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **CollatingOrder** プロパティと **Attributes** プロパティの設定値は、インデックス内の並べ替え順の順番と方向によって決まります。ただし、それぞれのインデックスの照合順序は設定できないため、テーブル全体に対して順序を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d89d7-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

