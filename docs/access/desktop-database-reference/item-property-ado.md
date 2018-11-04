---
title: Item プロパティ (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4afbb31fb95aeea66d9cf93624b95c8796e2d25
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949363"
---
# <a name="item-property-ado"></a><span data-ttu-id="90ca7-102">Item プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="90ca7-102">Item property (ADO)</span></span>

<span data-ttu-id="90ca7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="90ca7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90ca7-104">コレクションの特定のメンバーをその名前または序数で示します。</span><span class="sxs-lookup"><span data-stu-id="90ca7-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ca7-105">構文</span><span class="sxs-lookup"><span data-stu-id="90ca7-105">Syntax</span></span>

<span data-ttu-id="90ca7-106">*オブジェクト*を設定する = *コレクション*です。項目 (インデックス)</span><span class="sxs-lookup"><span data-stu-id="90ca7-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="90ca7-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="90ca7-107">Return value</span></span>

<span data-ttu-id="90ca7-108">オブジェクトへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="90ca7-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="90ca7-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90ca7-109">Parameters</span></span>

|<span data-ttu-id="90ca7-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90ca7-110">Parameter</span></span>|<span data-ttu-id="90ca7-111">説明</span><span class="sxs-lookup"><span data-stu-id="90ca7-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="90ca7-112">*Index*</span><span class="sxs-lookup"><span data-stu-id="90ca7-112">*Index*</span></span> |<span data-ttu-id="90ca7-113">コレクション内のオブジェクトの名前または序数に評価されるバリアント型 ( **Variant** ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="90ca7-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="90ca7-114">解説</span><span class="sxs-lookup"><span data-stu-id="90ca7-114">Remarks</span></span>

<span data-ttu-id="90ca7-115">コレクションから特定のオブジェクトを取得するのにには、 **Item**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="90ca7-115">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="90ca7-116">**項目**は、 *Index*引数に対応するコレクション内でオブジェクトを検索することはできません、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="90ca7-116">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="90ca7-117">また、いくつかのコレクションをサポートしていない名前付きオブジェクトです。これらのコレクションでは、序数参照を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90ca7-117">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="90ca7-118">**Item** プロパティはすべてのコレクションの既定プロパティなので、次のいずれの構文形式でも同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="90ca7-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
