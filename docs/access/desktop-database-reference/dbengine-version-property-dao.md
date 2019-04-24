---
title: DBEngine プロパティ (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294191"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="0e777-102">DBEngine プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="0e777-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="0e777-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e777-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e777-104">rreturns 現在使用されている DAO のバージョンを返します。</span><span class="sxs-lookup"><span data-stu-id="0e777-104">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="0e777-105">値の取得のみ可能な文字列型 (**String**) の値です。</span><span class="sxs-lookup"><span data-stu-id="0e777-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e777-106">構文</span><span class="sxs-lookup"><span data-stu-id="0e777-106">Syntax</span></span>

<span data-ttu-id="0e777-107">*式*。バージョン</span><span class="sxs-lookup"><span data-stu-id="0e777-107">*expression* .Version</span></span>

<span data-ttu-id="0e777-108">\*式\***DBEngine**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e777-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e777-109">注釈</span><span class="sxs-lookup"><span data-stu-id="0e777-109">Remarks</span></span>

<span data-ttu-id="0e777-110">戻り値は、"<メジャー>.<マイナー>" の形式で評価結果がバージョン番号になる文字列型 (String) の値です。</span><span class="sxs-lookup"><span data-stu-id="0e777-110">The return value is a String that evaluates to a version number in the form "major.minor".</span></span> <span data-ttu-id="0e777-111">For example, "3.0".</span><span class="sxs-lookup"><span data-stu-id="0e777-111">For example, "3.0".</span></span> <span data-ttu-id="0e777-112">The product version number consists of the version number (3), a period, and the release number (0).</span><span class="sxs-lookup"><span data-stu-id="0e777-112">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

