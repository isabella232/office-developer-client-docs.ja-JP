---
title: フィルターによるテーブルの位置設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565593"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="fbff9-103">フィルターによるテーブルの位置設定</span><span class="sxs-lookup"><span data-stu-id="fbff9-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="fbff9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbff9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbff9-105">テーブルのユーザーは、一連のフィルター条件に一致する行にカーソルを移動できます。</span><span class="sxs-lookup"><span data-stu-id="fbff9-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="fbff9-106">フィルターは、さまざまな列プロパティの値やビットマスク、サブオブジェクトなどのガイドラインに基づいていることができます。</span><span class="sxs-lookup"><span data-stu-id="fbff9-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="fbff9-107">[SRestriction](srestriction.md)構造体を使用して MAPI では、フィルターが指定されています。</span><span class="sxs-lookup"><span data-stu-id="fbff9-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="fbff9-108">**制限の中で確立された条件に一致する最初の行に表を配置するには**</span><span class="sxs-lookup"><span data-stu-id="fbff9-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="fbff9-109">[IMAPITable::FindRow](imapitable-findrow.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fbff9-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="fbff9-110">**FindRow**は特定のブックマークで表される行から始めて、前方または後方のいずれかの方向の制限で指定された条件に一致するローを検索します検索します。</span><span class="sxs-lookup"><span data-stu-id="fbff9-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="fbff9-111">**FindRow**は、小数部の値ではなく、文字の文字列に基づくスクロール バーを実装するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fbff9-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="fbff9-112">などの指定された文字で始まる最初の名前を検索するのには、1 つまたは複数の文字を入力することにより、ユーザーを有効にする統合されたアドレス帳から検索する場合、クライアントは**FindRow**の MAPI の実装を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="fbff9-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fbff9-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="fbff9-113">See also</span></span>



[<span data-ttu-id="fbff9-114">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="fbff9-114">MAPI Tables</span></span>](mapi-tables.md)

