---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419591"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="df730-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="df730-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="df730-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df730-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df730-105">プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="df730-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="df730-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="df730-106">Parameters</span></span>

 <span data-ttu-id="df730-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="df730-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="df730-108">[in]削除するプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="df730-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="df730-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="df730-109">_ulFlags_</span></span>
  
> <span data-ttu-id="df730-110">[in]常に NULL。</span><span class="sxs-lookup"><span data-stu-id="df730-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="df730-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="df730-111">Return value</span></span>

<span data-ttu-id="df730-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="df730-112">S_OK</span></span> 
  
> <span data-ttu-id="df730-113">プロファイルが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="df730-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="df730-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="df730-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="df730-115">指定したプロファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="df730-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df730-116">注釈</span><span class="sxs-lookup"><span data-stu-id="df730-116">Remarks</span></span>

<span data-ttu-id="df730-117">**IProfAdmin::D eleteProfile** メソッドはプロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="df730-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="df730-118">DeleteProfile の呼び出し時に削除するプロファイルが使用されている場合 **、DeleteProfile** は S_OKを返しますが、プロファイルはすぐには削除されません。 </span><span class="sxs-lookup"><span data-stu-id="df730-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="df730-119">代わりに **、DeleteProfile は** プロファイルに削除のマークを付け、すべてのアクティブ なセッションが終了すると、使用されなくなった後にプロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="df730-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="df730-120">プロファイル内の各メッセージ サービスのエントリ ポイント関数は、ulContext パラメーターに設定MSG_SERVICE_DELETEを使用して  _呼び出_ されます。</span><span class="sxs-lookup"><span data-stu-id="df730-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="df730-121">最初に、関数はサービスを削除し、次にサービスのプロファイル セクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="df730-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="df730-122">サービスが削除された後、メッセージ サービスエントリ ポイント関数は再度呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="df730-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="df730-123">プロファイルを削除するには、パスワードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="df730-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="df730-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="df730-124">MFCMAPI reference</span></span>

<span data-ttu-id="df730-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df730-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="df730-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="df730-126">**File**</span></span>|<span data-ttu-id="df730-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="df730-127">**Function**</span></span>|<span data-ttu-id="df730-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="df730-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="df730-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="df730-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="df730-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="df730-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="df730-131">MFCMAPI は **、IProfAdmin::D eleteProfile** メソッドを使用して、選択したプロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="df730-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df730-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="df730-132">See also</span></span>



[<span data-ttu-id="df730-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="df730-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="df730-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="df730-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="df730-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df730-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="df730-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="df730-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

