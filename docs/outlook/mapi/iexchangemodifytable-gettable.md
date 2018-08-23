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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d28ce67c6b45f3d0b04d645946ea3f4b3a263c48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578991"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="01eea-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="01eea-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="01eea-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01eea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01eea-105">MAPI テーブルのオブジェクトのインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="01eea-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="01eea-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="01eea-106">Parameters</span></span>

 <span data-ttu-id="01eea-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="01eea-107">_ulFlags_</span></span>
  
> <span data-ttu-id="01eea-108">[in]予約されています。0 (ゼロ) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="01eea-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="01eea-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="01eea-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="01eea-110">新しい権限を設定します。</span><span class="sxs-lookup"><span data-stu-id="01eea-110">Sets new rights.</span></span>
    
<span data-ttu-id="01eea-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="01eea-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="01eea-112">ACLTABLE_FREEBUSY が渡された場合は、新しい空き時間情報の権限の詳細を表示を提供します。</span><span class="sxs-lookup"><span data-stu-id="01eea-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="01eea-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="01eea-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="01eea-114">ACLTABLE_FREEBUSY が渡された場合は、新しい空き時間情報の権限の表示を提供します。</span><span class="sxs-lookup"><span data-stu-id="01eea-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="01eea-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="01eea-115">_lppTable_</span></span>
  
> <span data-ttu-id="01eea-116">[out]指す、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスは、テーブル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="01eea-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="01eea-117">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="01eea-117">MFCMAPI reference</span></span>

<span data-ttu-id="01eea-118">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="01eea-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="01eea-119">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="01eea-119">**File**</span></span>|<span data-ttu-id="01eea-120">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="01eea-120">**Function**</span></span>|<span data-ttu-id="01eea-121">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="01eea-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="01eea-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="01eea-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="01eea-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="01eea-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="01eea-124">MFCMAPI では、 **IExchangeModifyTable::GetTable**メソッドを使用して、ルールのテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="01eea-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01eea-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="01eea-125">See also</span></span>



[<span data-ttu-id="01eea-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="01eea-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


<span data-ttu-id="01eea-127">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="01eea-127">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

