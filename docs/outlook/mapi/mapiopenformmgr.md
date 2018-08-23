---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2ed71b5eef0c25a78d7c8ec695a756a02e796dbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586033"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="94287-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="94287-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="94287-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94287-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94287-105">既存のセッションのコンテキストでは、フォーム ライブラリのプロバイダー オブジェクトの[IMAPIFormMgr](imapiformmgriunknown.md)インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="94287-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94287-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="94287-106">Header file:</span></span>  <br/> |<span data-ttu-id="94287-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="94287-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="94287-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="94287-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="94287-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="94287-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="94287-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="94287-110">Called by:</span></span>  <br/> |<span data-ttu-id="94287-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="94287-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="94287-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="94287-112">Parameters</span></span>

 <span data-ttu-id="94287-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="94287-113">_pSession_</span></span>
  
> <span data-ttu-id="94287-114">[in]クライアント アプリケーションによって使用中のセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="94287-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="94287-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="94287-115">_ppmgr_</span></span>
  
> <span data-ttu-id="94287-116">[out]返される**IMAPIFormMgr**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="94287-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="94287-117">Return value</span><span class="sxs-lookup"><span data-stu-id="94287-117">Return value</span></span>

<span data-ttu-id="94287-118">なし。</span><span class="sxs-lookup"><span data-stu-id="94287-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94287-119">注釈</span><span class="sxs-lookup"><span data-stu-id="94287-119">Remarks</span></span>

<span data-ttu-id="94287-120">クライアント アプリケーションを**MAPIOpenFormMgr**関数の呼び出しを行った後のほとんどのフォームに関連する操作が行わフォーム ライブラリ プロバイダーまたはフォーム ライブラリ プロバイダーによって返されるインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="94287-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="94287-121">**IMAPIFormMgr**インターフェイスは、メッセージ ハンドラーを使用し、メッセージ クラスとフォーム ライブラリの間での解決策を実行するクライアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="94287-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="94287-122">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="94287-122">MFCMAPI reference</span></span>

<span data-ttu-id="94287-123">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="94287-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="94287-124">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="94287-124">**File**</span></span>|<span data-ttu-id="94287-125">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="94287-125">**Function**</span></span>|<span data-ttu-id="94287-126">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="94287-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="94287-127">MainDlg.cpp は、フォームを選択できるように、フォーム マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="94287-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="94287-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="94287-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="94287-129">MFCMAPI では、 **MAPIOpenFormMgr**メソッドを使用して、フォームを選択できるように、フォーム マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="94287-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94287-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="94287-130">See also</span></span>



<span data-ttu-id="94287-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="94287-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

