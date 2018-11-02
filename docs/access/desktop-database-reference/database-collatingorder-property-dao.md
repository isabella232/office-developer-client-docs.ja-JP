---
title: Database.CollatingOrder プロパティ (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e3219d9691fa61fd1ae234cecd273ec9720ed9e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923869"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="8c82d-102">Database.CollatingOrder プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="8c82d-102">Database.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="8c82d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8c82d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c82d-p101">文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8c82d-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c82d-106">構文</span><span class="sxs-lookup"><span data-stu-id="8c82d-106">Syntax</span></span>

<span data-ttu-id="8c82d-107">*式*です。照合順序</span><span class="sxs-lookup"><span data-stu-id="8c82d-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="8c82d-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="8c82d-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c82d-109">注釈</span><span class="sxs-lookup"><span data-stu-id="8c82d-109">Remarks</span></span>

<span data-ttu-id="8c82d-110">戻り値は、長整数型 ( **Long**) の値、または次のいずれかの値の定数です。</span><span class="sxs-lookup"><span data-stu-id="8c82d-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c82d-111">定数</span><span class="sxs-lookup"><span data-stu-id="8c82d-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="8c82d-112">並べ替え順</span><span class="sxs-lookup"><span data-stu-id="8c82d-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-114">標準 (英語、フランス語、ドイツ語、ポルトガル語、イタリア語、および現代スペイン語)</span><span class="sxs-lookup"><span data-stu-id="8c82d-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-116">アラビア語</span><span class="sxs-lookup"><span data-stu-id="8c82d-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-118">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="8c82d-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-120">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="8c82d-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-122">ロシア語</span><span class="sxs-lookup"><span data-stu-id="8c82d-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-124">チェコ語</span><span class="sxs-lookup"><span data-stu-id="8c82d-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-126">オランダ語</span><span class="sxs-lookup"><span data-stu-id="8c82d-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-128">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="8c82d-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-130">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="8c82d-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-132">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="8c82d-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-134">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="8c82d-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-136">日本語</span><span class="sxs-lookup"><span data-stu-id="8c82d-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-138">韓国語</span><span class="sxs-lookup"><span data-stu-id="8c82d-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-140">ニュートラル</span><span class="sxs-lookup"><span data-stu-id="8c82d-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-142">ノルウェー語またはデンマーク語</span><span class="sxs-lookup"><span data-stu-id="8c82d-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-144">Paradox インターナショナル版</span><span class="sxs-lookup"><span data-stu-id="8c82d-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-146">Paradox ノルウェー語版または Paradox デンマーク語版</span><span class="sxs-lookup"><span data-stu-id="8c82d-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-148">Paradox スウェーデン語版または Paradox フィンランド語版</span><span class="sxs-lookup"><span data-stu-id="8c82d-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-150">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="8c82d-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-152">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="8c82d-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-154">スペイン語</span><span class="sxs-lookup"><span data-stu-id="8c82d-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-156">スウェーデン語またはフィンランド語</span><span class="sxs-lookup"><span data-stu-id="8c82d-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-158">タイ語</span><span class="sxs-lookup"><span data-stu-id="8c82d-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c82d-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-160">トルコ語</span><span class="sxs-lookup"><span data-stu-id="8c82d-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c82d-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="8c82d-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="8c82d-162">未定義または不明</span><span class="sxs-lookup"><span data-stu-id="8c82d-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8c82d-163">**照合順序**プロパティの設定は、データベースの最適化を最後に、 **CompactDatabase**メソッド、データベースの作成時に、 **CreateDatabase**メソッドの locale 引数に対応します。</span><span class="sxs-lookup"><span data-stu-id="8c82d-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="8c82d-p102">データベースまたはフィールドの文字列比較方法を調べるには、 **Database** オブジェクトまたは **Field** オブジェクトの **CollatingOrder** プロパティの設定値を確認します。 **Field** オブジェクトの設定値を、それを含む **Database** オブジェクトの設定値と別に設定する場合は、追加されていない新しい **Field** オブジェクトの **CollatingOrder** プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8c82d-p102">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field. You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

