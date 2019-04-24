---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279602"
---
# <a name="rowentry"></a><span data-ttu-id="f5f3d-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="f5f3d-103">ROWENTRY</span></span>

<span data-ttu-id="f5f3d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5f3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5f3d-105">[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスを使用して、テーブル内のその行に対して実行される行と操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="f5f3d-106">Members</span><span class="sxs-lookup"><span data-stu-id="f5f3d-106">Members</span></span>

<span data-ttu-id="f5f3d-107">**ulrowflags**</span><span class="sxs-lookup"><span data-stu-id="f5f3d-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="f5f3d-108">データに対して実行する操作の1つを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="f5f3d-109">ROW_ADD: 新しい行としてテーブルにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="f5f3d-110">ROW_MODIFY: テーブルのこの行を変更します。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="f5f3d-111">ROW_REMOVE: この行を表から削除します。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="f5f3d-112">ROW_EMPTY: 行データをテーブルに追加しません。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="f5f3d-113">(行は空です。)</span><span class="sxs-lookup"><span data-stu-id="f5f3d-113">(The row is empty.)</span></span>
    
<span data-ttu-id="f5f3d-114">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="f5f3d-114">**cValues**</span></span>
  
> <span data-ttu-id="f5f3d-115">**rgPropvals**のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="f5f3d-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="f5f3d-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="f5f3d-117">テーブルに挿入する列の値を表す[spropvalue](spropvalue.md)構造の配列。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f5f3d-118">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="f5f3d-118">MFCMAPI reference</span></span>

<span data-ttu-id="f5f3d-119">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f5f3d-120">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="f5f3d-120">**File**</span></span>|<span data-ttu-id="f5f3d-121">**関数**</span><span class="sxs-lookup"><span data-stu-id="f5f3d-121">**Function**</span></span>|<span data-ttu-id="f5f3d-122">**コメント**</span><span class="sxs-lookup"><span data-stu-id="f5f3d-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5f3d-123">ルール</span><span class="sxs-lookup"><span data-stu-id="f5f3d-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="f5f3d-124">crulesdlg:: GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="f5f3d-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="f5f3d-125">以降の**modifytable**アクションに対して選択されたルールの一覧を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5f3d-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5f3d-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5f3d-126">See also</span></span>
  
- [<span data-ttu-id="f5f3d-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5f3d-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="f5f3d-128">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f5f3d-128">MAPI Structures</span></span>](mapi-structures.md)

