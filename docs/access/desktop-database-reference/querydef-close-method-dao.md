---
title: QueryDef メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303305"
---
# <a name="querydefclose-method-dao"></a><span data-ttu-id="90ce0-102">QueryDef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="90ce0-102">QueryDef.Close method (DAO)</span></span>


<span data-ttu-id="90ce0-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="90ce0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90ce0-104">開いている **QueryDef** を閉じます。</span><span class="sxs-lookup"><span data-stu-id="90ce0-104">Closes an open **QueryDef**.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ce0-105">構文</span><span class="sxs-lookup"><span data-stu-id="90ce0-105">Syntax</span></span>

<span data-ttu-id="90ce0-106">*式*。いったん</span><span class="sxs-lookup"><span data-stu-id="90ce0-106">*expression* .Close</span></span>

<span data-ttu-id="90ce0-107">\*式\***QueryDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="90ce0-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ce0-108">注釈</span><span class="sxs-lookup"><span data-stu-id="90ce0-108">Remarks</span></span>

<span data-ttu-id="90ce0-109">**Close** を使用したときに **QueryDef** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="90ce0-109">If the **QueryDef** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="90ce0-110">**Close**メソッドの代わりに、オブジェクト変数の値を**nothing**に設定します (dbsTemp = nothing を設定します)。</span><span class="sxs-lookup"><span data-stu-id="90ce0-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

