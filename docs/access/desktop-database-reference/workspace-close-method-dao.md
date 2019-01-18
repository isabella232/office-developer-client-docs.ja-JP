---
title: Workspace.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708628"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="46171-102">Workspace.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="46171-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="46171-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="46171-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46171-104">開いている **Workspace** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="46171-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="46171-105">構文</span><span class="sxs-lookup"><span data-stu-id="46171-105">Syntax</span></span>

<span data-ttu-id="46171-106">*式*です。閉じる</span><span class="sxs-lookup"><span data-stu-id="46171-106">*expression* .Close</span></span>

<span data-ttu-id="46171-107">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="46171-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="46171-108">注釈</span><span class="sxs-lookup"><span data-stu-id="46171-108">Remarks</span></span>

<span data-ttu-id="46171-109">**Close** の使用時に **Workspace** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="46171-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="46171-110">代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。</span><span class="sxs-lookup"><span data-stu-id="46171-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

