---
title: Unicode 列の操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ffeee38920bf1c864b93e6513913c140cb658d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595308"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="b41ef-103">Unicode 列の操作</span><span class="sxs-lookup"><span data-stu-id="b41ef-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="b41ef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b41ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b41ef-105">PT_STRING8 プロパティの型であり、標準の 8 ビット文字または 16 ビット Unicode 文字は、PT_UNICODE プロパティの型は、使用して、テーブル内の文字列を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="b41ef-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="b41ef-106">テーブルの実装側は、自由に、それぞれのテーブルが Unicode 文字列をサポートするかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="b41ef-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="b41ef-107">Unicode では、機能セットを拡張することによって、クライアントとサービス ・ プロバイダーの両方の値を追加、ためには、Unicode をサポート可能な限りことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b41ef-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="b41ef-108">テーブルの多くのメソッドは、Unicode を使用する、文字列プロパティの値が期待どおりかどうかを決定するフラグを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="b41ef-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="b41ef-109">入力で MAPI_UNICODE フラグを指定することを示しますテーブル実装する呼び出しで渡されるすべての文字列プロパティの値が Unicode 文字列であり、PT_UNICODE のプロパティの種類があること。</span><span class="sxs-lookup"><span data-stu-id="b41ef-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="b41ef-110">出力では、このフラグは、返される文字列のすべてのプロパティ値に Unicode 文字列では、可能な場合を示します。</span><span class="sxs-lookup"><span data-stu-id="b41ef-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="b41ef-111">フラグが入力または出力の意味を持つかどうかは、このメソッドによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b41ef-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="b41ef-112">Unicode をサポートしていませんし、MAPI_UNICODE フラグが渡されるテーブルの実装では、MAPI_E_BAD_CHAR_WIDTH の値を返します。</span><span class="sxs-lookup"><span data-stu-id="b41ef-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b41ef-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="b41ef-113">See also</span></span>



[<span data-ttu-id="b41ef-114">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="b41ef-114">MAPI Tables</span></span>](mapi-tables.md)

