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
# <a name="hrqueryallrows"></a><span data-ttu-id="3f5c0-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="3f5c0-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="3f5c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f5c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f5c0-105">テーブルのすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f5c0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3f5c0-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f5c0-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="3f5c0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3f5c0-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="3f5c0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f5c0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3f5c0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3f5c0-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3f5c0-110">Called by:</span></span>  <br/> |<span data-ttu-id="3f5c0-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="3f5c0-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="3f5c0-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3f5c0-112">Parameters</span></span>

 <span data-ttu-id="3f5c0-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="3f5c0-113">_ptable_</span></span>
  
> <span data-ttu-id="3f5c0-114">順番行を取得する MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="3f5c0-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="3f5c0-115">_ptaga_</span></span>
  
> <span data-ttu-id="3f5c0-116">順番表の列を示すプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="3f5c0-117">これらのタグは、取得する特定の列を選択するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="3f5c0-118">_ptaga_パラメーターが NULL の場合、 **hrqueryallrows**は、 _ptable_パラメーターで渡された現在のテーブルビューの列セット全体を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="3f5c0-119">_感情_</span><span class="sxs-lookup"><span data-stu-id="3f5c0-119">_pres_</span></span>
  
> <span data-ttu-id="3f5c0-120">順番取得制限を含む[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="3f5c0-121">_プレゼン_パラメーターが NULL の場合、 **hrqueryallrows**は制限を行いません。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="3f5c0-122">_pso_</span><span class="sxs-lookup"><span data-stu-id="3f5c0-122">_psos_</span></span>
  
> <span data-ttu-id="3f5c0-123">順番取得する列の並べ替え順序を識別する[ssortorderset](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="3f5c0-124">_pso_パラメーターが NULL の場合は、テーブルの既定の並べ替え順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="3f5c0-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="3f5c0-125">_crowsMax_</span></span>
  
> <span data-ttu-id="3f5c0-126">順番取得する行の最大数。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="3f5c0-127">_crowsMax_パラメーターの値が0の場合、取得される行の数に制限は設定されません。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="3f5c0-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="3f5c0-128">_pprows_</span></span>
  
> <span data-ttu-id="3f5c0-129">読み上げ取得したテーブルの行へのポインターの配列を含む、返された[rowset](srowset.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3f5c0-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="3f5c0-130">Return value</span></span>

<span data-ttu-id="3f5c0-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f5c0-131">S_OK</span></span> 
  
> <span data-ttu-id="3f5c0-132">呼び出しは、テーブルの予測された行を取得しています。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="3f5c0-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="3f5c0-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="3f5c0-134">テーブル内の行数が、 _crowsMax_パラメーターに渡された数値よりも大きくなっています。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3f5c0-135">注釈</span><span class="sxs-lookup"><span data-stu-id="3f5c0-135">Remarks</span></span>

<span data-ttu-id="3f5c0-136">クライアントアプリケーションまたはサービスプロバイダーは、"終了" パラメーターで指定された制限を課すのではなく、 **hrqueryallrows**が取得し__ ようとしている行の数を制御できません。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="3f5c0-137">_crowsMax_パラメーターでは、取得を特定の数のテーブル行に制限せずに、取得したすべての行の保持に使用できるメモリの最大量を定義します。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="3f5c0-138">大規模メモリオーバーフローに対する保護は、 _crowsMax_を設定することによって提供される stopgap 機能です。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="3f5c0-139">error return MAPI_E_TABLE_TOO_BIG は、テーブルに含まれる行が多すぎて、一度にすべてのメモリに保持されていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="3f5c0-140">通常、メッセージストアテーブルやプロバイダーテーブルなどの小さなテーブルは、通常**hrqueryallrows**を使用して安全に取得できます。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="3f5c0-141">contents [:: QueryRows](imapitable-queryrows.md)メソッドを使用して、コンテンツテーブルや受信者テーブルなど、非常に大きなテーブルがサブセクションでトラバースされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="3f5c0-142">**hrqueryallrows**が呼び出されたときにテーブルのプロパティが未定義になっている場合は、プロパティの種類が PT_NULL およびプロパティ識別子の PROP_ID_NULL で返されます。</span><span class="sxs-lookup"><span data-stu-id="3f5c0-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

