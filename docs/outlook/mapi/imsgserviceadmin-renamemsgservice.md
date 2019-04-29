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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422104"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="85a28-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="85a28-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="85a28-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85a28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85a28-105">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="85a28-105">Deprecated.</span></span> <span data-ttu-id="85a28-106">メッセージサービスに新しい名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="85a28-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="85a28-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85a28-107">Parameters</span></span>

 <span data-ttu-id="85a28-108">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="85a28-108">_lpUID_</span></span>
  
> <span data-ttu-id="85a28-109">順番名前を変更するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="85a28-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="85a28-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85a28-110">_ulFlags_</span></span>
  
> <span data-ttu-id="85a28-111">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="85a28-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="85a28-112">_lpszdisplayname_</span><span class="sxs-lookup"><span data-stu-id="85a28-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="85a28-113">順番メッセージサービスの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="85a28-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85a28-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="85a28-114">Return value</span></span>

<span data-ttu-id="85a28-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="85a28-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="85a28-116">MAPI では、このメッセージサービスの名前変更はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="85a28-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="85a28-117">**RenameMsgService**は、常にこの値を返します。</span><span class="sxs-lookup"><span data-stu-id="85a28-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="85a28-118">注釈</span><span class="sxs-lookup"><span data-stu-id="85a28-118">Remarks</span></span>

<span data-ttu-id="85a28-119">メッセージサービスに新しい名前を割り当てるには、クライアントでメッセージサービスの**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85a28-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="85a28-120">メッセージサービスのサービスプロバイダーの名前は、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="85a28-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85a28-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="85a28-121">See also</span></span>



[<span data-ttu-id="85a28-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="85a28-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="85a28-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85a28-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

