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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1a95989cea7ad5529eb73276b4c771e4900804b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579901"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="00b7b-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="00b7b-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="00b7b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00b7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00b7b-105">変更後のフォームを元に読み込みまたは作成したメッセージに保存します。</span><span class="sxs-lookup"><span data-stu-id="00b7b-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="00b7b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="00b7b-106">Parameters</span></span>

 <span data-ttu-id="00b7b-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="00b7b-107">_pMessage_</span></span>
  
> <span data-ttu-id="00b7b-108">[in]メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="00b7b-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="00b7b-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="00b7b-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="00b7b-110">[in]メッセージに示されることを指定する場合は TRUE _pMessage_では、メッセージ フォームが読み込まれるか作成。それ以外の場合、FALSE です。</span><span class="sxs-lookup"><span data-stu-id="00b7b-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="00b7b-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="00b7b-111">Return value</span></span>

<span data-ttu-id="00b7b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="00b7b-112">S_OK</span></span> 
  
> <span data-ttu-id="00b7b-113">フォームが正常に保存されました。</span><span class="sxs-lookup"><span data-stu-id="00b7b-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00b7b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="00b7b-114">Remarks</span></span>

<span data-ttu-id="00b7b-115">フォームの閲覧者は、変更後のフォームを元に読み込みまたは作成したメッセージに保存するのには**IPersistMessage::Save**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="00b7b-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="00b7b-116">**保存**する必要がありますのみ呼び出すことは、フォームの[標準](normal-state.md)の状態で。</span><span class="sxs-lookup"><span data-stu-id="00b7b-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="00b7b-117">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="00b7b-117">Notes to implementers</span></span>

<span data-ttu-id="00b7b-118">保存した変更をコミットしません。変更をコミットする呼び出し元の責任です。</span><span class="sxs-lookup"><span data-stu-id="00b7b-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="00b7b-119">**保存**の呼び出し時に除いて、フォームのメッセージに属するプロパティに変更を加えることはありません。</span><span class="sxs-lookup"><span data-stu-id="00b7b-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="00b7b-120">_FSameAsLoad_が TRUE に設定されている場合は、フォームの既存のメッセージに変更を保存することができます。</span><span class="sxs-lookup"><span data-stu-id="00b7b-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="00b7b-121">_FSameAsLoad_が FALSE に設定されている場合が指す_pMessage_保存を実行する前にメッセージに元のメッセージからコピーすべてのプロパティ必要があります。</span><span class="sxs-lookup"><span data-stu-id="00b7b-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="00b7b-122">プロパティをコピーするのにには、元のメッセージの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="00b7b-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="00b7b-123">すべてのプロパティがコピーされたら、 [NoScribble](noscribble-state.md)の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="00b7b-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="00b7b-124">エラーが発生しない場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="00b7b-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="00b7b-125">それ以外の場合、失敗した操作からのエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="00b7b-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="00b7b-126">フォームは、標準以外の任意の状態にすると、 **Save**が呼び出される、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="00b7b-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="00b7b-127">ストレージ ・ オブジェクトを保存する方法の詳細については、[すること](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)の方法のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="00b7b-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00b7b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="00b7b-128">See also</span></span>



[<span data-ttu-id="00b7b-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00b7b-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="00b7b-130">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="00b7b-130">Form States</span></span>](form-states.md)

