---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417162"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="cfdbf-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="cfdbf-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="cfdbf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfdbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfdbf-105">新しい行を追加するか、既存の行を変更して、状態テーブルを変更します。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cfdbf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cfdbf-106">Parameters</span></span>

 <span data-ttu-id="cfdbf-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="cfdbf-107">_cValues_</span></span>
  
> <span data-ttu-id="cfdbf-108">[in]新しいまたは変更された状態テーブル行に含めるプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="cfdbf-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="cfdbf-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="cfdbf-110">[in]新しいまたは変更された状態テーブル行に列として含めるプロパティを記述するプロパティ値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="cfdbf-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cfdbf-111">_ulFlags_</span></span>
  
> <span data-ttu-id="cfdbf-112">[in]状態テーブル行を定義する情報の処理方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="cfdbf-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-113">The following flag can be set:</span></span>
    
<span data-ttu-id="cfdbf-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="cfdbf-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="cfdbf-115">新しい行ではなく  _、lpColumnVals_ が指す配列に含まれるプロパティを既存の状態テーブル行と結合する MAPI を指示します。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cfdbf-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="cfdbf-116">Return value</span></span>

<span data-ttu-id="cfdbf-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="cfdbf-117">S_OK</span></span> 
  
> <span data-ttu-id="cfdbf-118">状態テーブルが正常に更新されました。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cfdbf-119">注釈</span><span class="sxs-lookup"><span data-stu-id="cfdbf-119">Remarks</span></span>

<span data-ttu-id="cfdbf-120">**IMAPISupport::ModifyStatusRow** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="cfdbf-121">サービス プロバイダーは、 **ログオン時に ModifyStatusRow** を呼び出して、状態テーブルに行を追加し、セッション中に行を更新します。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="cfdbf-122">**ModifyStatusRow は** 、状態テーブルの構築に必要な情報を MAPI に提供します。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cfdbf-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cfdbf-123">Notes to callers</span></span>

<span data-ttu-id="cfdbf-124">**ModifyStatusRow** STATUSROW_UPDATEを呼び出して、既存の状態テーブル行のプロパティを変更するときに、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="cfdbf-125">これにより、変更される列だけが  _lpColumnVals_ パラメーターに渡されるという MAPI が通知されます。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="cfdbf-126">クライアントは、状態テーブルの情報を使用して、status オブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="cfdbf-127">状態テーブルの行に含める必要がある列の完全な一覧については、「Status [Tables」を参照してください](status-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="cfdbf-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cfdbf-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="cfdbf-128">See also</span></span>



[<span data-ttu-id="cfdbf-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfdbf-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

