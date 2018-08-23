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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 87696ceea96bd2f51bfe5a0b062499946179c8b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582561"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="1ddd6-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="1ddd6-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="1ddd6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ddd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ddd6-105">ローカル フォーム ライブラリへのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1ddd6-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ddd6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1ddd6-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ddd6-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="1ddd6-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1ddd6-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="1ddd6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1ddd6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1ddd6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1ddd6-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1ddd6-110">Called by:</span></span>  <br/> |<span data-ttu-id="1ddd6-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="1ddd6-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="1ddd6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1ddd6-112">Parameters</span></span>

 <span data-ttu-id="1ddd6-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="1ddd6-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="1ddd6-114">[out]ローカル フォーム ライブラリのインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1ddd6-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ddd6-115">Return value</span><span class="sxs-lookup"><span data-stu-id="1ddd6-115">Return value</span></span>

<span data-ttu-id="1ddd6-116">なし。</span><span class="sxs-lookup"><span data-stu-id="1ddd6-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ddd6-117">注釈</span><span class="sxs-lookup"><span data-stu-id="1ddd6-117">Remarks</span></span>

<span data-ttu-id="1ddd6-118">ライブラリに、プログラムすることがなく MAPI にログオン フォームの特定のアプリケーションをインストールするのには、サード ・ パーティ製のインストール プログラムによってポインターが返されるインターフェイスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1ddd6-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ddd6-119">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1ddd6-119">MFCMAPI reference</span></span>

<span data-ttu-id="1ddd6-120">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1ddd6-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ddd6-121">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1ddd6-121">**File**</span></span>|<span data-ttu-id="1ddd6-122">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1ddd6-122">**Function**</span></span>|<span data-ttu-id="1ddd6-123">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1ddd6-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ddd6-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1ddd6-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="1ddd6-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="1ddd6-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="1ddd6-126">MFCMAPI では、 **MAPIOpenLocalFormContainer**メソッドを使用して、新しいウィンドウで表示するのにはローカルのフォームのコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="1ddd6-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ddd6-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ddd6-127">See also</span></span>



<span data-ttu-id="1ddd6-128">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1ddd6-128">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

