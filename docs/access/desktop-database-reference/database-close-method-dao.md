---
title: Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295024"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="e3110-102">Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="e3110-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="e3110-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3110-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3110-104">開いている **Database** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="e3110-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3110-105">構文</span><span class="sxs-lookup"><span data-stu-id="e3110-105">Syntax</span></span>

<span data-ttu-id="e3110-106">*式*。いったん</span><span class="sxs-lookup"><span data-stu-id="e3110-106">*expression* .Close</span></span>

<span data-ttu-id="e3110-107">\*式\***Database**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="e3110-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3110-108">注釈</span><span class="sxs-lookup"><span data-stu-id="e3110-108">Remarks</span></span>

<span data-ttu-id="e3110-109">**Close** を使用したときに **Database** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e3110-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="e3110-110">**Close**メソッドの代わりに、オブジェクト変数の値を**nothing**に設定します (dbsTemp = nothing を設定します)。</span><span class="sxs-lookup"><span data-stu-id="e3110-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

