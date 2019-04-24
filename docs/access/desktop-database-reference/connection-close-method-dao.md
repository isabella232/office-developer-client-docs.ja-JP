---
title: Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295962"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="f6f6b-102">Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="f6f6b-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="f6f6b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6f6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6f6b-104">開いている **Connection** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="f6f6b-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f6b-105">構文</span><span class="sxs-lookup"><span data-stu-id="f6f6b-105">Syntax</span></span>

<span data-ttu-id="f6f6b-106">*式*。いったん</span><span class="sxs-lookup"><span data-stu-id="f6f6b-106">*expression* .Close</span></span>

<span data-ttu-id="f6f6b-107">\*式\***Connection**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="f6f6b-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6f6b-108">注釈</span><span class="sxs-lookup"><span data-stu-id="f6f6b-108">Remarks</span></span>

<span data-ttu-id="f6f6b-109">**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f6f6b-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="f6f6b-p101">開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。</span><span class="sxs-lookup"><span data-stu-id="f6f6b-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="f6f6b-112">**Close**メソッドの代わりに、オブジェクト変数の値を**nothing**に設定します (dbsTemp = nothing を設定します)。</span><span class="sxs-lookup"><span data-stu-id="f6f6b-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

