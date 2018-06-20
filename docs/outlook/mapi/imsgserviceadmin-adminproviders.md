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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9b65c8e32580fa85302b874bd17c1829ad67fd63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800974"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="dee7c-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="dee7c-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="dee7c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dee7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dee7c-105">プロバイダー管理オブジェクトへのアクセスを提供するポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="dee7c-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="dee7c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dee7c-106">Parameters</span></span>

 <span data-ttu-id="dee7c-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="dee7c-107">_lpUID_</span></span>
  
> <span data-ttu-id="dee7c-108">[in]管理するメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dee7c-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="dee7c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dee7c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="dee7c-110">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="dee7c-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="dee7c-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="dee7c-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="dee7c-112">[out]プロバイダーの管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dee7c-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dee7c-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="dee7c-113">Return value</span></span>

<span data-ttu-id="dee7c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="dee7c-114">S_OK</span></span> 
  
> <span data-ttu-id="dee7c-115">プロバイダーの管理オブジェクトが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="dee7c-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="dee7c-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dee7c-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="dee7c-117">_LpUID_で示される**MAPIUID**は存在しません。</span><span class="sxs-lookup"><span data-stu-id="dee7c-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dee7c-118">備考</span><span class="sxs-lookup"><span data-stu-id="dee7c-118">Remarks</span></span>

<span data-ttu-id="dee7c-119">**IMsgServiceAdmin::AdminProviders**メソッドは、プロバイダーの管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="dee7c-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="dee7c-120">プロバイダーの管理は、 [IProviderAdmin](iprovideradminiunknown.md)インターフェイスをサポートしていて、クライアントは、次の操作を可能にするオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="dee7c-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="dee7c-121">メッセージ サービスにサービス プロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="dee7c-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="dee7c-122">メッセージ サービスからサービス プロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="dee7c-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="dee7c-123">プロファイル セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="dee7c-123">Open profile sections.</span></span>
    
- <span data-ttu-id="dee7c-124">メッセージ サービス プロバイダー テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="dee7c-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="dee7c-125">実際に可能なメッセージ サービスにプロファイルを使用中に変更の種類は、メッセージ サービスに依存します。</span><span class="sxs-lookup"><span data-stu-id="dee7c-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="dee7c-126">ただし、ほとんどのメッセージ サービスには、追加し、プロファイルを使用している間に、プロバイダーを削除するなどの変更はできません。</span><span class="sxs-lookup"><span data-stu-id="dee7c-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="dee7c-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="dee7c-127">Notes to callers</span></span>

<span data-ttu-id="dee7c-128">メッセージ サービスを管理するための**MAPIUID**構造体を取得するには、メッセージ サービスのテーブルの行のメッセージ サービスから**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) のプロパティの列を取得します。</span><span class="sxs-lookup"><span data-stu-id="dee7c-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="dee7c-129">詳細については、 [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドで説明する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dee7c-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dee7c-130">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="dee7c-130">MFCMAPI reference</span></span>

<span data-ttu-id="dee7c-131">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="dee7c-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dee7c-132">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="dee7c-132">**File**</span></span>|<span data-ttu-id="dee7c-133">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="dee7c-133">**Function**</span></span>|<span data-ttu-id="dee7c-134">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="dee7c-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dee7c-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dee7c-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="dee7c-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="dee7c-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="dee7c-137">MFCMAPI では、 **IMsgServiceAdmin::AdminProviders**メソッドを使用して、サービス プロバイダーの管理オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="dee7c-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dee7c-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="dee7c-138">See also</span></span>



[<span data-ttu-id="dee7c-139">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dee7c-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="dee7c-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="dee7c-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="dee7c-141">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dee7c-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="dee7c-142">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="dee7c-142">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

