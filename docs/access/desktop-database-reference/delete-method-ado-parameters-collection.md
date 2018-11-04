---
title: メソッド (ADO Parameters コレクション) を削除します。
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 213d29ecd6599803c0fa2211a17ac14da7dc698a
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949454"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="06ac8-102">メソッド (ADO Parameters コレクション) を削除します。</span><span class="sxs-lookup"><span data-stu-id="06ac8-102">Delete method (ADO Parameters Collection)</span></span>

<span data-ttu-id="06ac8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="06ac8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06ac8-104">[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="06ac8-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ac8-105">構文</span><span class="sxs-lookup"><span data-stu-id="06ac8-105">Syntax</span></span>

<span data-ttu-id="06ac8-106">*パラメーター*です。*インデックス*を削除します。</span><span class="sxs-lookup"><span data-stu-id="06ac8-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="06ac8-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="06ac8-107">Parameters</span></span>

|<span data-ttu-id="06ac8-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="06ac8-108">Parameter</span></span>|<span data-ttu-id="06ac8-109">説明</span><span class="sxs-lookup"><span data-stu-id="06ac8-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="06ac8-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="06ac8-110">*Index*</span></span> |<span data-ttu-id="06ac8-111">削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="06ac8-111">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="06ac8-112">解説</span><span class="sxs-lookup"><span data-stu-id="06ac8-112">Remarks</span></span>

<span data-ttu-id="06ac8-p101">コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、 **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションでのみ使用できます。 [Delete](parameter-object-ado.md) メソッドを呼び出すときは、 [Parameter](name-property-ado.md) オブジェクトの **Name** プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。</span><span class="sxs-lookup"><span data-stu-id="06ac8-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

