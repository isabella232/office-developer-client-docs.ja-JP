---
title: Delete メソッド (ADO Parameters コレクション)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294093"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="1e45f-102">Delete メソッド (ADO Parameters コレクション)</span><span class="sxs-lookup"><span data-stu-id="1e45f-102">Delete method (ADO Parameters Collection)</span></span>

<span data-ttu-id="1e45f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e45f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e45f-104">[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="1e45f-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e45f-105">構文</span><span class="sxs-lookup"><span data-stu-id="1e45f-105">Syntax</span></span>

<span data-ttu-id="1e45f-106">*パラメーター*。*インデックス*の削除</span><span class="sxs-lookup"><span data-stu-id="1e45f-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="1e45f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1e45f-107">Parameters</span></span>

|<span data-ttu-id="1e45f-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1e45f-108">Parameter</span></span>|<span data-ttu-id="1e45f-109">説明</span><span class="sxs-lookup"><span data-stu-id="1e45f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1e45f-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="1e45f-110">*Index*</span></span> |<span data-ttu-id="1e45f-111">削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="1e45f-111">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1e45f-112">注釈</span><span class="sxs-lookup"><span data-stu-id="1e45f-112">Remarks</span></span>

<span data-ttu-id="1e45f-p101">コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、[Command](command-object-ado.md) オブジェクトの **Parameters** コレクションでのみ使用できます。**Delete** メソッドを呼び出すときは、[Parameter](parameter-object-ado.md) オブジェクトの [Name](name-property-ado.md) プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。</span><span class="sxs-lookup"><span data-stu-id="1e45f-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

