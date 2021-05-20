---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436245"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="a8e67-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="a8e67-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="a8e67-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8e67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8e67-105">MAPI テーブル オブジェクトのインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a8e67-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="a8e67-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a8e67-106">Parameters</span></span>

 <span data-ttu-id="a8e67-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8e67-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a8e67-108">[in]予約済み。0 (ゼロ) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8e67-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="a8e67-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="a8e67-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="a8e67-110">新しい権限を設定します。</span><span class="sxs-lookup"><span data-stu-id="a8e67-110">Sets new rights.</span></span>
    
<span data-ttu-id="a8e67-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="a8e67-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="a8e67-112">このACLTABLE_FREEBUSY、新しい空き時間情報の権限の詳細な表示を提供します。</span><span class="sxs-lookup"><span data-stu-id="a8e67-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="a8e67-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="a8e67-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="a8e67-114">このACLTABLE_FREEBUSY、新しい空き時間情報の権限を簡単に表示します。</span><span class="sxs-lookup"><span data-stu-id="a8e67-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="a8e67-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a8e67-115">_lppTable_</span></span>
  
> <span data-ttu-id="a8e67-116">[out] [IMAPITable : テーブル オブジェクトを含む IUnknown](imapitableiunknown.md) インターフェイスをポイントします。</span><span class="sxs-lookup"><span data-stu-id="a8e67-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="a8e67-117">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a8e67-117">MFCMAPI reference</span></span>

<span data-ttu-id="a8e67-118">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8e67-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a8e67-119">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a8e67-119">**File**</span></span>|<span data-ttu-id="a8e67-120">**関数**</span><span class="sxs-lookup"><span data-stu-id="a8e67-120">**Function**</span></span>|<span data-ttu-id="a8e67-121">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a8e67-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a8e67-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a8e67-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="a8e67-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="a8e67-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="a8e67-124">MFCMAPI は **、IExchangeModifyTable::GetTable** メソッドを使用してルールのテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="a8e67-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8e67-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8e67-125">See also</span></span>



[<span data-ttu-id="a8e67-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8e67-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


<span data-ttu-id="a8e67-127">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a8e67-127">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

