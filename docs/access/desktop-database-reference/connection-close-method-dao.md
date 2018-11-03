---
title: Connection.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6f84b9580fbd6256069de57b2295cf3460edaf8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928979"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="d71f8-102">Connection.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="d71f8-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="d71f8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d71f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d71f8-104">開いている **Connection** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="d71f8-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d71f8-105">構文</span><span class="sxs-lookup"><span data-stu-id="d71f8-105">Syntax</span></span>

<span data-ttu-id="d71f8-106">*式*です。閉じる</span><span class="sxs-lookup"><span data-stu-id="d71f8-106">*expression* .Close</span></span>

<span data-ttu-id="d71f8-107">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d71f8-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d71f8-108">注釈</span><span class="sxs-lookup"><span data-stu-id="d71f8-108">Remarks</span></span>

<span data-ttu-id="d71f8-109">**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d71f8-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="d71f8-p101">開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。</span><span class="sxs-lookup"><span data-stu-id="d71f8-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="d71f8-112">代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。</span><span class="sxs-lookup"><span data-stu-id="d71f8-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

