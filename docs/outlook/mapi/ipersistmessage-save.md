---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309619"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="ee913-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="ee913-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="ee913-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee913-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee913-105">変更したフォームを、読み込みまたは作成されたメッセージに保存し直します。</span><span class="sxs-lookup"><span data-stu-id="ee913-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="ee913-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ee913-106">Parameters</span></span>

 <span data-ttu-id="ee913-107">_pmessage_</span><span class="sxs-lookup"><span data-stu-id="ee913-107">_pMessage_</span></span>
  
> <span data-ttu-id="ee913-108">順番メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ee913-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="ee913-109">_fsameasload_</span><span class="sxs-lookup"><span data-stu-id="ee913-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="ee913-110">順番_pmessage_が指すメッセージが、フォームが読み込まれた、または作成されたメッセージであることを示す場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="ee913-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee913-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="ee913-111">Return value</span></span>

<span data-ttu-id="ee913-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee913-112">S_OK</span></span> 
  
> <span data-ttu-id="ee913-113">フォームが正常に保存されました。</span><span class="sxs-lookup"><span data-stu-id="ee913-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee913-114">解説</span><span class="sxs-lookup"><span data-stu-id="ee913-114">Remarks</span></span>

<span data-ttu-id="ee913-115">フォームビューアーは、 **IPersistMessage:: save**メソッドを呼び出して、変更されたフォームを読み込みまたは作成されたメッセージに戻します。</span><span class="sxs-lookup"><span data-stu-id="ee913-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="ee913-116">**Save**は、フォームが[通常](normal-state.md)の状態にある場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee913-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ee913-117">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="ee913-117">Notes to implementers</span></span>

<span data-ttu-id="ee913-118">保存された変更をコミットしません。変更をコミットするのは発信者のことです。</span><span class="sxs-lookup"><span data-stu-id="ee913-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="ee913-119">[**保存**] 呼び出し時以外は、フォームのメッセージに属するプロパティを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="ee913-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="ee913-120">_fsameasload_が TRUE に設定されている場合は、フォームの既存のメッセージに対する変更を保存できます。</span><span class="sxs-lookup"><span data-stu-id="ee913-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="ee913-121">_fsameasload_が FALSE に設定されている場合は、保存を実行する前に、元のメッセージのすべてのプロパティを_pmessage_で示されるメッセージにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee913-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="ee913-122">元のメッセージの[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを使用して、プロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="ee913-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="ee913-123">すべてのプロパティがコピーされたら、 [noscribble](noscribble-state.md)状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee913-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="ee913-124">エラーが発生しない場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="ee913-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="ee913-125">それ以外の場合は、失敗したアクションからエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="ee913-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="ee913-126">フォームが通常以外の状態になっているときに**Save**を呼び出すと、E_UNEXPECTED が返されます。</span><span class="sxs-lookup"><span data-stu-id="ee913-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="ee913-127">ストレージオブジェクトの保存の詳細については、 [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)メソッドのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee913-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee913-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee913-128">See also</span></span>



[<span data-ttu-id="ee913-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee913-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="ee913-130">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="ee913-130">Form States</span></span>](form-states.md)

