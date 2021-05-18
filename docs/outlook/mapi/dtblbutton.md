---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412787"
---
# <a name="dtblbutton"></a><span data-ttu-id="3568a-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="3568a-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="3568a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3568a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3568a-105">表示テーブルから作成されたダイアログ ボックスのボタン コントロールに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="3568a-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3568a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3568a-106">Header file:</span></span>  <br/> |<span data-ttu-id="3568a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3568a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3568a-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="3568a-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="3568a-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="3568a-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="3568a-110">Members</span><span class="sxs-lookup"><span data-stu-id="3568a-110">Members</span></span>

 <span data-ttu-id="3568a-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="3568a-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="3568a-112">ボタンに表示される文字列のメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="3568a-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="3568a-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3568a-113">**ulFlags**</span></span>
  
> <span data-ttu-id="3568a-114">**ulbLpszLabel** メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="3568a-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="3568a-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3568a-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="3568a-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3568a-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3568a-117">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="3568a-117">The label is in Unicode format.</span></span> <span data-ttu-id="3568a-118">このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="3568a-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="3568a-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="3568a-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="3568a-120">[IMAPIControl](imapicontroliunknown.md)インターフェイスを実装するPT_OBJECTのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="3568a-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="3568a-121">ボタンをクリックすると、MAPI は表示テーブルの IMAPIProp 実装の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して、このプロパティを取得します。 [](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="3568a-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3568a-122">注釈</span><span class="sxs-lookup"><span data-stu-id="3568a-122">Remarks</span></span>

<span data-ttu-id="3568a-123">**DTBLBUTTON 構造体は**、ボタンをクリックすると、ユーザーが操作を開始できるコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="3568a-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="3568a-124">通常、ボタンをクリックすると、モーダル ダイアログ ボックスが表示される、またはプログラムによるタスクが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3568a-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="3568a-125">サービス プロバイダーは、ボタン コントロールを通じて何でも実装できます。</span><span class="sxs-lookup"><span data-stu-id="3568a-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="3568a-126">ボタンが他のコントロールの値に基づいてタスクを実行する必要がある場合は、これらのコントロールでタスク フラグDT_SET_IMMEDIATEがあります。</span><span class="sxs-lookup"><span data-stu-id="3568a-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="3568a-127">**ulbLpszLabel** メンバーは、ボタンに表示される文字列のメモリ内の位置です。</span><span class="sxs-lookup"><span data-stu-id="3568a-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="3568a-128">サービス プロバイダーは、アンパサンド文字 ( ) を追加して、ボタン ラベルにWindows &amp; アクセラレータを示します。</span><span class="sxs-lookup"><span data-stu-id="3568a-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="3568a-129">アクセラレータ キーを押すと、ボタンをクリックした場合と同じ効果が得られます。</span><span class="sxs-lookup"><span data-stu-id="3568a-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="3568a-130">**ulPRControl** メンバーは **、IMAPIProp::OpenProperty** メソッドで開いた場合に、コントロール オブジェクトへのポインターを返すオブジェクト プロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="3568a-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="3568a-131">**IMAPIControl** インターフェイスをサポートするコントロール オブジェクトを実装すると、MAPI 機能セットを拡張し、ボタンをクリックするときに発生する操作またはタスクを定義できます。</span><span class="sxs-lookup"><span data-stu-id="3568a-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="3568a-132">**IMAPIControl には** 、ボタンを操作するための 2 つのメソッドが提供されています。ボタンを無効または有効にする [GetState](imapicontrol-getstate.md) と、ボタンのクリックを処理するための [アクティブ](imapicontrol-activate.md) 化。</span><span class="sxs-lookup"><span data-stu-id="3568a-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="3568a-133">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="3568a-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="3568a-134">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="3568a-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3568a-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="3568a-135">See also</span></span>



[<span data-ttu-id="3568a-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="3568a-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="3568a-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="3568a-137">MAPI Structures</span></span>](mapi-structures.md)

