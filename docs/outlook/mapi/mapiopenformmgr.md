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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418051"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="48ba3-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="48ba3-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="48ba3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48ba3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48ba3-105">既存の [セッションのコンテキストで](imapiformmgriunknown.md) フォーム ライブラリ プロバイダー オブジェクトの IMAPIFormMgr インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="48ba3-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48ba3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="48ba3-106">Header file:</span></span>  <br/> |<span data-ttu-id="48ba3-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="48ba3-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="48ba3-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="48ba3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48ba3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="48ba3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="48ba3-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="48ba3-110">Called by:</span></span>  <br/> |<span data-ttu-id="48ba3-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="48ba3-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="48ba3-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="48ba3-112">Parameters</span></span>

 <span data-ttu-id="48ba3-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="48ba3-113">_pSession_</span></span>
  
> <span data-ttu-id="48ba3-114">[in]クライアント アプリケーションで使用されているセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="48ba3-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="48ba3-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="48ba3-115">_ppmgr_</span></span>
  
> <span data-ttu-id="48ba3-116">[out]返される **IMAPIFormMgr インターフェイスへの** ポインター。</span><span class="sxs-lookup"><span data-stu-id="48ba3-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48ba3-117">Return value</span><span class="sxs-lookup"><span data-stu-id="48ba3-117">Return value</span></span>

<span data-ttu-id="48ba3-118">なし。</span><span class="sxs-lookup"><span data-stu-id="48ba3-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48ba3-119">注釈</span><span class="sxs-lookup"><span data-stu-id="48ba3-119">Remarks</span></span>

<span data-ttu-id="48ba3-120">クライアント アプリケーションが **MAPIOpenFormMgr** 関数を呼び出した後、フォーム ライブラリ プロバイダーまたはフォーム ライブラリ プロバイダーによって返されるインターフェイスを介して、フォーム関連のほとんどの操作が行います。</span><span class="sxs-lookup"><span data-stu-id="48ba3-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="48ba3-121">**IMAPIFormMgr** インターフェイスを使用すると、クライアントはメッセージ ハンドラーを操作し、メッセージ クラスとフォーム ライブラリの間で解決を実行できます。</span><span class="sxs-lookup"><span data-stu-id="48ba3-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="48ba3-122">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="48ba3-122">MFCMAPI reference</span></span>

<span data-ttu-id="48ba3-123">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48ba3-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="48ba3-124">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="48ba3-124">**File**</span></span>|<span data-ttu-id="48ba3-125">**関数**</span><span class="sxs-lookup"><span data-stu-id="48ba3-125">**Function**</span></span>|<span data-ttu-id="48ba3-126">**コメント**</span><span class="sxs-lookup"><span data-stu-id="48ba3-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48ba3-127">MainDlg.cpp はフォーム マネージャーを開き、フォームを選択できます。</span><span class="sxs-lookup"><span data-stu-id="48ba3-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="48ba3-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="48ba3-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="48ba3-129">MFCMAPI は **MAPIOpenFormMgr** メソッドを使用してフォーム マネージャーを開き、フォームを選択できます。</span><span class="sxs-lookup"><span data-stu-id="48ba3-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48ba3-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="48ba3-130">See also</span></span>



<span data-ttu-id="48ba3-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="48ba3-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

