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
ms.openlocfilehash: 4cbaf08c58a98be45ad33aebb8f230fb53c234f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577661"
---
# <a name="rowlist"></a><span data-ttu-id="71d38-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="71d38-103">ROWLIST</span></span>

  
  
<span data-ttu-id="71d38-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71d38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71d38-105">行と[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスを使用して、テーブルの行に対して実行される操作を表す[ROWENTRY](rowentry.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71d38-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="71d38-106">Members</span><span class="sxs-lookup"><span data-stu-id="71d38-106">Members</span></span>

 <span data-ttu-id="71d38-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="71d38-107">**cEntries**</span></span>
  
> <span data-ttu-id="71d38-108">**AEntries**メンバーによって指定された配列内のエントリの数です。</span><span class="sxs-lookup"><span data-stu-id="71d38-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="71d38-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="71d38-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="71d38-110">行とテーブル内のこれらの行に対して実行される操作を含む**ROWENTRY**構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="71d38-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="71d38-111">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="71d38-111">MFCMAPI reference</span></span>

<span data-ttu-id="71d38-112">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="71d38-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="71d38-113">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="71d38-113">**File**</span></span>|<span data-ttu-id="71d38-114">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="71d38-114">**Function**</span></span>|<span data-ttu-id="71d38-115">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="71d38-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="71d38-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="71d38-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="71d38-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="71d38-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="71d38-118">**ModifyTable**の後続のアクションを選択したルールの一覧を作成するために使用します。</span><span class="sxs-lookup"><span data-stu-id="71d38-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71d38-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="71d38-119">See also</span></span>



[<span data-ttu-id="71d38-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="71d38-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="71d38-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71d38-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="71d38-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="71d38-122">MAPI Structures</span></span>](mapi-structures.md)

