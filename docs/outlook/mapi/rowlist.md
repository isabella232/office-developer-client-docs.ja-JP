---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419185"
---
# <a name="rowlist"></a><span data-ttu-id="db7b4-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="db7b4-103">ROWLIST</span></span>

  
  
<span data-ttu-id="db7b4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db7b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db7b4-105">行を表す [ROWENTRY](rowentry.md) 構造体の配列と [、IExchangeModifyTable](iexchangemodifytableiunknown.md) インターフェイスを介してテーブル内の行に対して実行される操作を格納します。</span><span class="sxs-lookup"><span data-stu-id="db7b4-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="db7b4-106">Members</span><span class="sxs-lookup"><span data-stu-id="db7b4-106">Members</span></span>

 <span data-ttu-id="db7b4-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="db7b4-107">**cEntries**</span></span>
  
> <span data-ttu-id="db7b4-108">**aEntries** メンバーで指定された配列内のエントリの数。</span><span class="sxs-lookup"><span data-stu-id="db7b4-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="db7b4-109">**aEntries[MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="db7b4-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="db7b4-110">行と、テーブル内のそれらの行に対して実行される操作を含む **ROWENTRY** 構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="db7b4-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="db7b4-111">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="db7b4-111">MFCMAPI reference</span></span>

<span data-ttu-id="db7b4-112">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db7b4-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="db7b4-113">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="db7b4-113">**File**</span></span>|<span data-ttu-id="db7b4-114">**関数**</span><span class="sxs-lookup"><span data-stu-id="db7b4-114">**Function**</span></span>|<span data-ttu-id="db7b4-115">**コメント**</span><span class="sxs-lookup"><span data-stu-id="db7b4-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="db7b4-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="db7b4-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="db7b4-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="db7b4-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="db7b4-118">後続の ModifyTable アクションで選択したルールの一覧を **作成するために使用** します。</span><span class="sxs-lookup"><span data-stu-id="db7b4-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db7b4-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="db7b4-119">See also</span></span>



[<span data-ttu-id="db7b4-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="db7b4-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="db7b4-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="db7b4-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="db7b4-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="db7b4-122">MAPI Structures</span></span>](mapi-structures.md)

