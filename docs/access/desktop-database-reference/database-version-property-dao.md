---
title: Database.Version プロパティ (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611fed16c9020b0a6499427af0788bf9ff050c28
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936561"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="bc3cd-102">Database.Version プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="bc3cd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bc3cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc3cd-p101">Microsoft Access ワークスペースで、データベースを作成した Microsoft Jet または Microsoft Office Access のデータベース エンジンのバージョンを取得します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bc3cd-p101">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3cd-106">構文</span><span class="sxs-lookup"><span data-stu-id="bc3cd-106">Syntax</span></span>

<span data-ttu-id="bc3cd-107">*式*です。バージョン</span><span class="sxs-lookup"><span data-stu-id="bc3cd-107">*expression* .Version</span></span>

<span data-ttu-id="bc3cd-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="bc3cd-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc3cd-109">注釈</span><span class="sxs-lookup"><span data-stu-id="bc3cd-109">Remarks</span></span>

<span data-ttu-id="bc3cd-110">戻り値は、次の書式設定のバージョン番号として評価される文字列型 (String) の値となります。</span><span class="sxs-lookup"><span data-stu-id="bc3cd-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="bc3cd-p102">Microsoft Access ワークスペースでは、このバージョン番号を "*major.minor*" という形式で表します。たとえば、"3.0"と表します。製品のバージョン番号は、バージョン番号 (3)、ピリオド、およびリリース番号 (0) から構成されます。</span><span class="sxs-lookup"><span data-stu-id="bc3cd-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="bc3cd-114">次の表は、Microsoft 製品の各種バージョンに搭載されているデータベース エンジンのバージョンの一覧です。</span><span class="sxs-lookup"><span data-stu-id="bc3cd-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

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
<th><p><span data-ttu-id="bc3cd-115">データベース エンジン</span><span class="sxs-lookup"><span data-stu-id="bc3cd-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="bc3cd-116">バージョン (リリース年)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="bc3cd-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="bc3cd-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="bc3cd-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bc3cd-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="bc3cd-119">Excel</span><span class="sxs-lookup"><span data-stu-id="bc3cd-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="bc3cd-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="bc3cd-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc3cd-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="bc3cd-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-123">1.0</span><span class="sxs-lookup"><span data-stu-id="bc3cd-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-124">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-125">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-126">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc3cd-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="bc3cd-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-129">1.1</span><span class="sxs-lookup"><span data-stu-id="bc3cd-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-130">3.0</span><span class="sxs-lookup"><span data-stu-id="bc3cd-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-131">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-132">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc3cd-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="bc3cd-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-135">2.0</span><span class="sxs-lookup"><span data-stu-id="bc3cd-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-136">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-137">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-138">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc3cd-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="bc3cd-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-141">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-142">4.0 (16 ビット)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-143">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-144">N/A</span><span class="sxs-lookup"><span data-stu-id="bc3cd-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc3cd-145">Jet</span><span class="sxs-lookup"><span data-stu-id="bc3cd-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-147">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-148">4.0 (32 ビット)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-149">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-150">4.x</span><span class="sxs-lookup"><span data-stu-id="bc3cd-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc3cd-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="bc3cd-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-154">5.0</span><span class="sxs-lookup"><span data-stu-id="bc3cd-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-156">5.0</span><span class="sxs-lookup"><span data-stu-id="bc3cd-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc3cd-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="bc3cd-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc3cd-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc3cd-161">Microsoft Access データベース エンジン</span><span class="sxs-lookup"><span data-stu-id="bc3cd-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="bc3cd-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="bc3cd-163">2007</span><span class="sxs-lookup"><span data-stu-id="bc3cd-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

