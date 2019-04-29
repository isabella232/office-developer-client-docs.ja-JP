---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427739"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="6b341-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b341-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="6b341-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b341-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b341-105">ローカルフォームライブラリへのインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="6b341-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b341-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6b341-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b341-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="6b341-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="6b341-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6b341-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b341-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6b341-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6b341-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6b341-110">Called by:</span></span>  <br/> |<span data-ttu-id="6b341-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6b341-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="6b341-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b341-112">Parameters</span></span>

 <span data-ttu-id="6b341-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="6b341-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="6b341-114">読み上げローカルフォームライブラリのインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b341-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b341-115">Return value</span><span class="sxs-lookup"><span data-stu-id="6b341-115">Return value</span></span>

<span data-ttu-id="6b341-116">なし。</span><span class="sxs-lookup"><span data-stu-id="6b341-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b341-117">注釈</span><span class="sxs-lookup"><span data-stu-id="6b341-117">Remarks</span></span>

<span data-ttu-id="6b341-118">ポインターが返されるインターフェイスは、サードパーティのインストールプログラムによって使用され、アプリケーション固有のフォームをプログラムが MAPI にログオンすることなく、ライブラリにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="6b341-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6b341-119">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="6b341-119">MFCMAPI reference</span></span>

<span data-ttu-id="6b341-120">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b341-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6b341-121">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="6b341-121">**File**</span></span>|<span data-ttu-id="6b341-122">**関数**</span><span class="sxs-lookup"><span data-stu-id="6b341-122">**Function**</span></span>|<span data-ttu-id="6b341-123">**コメント**</span><span class="sxs-lookup"><span data-stu-id="6b341-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b341-124">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="6b341-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="6b341-125">CMainDlg:: OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b341-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="6b341-126">mfcmapi は、 **MAPIOpenLocalFormContainer**メソッドを使用して、ローカルフォームコンテナーを開き、新しいウィンドウにレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="6b341-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b341-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b341-127">See also</span></span>



<span data-ttu-id="6b341-128">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="6b341-128">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

