---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411310"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="c0f9c-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="c0f9c-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="c0f9c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0f9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0f9c-105">メッセージ サービスサポート オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c0f9c-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="c0f9c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c0f9c-106">Parameters</span></span>

 <span data-ttu-id="c0f9c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0f9c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c0f9c-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="c0f9c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c0f9c-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="c0f9c-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="c0f9c-110">[out]新しいメッセージ サービス サポート オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c0f9c-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0f9c-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="c0f9c-111">Return value</span></span>

<span data-ttu-id="c0f9c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0f9c-112">S_OK</span></span> 
  
> <span data-ttu-id="c0f9c-113">構成サポート オブジェクトが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="c0f9c-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0f9c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c0f9c-114">Remarks</span></span>

<span data-ttu-id="c0f9c-115">**IMAPISupport::GetSvcConfigSupportObj** メソッドは、すべてのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="c0f9c-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="c0f9c-116">サービス プロバイダーは **GetSvcConfigSupportObj** を呼び出して、メッセージ サービス エントリ ポイント関数に渡す構成サポート オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c0f9c-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="c0f9c-117">メッセージ サービスエントリ ポイント関数は [、MSGSERVICEENTRY](msgserviceentry.md) プロトタイプに基づいており [、IMsgServiceAdmin インターフェイスのメソッドによって呼び出](imsgserviceadminiunknown.md) されます。</span><span class="sxs-lookup"><span data-stu-id="c0f9c-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="c0f9c-118">メッセージ サービス エントリ ポイント関数を使用すると、プロファイルが変更された場合に、メッセージ サービスが自分自身を構成したり、他のアクションを実行したりできます。</span><span class="sxs-lookup"><span data-stu-id="c0f9c-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="c0f9c-119">メッセージ サービスエントリ ポイント関数は、プロパティ シートを表示するか [、IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) メソッドに渡されるプロパティ値配列を介して構成の変更をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="c0f9c-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0f9c-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0f9c-120">See also</span></span>



[<span data-ttu-id="c0f9c-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0f9c-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="c0f9c-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="c0f9c-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="c0f9c-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="c0f9c-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="c0f9c-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0f9c-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="c0f9c-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c0f9c-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="c0f9c-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0f9c-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

