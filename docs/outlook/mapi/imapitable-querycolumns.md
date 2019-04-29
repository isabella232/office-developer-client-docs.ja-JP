---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410106"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="0e286-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="0e286-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="0e286-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e286-105">テーブルの列のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="0e286-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="0e286-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e286-106">Parameters</span></span>

 <span data-ttu-id="0e286-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e286-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0e286-108">順番返される列セットを示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0e286-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="0e286-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0e286-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0e286-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="0e286-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="0e286-111">テーブルは使用可能なすべての列を返します。</span><span class="sxs-lookup"><span data-stu-id="0e286-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="0e286-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="0e286-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="0e286-113">読み上げ列セットのプロパティタグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0e286-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0e286-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e286-114">Return value</span></span>

<span data-ttu-id="0e286-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e286-115">S_OK</span></span> 
  
> <span data-ttu-id="0e286-116">列セットが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="0e286-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="0e286-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="0e286-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="0e286-118">別の操作が進行中であるため、列セットの取得操作を開始できません。</span><span class="sxs-lookup"><span data-stu-id="0e286-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="0e286-119">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e286-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e286-120">注釈</span><span class="sxs-lookup"><span data-stu-id="0e286-120">Remarks</span></span>

<span data-ttu-id="0e286-121">**IMAPITable:: querycolumns**メソッドを呼び出すと、次のものを取得できます。</span><span class="sxs-lookup"><span data-stu-id="0e286-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="0e286-122">テーブルの既定の列セット。</span><span class="sxs-lookup"><span data-stu-id="0e286-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="0e286-123">[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドの呼び出しによって確立された、テーブルの現在の列セット。</span><span class="sxs-lookup"><span data-stu-id="0e286-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="0e286-124">テーブルの完全な列セット。使用可能な列ですが、現在のセットの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="0e286-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="0e286-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0e286-125">Notes to callers</span></span>

<span data-ttu-id="0e286-126">TBL_ALL_COLUMNS フラグを設定しない場合、 **imapitable:: querycolumns**は、テーブルの既定または現在の列セットを返します。これは、テーブルが**IMAPITable:: SetColumns**の呼び出しの影響を受けたかどうかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="0e286-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="0e286-127">**SetColumns**は、テーブルの列セット内の列の順序と選択範囲を変更します。</span><span class="sxs-lookup"><span data-stu-id="0e286-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="0e286-128">TBL_ALL_COLUMNS フラグを設定した場合、 **querycolumns**は、テーブルの列セットに設定可能なすべての列を返します。</span><span class="sxs-lookup"><span data-stu-id="0e286-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="0e286-129">[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 _lpPropTagArray_パラメーターによって示されるプロパティタグ配列のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="0e286-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e286-130">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="0e286-130">MFCMAPI reference</span></span>

<span data-ttu-id="0e286-131">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e286-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e286-132">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="0e286-132">**File**</span></span>|<span data-ttu-id="0e286-133">**関数**</span><span class="sxs-lookup"><span data-stu-id="0e286-133">**Function**</span></span>|<span data-ttu-id="0e286-134">**コメント**</span><span class="sxs-lookup"><span data-stu-id="0e286-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e286-135">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="0e286-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="0e286-136">CContentsTableListCtrl::D osetcolumns</span><span class="sxs-lookup"><span data-stu-id="0e286-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="0e286-137">mfcmapi は、 **IMAPITable:: querycolumns**メソッドを使用して、テーブルの現在の列セットを取得し、ユーザーが編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="0e286-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e286-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e286-138">See also</span></span>



[<span data-ttu-id="0e286-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="0e286-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="0e286-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0e286-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0e286-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="0e286-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="0e286-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e286-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="0e286-143">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0e286-143">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

