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
ms.openlocfilehash: 1723deea7f29c59fb388a11acc5e5ffcced4abe1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924597"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="2b79e-102">DBEngine.Version プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b79e-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="2b79e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2b79e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b79e-p101">現在使用中の DAO のバージョンを返します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2b79e-p101">Rreturns the version of DAO currently in use. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b79e-106">構文</span><span class="sxs-lookup"><span data-stu-id="2b79e-106">Syntax</span></span>

<span data-ttu-id="2b79e-107">*式*です。バージョン</span><span class="sxs-lookup"><span data-stu-id="2b79e-107">*expression* .Version</span></span>

<span data-ttu-id="2b79e-108">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="2b79e-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b79e-109">備考</span><span class="sxs-lookup"><span data-stu-id="2b79e-109">Remarks</span></span>

<span data-ttu-id="2b79e-p102">戻り値は、"<メジャー>.<マイナー>" の形式で評価結果がバージョン番号になる文字列型 (String) の値です。たとえば、"3.0" などです。製品のバージョン番号は、バージョン番号 (3)、ピリオド、およびリリース番号 (0) で構成されます。</span><span class="sxs-lookup"><span data-stu-id="2b79e-p102">The return value is a String that evaluates to a version number in the form "major.minor". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

