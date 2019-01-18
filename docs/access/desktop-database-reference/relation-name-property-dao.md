---
title: Relation.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: 7ad17dcd-9fe2-a4b0-2fab-c5b13e66fedc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196187(v=office.15)
ms:contentKeyID: 48545802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 82075a2421632c08daf40903aa389774e65231e4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718841"
---
# <a name="relationname-property-dao"></a><span data-ttu-id="c7027-102">Relation.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c7027-102">Relation.Name property (DAO)</span></span>


<span data-ttu-id="c7027-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c7027-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7027-p101">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c7027-p101">Returns or sets the name of the specified object. Read/write **String** if the object has not been appended to a collection. Read-only **String** if the object has been appended to a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7027-107">構文</span><span class="sxs-lookup"><span data-stu-id="c7027-107">Syntax</span></span>

<span data-ttu-id="c7027-108">*式*です。名</span><span class="sxs-lookup"><span data-stu-id="c7027-108">*expression* .Name</span></span>

<span data-ttu-id="c7027-109">\*式\***Relation**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c7027-109">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7027-110">注釈</span><span class="sxs-lookup"><span data-stu-id="c7027-110">Remarks</span></span>

<span data-ttu-id="c7027-111">**Relation** オブジェクトの名前の最大長は 64 文字です。</span><span class="sxs-lookup"><span data-stu-id="c7027-111">The maximum length for the name of a **Relation** object is 64 characters.</span></span>

