---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412353"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="2428c-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="2428c-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="2428c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2428c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2428c-105">プロファイル管理オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="2428c-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2428c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2428c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2428c-107">mapix</span><span class="sxs-lookup"><span data-stu-id="2428c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="2428c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="2428c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2428c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2428c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2428c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2428c-110">Called by:</span></span>  <br/> |<span data-ttu-id="2428c-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2428c-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="2428c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2428c-112">Parameters</span></span>

 <span data-ttu-id="2428c-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2428c-113">_ulFlags_</span></span>
  
> <span data-ttu-id="2428c-114">順番サービスエントリ関数のオプションを示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2428c-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="2428c-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="2428c-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="2428c-116">読み上げ新しいプロファイル管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2428c-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2428c-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="2428c-117">Return value</span></span>

<span data-ttu-id="2428c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2428c-118">S_OK</span></span> 
  
> <span data-ttu-id="2428c-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2428c-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2428c-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2428c-120">MFCMAPI reference</span></span>

<span data-ttu-id="2428c-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2428c-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2428c-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2428c-122">**File**</span></span>|<span data-ttu-id="2428c-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="2428c-123">**Function**</span></span>|<span data-ttu-id="2428c-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2428c-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2428c-125">MAPIObjects</span><span class="sxs-lookup"><span data-stu-id="2428c-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="2428c-126">cmapiobjects:: GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="2428c-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="2428c-127">mfcmapi は、 **MAPIAdminProfiles**メソッドを使用して、プロファイル管理オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="2428c-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2428c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="2428c-128">See also</span></span>



[<span data-ttu-id="2428c-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="2428c-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


<span data-ttu-id="2428c-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2428c-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

