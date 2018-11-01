---
title: Property.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: 0dae15e0-5d2e-3bb4-8a44-98db4a8ce516
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845211(v=office.15)
ms:contentKeyID: 48543225
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09a5e37bf9874888ca37935db38c98773cb03806
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867302"
---
# <a name="propertyname-property-dao"></a><span data-ttu-id="08d24-102">Property.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="08d24-102">Property.Name Property (DAO)</span></span>


<span data-ttu-id="08d24-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="08d24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08d24-p101">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="08d24-p101">Returns or sets the name of the specified object. Read/write **String** if the object has not been appended to a collection. Read-only **String** if the object has been appended to a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d24-107">構文</span><span class="sxs-lookup"><span data-stu-id="08d24-107">Syntax</span></span>

<span data-ttu-id="08d24-108">*式*です。名</span><span class="sxs-lookup"><span data-stu-id="08d24-108">*expression* .Name</span></span>

<span data-ttu-id="08d24-109">\*式\***Property**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="08d24-109">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="08d24-110">注釈</span><span class="sxs-lookup"><span data-stu-id="08d24-110">Remarks</span></span>

<span data-ttu-id="08d24-111">組み込みプロパティの **Name** プロパティは、常に値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="08d24-111">The **Name** property of a built-in property is always read-only.</span></span>

<span data-ttu-id="08d24-112">**Property** オブジェクトの名前の最大長は 64 文字です。</span><span class="sxs-lookup"><span data-stu-id="08d24-112">The maximum length for the name of a **Property** object is 64 characters.</span></span>

