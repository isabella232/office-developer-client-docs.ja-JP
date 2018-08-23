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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 06a5c9de5c0ce4c0f936791086a731a55510a124
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592144"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="01e01-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="01e01-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="01e01-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01e01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01e01-105">ステータス テーブルを変更するには、新しい行を追加したり、既存の行を変更します。</span><span class="sxs-lookup"><span data-stu-id="01e01-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="01e01-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="01e01-106">Parameters</span></span>

 <span data-ttu-id="01e01-107">_あう_</span><span class="sxs-lookup"><span data-stu-id="01e01-107">_cValues_</span></span>
  
> <span data-ttu-id="01e01-108">[in]新しいまたは変更された状態のテーブルの行に含まれるプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="01e01-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="01e01-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="01e01-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="01e01-110">[in]新しいまたは変更された状態のテーブルの行の列に含まれるプロパティを記述するプロパティ値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="01e01-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="01e01-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="01e01-111">_ulFlags_</span></span>
  
> <span data-ttu-id="01e01-112">[in]状態テーブルの行を定義する情報の処理方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="01e01-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="01e01-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="01e01-113">The following flag can be set:</span></span>
    
<span data-ttu-id="01e01-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="01e01-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="01e01-115">新しい行ではなく、既存の状態のテーブルの行を_lpColumnVals_が指す配列に含まれるプロパティをマージするための MAPI に指示します。</span><span class="sxs-lookup"><span data-stu-id="01e01-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="01e01-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="01e01-116">Return value</span></span>

<span data-ttu-id="01e01-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="01e01-117">S_OK</span></span> 
  
> <span data-ttu-id="01e01-118">状態テーブルは正しく更新されました。</span><span class="sxs-lookup"><span data-stu-id="01e01-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01e01-119">注釈</span><span class="sxs-lookup"><span data-stu-id="01e01-119">Remarks</span></span>

<span data-ttu-id="01e01-120">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::ModifyStatusRow**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="01e01-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="01e01-121">サービス プロバイダーは、状態テーブルに行を追加するのにはログオン時に、行を更新するのにはセッション中に他の時間に**ModifyStatusRow**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01e01-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="01e01-122">**ModifyStatusRow**は、状態テーブルを構築するために必要な情報を使用して MAPI を提供します。</span><span class="sxs-lookup"><span data-stu-id="01e01-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="01e01-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="01e01-123">Notes to callers</span></span>

<span data-ttu-id="01e01-124">既存の状態テーブルの行のプロパティを変更するのには、 **ModifyStatusRow**を呼び出すときは、STATUSROW_UPDATE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="01e01-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="01e01-125">そう通知 MAPI が変更される列のみが、 _lpColumnVals_パラメーターに渡されています。</span><span class="sxs-lookup"><span data-stu-id="01e01-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="01e01-126">クライアントは、状態オブジェクトにアクセスするのには、状態テーブルの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="01e01-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="01e01-127">状態テーブルの行を列に含める列の一覧については、[ステータス ・ テーブル](status-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01e01-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01e01-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="01e01-128">See also</span></span>



[<span data-ttu-id="01e01-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="01e01-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

