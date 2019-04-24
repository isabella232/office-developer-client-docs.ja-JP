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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338312"
---
# <a name="dtblbutton"></a><span data-ttu-id="875fe-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="875fe-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="875fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="875fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="875fe-105">表示テーブルから作成されたダイアログボックスのボタンコントロールに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="875fe-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="875fe-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="875fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="875fe-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="875fe-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="875fe-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="875fe-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="875fe-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="875fe-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="875fe-110">Members</span><span class="sxs-lookup"><span data-stu-id="875fe-110">Members</span></span>

 <span data-ttu-id="875fe-111">**ulblpszlabel**</span><span class="sxs-lookup"><span data-stu-id="875fe-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="875fe-112">ボタンに表示される文字列のメモリ内での位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="875fe-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="875fe-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="875fe-113">**ulFlags**</span></span>
  
> <span data-ttu-id="875fe-114">**ulblpszlabel**メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="875fe-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="875fe-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="875fe-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="875fe-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="875fe-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="875fe-117">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="875fe-117">The label is in Unicode format.</span></span> <span data-ttu-id="875fe-118">MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="875fe-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="875fe-119">**ulprcontrol**</span><span class="sxs-lookup"><span data-stu-id="875fe-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="875fe-120">[IMAPIControl](imapicontroliunknown.md)インターフェイスを実装する PT_OBJECT 型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="875fe-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="875fe-121">ボタンがクリックされると、MAPI は、表示テーブルの[imapiprop](imapipropiunknown.md)実装に対して[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出し、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="875fe-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="875fe-122">解説</span><span class="sxs-lookup"><span data-stu-id="875fe-122">Remarks</span></span>

<span data-ttu-id="875fe-123">**dtblbutton**構造体は、ボタンをクリックすると、ユーザーが操作を開始できるようにするコントロールを記述します。</span><span class="sxs-lookup"><span data-stu-id="875fe-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="875fe-124">通常、ボタンをクリックすると、モーダルダイアログボックスが表示されるか、プログラムによってタスクが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="875fe-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="875fe-125">サービスプロバイダーは、ボタンコントロールを使用して任意のものを実装できます。</span><span class="sxs-lookup"><span data-stu-id="875fe-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="875fe-126">他のコントロールの値に基づいてタスクを実行するようにボタンが設定されている場合、これらのコントロールでは DT_SET_IMMEDIATE フラグが設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="875fe-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="875fe-127">**ulblpszlabel**メンバーは、ボタンに表示される文字列のメモリ内の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="875fe-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="875fe-128">サービスプロバイダーは、ボタンのラベルで&amp;Windows accelerator を示すために、アンパサンド文字 () を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="875fe-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="875fe-129">アクセラレータキーを押すと、ボタンをクリックした場合と同じ結果になります。</span><span class="sxs-lookup"><span data-stu-id="875fe-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="875fe-130">**ulprcontrol**メンバーは、 **imapiprop:: openproperty**メソッドを使用して開かれたときに、コントロールオブジェクトへのポインターを取得するオブジェクトのプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="875fe-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="875fe-131">**IMAPIControl**インターフェイスをサポートする control オブジェクトを実装することは、MAPI 機能セットを拡張し、ボタンがクリックされたときに実行する操作またはタスクを定義する方法です。</span><span class="sxs-lookup"><span data-stu-id="875fe-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="875fe-132">**IMAPIControl**では、ボタンを有効または無効にするための 2 [](imapicontrol-activate.md)つのメソッドと、ボタンのクリックを処理するための[GetState](imapicontrol-getstate.md)を提供します。</span><span class="sxs-lookup"><span data-stu-id="875fe-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="875fe-133">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="875fe-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="875fe-134">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="875fe-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="875fe-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="875fe-135">See also</span></span>



[<span data-ttu-id="875fe-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="875fe-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="875fe-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="875fe-137">MAPI Structures</span></span>](mapi-structures.md)

