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
# <a name="ipersistmessagesave"></a><span data-ttu-id="440f1-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="440f1-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="440f1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="440f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="440f1-105">変更されたフォームを、読み込まれたメッセージまたは作成されたメッセージに保存します。</span><span class="sxs-lookup"><span data-stu-id="440f1-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="440f1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="440f1-106">Parameters</span></span>

 <span data-ttu-id="440f1-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="440f1-107">_pMessage_</span></span>
  
> <span data-ttu-id="440f1-108">[in]メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="440f1-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="440f1-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="440f1-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="440f1-110">[in]TRUE を指定すると  _、pMessage_ が示すメッセージが、フォームの読み込みまたは作成のメッセージになります。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="440f1-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="440f1-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="440f1-111">Return value</span></span>

<span data-ttu-id="440f1-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="440f1-112">S_OK</span></span> 
  
> <span data-ttu-id="440f1-113">フォームが正常に保存されました。</span><span class="sxs-lookup"><span data-stu-id="440f1-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="440f1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="440f1-114">Remarks</span></span>

<span data-ttu-id="440f1-115">フォーム ビューアーは **、IPersistMessage::Save** メソッドを呼び出して、変更されたフォームを読み込まれたメッセージまたは作成されたメッセージに戻します。</span><span class="sxs-lookup"><span data-stu-id="440f1-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="440f1-116">**保存** は、フォームが標準状態の場合にのみ [呼び出す必要](normal-state.md) があります。</span><span class="sxs-lookup"><span data-stu-id="440f1-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="440f1-117">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="440f1-117">Notes to implementers</span></span>

<span data-ttu-id="440f1-118">保存された変更をコミットしない。変更をコミットするには、呼び出し元が行います。</span><span class="sxs-lookup"><span data-stu-id="440f1-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="440f1-119">Save 呼び出し中を除き、フォームのメッセージに属するプロパティを **変更** しない。</span><span class="sxs-lookup"><span data-stu-id="440f1-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="440f1-120">_fSameAsLoad が_ TRUE に設定されている場合は、フォームの既存のメッセージに対する変更を保存できます。</span><span class="sxs-lookup"><span data-stu-id="440f1-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="440f1-121">_fSameAsLoad_ が FALSE に設定されている場合は、保存を実行する前に、元のメッセージのすべてのプロパティを _pMessage_ が指すメッセージにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="440f1-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="440f1-122">元のメッセージの [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを使用してプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="440f1-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="440f1-123">すべてのプロパティがコピーされた場合は [、NoScribble 状態を入力](noscribble-state.md) します。</span><span class="sxs-lookup"><span data-stu-id="440f1-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="440f1-124">エラーが発生しない場合は、S_OK。</span><span class="sxs-lookup"><span data-stu-id="440f1-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="440f1-125">それ以外の場合は、失敗したアクションからエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="440f1-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="440f1-126">フォーム **が Normal** 以外の状態にあるときに Save が呼び出された場合は、次のE_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="440f1-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="440f1-127">ストレージ オブジェクトの保存の詳細については [、IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) メソッドのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="440f1-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="440f1-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="440f1-128">See also</span></span>



[<span data-ttu-id="440f1-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="440f1-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="440f1-130">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="440f1-130">Form States</span></span>](form-states.md)

