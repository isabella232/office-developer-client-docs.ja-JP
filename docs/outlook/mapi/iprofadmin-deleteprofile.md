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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801144"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="ac6c6-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="ac6c6-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="ac6c6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac6c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac6c6-105">プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ac6c6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ac6c6-106">Parameters</span></span>

 <span data-ttu-id="ac6c6-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="ac6c6-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="ac6c6-108">[in]削除するプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="ac6c6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac6c6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ac6c6-110">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ac6c6-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ac6c6-111">Return value</span></span>

<span data-ttu-id="ac6c6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac6c6-112">S_OK</span></span> 
  
> <span data-ttu-id="ac6c6-113">プロファイルが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="ac6c6-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ac6c6-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ac6c6-115">指定されたプロファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac6c6-116">備考</span><span class="sxs-lookup"><span data-stu-id="ac6c6-116">Remarks</span></span>

<span data-ttu-id="ac6c6-117">**IProfAdmin::DeleteProfile**メソッドは、プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="ac6c6-118">**DeleteProfile**が呼び出されたときに削除するプロファイルを使用している場合、 **DeleteProfile**は S_OK を返しますが、すぐに、プロファイルは削除されません。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="ac6c6-119">代わりに、 **DeleteProfile**は、プロファイルの削除をマークし、不要になった使用されている、すべてのアクティブ ・ セッションの終了したときに後でそれを削除します。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="ac6c6-120">プロファイルでは、各メッセージ サービスのエントリ ポイント関数は、 _ulContext_パラメーターに設定された MSG_SERVICE_DELETE 値で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="ac6c6-121">関数は、サービスを削除し、サービスのプロファイル セクションを削除し、最初に、します。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="ac6c6-122">サービスが削除された後、メッセージ サービスのエントリ ポイント関数は再び呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="ac6c6-123">パスワードがプロファイルを削除する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac6c6-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ac6c6-124">MFCMAPI reference</span></span>

<span data-ttu-id="ac6c6-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ac6c6-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac6c6-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ac6c6-126">**File**</span></span>|<span data-ttu-id="ac6c6-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ac6c6-127">**Function**</span></span>|<span data-ttu-id="ac6c6-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ac6c6-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac6c6-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ac6c6-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ac6c6-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="ac6c6-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="ac6c6-131">MFCMAPI では、 **IProfAdmin::DeleteProfile**メソッドを使用して、選択したプロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="ac6c6-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac6c6-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac6c6-132">See also</span></span>



[<span data-ttu-id="ac6c6-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="ac6c6-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="ac6c6-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="ac6c6-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="ac6c6-135">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac6c6-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="ac6c6-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ac6c6-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

