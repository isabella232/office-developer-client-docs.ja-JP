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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322415"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="1e955-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="1e955-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="1e955-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e955-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e955-105">メッセージサービスに変更を加えるための[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1e955-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="1e955-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1e955-106">Parameters</span></span>

 <span data-ttu-id="1e955-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e955-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1e955-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="1e955-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1e955-109">_lppserviceadmin_</span><span class="sxs-lookup"><span data-stu-id="1e955-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="1e955-110">読み上げメッセージサービス管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1e955-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e955-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="1e955-111">Return value</span></span>

<span data-ttu-id="1e955-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e955-112">S_OK</span></span> 
  
> <span data-ttu-id="1e955-113">メッセージサービス管理オブジェクトへのポインターが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="1e955-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="1e955-114">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1e955-114">Notes to callers</span></span>

<span data-ttu-id="1e955-115">**imapisession:: adminservices**メソッドは、 **IMsgServiceAdmin**インターフェイスをサポートするオブジェクトであるメッセージサービス管理オブジェクトを作成し、ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1e955-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="1e955-116">このポインターを使用すると、 **IMsgServiceAdmin**メソッドを呼び出して、セッションプロファイル内の任意のメッセージサービスを変更できます。</span><span class="sxs-lookup"><span data-stu-id="1e955-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="1e955-117">これらの変更は、次のセッションが終了するまで有効にならないことに注意してください。現在のセッションは影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="1e955-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1e955-118">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="1e955-118">MFCMAPI reference</span></span>

<span data-ttu-id="1e955-119">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e955-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1e955-120">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="1e955-120">**File**</span></span>|<span data-ttu-id="1e955-121">**関数**</span><span class="sxs-lookup"><span data-stu-id="1e955-121">**Function**</span></span>|<span data-ttu-id="1e955-122">**コメント**</span><span class="sxs-lookup"><span data-stu-id="1e955-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e955-123">MAPIStoreFunctions</span><span class="sxs-lookup"><span data-stu-id="1e955-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1e955-124">getservername</span><span class="sxs-lookup"><span data-stu-id="1e955-124">GetServerName</span></span>  <br/> |<span data-ttu-id="1e955-125">mfcmapi は、 **imapisession:: adminservices**メソッドを使用して、プロファイルにアクセスしてサーバー名を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="1e955-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e955-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e955-126">See also</span></span>



[<span data-ttu-id="1e955-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e955-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="1e955-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="1e955-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="1e955-129">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e955-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="1e955-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1e955-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

