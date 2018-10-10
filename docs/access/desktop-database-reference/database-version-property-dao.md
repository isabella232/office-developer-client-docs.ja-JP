---
title: Database.Version プロパティ (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bcb360caa71131f4892409805c7afe3ceb2dcce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479548"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="ae922-102">Database.Version プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="ae922-102">Database.Version Property (DAO)</span></span>


<span data-ttu-id="ae922-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae922-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ae922-p101">Microsoft Access ワークスペースで、データベースを作成した Microsoft Jet または Microsoft Office Access のデータベース エンジンのバージョンを取得します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae922-p101">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae922-106">構文</span><span class="sxs-lookup"><span data-stu-id="ae922-106">Syntax</span></span>

<span data-ttu-id="ae922-107">*式*です。バージョン</span><span class="sxs-lookup"><span data-stu-id="ae922-107">*expression* .Version</span></span>

<span data-ttu-id="ae922-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ae922-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae922-109">注釈</span><span class="sxs-lookup"><span data-stu-id="ae922-109">Remarks</span></span>

<span data-ttu-id="ae922-110">戻り値は、次の書式設定のバージョン番号として評価される文字列型 (String) の値となります。</span><span class="sxs-lookup"><span data-stu-id="ae922-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

  - <span data-ttu-id="ae922-p102">Microsoft Access ワークスペースでは、このバージョン番号を "*major.minor*" という形式で表します。たとえば、"3.0"と表します。製品のバージョン番号は、バージョン番号 (3)、ピリオド、およびリリース番号 (0) から構成されます。</span><span class="sxs-lookup"><span data-stu-id="ae922-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="ae922-114">次の表は、Microsoft 製品の各種バージョンに搭載されているデータベース エンジンのバージョンの一覧です。</span><span class="sxs-lookup"><span data-stu-id="ae922-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae922-115">データベース エンジン</span><span class="sxs-lookup"><span data-stu-id="ae922-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="ae922-116">バージョン (リリース年)</span><span class="sxs-lookup"><span data-stu-id="ae922-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="ae922-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="ae922-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="ae922-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ae922-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="ae922-119">Excel</span><span class="sxs-lookup"><span data-stu-id="ae922-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="ae922-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="ae922-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae922-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="ae922-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="ae922-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="ae922-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="ae922-123">1.0</span><span class="sxs-lookup"><span data-stu-id="ae922-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="ae922-124">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="ae922-125">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="ae922-126">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae922-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="ae922-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="ae922-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="ae922-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="ae922-129">1.1</span><span class="sxs-lookup"><span data-stu-id="ae922-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="ae922-130">3.0</span><span class="sxs-lookup"><span data-stu-id="ae922-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="ae922-131">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="ae922-132">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae922-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="ae922-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="ae922-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="ae922-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="ae922-135">2.0</span><span class="sxs-lookup"><span data-stu-id="ae922-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="ae922-136">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="ae922-137">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="ae922-138">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae922-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="ae922-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="ae922-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="ae922-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="ae922-141">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="ae922-142">4.0 (16 ビット)</span><span class="sxs-lookup"><span data-stu-id="ae922-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="ae922-143">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="ae922-144">N/A</span><span class="sxs-lookup"><span data-stu-id="ae922-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae922-145">Jet</span><span class="sxs-lookup"><span data-stu-id="ae922-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="ae922-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="ae922-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="ae922-147">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="ae922-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="ae922-148">4.0 (32 ビット)</span><span class="sxs-lookup"><span data-stu-id="ae922-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="ae922-149">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="ae922-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="ae922-150">4.x</span><span class="sxs-lookup"><span data-stu-id="ae922-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae922-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="ae922-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="ae922-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="ae922-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="ae922-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="ae922-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="ae922-154">5.0</span><span class="sxs-lookup"><span data-stu-id="ae922-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="ae922-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="ae922-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="ae922-156">5.0</span><span class="sxs-lookup"><span data-stu-id="ae922-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae922-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="ae922-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="ae922-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="ae922-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="ae922-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="ae922-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ae922-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="ae922-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae922-161">Microsoft Access データベース エンジン</span><span class="sxs-lookup"><span data-stu-id="ae922-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="ae922-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="ae922-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="ae922-163">2007</span><span class="sxs-lookup"><span data-stu-id="ae922-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

