---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338277"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="06e71-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="06e71-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="06e71-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06e71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06e71-105">表示テーブルから構築されたダイアログボックスに表示される複数値リストを記述します。</span><span class="sxs-lookup"><span data-stu-id="06e71-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06e71-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="06e71-106">Header file:</span></span>  <br/> |<span data-ttu-id="06e71-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06e71-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="06e71-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="06e71-108">Members</span></span>

 <span data-ttu-id="06e71-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="06e71-109">**ulFlags**</span></span>
  
> <span data-ttu-id="06e71-110">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="06e71-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="06e71-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="06e71-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="06e71-112">PT_MV_TSTRING 型の複数値プロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="06e71-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06e71-113">解説</span><span class="sxs-lookup"><span data-stu-id="06e71-113">Remarks</span></span>

<span data-ttu-id="06e71-114">**DTBLMVLISTBOX**構造体には、アイテムの読み取り専用リストを持つ標準的な複数値リストが記述されています。</span><span class="sxs-lookup"><span data-stu-id="06e71-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="06e71-115">標準の複数値を持つリストを使用すると、値がすぐに表示されます。</span><span class="sxs-lookup"><span data-stu-id="06e71-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="06e71-116">表示されるデータは、 **ulMVPropTag**メンバーで識別されるプロパティから取得されます。</span><span class="sxs-lookup"><span data-stu-id="06e71-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="06e71-117">表示テーブルに関連付けられているプロパティインターフェイスを読み取るための要件はありません。</span><span class="sxs-lookup"><span data-stu-id="06e71-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="06e71-118">また、ユーザーはこれらの種類のリストから選択することができないため、データはプロパティインターフェイスに書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="06e71-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="06e71-119">複数値のリストでは、複数値の文字列プロパティのみがサポートされています。その他の複数値プロパティの型はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="06e71-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="06e71-120">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06e71-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="06e71-121">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06e71-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06e71-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="06e71-122">See also</span></span>



[<span data-ttu-id="06e71-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="06e71-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="06e71-124">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="06e71-124">MAPI Structures</span></span>](mapi-structures.md)

