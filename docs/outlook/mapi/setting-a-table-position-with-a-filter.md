---
title: フィルターによるテーブルの位置設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316045"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="23957-103">フィルターによるテーブルの位置設定</span><span class="sxs-lookup"><span data-stu-id="23957-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="23957-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23957-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23957-105">Table ユーザーは、フィルタ条件のセットに一致する行にカーソルを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="23957-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="23957-106">フィルターは、列のプロパティ値、ビットマスク、サブオブジェクトなど、さまざまなガイドラインに基づいて行うことができます。</span><span class="sxs-lookup"><span data-stu-id="23957-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="23957-107">フィルターは、 [srestriction](srestriction.md)構造を使用して MAPI で指定されます。</span><span class="sxs-lookup"><span data-stu-id="23957-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="23957-108">**制限で設定された条件に一致する最初の行にテーブルを配置するには**</span><span class="sxs-lookup"><span data-stu-id="23957-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="23957-109">[IMAPITable:: FindRow](imapitable-findrow.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="23957-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="23957-110">**FindRow**は、特定のブックマークで表される行から順に検索し、制限で指定された条件に一致する行を検索します。</span><span class="sxs-lookup"><span data-stu-id="23957-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="23957-111">**FindRow**は、小数点以下の値ではなく、文字列に基づくスクロールバーを実装するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="23957-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="23957-112">たとえば、クライアントは、統合されたアドレス帳を検索するときに、MAPI の**FindRow**の実装を呼び出すことができます。これにより、ユーザーは1つ以上の文字を入力して、指定した文字で始まる最初の名前を検索できます。</span><span class="sxs-lookup"><span data-stu-id="23957-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="23957-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="23957-113">See also</span></span>



[<span data-ttu-id="23957-114">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="23957-114">MAPI Tables</span></span>](mapi-tables.md)

