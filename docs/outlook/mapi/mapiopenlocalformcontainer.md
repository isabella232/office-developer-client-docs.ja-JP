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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c00c2fa04ae7e89f8c23c085ba021a935748ad4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801523"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="1e94e-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="1e94e-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="1e94e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e94e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e94e-105">ローカル フォーム ライブラリへのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1e94e-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e94e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1e94e-106">Header file:</span></span>  <br/> |<span data-ttu-id="1e94e-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="1e94e-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1e94e-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="1e94e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1e94e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1e94e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1e94e-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1e94e-110">Called by:</span></span>  <br/> |<span data-ttu-id="1e94e-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="1e94e-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="1e94e-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="1e94e-112">Parameters</span></span>

 <span data-ttu-id="1e94e-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="1e94e-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="1e94e-114">[out]ローカル フォーム ライブラリのインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1e94e-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e94e-115">Return value</span><span class="sxs-lookup"><span data-stu-id="1e94e-115">Return value</span></span>

<span data-ttu-id="1e94e-116">なし。</span><span class="sxs-lookup"><span data-stu-id="1e94e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e94e-117">備考</span><span class="sxs-lookup"><span data-stu-id="1e94e-117">Remarks</span></span>

<span data-ttu-id="1e94e-118">ライブラリに、プログラムすることがなく MAPI にログオン フォームの特定のアプリケーションをインストールするのには、サード ・ パーティ製のインストール プログラムによってポインターが返されるインターフェイスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1e94e-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1e94e-119">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1e94e-119">MFCMAPI reference</span></span>

<span data-ttu-id="1e94e-120">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1e94e-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1e94e-121">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1e94e-121">**File**</span></span>|<span data-ttu-id="1e94e-122">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1e94e-122">**Function**</span></span>|<span data-ttu-id="1e94e-123">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1e94e-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e94e-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1e94e-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="1e94e-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="1e94e-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="1e94e-126">MFCMAPI では、 **MAPIOpenLocalFormContainer**メソッドを使用して、新しいウィンドウで表示するのにはローカルのフォームのコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="1e94e-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e94e-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e94e-127">See also</span></span>



<span data-ttu-id="1e94e-128">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1e94e-128">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

