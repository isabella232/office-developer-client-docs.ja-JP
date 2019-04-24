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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316559"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="6b1f2-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="6b1f2-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="6b1f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b1f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b1f2-105">メッセージサービスサポートオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6b1f2-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="6b1f2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b1f2-106">Parameters</span></span>

 <span data-ttu-id="6b1f2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b1f2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6b1f2-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6b1f2-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6b1f2-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="6b1f2-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="6b1f2-110">読み上げ新しいメッセージサービスサポートオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b1f2-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b1f2-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b1f2-111">Return value</span></span>

<span data-ttu-id="6b1f2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b1f2-112">S_OK</span></span> 
  
> <span data-ttu-id="6b1f2-113">構成サポートオブジェクトが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="6b1f2-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b1f2-114">解説</span><span class="sxs-lookup"><span data-stu-id="6b1f2-114">Remarks</span></span>

<span data-ttu-id="6b1f2-115">**imapisupport:: GetSvcConfigSupportObj**メソッドは、すべてのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="6b1f2-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="6b1f2-116">サービスプロバイダーは**GetSvcConfigSupportObj**を呼び出して、メッセージサービスエントリポイント関数に渡す構成サポートオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6b1f2-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="6b1f2-117">メッセージサービスエントリポイント関数は、 [msgserviceentry](msgserviceentry.md)プロトタイプに基づいており、 [IMsgServiceAdmin](imsgserviceadminiunknown.md)インターフェイスのメソッドによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6b1f2-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="6b1f2-118">メッセージサービスエントリポイント関数を使用すると、メッセージサービスが自分自身を構成したり、プロファイルが変更されたときに他のアクションを実行したりできます。</span><span class="sxs-lookup"><span data-stu-id="6b1f2-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="6b1f2-119">メッセージサービスエントリポイント関数は、プロパティシートを表示するか、 [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡されたプロパティ値配列を使用して、構成の変更をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="6b1f2-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b1f2-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b1f2-120">See also</span></span>



[<span data-ttu-id="6b1f2-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b1f2-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="6b1f2-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="6b1f2-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="6b1f2-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="6b1f2-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="6b1f2-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b1f2-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="6b1f2-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="6b1f2-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="6b1f2-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b1f2-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

