---
title: QueryDef.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720003"
---
# <a name="querydefclose-method-dao"></a><span data-ttu-id="7d551-102">QueryDef.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="7d551-102">QueryDef.Close method (DAO)</span></span>


<span data-ttu-id="7d551-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7d551-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d551-104">開いている **QueryDef** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d551-104">Closes an open **QueryDef**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d551-105">構文</span><span class="sxs-lookup"><span data-stu-id="7d551-105">Syntax</span></span>

<span data-ttu-id="7d551-106">*式*です。閉じる</span><span class="sxs-lookup"><span data-stu-id="7d551-106">*expression* .Close</span></span>

<span data-ttu-id="7d551-107">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="7d551-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d551-108">注釈</span><span class="sxs-lookup"><span data-stu-id="7d551-108">Remarks</span></span>

<span data-ttu-id="7d551-109">**Close** を使用したときに **QueryDef** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7d551-109">If the **QueryDef** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="7d551-110">代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。</span><span class="sxs-lookup"><span data-stu-id="7d551-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

