---
title: MAPI プロパティのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415048"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="66d44-103">MAPI プロパティのコピー</span><span class="sxs-lookup"><span data-stu-id="66d44-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="66d44-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66d44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66d44-105">クライアントとサービス プロバイダーは、次の **IMAPIProp** メソッドと API 関数を使用して、1 つ以上のオブジェクトのプロパティをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="66d44-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="66d44-106">[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドは、オブジェクトのすべてのプロパティを別のオブジェクトにコピーします。必要に応じて、選択したプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="66d44-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="66d44-107">**CopyTo** は、任意の種類のオブジェクトをコピーまたは移動するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="66d44-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="66d44-108">[IMAPIProp::CopyProps](imapiprop-copyprops.md)メソッドは、オブジェクトの選択したプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="66d44-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="66d44-109">**CopyProps は** 主にメッセージと一緒に使用されます。</span><span class="sxs-lookup"><span data-stu-id="66d44-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="66d44-110">クライアントがメッセージまたは返信の転送されたコピーを作成すると **、CopyProps は** 元のメッセージから適切なプロパティのコピーを処理します。</span><span class="sxs-lookup"><span data-stu-id="66d44-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="66d44-111">[PropCopyMore](propcopymore.md)関数は、1 つのプロパティ値を 1 つの場所から別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="66d44-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="66d44-112">**PropCopyMore を使用する場合は** 注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="66d44-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="66d44-113">一度に 1 つの値をコピーするときに、メモリの小さいブロックを多数割り当て、メモリをフラグメント化することができます。</span><span class="sxs-lookup"><span data-stu-id="66d44-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="66d44-114">[ScCopyProps 関数は](sccopyprops.md)、プロパティ値を一括でコピーします。</span><span class="sxs-lookup"><span data-stu-id="66d44-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="66d44-115">**ScCopyProps は** 、不一部のメモリ ブロックから構築されたプロパティ値をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="66d44-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="66d44-116">新しいプロパティ配列を返します。</span><span class="sxs-lookup"><span data-stu-id="66d44-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="66d44-117">**ScCopyProps** によって返されるプロパティ配列をディスクに格納する場合は [、ScRelocProps](screlocprops.md)関数を使用してポインターを調整します。</span><span class="sxs-lookup"><span data-stu-id="66d44-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="66d44-118">**ScRelocProps は** 2 回呼び出す必要があります。データ操作を書き込む前にアドレスを調整してから、読み取り操作中にもう一度アドレスを調整します。</span><span class="sxs-lookup"><span data-stu-id="66d44-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="66d44-119">**ScRelocProps 関数** は、プロパティ値配列が最初に 1 つの割り当てで割り当てられたと仮定します。</span><span class="sxs-lookup"><span data-stu-id="66d44-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="66d44-120">前述のリスト で説明した API 関数は、オブジェクト間ではなくメモリ内のプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="66d44-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="66d44-121">これらの関数は現在サポートされますが、今後のリリースではサポートされない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="66d44-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66d44-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="66d44-122">See also</span></span>



[<span data-ttu-id="66d44-123">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="66d44-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

