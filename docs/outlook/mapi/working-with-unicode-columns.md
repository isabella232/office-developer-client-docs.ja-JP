---
title: Unicode 列の操作
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
# <a name="working-with-unicode-columns"></a><span data-ttu-id="cf161-103">Unicode 列の操作</span><span class="sxs-lookup"><span data-stu-id="cf161-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="cf161-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf161-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf161-105">テーブル内の文字列は、プロパティ型 PT_STRING8 または 16 ビット Unicode 文字 (プロパティ型 PT_UNICODE) である標準の 8 ビット文字を使用して表されます。</span><span class="sxs-lookup"><span data-stu-id="cf161-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="cf161-106">テーブル実装者は、テーブルが Unicode 文字列をサポートするかどうかを自由に選択できます。</span><span class="sxs-lookup"><span data-stu-id="cf161-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="cf161-107">Unicode は機能セットを拡張してクライアントとサービス プロバイダーの両方に値を追加しますので、可能な限り Unicode をサポートする方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cf161-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="cf161-108">多くのテーブル メソッドは、文字列プロパティの値が Unicode と予想されるかどうかを示すフラグを受け入れています。</span><span class="sxs-lookup"><span data-stu-id="cf161-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="cf161-109">入力時に、MAPI_UNICODE フラグを指定すると、呼び出しで渡される文字列プロパティの値はすべて Unicode 文字列であり、プロパティの種類は PT_UNICODE です。</span><span class="sxs-lookup"><span data-stu-id="cf161-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="cf161-110">出力時に、このフラグは、返される文字列プロパティの値はすべて、可能であれば Unicode 文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf161-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="cf161-111">フラグが入力または出力の意味を持つかどうかは、メソッドによって異なります。</span><span class="sxs-lookup"><span data-stu-id="cf161-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="cf161-112">Unicode をサポートしていないテーブル実装者は、MAPI_UNICODE値をMAPI_E_BAD_CHAR_WIDTHします。</span><span class="sxs-lookup"><span data-stu-id="cf161-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf161-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf161-113">See also</span></span>



[<span data-ttu-id="cf161-114">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="cf161-114">MAPI Tables</span></span>](mapi-tables.md)

