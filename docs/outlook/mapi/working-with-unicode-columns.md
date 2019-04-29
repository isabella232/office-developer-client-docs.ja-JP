---
title: Unicode 列の使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408384"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="8c220-103">Unicode 列の使用</span><span class="sxs-lookup"><span data-stu-id="8c220-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="8c220-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c220-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c220-105">表の文字列は、プロパティの種類が PT_STRING8 の標準の8ビット文字、またはプロパティの種類が PT_UNICODE である16ビットの Unicode 文字を使用して表すことができます。</span><span class="sxs-lookup"><span data-stu-id="8c220-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="8c220-106">表の実装者は、テーブルが Unicode 文字列をサポートしているかどうかを自由に選択できます。</span><span class="sxs-lookup"><span data-stu-id="8c220-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="8c220-107">unicode は、機能セットを拡張することによって、クライアントとサービスプロバイダーの両方の値を追加するため、可能な限り unicode をサポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8c220-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="8c220-108">多くの table メソッドは、文字列プロパティの値が Unicode であることを想定しているかどうかを指定するフラグを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="8c220-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="8c220-109">入力時に、MAPI_UNICODE フラグを指定すると、呼び出しに渡されたすべての文字列プロパティの値が UNICODE 文字列であり、プロパティの種類が PT_UNICODE であることをテーブルの実装に示します。</span><span class="sxs-lookup"><span data-stu-id="8c220-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="8c220-110">出力時、このフラグは、返されるすべての文字列プロパティ値が Unicode 文字列であることを示します (可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="8c220-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="8c220-111">フラグが入力または出力に対して意味を持つかどうかは、メソッドによって決まります。</span><span class="sxs-lookup"><span data-stu-id="8c220-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="8c220-112">Unicode をサポートしておらず、MAPI_UNICODE フラグが渡されるテーブル実装では、MAPI_E_BAD_CHAR_WIDTH 値を返します。</span><span class="sxs-lookup"><span data-stu-id="8c220-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c220-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c220-113">See also</span></span>



[<span data-ttu-id="8c220-114">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="8c220-114">MAPI Tables</span></span>](mapi-tables.md)

