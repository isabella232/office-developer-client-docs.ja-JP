---
title: 大きな列の操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420424"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="9df2e-103">大きな列の操作</span><span class="sxs-lookup"><span data-stu-id="9df2e-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="9df2e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9df2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9df2e-105">文字列またはバイナリ プロパティ データを持つ列は、大きく、数千バイトの長さになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9df2e-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="9df2e-106">ビューに数百バイトを含む 1 つ以上の列を含めることはできませんが、多くの場合、MAPI を使用すると、テーブルの実装者は値を切り捨て、ほとんどの場合は 255 バイト、頻度は 510 バイトに切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="9df2e-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="9df2e-107">可能な限り、テーブルの実装者は、プロパティの完全な値をテーブル列に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="9df2e-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="9df2e-108">推奨される代替手段は、最初の 255 バイトのみを含める方法です。</span><span class="sxs-lookup"><span data-stu-id="9df2e-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="9df2e-109">クライアントは、使用しているテーブルが大きな列を切り捨てるかどうかを事前に知る必要があります。</span><span class="sxs-lookup"><span data-stu-id="9df2e-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="9df2e-110">列の長さが 255 バイトまたは 510 バイトの場合、列は切り捨てられたプロパティを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9df2e-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="9df2e-111">必要に応じて、クライアントはオブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出すことによって、オブジェクトから切り捨てられた列の完全な値を直接取得できます。</span><span class="sxs-lookup"><span data-stu-id="9df2e-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="9df2e-112">大規模なプロパティを使用して制限を構築するクライアントは、これらの制限がどのように動作するのかについては、テーブル実装者が行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9df2e-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="9df2e-113">一部のテーブル実装者は、切り捨てられた列で構築される制限を切り捨てられたサイズに基づいて設定し、他の実装者は値全体に基づいて制限を設定できます。</span><span class="sxs-lookup"><span data-stu-id="9df2e-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9df2e-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="9df2e-114">See also</span></span>



[<span data-ttu-id="9df2e-115">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="9df2e-115">MAPI Tables</span></span>](mapi-tables.md)

