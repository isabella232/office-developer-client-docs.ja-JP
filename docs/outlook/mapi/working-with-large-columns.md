---
title: 大きな列を処理する
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
# <a name="working-with-large-columns"></a><span data-ttu-id="0c176-103">大きな列を処理する</span><span class="sxs-lookup"><span data-stu-id="0c176-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="0c176-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c176-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c176-105">文字列またはバイナリのプロパティデータを持つ列は大規模である可能性があり、多くの場合、長さが何千バイトになることがあります。</span><span class="sxs-lookup"><span data-stu-id="0c176-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="0c176-106">ビュー内の1つまたは複数の列が表示されている場合、多くの場合、MAPI を使用すると、テーブル実装者は値を切り捨てることができます。通常は255バイト、それよりも510バイトになります。</span><span class="sxs-lookup"><span data-stu-id="0c176-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="0c176-107">テーブルの実装では、可能であれば、テーブルの列にプロパティの完全な値を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c176-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="0c176-108">推奨される代替方法は、最初の255バイトのみを含めることです。</span><span class="sxs-lookup"><span data-stu-id="0c176-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="0c176-109">クライアントは、使用しているテーブルが大きな列を切り捨てているかどうかを事前に知ることはできません。</span><span class="sxs-lookup"><span data-stu-id="0c176-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="0c176-110">列の長さが255または510バイトの場合、列が切り捨てられたプロパティを表すと想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c176-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="0c176-111">必要に応じて、オブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出すことにより、切り捨てられた列の完全な値をクライアントが直接取得することができます。</span><span class="sxs-lookup"><span data-stu-id="0c176-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="0c176-112">大規模なプロパティを使用して構築するクライアントは、これらの制限がどのように機能するかについて、テーブルの実装者に依存していることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c176-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="0c176-113">表の実装によっては、切り捨てられたサイズに基づいて、切り捨てられた列を使用して作成された制限を使用している場合や、値全体を基準とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="0c176-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c176-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c176-114">See also</span></span>



[<span data-ttu-id="0c176-115">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="0c176-115">MAPI Tables</span></span>](mapi-tables.md)

