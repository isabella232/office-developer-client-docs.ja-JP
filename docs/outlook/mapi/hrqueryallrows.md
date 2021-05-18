---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422895"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="373fa-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="373fa-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="373fa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="373fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="373fa-105">テーブルのすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="373fa-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="373fa-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="373fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="373fa-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="373fa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="373fa-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="373fa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="373fa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="373fa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="373fa-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="373fa-110">Called by:</span></span>  <br/> |<span data-ttu-id="373fa-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="373fa-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a><span data-ttu-id="373fa-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="373fa-112">Parameters</span></span>

 <span data-ttu-id="373fa-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="373fa-113">_ptable_</span></span>
  
> <span data-ttu-id="373fa-114">[in]行を取得する MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="373fa-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="373fa-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="373fa-115">_ptaga_</span></span>
  
> <span data-ttu-id="373fa-116">[in]テーブル列を示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="373fa-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="373fa-117">これらのタグは、取得する特定の列を選択するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="373fa-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="373fa-118">_ptaga パラメーターが_ NULL の場合 **、HrQueryAllRows は** _ptable_ パラメーターで渡された現在のテーブル ビューの列セット全体を取得します。</span><span class="sxs-lookup"><span data-stu-id="373fa-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="373fa-119">_pres_</span><span class="sxs-lookup"><span data-stu-id="373fa-119">_pres_</span></span>
  
> <span data-ttu-id="373fa-120">[in]取得の [制限を含む SRestriction](srestriction.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="373fa-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="373fa-121">_pres パラメーターが_ NULL の場合 **、HrQueryAllRows は** 制限を行います。</span><span class="sxs-lookup"><span data-stu-id="373fa-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="373fa-122">_psos_</span><span class="sxs-lookup"><span data-stu-id="373fa-122">_psos_</span></span>
  
> <span data-ttu-id="373fa-123">[in]取得する列の並べ替え順序を識別する [SSortOrderSet](ssortorderset.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="373fa-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="373fa-124">_psos パラメーターが_ NULL の場合、テーブルの既定の並べ替え順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="373fa-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="373fa-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="373fa-125">_crowsMax_</span></span>
  
> <span data-ttu-id="373fa-126">[in]取得する行の最大数。</span><span class="sxs-lookup"><span data-stu-id="373fa-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="373fa-127">_crowsMax_ パラメーターの値が 0 の場合、取得される行数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="373fa-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="373fa-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="373fa-128">_pprows_</span></span>
  
> <span data-ttu-id="373fa-129">[out]取得したテーブル行へのポインターの配列を含む、返される [SRowSet](srowset.md) 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="373fa-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="373fa-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="373fa-130">Return value</span></span>

<span data-ttu-id="373fa-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="373fa-131">S_OK</span></span> 
  
> <span data-ttu-id="373fa-132">呼び出しは、テーブルの予想される行を取得しました。</span><span class="sxs-lookup"><span data-stu-id="373fa-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="373fa-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="373fa-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="373fa-134">テーブル内の行数は  _、crowsMax_ パラメーターに渡される数よりも大きくなります。</span><span class="sxs-lookup"><span data-stu-id="373fa-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="373fa-135">注釈</span><span class="sxs-lookup"><span data-stu-id="373fa-135">Remarks</span></span>

<span data-ttu-id="373fa-136">クライアント アプリケーションまたはサービス プロバイダーは、pres パラメーターによって指される制限を課す以外に **、HrQueryAllRows** が取得しようとする行数を  _制御_ できません。</span><span class="sxs-lookup"><span data-stu-id="373fa-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="373fa-137">_crowsMax_ パラメーターは、取得を特定の数のテーブル行に制限するのではなく、取得された行を保持するために使用できる最大メモリ量を定義します。</span><span class="sxs-lookup"><span data-stu-id="373fa-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="373fa-138">大量のメモリ オーバーフローに対する唯一の保護は  _、crowsMax_ を設定することで提供される stopgap 機能です。</span><span class="sxs-lookup"><span data-stu-id="373fa-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="373fa-139">エラーが返MAPI_E_TABLE_TOO_BIGテーブルに含まれる行が多すぎて、メモリ内で一度に保持される行が多すぎます。</span><span class="sxs-lookup"><span data-stu-id="373fa-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="373fa-140">通常、メッセージ ストア テーブルやプロバイダー テーブルなど、小さいテーブルは **、通常、HrQueryAllRows** を使用して安全に取得できます。</span><span class="sxs-lookup"><span data-stu-id="373fa-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="373fa-141">コンテンツ テーブルや受信者テーブルなど、非常に大きい可能性があるテーブルは [、IMAPITable::QueryRows](imapitable-queryrows.md) メソッドを使用してサブセクションで走査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="373fa-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="373fa-142">**HrQueryAllRows** が呼び出された場合、テーブルプロパティが未定義の場合、テーブルプロパティの種類とプロパティPT_NULLプロパティ識別子が返PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="373fa-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

