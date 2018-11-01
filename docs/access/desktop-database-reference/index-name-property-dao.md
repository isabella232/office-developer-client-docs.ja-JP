---
title: Index.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: 83cb72c8-068a-229d-c95d-ba16567505c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196754(v=office.15)
ms:contentKeyID: 48546017
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2e3e18d8163084149ce986a557c1216dab15de09
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887223"
---
# <a name="indexname-property-dao"></a><span data-ttu-id="839c8-102">Index.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="839c8-102">Index.Name Property (DAO)</span></span>


<span data-ttu-id="839c8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="839c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="839c8-p101">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="839c8-p101">Returns or sets the name of the specified object. Read/write **String** if the object has not been appended to a collection. Read-only **String** if the object has been appended to a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="839c8-107">構文</span><span class="sxs-lookup"><span data-stu-id="839c8-107">Syntax</span></span>

<span data-ttu-id="839c8-108">*式*です。名</span><span class="sxs-lookup"><span data-stu-id="839c8-108">*expression* .Name</span></span>

<span data-ttu-id="839c8-109">\*式\***Index**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="839c8-109">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="839c8-110">注釈</span><span class="sxs-lookup"><span data-stu-id="839c8-110">Remarks</span></span>

<span data-ttu-id="839c8-111">**Index** オブジェクトの名前の最大長は 64 文字です。</span><span class="sxs-lookup"><span data-stu-id="839c8-111">The maximum length for the name of a **Index** object is 64 characters.</span></span>

