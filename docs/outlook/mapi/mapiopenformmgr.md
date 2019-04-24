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
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270099"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="5d6e8-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="5d6e8-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="5d6e8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d6e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d6e8-105">既存のセッションのコンテキストで、フォームライブラリプロバイダオブジェクトの[imapiformmgr](imapiformmgriunknown.md)インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d6e8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5d6e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d6e8-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="5d6e8-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5d6e8-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="5d6e8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5d6e8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5d6e8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5d6e8-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5d6e8-110">Called by:</span></span>  <br/> |<span data-ttu-id="5d6e8-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5d6e8-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="5d6e8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5d6e8-112">Parameters</span></span>

 <span data-ttu-id="5d6e8-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="5d6e8-113">_pSession_</span></span>
  
> <span data-ttu-id="5d6e8-114">順番クライアントアプリケーションによって使用されているセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="5d6e8-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="5d6e8-115">_ppmgr_</span></span>
  
> <span data-ttu-id="5d6e8-116">読み上げ返された**imapiformmgr**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5d6e8-117">Return value</span><span class="sxs-lookup"><span data-stu-id="5d6e8-117">Return value</span></span>

<span data-ttu-id="5d6e8-118">なし。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d6e8-119">解説</span><span class="sxs-lookup"><span data-stu-id="5d6e8-119">Remarks</span></span>

<span data-ttu-id="5d6e8-120">クライアントアプリケーションが**MAPIOpenFormMgr**関数を呼び出すと、その後のフォーム関連のやり取りは、フォームライブラリプロバイダまたはフォームライブラリプロバイダによって返されるインターフェイスを通じて行われます。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="5d6e8-121">**imapiformmgr**インターフェイスを使用すると、クライアントはメッセージハンドラーを操作し、メッセージクラスとフォームライブラリの間で解決を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5d6e8-122">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="5d6e8-122">MFCMAPI reference</span></span>

<span data-ttu-id="5d6e8-123">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5d6e8-124">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="5d6e8-124">**File**</span></span>|<span data-ttu-id="5d6e8-125">**関数**</span><span class="sxs-lookup"><span data-stu-id="5d6e8-125">**Function**</span></span>|<span data-ttu-id="5d6e8-126">**コメント**</span><span class="sxs-lookup"><span data-stu-id="5d6e8-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5d6e8-127">フォームマネージャーが開き、フォームを選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="5d6e8-128">CMainDlg:: onselectform</span><span class="sxs-lookup"><span data-stu-id="5d6e8-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="5d6e8-129">mfcmapi は、 **MAPIOpenFormMgr**メソッドを使用してフォームマネージャーを開き、フォームを選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5d6e8-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d6e8-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d6e8-130">See also</span></span>



<span data-ttu-id="5d6e8-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5d6e8-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

