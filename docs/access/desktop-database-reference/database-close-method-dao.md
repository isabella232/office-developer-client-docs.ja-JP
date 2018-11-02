---
title: Database.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c97786db2e909074f1a1e0d81e4af03d34301602
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920684"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="f7157-102">Database.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="f7157-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="f7157-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f7157-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7157-104">開いている **Database** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="f7157-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7157-105">構文</span><span class="sxs-lookup"><span data-stu-id="f7157-105">Syntax</span></span>

<span data-ttu-id="f7157-106">*式*です。閉じる</span><span class="sxs-lookup"><span data-stu-id="f7157-106">*expression* .Close</span></span>

<span data-ttu-id="f7157-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f7157-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7157-108">注釈</span><span class="sxs-lookup"><span data-stu-id="f7157-108">Remarks</span></span>

<span data-ttu-id="f7157-109">**Close** を使用したときに **Database** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f7157-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="f7157-110">代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。</span><span class="sxs-lookup"><span data-stu-id="f7157-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

