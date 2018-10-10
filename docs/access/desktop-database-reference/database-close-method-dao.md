---
title: Database.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 97246da6224ee04fa435638a0cb11d1bdac8859f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476925"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="f512c-102">Database.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="f512c-102">Database.Close Method (DAO)</span></span>


<span data-ttu-id="f512c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f512c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f512c-104">開いている **Database** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="f512c-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f512c-105">構文</span><span class="sxs-lookup"><span data-stu-id="f512c-105">Syntax</span></span>

<span data-ttu-id="f512c-106">*式*です。閉じる</span><span class="sxs-lookup"><span data-stu-id="f512c-106">*expression* .Close</span></span>

<span data-ttu-id="f512c-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f512c-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f512c-108">注釈</span><span class="sxs-lookup"><span data-stu-id="f512c-108">Remarks</span></span>

<span data-ttu-id="f512c-109">**Close** を使用したときに **Database** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f512c-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="f512c-110">代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。</span><span class="sxs-lookup"><span data-stu-id="f512c-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

