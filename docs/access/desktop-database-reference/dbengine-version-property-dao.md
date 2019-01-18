---
title: DBEngine.Version プロパティ (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7e22645127f18ad815c398fd38f9ac4615dfadc9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712786"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="33aba-102">DBEngine.Version プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="33aba-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="33aba-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="33aba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33aba-p101">現在使用中の DAO のバージョンを返します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="33aba-p101">Rreturns the version of DAO currently in use. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="33aba-106">構文</span><span class="sxs-lookup"><span data-stu-id="33aba-106">Syntax</span></span>

<span data-ttu-id="33aba-107">*式*です。バージョン</span><span class="sxs-lookup"><span data-stu-id="33aba-107">*expression* .Version</span></span>

<span data-ttu-id="33aba-108">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="33aba-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="33aba-109">注釈</span><span class="sxs-lookup"><span data-stu-id="33aba-109">Remarks</span></span>

<span data-ttu-id="33aba-p102">戻り値は、"<メジャー>.<マイナー>" の形式で評価結果がバージョン番号になる文字列型 (String) の値です。たとえば、"3.0" などです。製品のバージョン番号は、バージョン番号 (3)、ピリオド、およびリリース番号 (0) で構成されます。</span><span class="sxs-lookup"><span data-stu-id="33aba-p102">The return value is a String that evaluates to a version number in the form "major.minor". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

