---
title: Workspace メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305958"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="c6ba7-102">Workspace メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="c6ba7-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="c6ba7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6ba7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6ba7-104">開いている **Workspace** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="c6ba7-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ba7-105">構文</span><span class="sxs-lookup"><span data-stu-id="c6ba7-105">Syntax</span></span>

<span data-ttu-id="c6ba7-106">*式*。いったん</span><span class="sxs-lookup"><span data-stu-id="c6ba7-106">*expression* .Close</span></span>

<span data-ttu-id="c6ba7-107">\*式\***Workspace**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c6ba7-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6ba7-108">注釈</span><span class="sxs-lookup"><span data-stu-id="c6ba7-108">Remarks</span></span>

<span data-ttu-id="c6ba7-109">**Close** の使用時に **Workspace** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c6ba7-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="c6ba7-110">**Close**メソッドの代わりに、オブジェクト変数の値を**nothing**に設定します (dbsTemp = nothing を設定します)。</span><span class="sxs-lookup"><span data-stu-id="c6ba7-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

