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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 96fd317c28d95335a3acc5d0603298f2fe8345e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800844"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="da976-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="da976-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="da976-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da976-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da976-105">テーブルの列の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="da976-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="da976-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="da976-106">Parameters</span></span>

 <span data-ttu-id="da976-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da976-107">_ulFlags_</span></span>
  
> <span data-ttu-id="da976-108">[in]のどの列の設定を示すフラグのビットマスクが返されます。</span><span class="sxs-lookup"><span data-stu-id="da976-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="da976-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="da976-109">The following flag can be set:</span></span>
    
<span data-ttu-id="da976-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="da976-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="da976-111">テーブルは、すべての利用可能な列を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="da976-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="da976-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="da976-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="da976-113">[out]列のプロパティ タグを含む[SPropTagArray](sproptagarray.md)構造体へのポインターを設定します。</span><span class="sxs-lookup"><span data-stu-id="da976-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="da976-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="da976-114">Return value</span></span>

<span data-ttu-id="da976-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="da976-115">S_OK</span></span> 
  
> <span data-ttu-id="da976-116">列セットが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="da976-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="da976-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="da976-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="da976-118">別の操作により、列の進行状況の設定の取得操作の開始されます。</span><span class="sxs-lookup"><span data-stu-id="da976-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="da976-119">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da976-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da976-120">備考</span><span class="sxs-lookup"><span data-stu-id="da976-120">Remarks</span></span>

<span data-ttu-id="da976-121">取得する場合に、 **IMAPITable::QueryColumns**メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="da976-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="da976-122">既定の列をテーブルに設定します。</span><span class="sxs-lookup"><span data-stu-id="da976-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="da976-123">表については、 [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドの呼び出しによって設定されるを設定します。</span><span class="sxs-lookup"><span data-stu-id="da976-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="da976-124">テーブル、使用可能な列は必ずしも現在のセットの一部の設定の完全な列。</span><span class="sxs-lookup"><span data-stu-id="da976-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="da976-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="da976-125">Notes to callers</span></span>

<span data-ttu-id="da976-126">TBL_ALL_COLUMNS フラグが設定されていない場合、 **IMAPITable::QueryColumns**は、テーブルの既定値または**IMAPITable::SetColumns**を呼び出すことで、テーブルが影響を受けてかどうかによって、現在の列のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="da976-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="da976-127">**SetColumns**では、順序とテーブルの列のセット内の列の選択範囲を変更します。</span><span class="sxs-lookup"><span data-stu-id="da976-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="da976-128">TBL_ALL_COLUMNS フラグを設定すると、すべての列がテーブルの列のセットにすることのできる**QueryColumns**が返されます。</span><span class="sxs-lookup"><span data-stu-id="da976-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="da976-129">関数を呼び出して、 [MAPIFreeBuffer](mapifreebuffer.md) 、 _lpPropTagArray_パラメーターで示されるプロパティ タグ配列用のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="da976-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="da976-130">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="da976-130">MFCMAPI reference</span></span>

<span data-ttu-id="da976-131">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="da976-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="da976-132">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="da976-132">**File**</span></span>|<span data-ttu-id="da976-133">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="da976-133">**Function**</span></span>|<span data-ttu-id="da976-134">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="da976-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="da976-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="da976-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="da976-136">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="da976-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="da976-137">MFCMAPI では、 **IMAPITable::QueryColumns**メソッドを使用して、現在の列をユーザーが編集できるように、テーブルの設定を取得します。</span><span class="sxs-lookup"><span data-stu-id="da976-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da976-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="da976-138">See also</span></span>



[<span data-ttu-id="da976-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="da976-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="da976-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="da976-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="da976-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="da976-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="da976-142">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="da976-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="da976-143">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="da976-143">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

