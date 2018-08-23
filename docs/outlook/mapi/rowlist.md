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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803787"
---
# <a name="rowlist"></a><span data-ttu-id="d7d45-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="d7d45-103">ROWLIST</span></span>

  
  
<span data-ttu-id="d7d45-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7d45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7d45-105">行と[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスを使用して、テーブルの行に対して実行される操作を表す[ROWENTRY](rowentry.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7d45-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="d7d45-106">Members</span><span class="sxs-lookup"><span data-stu-id="d7d45-106">Members</span></span>

 <span data-ttu-id="d7d45-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="d7d45-107">**cEntries**</span></span>
  
> <span data-ttu-id="d7d45-108">**AEntries**メンバーによって指定された配列内のエントリの数です。</span><span class="sxs-lookup"><span data-stu-id="d7d45-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="d7d45-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="d7d45-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="d7d45-110">行とテーブル内のこれらの行に対して実行される操作を含む**ROWENTRY**構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="d7d45-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d7d45-111">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="d7d45-111">MFCMAPI reference</span></span>

<span data-ttu-id="d7d45-112">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="d7d45-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d7d45-113">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="d7d45-113">**File**</span></span>|<span data-ttu-id="d7d45-114">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="d7d45-114">**Function**</span></span>|<span data-ttu-id="d7d45-115">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="d7d45-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7d45-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d7d45-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="d7d45-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="d7d45-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="d7d45-118">**ModifyTable**の後続のアクションを選択したルールの一覧を作成するために使用します。</span><span class="sxs-lookup"><span data-stu-id="d7d45-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7d45-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7d45-119">See also</span></span>



[<span data-ttu-id="d7d45-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="d7d45-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="d7d45-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7d45-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="d7d45-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d7d45-122">MAPI Structures</span></span>](mapi-structures.md)

