---
title: Item プロパティ (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73e6240b92a34a6ff1d215cd3211a844f10fe766
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868310"
---
# <a name="item-property-ado"></a><span data-ttu-id="5d479-102">Item プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="5d479-102">Item property (ADO)</span></span>

<span data-ttu-id="5d479-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5d479-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d479-104">コレクションの特定のメンバーをその名前または序数で示します。</span><span class="sxs-lookup"><span data-stu-id="5d479-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d479-105">構文</span><span class="sxs-lookup"><span data-stu-id="5d479-105">Syntax</span></span>

<span data-ttu-id="5d479-106">*オブジェクト*を設定する = *コレクション*です。項目 (インデックス)</span><span class="sxs-lookup"><span data-stu-id="5d479-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="5d479-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="5d479-107">Return value</span></span>

<span data-ttu-id="5d479-108">オブジェクトへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="5d479-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d479-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5d479-109">Parameters</span></span>

- <span data-ttu-id="5d479-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="5d479-110">*Index*</span></span>

- <span data-ttu-id="5d479-111">コレクション内のオブジェクトの名前または序数に評価されるバリアント型 ( **Variant** ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d479-111">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d479-112">解説</span><span class="sxs-lookup"><span data-stu-id="5d479-112">Remarks</span></span>

<span data-ttu-id="5d479-113">コレクションから特定のオブジェクトを取得するのにには、 **Item**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d479-113">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="5d479-114">**項目**は、 *Index*引数に対応するコレクション内でオブジェクトを検索することはできません、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5d479-114">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="5d479-115">また、いくつかのコレクションをサポートしていない名前付きオブジェクトです。これらのコレクションでは、序数参照を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d479-115">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="5d479-116">**Item** プロパティはすべてのコレクションの既定プロパティなので、次のいずれの構文形式でも同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="5d479-116">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
