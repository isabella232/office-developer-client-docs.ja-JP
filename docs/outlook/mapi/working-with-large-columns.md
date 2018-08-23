---
title: 大規模列の操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a191a8551d425d7e8b3b9a281936a4a0e2dfd587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804220"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="f8baa-103">大規模列の操作</span><span class="sxs-lookup"><span data-stu-id="f8baa-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="f8baa-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8baa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8baa-105">文字列またはバイナリ プロパティ データを持つ列が大きくなる可能性のある膨大な数のバイト長です。</span><span class="sxs-lookup"><span data-stu-id="f8baa-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="f8baa-106">ビューで、数百バイトの 1 つまたは複数の列を含む多くの場合実用的ではありません、ために、MAPI には、テーブル実装側は、255 バイトには多くの場合、使用頻度は少ない 510 バイトに値を切り詰めますが有効にします。</span><span class="sxs-lookup"><span data-stu-id="f8baa-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="f8baa-107">可能な限り、テーブルの実装者は、テーブルの列にプロパティの完全な値を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8baa-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="f8baa-108">最初の 255 バイトを含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f8baa-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="f8baa-109">クライアントは、使用しているテーブルに行が切り捨てられますかどうか事前に知ることはできません。</span><span class="sxs-lookup"><span data-stu-id="f8baa-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="f8baa-110">列の長さが 255 であるか、510 バイトである場合、列が切り捨てられたプロパティを表すことを想定してください。</span><span class="sxs-lookup"><span data-stu-id="f8baa-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="f8baa-111">必要に応じて、クライアント直接値を取得完全切り捨てられた列のオブジェクトからオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すことによって。</span><span class="sxs-lookup"><span data-stu-id="f8baa-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="f8baa-112">大きなプロパティの制限を作成するクライアントは、対応することがテーブルの実装方法にこれらの制限を次のように動作します。 はずです。</span><span class="sxs-lookup"><span data-stu-id="f8baa-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="f8baa-113">いくつかのテーブルの実装では、切り捨てられた列全体の値を基に他のユーザー中に切り捨てられたサイズに基づく構築された制限を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8baa-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f8baa-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8baa-114">See also</span></span>



[<span data-ttu-id="f8baa-115">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="f8baa-115">MAPI Tables</span></span>](mapi-tables.md)

