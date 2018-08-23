---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800982"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="90e64-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="90e64-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="90e64-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90e64-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90e64-105">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="90e64-105">Deprecated.</span></span> <span data-ttu-id="90e64-106">メッセージ サービスに新しい名前が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="90e64-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="90e64-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90e64-107">Parameters</span></span>

 <span data-ttu-id="90e64-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="90e64-108">_lpUID_</span></span>
  
> <span data-ttu-id="90e64-109">[in]名前を変更するメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="90e64-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="90e64-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90e64-110">_ulFlags_</span></span>
  
> <span data-ttu-id="90e64-111">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="90e64-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="90e64-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="90e64-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="90e64-113">[in]メッセージ サービスの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="90e64-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90e64-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="90e64-114">Return value</span></span>

<span data-ttu-id="90e64-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="90e64-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="90e64-116">MAPI では、このメッセージ サービスの名前を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="90e64-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="90e64-117">**RenameMsgService**は、常にこの値を返します。</span><span class="sxs-lookup"><span data-stu-id="90e64-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="90e64-118">注釈</span><span class="sxs-lookup"><span data-stu-id="90e64-118">Remarks</span></span>

<span data-ttu-id="90e64-119">メッセージ サービスに新しい名前を割り当てるには、クライアントは、メッセージ サービスの**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="90e64-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="90e64-120">メッセージ サービスのサービス プロバイダーの名前は、それらのプロパティの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に格納されます。</span><span class="sxs-lookup"><span data-stu-id="90e64-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90e64-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="90e64-121">See also</span></span>



[<span data-ttu-id="90e64-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="90e64-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="90e64-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90e64-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

