---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 28f6471f74fb0fcc4f7e2f4114f0790e1564e17e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799987"
---
# <a name="dtbllabel"></a><span data-ttu-id="490b9-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="490b9-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="490b9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="490b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="490b9-105">ディスプレイ テーブルから組み込まれているダイアログ ボックスで使用するラベルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="490b9-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="490b9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="490b9-106">Header file:</span></span>  <br/> |<span data-ttu-id="490b9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="490b9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="490b9-108">関連マクロ</span><span class="sxs-lookup"><span data-stu-id="490b9-108">Related macro</span></span>  <br/> |[<span data-ttu-id="490b9-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="490b9-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="490b9-110">Members</span><span class="sxs-lookup"><span data-stu-id="490b9-110">Members</span></span>

 <span data-ttu-id="490b9-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="490b9-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="490b9-112">文字の文字列のラベルのメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="490b9-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="490b9-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="490b9-113">**ulFlags**</span></span>
  
> <span data-ttu-id="490b9-114">**UlbLpszLabelName**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="490b9-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="490b9-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="490b9-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="490b9-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="490b9-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="490b9-117">ラベルは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="490b9-117">The label is in Unicode format.</span></span> <span data-ttu-id="490b9-118">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。</span><span class="sxs-lookup"><span data-stu-id="490b9-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="490b9-119">注釈</span><span class="sxs-lookup"><span data-stu-id="490b9-119">Remarks</span></span>

<span data-ttu-id="490b9-120">**DTBLLABEL**構造体では、別の種類の意味をそのコントロールに追加するコントロールに表示されるラベル コントロールのテキストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="490b9-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="490b9-121">たとえば、入力する情報の種類のユーザーに通知するラベルの横にあるほとんどのエディット コントロールが配置されます。</span><span class="sxs-lookup"><span data-stu-id="490b9-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="490b9-122">グループ ボックスやラジオ ボタンなど、いくつかのコントロールは、独自のラベルを保持します。</span><span class="sxs-lookup"><span data-stu-id="490b9-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="490b9-123">ラベルは、アンパサンドの直後の文字として識別される、ウィンドウのアクセラレータを含めることができます (&amp;)。</span><span class="sxs-lookup"><span data-stu-id="490b9-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="490b9-124">アクセラレータ キーを押すと最初の nonlabel では、次の次のラベルが表示された表のボタン以外のコントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="490b9-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="490b9-125">複数行のラベルのサポートはありません。</span><span class="sxs-lookup"><span data-stu-id="490b9-125">There is no support for multiline labels.</span></span> <span data-ttu-id="490b9-126">複数の明細行を表示するには、複数のラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="490b9-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="490b9-127">読み取り専用のエディット コントロールとラベルを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="490b9-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="490b9-128">違いは、エディット コントロールを選択し、ラベルのことはできませんが、コピーされることです。</span><span class="sxs-lookup"><span data-stu-id="490b9-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="490b9-129">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="490b9-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="490b9-130">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="490b9-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="490b9-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="490b9-131">See also</span></span>



[<span data-ttu-id="490b9-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="490b9-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="490b9-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="490b9-133">MAPI Structures</span></span>](mapi-structures.md)

