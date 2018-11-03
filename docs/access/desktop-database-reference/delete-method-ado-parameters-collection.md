---
title: メソッド (ADO Parameters コレクション) を削除します。
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b18a09d6a0c9d6a6ad8e9f579068c4f6d7162d1f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944873"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="fa9a6-102">メソッド (ADO Parameters コレクション) を削除します。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-102">Delete method (ADO Parameters Collection)</span></span>


<span data-ttu-id="fa9a6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="fa9a6-104">[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa9a6-105">構文</span><span class="sxs-lookup"><span data-stu-id="fa9a6-105">Syntax</span></span>

<span data-ttu-id="fa9a6-106">*パラメーター*です。*インデックス*を削除します。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="fa9a6-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fa9a6-107">Parameters</span></span>

- <span data-ttu-id="fa9a6-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="fa9a6-108">*Index*</span></span>

  - <span data-ttu-id="fa9a6-109">削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa9a6-110">解説</span><span class="sxs-lookup"><span data-stu-id="fa9a6-110">Remarks</span></span>

<span data-ttu-id="fa9a6-p101">コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、 **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションでのみ使用できます。 [Delete](parameter-object-ado.md) メソッドを呼び出すときは、 [Parameter](name-property-ado.md) オブジェクトの **Name** プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

