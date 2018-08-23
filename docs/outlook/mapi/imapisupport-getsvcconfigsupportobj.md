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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5d7e3e89f15b1bc08c7ce9faab0d0a6326300e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800740"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="40300-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="40300-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="40300-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40300-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40300-105">メッセージ サービスのサポート オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="40300-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="40300-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="40300-106">Parameters</span></span>

 <span data-ttu-id="40300-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40300-107">_ulFlags_</span></span>
  
> <span data-ttu-id="40300-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="40300-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="40300-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="40300-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="40300-110">[out]メッセージ サービスのサポートの新しいオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="40300-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40300-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="40300-111">Return value</span></span>

<span data-ttu-id="40300-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="40300-112">S_OK</span></span> 
  
> <span data-ttu-id="40300-113">構成のサポート オブジェクトが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="40300-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40300-114">注釈</span><span class="sxs-lookup"><span data-stu-id="40300-114">Remarks</span></span>

<span data-ttu-id="40300-115">サポートのすべてのオブジェクトの**IMAPISupport::GetSvcConfigSupportObj**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="40300-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="40300-116">サービス プロバイダーは、メッセージ サービスのエントリ ポイント関数に渡す設定のサポート オブジェクトを作成するのには**GetSvcConfigSupportObj**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="40300-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="40300-117">メッセージ サービスのエントリ ポイント関数では、 [MSGSERVICEENTRY](msgserviceentry.md)のプロトタイプに基づいており、 [IMsgServiceAdmin](imsgserviceadminiunknown.md)インターフェイスのメソッドによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="40300-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="40300-118">メッセージ サービスのエントリ ポイント関数は、メッセージ サービス自体を構成するか、プロファイルが変更されたときに、その他のアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="40300-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="40300-119">メッセージ サービスのエントリ ポイント関数は、プロパティ シートを表示することによって、またはプロパティ値の配列を構成の変更をサポートできますが、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="40300-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40300-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="40300-120">See also</span></span>



[<span data-ttu-id="40300-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40300-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="40300-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="40300-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="40300-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="40300-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="40300-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40300-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="40300-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="40300-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="40300-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="40300-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

