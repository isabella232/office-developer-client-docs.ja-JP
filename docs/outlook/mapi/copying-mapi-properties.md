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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333076"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="39a74-103">MAPI プロパティのコピー</span><span class="sxs-lookup"><span data-stu-id="39a74-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="39a74-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39a74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39a74-105">クライアントおよびサービスプロバイダーは、次の**imapiprop**メソッドと API 関数を使用して、1つ以上のオブジェクトのプロパティをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="39a74-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="39a74-106">[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドは、必要に応じて、選択したプロパティを除外して、オブジェクトのすべてのプロパティを別のオブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="39a74-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="39a74-107">**CopyTo**は、任意の種類のオブジェクトをコピーまたは移動するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="39a74-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="39a74-108">[imapiprop:: copyprops](imapiprop-copyprops.md)メソッドは、オブジェクトの選択されたプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="39a74-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="39a74-109">**copyprops**は、主にメッセージで使用されます。</span><span class="sxs-lookup"><span data-stu-id="39a74-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="39a74-110">クライアントがメッセージの転送コピーまたは応答を作成すると、 **copyprops**は、元のメッセージから適切なプロパティをコピーする処理を行います。</span><span class="sxs-lookup"><span data-stu-id="39a74-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="39a74-111">[propcopymore](propcopymore.md)関数は、1つのプロパティ値をある場所から別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="39a74-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="39a74-112">**propcopymore**は慎重に使用してください。</span><span class="sxs-lookup"><span data-stu-id="39a74-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="39a74-113">これは、一度に1つの値をコピーするときに、少数のメモリブロックを割り当て、メモリをフラグメント化することができます。</span><span class="sxs-lookup"><span data-stu-id="39a74-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="39a74-114">[sccopyprops](sccopyprops.md)関数は、プロパティの値を一括でコピーします。</span><span class="sxs-lookup"><span data-stu-id="39a74-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="39a74-115">**sccopyprops**では、メモリブロックのないメモリブロックから構築されたプロパティ値をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="39a74-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="39a74-116">このメソッドは、新しいプロパティ配列を返します。</span><span class="sxs-lookup"><span data-stu-id="39a74-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="39a74-117">**sccopyprops**によって返されるプロパティの配列をディスクに格納する場合は、 [ScRelocProps](screlocprops.md)関数を使用してポインターを調整します。</span><span class="sxs-lookup"><span data-stu-id="39a74-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="39a74-118">**ScRelocProps**は2回呼び出す必要があります。データ操作を書き込む前にアドレスを調整した後、読み取り操作中に再びアドレスを調整します。</span><span class="sxs-lookup"><span data-stu-id="39a74-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="39a74-119">**ScRelocProps**関数は、プロパティ値の配列が最初は単一の割り当てで割り当てられていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="39a74-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="39a74-120">前のリストで説明した API 関数は、オブジェクトから別のオブジェクトへのプロパティではなく、メモリ内のプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="39a74-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="39a74-121">これらの関数は現在サポートされていますが、今後のリリースではサポートされない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="39a74-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="39a74-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="39a74-122">See also</span></span>



[<span data-ttu-id="39a74-123">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="39a74-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

