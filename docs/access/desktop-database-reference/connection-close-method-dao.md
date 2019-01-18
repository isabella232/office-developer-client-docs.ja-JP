---
title: Connection.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717217"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="21d00-102">Connection.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="21d00-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="21d00-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="21d00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21d00-104">開いている **Connection** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="21d00-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d00-105">構文</span><span class="sxs-lookup"><span data-stu-id="21d00-105">Syntax</span></span>

<span data-ttu-id="21d00-106">*式*です。閉じる</span><span class="sxs-lookup"><span data-stu-id="21d00-106">*expression* .Close</span></span>

<span data-ttu-id="21d00-107">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="21d00-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21d00-108">注釈</span><span class="sxs-lookup"><span data-stu-id="21d00-108">Remarks</span></span>

<span data-ttu-id="21d00-109">**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="21d00-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="21d00-p101">開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。</span><span class="sxs-lookup"><span data-stu-id="21d00-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="21d00-112">代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。</span><span class="sxs-lookup"><span data-stu-id="21d00-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

