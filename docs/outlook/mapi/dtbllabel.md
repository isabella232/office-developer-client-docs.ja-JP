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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410687"
---
# <a name="dtbllabel"></a><span data-ttu-id="0da75-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="0da75-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="0da75-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0da75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0da75-105">表示テーブルから作成されたダイアログ ボックスで使用されるラベルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0da75-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0da75-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0da75-106">Header file:</span></span>  <br/> |<span data-ttu-id="0da75-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0da75-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0da75-108">関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="0da75-108">Related macro</span></span>  <br/> |[<span data-ttu-id="0da75-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="0da75-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="0da75-110">Members</span><span class="sxs-lookup"><span data-stu-id="0da75-110">Members</span></span>

 <span data-ttu-id="0da75-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="0da75-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="0da75-112">文字列ラベルのメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="0da75-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="0da75-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="0da75-113">**ulFlags**</span></span>
  
> <span data-ttu-id="0da75-114">**ulbLpszLabelName** メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0da75-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="0da75-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0da75-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="0da75-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0da75-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0da75-117">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="0da75-117">The label is in Unicode format.</span></span> <span data-ttu-id="0da75-118">このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="0da75-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0da75-119">注釈</span><span class="sxs-lookup"><span data-stu-id="0da75-119">Remarks</span></span>

<span data-ttu-id="0da75-120">**DTBLLABEL 構造体** は、別の種類のコントロールと一緒に表示されるラベル コントロール テキストを表し、そのコントロールに意味を追加します。</span><span class="sxs-lookup"><span data-stu-id="0da75-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="0da75-121">たとえば、ほとんどの編集コントロールはラベルの横に配置され、入力する情報の種類をユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="0da75-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="0da75-122">グループ ボックスやラジオ ボタンなどの一部のコントロールは、独自のラベルを保持します。</span><span class="sxs-lookup"><span data-stu-id="0da75-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="0da75-123">ラベルには、アンパサンド () Windows文字として識別されるアクセラレータを含めできます &amp; 。</span><span class="sxs-lookup"><span data-stu-id="0da75-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="0da75-124">アクセラレータ キーを押すと、表示テーブルのこのラベルに続く最初の非ラベルの非ボタン コントロールにフォーカスが配置されます。</span><span class="sxs-lookup"><span data-stu-id="0da75-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="0da75-125">複数行ラベルはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0da75-125">There is no support for multiline labels.</span></span> <span data-ttu-id="0da75-126">複数の行を表示するには、複数のラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="0da75-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="0da75-127">ラベルを読み取り専用の編集コントロールとして使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="0da75-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="0da75-128">違いは、編集コントロールを選択してコピーできるのに対し、ラベルは選択できないことです。</span><span class="sxs-lookup"><span data-stu-id="0da75-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="0da75-129">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="0da75-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="0da75-130">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="0da75-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0da75-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="0da75-131">See also</span></span>



[<span data-ttu-id="0da75-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="0da75-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="0da75-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0da75-133">MAPI Structures</span></span>](mapi-structures.md)

