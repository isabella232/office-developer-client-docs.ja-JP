---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418177"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="579c6-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="579c6-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="579c6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="579c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="579c6-105">MAPI テーブル オブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="579c6-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="579c6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="579c6-106">Parameters</span></span>

 <span data-ttu-id="579c6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="579c6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="579c6-108">[in]次のいずれかの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="579c6-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="579c6-109">0 (ゼロ)</span><span class="sxs-lookup"><span data-stu-id="579c6-109">0 (zero)</span></span>
  
> <span data-ttu-id="579c6-110">ROWENTRY 構造体の **ulRowFlags** メンバー [の値を使用](rowentry.md) します。</span><span class="sxs-lookup"><span data-stu-id="579c6-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="579c6-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="579c6-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="579c6-112">新しい権限を設定します。</span><span class="sxs-lookup"><span data-stu-id="579c6-112">Sets new rights.</span></span>
    
<span data-ttu-id="579c6-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="579c6-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="579c6-114">このACLTABLE_FREEBUSY、新しい空き時間情報の権限の詳細な表示を提供します。</span><span class="sxs-lookup"><span data-stu-id="579c6-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="579c6-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="579c6-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="579c6-116">このACLTABLE_FREEBUSY、新しい空き時間情報の権限を簡単に表示します。</span><span class="sxs-lookup"><span data-stu-id="579c6-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="579c6-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="579c6-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="579c6-118">テーブル内のすべての行を置き換える。</span><span class="sxs-lookup"><span data-stu-id="579c6-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="579c6-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="579c6-119">_lpMods_</span></span>
  
> <span data-ttu-id="579c6-120">[in]テーブル オブジェクトのプロパティを含む [ROWLIST](rowlist.md) 構造体をポイントします。</span><span class="sxs-lookup"><span data-stu-id="579c6-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="579c6-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="579c6-121">MFCMAPI reference</span></span>

<span data-ttu-id="579c6-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="579c6-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="579c6-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="579c6-123">**File**</span></span>|<span data-ttu-id="579c6-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="579c6-124">**Function**</span></span>|<span data-ttu-id="579c6-125">**コメント**</span><span class="sxs-lookup"><span data-stu-id="579c6-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="579c6-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="579c6-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="579c6-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="579c6-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="579c6-128">MFCMAPI は **、IExchangeModifyTable::ModifyTable** メソッドを使用して、変更されたルールをルールのテーブルに書き戻します。</span><span class="sxs-lookup"><span data-stu-id="579c6-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="579c6-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="579c6-129">See also</span></span>



[<span data-ttu-id="579c6-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="579c6-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="579c6-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="579c6-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="579c6-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="579c6-132">ROWLIST</span></span>](rowlist.md)


<span data-ttu-id="579c6-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="579c6-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

