---
title: Field.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: b7093c63-6d57-31c8-5845-d65250386d0f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822416(v=office.15)
ms:contentKeyID: 48547292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f84ccf11069e98fb6a7183cc996f993e8d6ebb75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293078"
---
# <a name="fieldname-property-dao"></a><span data-ttu-id="3c560-102">Field.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="3c560-102">Field.Name property (DAO)</span></span>


<span data-ttu-id="3c560-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c560-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c560-p101">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c560-p101">Returns or sets the name of the specified object. Read/write **String** if the object has not been appended to a collection. Read-only **String** if the object has been appended to a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c560-107">構文</span><span class="sxs-lookup"><span data-stu-id="3c560-107">Syntax</span></span>

<span data-ttu-id="3c560-108">*式*。拡張子</span><span class="sxs-lookup"><span data-stu-id="3c560-108">*expression* .Name</span></span>

<span data-ttu-id="3c560-109">\*式\***Field**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="3c560-109">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c560-110">注釈</span><span class="sxs-lookup"><span data-stu-id="3c560-110">Remarks</span></span>

<span data-ttu-id="3c560-111">**Field** オブジェクトの名前の最大長は 64 文字です。</span><span class="sxs-lookup"><span data-stu-id="3c560-111">The maximum length for the name of a **Field** object is 64 characters.</span></span>

