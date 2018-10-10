---
title: Property.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: 0dae15e0-5d2e-3bb4-8a44-98db4a8ce516
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845211(v=office.15)
ms:contentKeyID: 48543225
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ccc0b9073dd0df2f2562995356c194bd91286ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477057"
---
# <a name="propertyname-property-dao"></a><span data-ttu-id="ef84a-102">Property.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="ef84a-102">Property.Name Property (DAO)</span></span>


<span data-ttu-id="ef84a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef84a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ef84a-p101">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ef84a-p101">Returns or sets the name of the specified object. Read/write **String** if the object has not been appended to a collection. Read-only **String** if the object has been appended to a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef84a-107">構文</span><span class="sxs-lookup"><span data-stu-id="ef84a-107">Syntax</span></span>

<span data-ttu-id="ef84a-108">*式*です。名</span><span class="sxs-lookup"><span data-stu-id="ef84a-108">*expression* .Name</span></span>

<span data-ttu-id="ef84a-109">\*式\***Property**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ef84a-109">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef84a-110">注釈</span><span class="sxs-lookup"><span data-stu-id="ef84a-110">Remarks</span></span>

<span data-ttu-id="ef84a-111">組み込みプロパティの **Name** プロパティは、常に値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="ef84a-111">The **Name** property of a built-in property is always read-only.</span></span>

<span data-ttu-id="ef84a-112">**Property** オブジェクトの名前の最大長は 64 文字です。</span><span class="sxs-lookup"><span data-stu-id="ef84a-112">The maximum length for the name of a **Property** object is 64 characters.</span></span>

