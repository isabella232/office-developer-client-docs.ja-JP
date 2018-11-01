---
title: Workspace.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38f1a7a525a2cf57a98ee3fa015ce29b368aab9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884129"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="ac3af-102">Workspace.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="ac3af-102">Workspace.Close Method (DAO)</span></span>


<span data-ttu-id="ac3af-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ac3af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac3af-104">開いている **Workspace** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="ac3af-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac3af-105">構文</span><span class="sxs-lookup"><span data-stu-id="ac3af-105">Syntax</span></span>

<span data-ttu-id="ac3af-106">*式*です。閉じる</span><span class="sxs-lookup"><span data-stu-id="ac3af-106">*expression* .Close</span></span>

<span data-ttu-id="ac3af-107">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ac3af-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac3af-108">注釈</span><span class="sxs-lookup"><span data-stu-id="ac3af-108">Remarks</span></span>

<span data-ttu-id="ac3af-109">**Close** の使用時に **Workspace** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ac3af-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="ac3af-110">代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。</span><span class="sxs-lookup"><span data-stu-id="ac3af-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

