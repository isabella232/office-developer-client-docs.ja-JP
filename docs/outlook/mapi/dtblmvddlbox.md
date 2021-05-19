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
# <a name="dtblmvddlbox"></a><span data-ttu-id="b242b-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="b242b-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="b242b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b242b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b242b-105">表示テーブルから作成されたダイアログ ボックスで使用されるドロップダウン リストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b242b-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b242b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b242b-106">Header file:</span></span>  <br/> |<span data-ttu-id="b242b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b242b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="b242b-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="b242b-108">Members</span></span>

 <span data-ttu-id="b242b-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b242b-109">**ulFlags**</span></span>
  
> <span data-ttu-id="b242b-110">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b242b-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b242b-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="b242b-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="b242b-112">型の複数値プロパティのプロパティ タグPT_MV_TSTRING。</span><span class="sxs-lookup"><span data-stu-id="b242b-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="b242b-113">このプロパティの異なる値は、ドロップダウン リストに個別のエントリとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="b242b-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b242b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b242b-114">Remarks</span></span>

<span data-ttu-id="b242b-115">**DTBLMVDDLBOX** 構造体は、複数値のドロップダウン リストを項目の読み取り専用リストとして記述します。</span><span class="sxs-lookup"><span data-stu-id="b242b-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="b242b-116">複数値のドロップダウン リストを使用すると、ユーザーがスクロール バーをクリックすると値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b242b-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="b242b-117">表示されるデータは **、ulMVPropTag** メンバーで識別されるプロパティから取得されます。</span><span class="sxs-lookup"><span data-stu-id="b242b-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="b242b-118">表示テーブルに関連付けられているプロパティ インターフェイスから読み取る必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b242b-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="b242b-119">また、ユーザーはこのような種類のリスト ボックスから選択を行えないので、データはプロパティ インターフェイスに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="b242b-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="b242b-120">複数値のドロップダウン リストでは、複数値の文字列プロパティだけがサポートされます。他の複数値プロパティの種類はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b242b-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="b242b-121">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="b242b-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="b242b-122">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="b242b-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b242b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b242b-123">See also</span></span>



[<span data-ttu-id="b242b-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="b242b-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="b242b-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b242b-125">MAPI Structures</span></span>](mapi-structures.md)

