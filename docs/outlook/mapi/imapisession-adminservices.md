---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 850d4d952102e11d11234fa3184b88e280a98c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800702"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="336c4-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="336c4-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="336c4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="336c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="336c4-105">メッセージ サービスを変更する場合、 [IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="336c4-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="336c4-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="336c4-106">Parameters</span></span>

 <span data-ttu-id="336c4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="336c4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="336c4-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="336c4-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="336c4-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="336c4-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="336c4-110">[out]メッセージ サービス管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="336c4-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="336c4-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="336c4-111">Return value</span></span>

<span data-ttu-id="336c4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="336c4-112">S_OK</span></span> 
  
> <span data-ttu-id="336c4-113">メッセージ サービス管理オブジェクトへのポインターが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="336c4-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="336c4-114">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="336c4-114">Notes to callers</span></span>

<span data-ttu-id="336c4-115">**IMAPISession::AdminServices**メソッドは、メッセージ サービスの管理オブジェクト、 **IMsgServiceAdmin**インターフェイスをサポートし、ポインターを返すオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="336c4-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="336c4-116">このポインターを使用すると、セッション ・ プロファイル内のメッセージ サービスのいずれかを変更するのには**IMsgServiceAdmin**メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="336c4-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="336c4-117">これらの変更は反映されません。 次のセッションまでに注意してください。現在のセッションには影響しません。</span><span class="sxs-lookup"><span data-stu-id="336c4-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="336c4-118">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="336c4-118">MFCMAPI reference</span></span>

<span data-ttu-id="336c4-119">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="336c4-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="336c4-120">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="336c4-120">**File**</span></span>|<span data-ttu-id="336c4-121">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="336c4-121">**Function**</span></span>|<span data-ttu-id="336c4-122">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="336c4-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="336c4-123">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="336c4-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="336c4-124">GetServerName</span><span class="sxs-lookup"><span data-stu-id="336c4-124">GetServerName</span></span>  <br/> |<span data-ttu-id="336c4-125">MFCMAPI では、 **IMAPISession::AdminServices**メソッドを使用して、サーバー名を読み取るためのプロファイルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="336c4-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="336c4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="336c4-126">See also</span></span>



[<span data-ttu-id="336c4-127">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="336c4-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="336c4-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="336c4-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="336c4-129">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="336c4-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="336c4-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="336c4-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

