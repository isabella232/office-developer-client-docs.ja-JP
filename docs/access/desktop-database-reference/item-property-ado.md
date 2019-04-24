---
title: Item プロパティ (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290794"
---
# <a name="item-property-ado"></a><span data-ttu-id="a1ba0-102">Item プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a1ba0-102">Item property (ADO)</span></span>

<span data-ttu-id="a1ba0-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1ba0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1ba0-104">コレクションの特定のメンバーをその名前または序数で示します。</span><span class="sxs-lookup"><span data-stu-id="a1ba0-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ba0-105">構文</span><span class="sxs-lookup"><span data-stu-id="a1ba0-105">Syntax</span></span>

<span data-ttu-id="a1ba0-106">*オブジェクト* = の*コレクション*を設定します。Item (Index)</span><span class="sxs-lookup"><span data-stu-id="a1ba0-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="a1ba0-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="a1ba0-107">Return value</span></span>

<span data-ttu-id="a1ba0-108">オブジェクトへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="a1ba0-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1ba0-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1ba0-109">Parameters</span></span>

|<span data-ttu-id="a1ba0-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1ba0-110">Parameter</span></span>|<span data-ttu-id="a1ba0-111">説明</span><span class="sxs-lookup"><span data-stu-id="a1ba0-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a1ba0-112">*Index*</span><span class="sxs-lookup"><span data-stu-id="a1ba0-112">*Index*</span></span> |<span data-ttu-id="a1ba0-113">コレクション内のオブジェクトの名前または序数に評価されるバリアント型 ( **Variant** ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a1ba0-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a1ba0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a1ba0-114">Remarks</span></span>

<span data-ttu-id="a1ba0-p101">**Item** プロパティは、コレクション内の特定のオブジェクトを返すために使います。コレクション内で **Item** が *Index* 引数に対応するオブジェクトを見つけられない場合は、エラーが発生します。また、コレクションの中には名前付きオブジェクトをサポートしていないものもあります。このようなコレクションでは、序数参照を使う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1ba0-p101">Use the **Item** property to return a specific object in a collection. If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs. Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="a1ba0-118">**Item** プロパティはすべてのコレクションの既定プロパティなので、次のいずれの構文形式でも同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="a1ba0-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
