---
title: imapisessionadminservices
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405906"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="b1674-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="b1674-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="b1674-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1674-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1674-105">メッセージサービスに変更を加えるための[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b1674-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="b1674-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1674-106">Parameters</span></span>

 <span data-ttu-id="b1674-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1674-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b1674-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="b1674-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b1674-109">_lppserviceadmin_</span><span class="sxs-lookup"><span data-stu-id="b1674-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="b1674-110">読み上げメッセージサービス管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b1674-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1674-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="b1674-111">Return value</span></span>

<span data-ttu-id="b1674-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1674-112">S_OK</span></span> 
  
> <span data-ttu-id="b1674-113">メッセージサービス管理オブジェクトへのポインターが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="b1674-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="b1674-114">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b1674-114">Notes to callers</span></span>

<span data-ttu-id="b1674-115">**imapisession:: adminservices**メソッドは、 **IMsgServiceAdmin**インターフェイスをサポートするオブジェクトであるメッセージサービス管理オブジェクトを作成し、ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b1674-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="b1674-116">このポインターを使用すると、 **IMsgServiceAdmin**メソッドを呼び出して、セッションプロファイル内の任意のメッセージサービスを変更できます。</span><span class="sxs-lookup"><span data-stu-id="b1674-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="b1674-117">これらの変更は、次のセッションが終了するまで有効にならないことに注意してください。現在のセッションは影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="b1674-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b1674-118">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b1674-118">MFCMAPI reference</span></span>

<span data-ttu-id="b1674-119">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1674-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b1674-120">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b1674-120">**File**</span></span>|<span data-ttu-id="b1674-121">**関数**</span><span class="sxs-lookup"><span data-stu-id="b1674-121">**Function**</span></span>|<span data-ttu-id="b1674-122">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b1674-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b1674-123">MAPIStoreFunctions</span><span class="sxs-lookup"><span data-stu-id="b1674-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b1674-124">getservername</span><span class="sxs-lookup"><span data-stu-id="b1674-124">GetServerName</span></span>  <br/> |<span data-ttu-id="b1674-125">mfcmapi は、 **imapisession:: adminservices**メソッドを使用して、プロファイルにアクセスしてサーバー名を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="b1674-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1674-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1674-126">See also</span></span>



[<span data-ttu-id="b1674-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1674-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="b1674-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="b1674-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="b1674-129">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1674-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="b1674-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b1674-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

