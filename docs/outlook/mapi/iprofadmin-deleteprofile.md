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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309563"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="329e1-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="329e1-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="329e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="329e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="329e1-105">プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="329e1-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="329e1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="329e1-106">Parameters</span></span>

 <span data-ttu-id="329e1-107">_lpszprofilename_</span><span class="sxs-lookup"><span data-stu-id="329e1-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="329e1-108">順番削除するプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="329e1-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="329e1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="329e1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="329e1-110">順番常に NULL。</span><span class="sxs-lookup"><span data-stu-id="329e1-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="329e1-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="329e1-111">Return value</span></span>

<span data-ttu-id="329e1-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="329e1-112">S_OK</span></span> 
  
> <span data-ttu-id="329e1-113">プロファイルが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="329e1-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="329e1-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="329e1-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="329e1-115">指定されたプロファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="329e1-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="329e1-116">解説</span><span class="sxs-lookup"><span data-stu-id="329e1-116">Remarks</span></span>

<span data-ttu-id="329e1-117">**IProfAdmin::D eleteprofile**メソッドは、プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="329e1-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="329e1-118">**deleteprofile**を呼び出したときに削除するプロファイルが使用されている場合、 **deleteprofile**は S_OK を返しますが、プロファイルはすぐには削除されません。</span><span class="sxs-lookup"><span data-stu-id="329e1-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="329e1-119">代わりに、 **deleteprofile**はプロファイルを削除対象としてマークし、使用されなくなった後に、すべてのアクティブなセッションが終了した時点で削除します。</span><span class="sxs-lookup"><span data-stu-id="329e1-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="329e1-120">プロファイル内の各メッセージサービスのエントリポイント関数は、 _ulcontext_パラメーターで設定された MSG_SERVICE_DELETE 値を使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329e1-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="329e1-121">最初に、この関数はサービスを削除してから、サービスの [プロファイル] セクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="329e1-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="329e1-122">サービスが削除された後に、メッセージサービスエントリポイント関数が再度呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="329e1-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="329e1-123">プロファイルを削除するためにパスワードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="329e1-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="329e1-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="329e1-124">MFCMAPI reference</span></span>

<span data-ttu-id="329e1-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="329e1-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="329e1-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="329e1-126">**File**</span></span>|<span data-ttu-id="329e1-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="329e1-127">**Function**</span></span>|<span data-ttu-id="329e1-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="329e1-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="329e1-129">MAPIProfileFunctions</span><span class="sxs-lookup"><span data-stu-id="329e1-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="329e1-130">hrremoveprofile</span><span class="sxs-lookup"><span data-stu-id="329e1-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="329e1-131">mfcmapi は、 **IProfAdmin::D eleteprofile**メソッドを使用して、選択されているプロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="329e1-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="329e1-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="329e1-132">See also</span></span>



[<span data-ttu-id="329e1-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="329e1-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="329e1-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="329e1-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="329e1-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="329e1-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="329e1-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="329e1-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

