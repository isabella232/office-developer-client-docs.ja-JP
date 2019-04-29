---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420746"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="8e065-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="8e065-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="8e065-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e065-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e065-105">表示テーブルから構築されたダイアログボックスで使用されるドロップダウンリストを表します。</span><span class="sxs-lookup"><span data-stu-id="8e065-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e065-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8e065-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e065-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e065-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="8e065-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="8e065-108">Members</span></span>

 <span data-ttu-id="8e065-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="8e065-109">**ulFlags**</span></span>
  
> <span data-ttu-id="8e065-110">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e065-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8e065-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="8e065-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="8e065-112">PT_MV_TSTRING 型の複数値プロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="8e065-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="8e065-113">このプロパティの異なる値は、ドロップダウンリストに個別のエントリとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e065-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e065-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8e065-114">Remarks</span></span>

<span data-ttu-id="8e065-115">**DTBLMVDDLBOX**構造体は、複数値を持つドロップダウンリストに、アイテムの読み取り専用リストを記述します。</span><span class="sxs-lookup"><span data-stu-id="8e065-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="8e065-116">複数値を持つドロップダウンリストを使用すると、ユーザーがスクロールバーをクリックしたときに値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e065-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="8e065-117">表示されるデータは、 **ulMVPropTag**メンバーで識別されるプロパティから取得されます。</span><span class="sxs-lookup"><span data-stu-id="8e065-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="8e065-118">表示テーブルに関連付けられているプロパティインターフェイスを読み取るための要件はありません。</span><span class="sxs-lookup"><span data-stu-id="8e065-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="8e065-119">また、ユーザーはこれらの種類のリストボックスから選択することができないため、データはプロパティインターフェイスに書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="8e065-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="8e065-120">複数値のドロップダウンリストでは、複数値の文字列プロパティのみがサポートされています。その他の複数値プロパティの型はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8e065-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="8e065-121">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e065-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="8e065-122">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e065-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e065-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e065-123">See also</span></span>



[<span data-ttu-id="8e065-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="8e065-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="8e065-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="8e065-125">MAPI Structures</span></span>](mapi-structures.md)

