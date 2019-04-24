---
title: Recordset2 メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307414"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="b8a13-102">Recordset2 メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="b8a13-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="b8a13-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8a13-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a13-104">構文</span><span class="sxs-lookup"><span data-stu-id="b8a13-104">Syntax</span></span>

<span data-ttu-id="b8a13-105">*式*。キャンセル</span><span class="sxs-lookup"><span data-stu-id="b8a13-105">*expression* .Cancel</span></span>

<span data-ttu-id="b8a13-106">\*式\***Recordset2**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8a13-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a13-107">注釈</span><span class="sxs-lookup"><span data-stu-id="b8a13-107">Remarks</span></span>

<span data-ttu-id="b8a13-108">**Cancel**メソッドを使用して、非同期の**Execute**メソッドまたは**openconnection**メソッドの呼び出し (つまり、dbrunasync オプションを指定してメソッドが呼び出された場合) の実行を終了します。</span><span class="sxs-lookup"><span data-stu-id="b8a13-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="b8a13-109">終了しようとしているメソッドで dbrunasync が使用されていない場合、 **Cancel**は実行時エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="b8a13-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

