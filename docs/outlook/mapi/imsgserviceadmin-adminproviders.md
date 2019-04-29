---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422762"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="4842f-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="4842f-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="4842f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4842f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4842f-105">プロバイダー管理オブジェクトへのアクセスを提供するポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="4842f-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="4842f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4842f-106">Parameters</span></span>

 <span data-ttu-id="4842f-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="4842f-107">_lpUID_</span></span>
  
> <span data-ttu-id="4842f-108">順番管理するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4842f-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="4842f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4842f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4842f-110">順番常に NULL。</span><span class="sxs-lookup"><span data-stu-id="4842f-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="4842f-111">_lppprovideradmin_</span><span class="sxs-lookup"><span data-stu-id="4842f-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="4842f-112">読み上げプロバイダー管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4842f-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4842f-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="4842f-113">Return value</span></span>

<span data-ttu-id="4842f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4842f-114">S_OK</span></span> 
  
> <span data-ttu-id="4842f-115">プロバイダー管理オブジェクトが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="4842f-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="4842f-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4842f-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4842f-117">_lpuid_が指す**MAPIUID**が存在しません。</span><span class="sxs-lookup"><span data-stu-id="4842f-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4842f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="4842f-118">Remarks</span></span>

<span data-ttu-id="4842f-119">**IMsgServiceAdmin:: adminproviders**メソッドは、プロバイダ管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="4842f-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="4842f-120">プロバイダー管理は、 [IProviderAdmin](iprovideradminiunknown.md)インターフェイスをサポートし、クライアントが次の操作を実行できるようにするオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="4842f-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="4842f-121">メッセージサービスにサービスプロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="4842f-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="4842f-122">メッセージサービスからサービスプロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="4842f-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="4842f-123">[プロファイル] セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="4842f-123">Open profile sections.</span></span>
    
- <span data-ttu-id="4842f-124">メッセージサービスプロバイダテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4842f-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="4842f-125">プロファイルが使用されている間にメッセージサービスに対して実際に行うことができる変更の種類は、メッセージサービスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="4842f-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="4842f-126">ただし、ほとんどのメッセージサービスでは、プロファイルの使用中にプロバイダーを追加および削除するなどの変更はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4842f-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4842f-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4842f-127">Notes to callers</span></span>

<span data-ttu-id="4842f-128">管理するメッセージサービスの**MAPIUID**構造を取得するには、メッセージサービステーブルのメッセージサービスの行から**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティ列を取得します。</span><span class="sxs-lookup"><span data-stu-id="4842f-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="4842f-129">詳細については、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドに記載されている手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4842f-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4842f-130">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="4842f-130">MFCMAPI reference</span></span>

<span data-ttu-id="4842f-131">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4842f-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4842f-132">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="4842f-132">**File**</span></span>|<span data-ttu-id="4842f-133">**関数**</span><span class="sxs-lookup"><span data-stu-id="4842f-133">**Function**</span></span>|<span data-ttu-id="4842f-134">**コメント**</span><span class="sxs-lookup"><span data-stu-id="4842f-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4842f-135">MsgServiceTableDlg</span><span class="sxs-lookup"><span data-stu-id="4842f-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="4842f-136">CMsgServiceTableDlg:: ondisplayitem</span><span class="sxs-lookup"><span data-stu-id="4842f-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="4842f-137">mfcmapi は、 **IMsgServiceAdmin:: adminproviders**メソッドを使用して、サービスのプロバイダー管理オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="4842f-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4842f-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="4842f-138">See also</span></span>



[<span data-ttu-id="4842f-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4842f-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="4842f-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4842f-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4842f-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4842f-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="4842f-142">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4842f-142">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

