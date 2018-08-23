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
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803789"
---
# <a name="rowentry"></a><span data-ttu-id="58730-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="58730-103">ROWENTRY</span></span>

<span data-ttu-id="58730-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58730-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58730-105">行および[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスを使用して、テーブルにその行に対して実行される操作が含まれています。</span><span class="sxs-lookup"><span data-stu-id="58730-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="58730-106">Members</span><span class="sxs-lookup"><span data-stu-id="58730-106">Members</span></span>

<span data-ttu-id="58730-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="58730-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="58730-108">データに対して実行する次の操作のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="58730-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="58730-109">ROW_ADD: は、新しい行としてテーブルにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="58730-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="58730-110">ROW_MODIFY: は、テーブルの列を変更します。</span><span class="sxs-lookup"><span data-stu-id="58730-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="58730-111">ROW_REMOVE: は、この行をテーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="58730-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="58730-112">ROW_EMPTY: は、テーブルに行のデータを追加できません。</span><span class="sxs-lookup"><span data-stu-id="58730-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="58730-113">(行は空です)。</span><span class="sxs-lookup"><span data-stu-id="58730-113">(The row is empty.)</span></span>
    
<span data-ttu-id="58730-114">**あう**</span><span class="sxs-lookup"><span data-stu-id="58730-114">**cValues**</span></span>
  
> <span data-ttu-id="58730-115">**RgPropvals**のプロパティの値の数。</span><span class="sxs-lookup"><span data-stu-id="58730-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="58730-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="58730-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="58730-117">[SPropValue](spropvalue.md)構造体をテーブルに挿入される列の値を表す配列。</span><span class="sxs-lookup"><span data-stu-id="58730-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="58730-118">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="58730-118">MFCMAPI reference</span></span>

<span data-ttu-id="58730-119">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="58730-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="58730-120">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="58730-120">**File**</span></span>|<span data-ttu-id="58730-121">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="58730-121">**Function**</span></span>|<span data-ttu-id="58730-122">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="58730-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="58730-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="58730-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="58730-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="58730-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="58730-125">**ModifyTable**の後続のアクションを選択したルールの一覧を作成するために使用します。</span><span class="sxs-lookup"><span data-stu-id="58730-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58730-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="58730-126">See also</span></span>
  
- [<span data-ttu-id="58730-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58730-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="58730-128">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="58730-128">MAPI Structures</span></span>](mapi-structures.md)

