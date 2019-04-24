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
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287161"
---
# <a name="dtbllabel"></a><span data-ttu-id="9d687-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="9d687-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="9d687-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d687-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d687-105">表示テーブルから作成されたダイアログボックスで使用されるラベルを記述します。</span><span class="sxs-lookup"><span data-stu-id="9d687-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d687-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9d687-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d687-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d687-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9d687-108">関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="9d687-108">Related macro</span></span>  <br/> |[<span data-ttu-id="9d687-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="9d687-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="9d687-110">Members</span><span class="sxs-lookup"><span data-stu-id="9d687-110">Members</span></span>

 <span data-ttu-id="9d687-111">**ulblpszlabelname**</span><span class="sxs-lookup"><span data-stu-id="9d687-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="9d687-112">文字列のラベルをメモリ内に配置します。</span><span class="sxs-lookup"><span data-stu-id="9d687-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="9d687-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9d687-113">**ulFlags**</span></span>
  
> <span data-ttu-id="9d687-114">**ulblpszlabelname**メンバーによって示されるラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9d687-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="9d687-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9d687-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="9d687-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9d687-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9d687-117">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="9d687-117">The label is in Unicode format.</span></span> <span data-ttu-id="9d687-118">MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="9d687-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d687-119">解説</span><span class="sxs-lookup"><span data-stu-id="9d687-119">Remarks</span></span>

<span data-ttu-id="9d687-120">**dtbllabel**構造体は、別の種類のコントロールと共に表示されるラベルコントロールテキストを記述して、そのコントロールに意味を追加します。</span><span class="sxs-lookup"><span data-stu-id="9d687-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="9d687-121">たとえば、ほとんどの編集コントロールはラベルの隣に配置され、入力する情報の種類をユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="9d687-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="9d687-122">グループボックスやラジオボタンなどの一部のコントロールは、独自のラベルを保持します。</span><span class="sxs-lookup"><span data-stu-id="9d687-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="9d687-123">ラベルには、Windows accelerator を含めることができます。アンパサンド (&amp;) の後の文字として識別されます。</span><span class="sxs-lookup"><span data-stu-id="9d687-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="9d687-124">アクセスキーを押すと、表示テーブルでこのラベルの下にある、ラベルのない最初のボタン以外のコントロールにフォーカスが置かれます。</span><span class="sxs-lookup"><span data-stu-id="9d687-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="9d687-125">複数行のラベルはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9d687-125">There is no support for multiline labels.</span></span> <span data-ttu-id="9d687-126">複数の行を表示するには、複数のラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="9d687-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="9d687-127">読み取り専用の編集コントロールとしてラベルを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="9d687-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="9d687-128">違いは、編集コントロールが選択され、ラベルをコピーできないことです。</span><span class="sxs-lookup"><span data-stu-id="9d687-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="9d687-129">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d687-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="9d687-130">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d687-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d687-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d687-131">See also</span></span>



[<span data-ttu-id="9d687-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="9d687-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="9d687-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9d687-133">MAPI Structures</span></span>](mapi-structures.md)

