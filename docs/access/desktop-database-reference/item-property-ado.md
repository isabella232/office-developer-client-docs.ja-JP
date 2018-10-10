---
title: Item プロパティ (ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476483"
---
# <a name="item-property-ado"></a><span data-ttu-id="08e12-102">Item プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="08e12-102">Item Property (ADO)</span></span>

<span data-ttu-id="08e12-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="08e12-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="08e12-104">コレクションの特定のメンバーをその名前または序数で示します。</span><span class="sxs-lookup"><span data-stu-id="08e12-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e12-105">構文</span><span class="sxs-lookup"><span data-stu-id="08e12-105">Syntax</span></span>

<span data-ttu-id="08e12-106">*オブジェクト*を設定する = *コレクション*です。項目 (インデックス)</span><span class="sxs-lookup"><span data-stu-id="08e12-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="08e12-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="08e12-107">Return Value</span></span>

<span data-ttu-id="08e12-108">オブジェクトへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="08e12-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="08e12-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="08e12-109">Parameters</span></span>

- <span data-ttu-id="08e12-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="08e12-110">*Index*</span></span>

- <span data-ttu-id="08e12-111">コレクション内のオブジェクトの名前または序数に評価されるバリアント型 ( **Variant** ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="08e12-111">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="08e12-112">解説</span><span class="sxs-lookup"><span data-stu-id="08e12-112">Remarks</span></span>

<span data-ttu-id="08e12-113">コレクションから特定のオブジェクトを取得するのにには、 **Item**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="08e12-113">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="08e12-114">**項目**は、 *Index*引数に対応するコレクション内でオブジェクトを検索することはできません、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="08e12-114">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="08e12-115">また、いくつかのコレクションをサポートしていない名前付きオブジェクトです。これらのコレクションでは、序数参照を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08e12-115">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="08e12-116">**Item** プロパティはすべてのコレクションの既定プロパティなので、次のいずれの構文形式でも同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="08e12-116">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
