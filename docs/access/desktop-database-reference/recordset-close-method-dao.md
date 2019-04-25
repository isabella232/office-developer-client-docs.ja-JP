---
title: Recordset.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f7cbd94bfacc91bfe080d33807ca7989c1dca661
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300554"
---
# <a name="recordsetclose-method-dao"></a><span data-ttu-id="73173-102">Recordset.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="73173-102">Recordset.Close Method (DAO)</span></span>


<span data-ttu-id="73173-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="73173-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73173-104">開いている **Recordset** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="73173-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="73173-105">構文</span><span class="sxs-lookup"><span data-stu-id="73173-105">Syntax</span></span>

<span data-ttu-id="73173-106">*式* .Close</span><span class="sxs-lookup"><span data-stu-id="73173-106">expression  . Close</span></span>

<span data-ttu-id="73173-107">*式* **Recordset** オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="73173-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="73173-108">注釈</span><span class="sxs-lookup"><span data-stu-id="73173-108">Remarks</span></span>

<span data-ttu-id="73173-109">**Close** の使用時に **Recordset** オブジェクトが既に閉じられている場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="73173-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="73173-p101">開いている **Recordset** オブジェクトがある場合に **Connection** オブジェクトを閉じようとすると、その **Recordset** オブジェクトが閉じられ、保留中の更新または編集がキャンセルされます。同様に、開いている **Connection** オブジェクトがある場合に **Workspace** オブジェクトを閉じようとすると、その **Connection** オブジェクトが閉じられ、それに含まれる **Recordset** オブジェクトも閉じられます。</span><span class="sxs-lookup"><span data-stu-id="73173-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="73173-112">**Close** メソッドに代わる方法は、オブジェクト変数の値を **Nothing** に設定することです (Set dbsTemp = Nothing)。</span><span class="sxs-lookup"><span data-stu-id="73173-112">An alternative to the Close method is to set the value of an object variable to Nothing (Set dbsTemp = Nothing).</span></span>

