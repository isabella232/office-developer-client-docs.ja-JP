---
title: QueryDef.StillExecuting プロパティ (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 60c0663eaa6857801555c6ce05f4256cfe4c290f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716692"
---
# <a name="querydefstillexecuting-property-dao"></a><span data-ttu-id="8622c-102">QueryDef.StillExecuting プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="8622c-102">QueryDef.StillExecuting property (DAO)</span></span>


<span data-ttu-id="8622c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8622c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8622c-104">構文</span><span class="sxs-lookup"><span data-stu-id="8622c-104">Syntax</span></span>

<span data-ttu-id="8622c-105">*式*です。StillExecuting</span><span class="sxs-lookup"><span data-stu-id="8622c-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="8622c-106">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="8622c-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8622c-107">注釈</span><span class="sxs-lookup"><span data-stu-id="8622c-107">Remarks</span></span>

<span data-ttu-id="8622c-p101">最後に呼び出した非同期の [**Execute**](querydef-execute-method-dao.md) メソッドまたは [**OpenConnection**](dbengine-openconnection-method-dao.md) メソッド (つまり、 **dbRunAsync** オプションで実行されるメソッド) が完了したかどうかを確認するには、 **StillExecuting** プロパティを使用します。 **StillExecuting** プロパティが **True** のときは、返されるオブジェクトにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="8622c-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **[Execute](querydef-execute-method-dao.md)** or **[OpenConnection](dbengine-openconnection-method-dao.md)** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="8622c-p102">関連する \*\*\*\*Connection\*\*\*\* オブジェクトを取得する **OpenConnection** メソッドの呼び出しに続いて、 [StillExecuting](connection-object-dao.md) プロパティで **False** が取得されると、そのオブジェクトを参照できます。 **StillExecuting** で **True** が取得される間は、 **StillExecuting** プロパティの取得を除き、そのオブジェクトに対する参照は実行できません。</span><span class="sxs-lookup"><span data-stu-id="8622c-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **[Connection](connection-object-dao.md)** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="8622c-112">処理中のタスクの実行を中止するには、 **[Cancel](connection-cancel-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8622c-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

