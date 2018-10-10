---
title: Delete メソッド (ADO Parameters コレクション)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43d193a78be10ec5cedc2fe1a4001e677878dfb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478447"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="f8b74-102">Delete メソッド (ADO Parameters コレクション)</span><span class="sxs-lookup"><span data-stu-id="f8b74-102">Delete Method (ADO Parameters Collection)</span></span>


<span data-ttu-id="f8b74-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8b74-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="f8b74-104">[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="f8b74-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b74-105">構文</span><span class="sxs-lookup"><span data-stu-id="f8b74-105">Syntax</span></span>

<span data-ttu-id="f8b74-106">*パラメーター*です。*インデックス*を削除します。</span><span class="sxs-lookup"><span data-stu-id="f8b74-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="f8b74-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8b74-107">Parameters</span></span>

  - <span data-ttu-id="f8b74-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="f8b74-108">*Index*</span></span>

  - <span data-ttu-id="f8b74-109">削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="f8b74-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b74-110">解説</span><span class="sxs-lookup"><span data-stu-id="f8b74-110">Remarks</span></span>

<span data-ttu-id="f8b74-p101">コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、 **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションでのみ使用できます。 [Delete](parameter-object-ado.md) メソッドを呼び出すときは、 [Parameter](name-property-ado.md) オブジェクトの **Name** プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。</span><span class="sxs-lookup"><span data-stu-id="f8b74-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

