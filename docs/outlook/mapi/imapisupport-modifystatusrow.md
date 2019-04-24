---
title: imapisupportmodifystatusrow
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316644"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="e2388-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="e2388-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="e2388-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2388-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2388-105">新しい行を追加するか、または既存の行を変更して、状態テーブルを変更します。</span><span class="sxs-lookup"><span data-stu-id="e2388-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e2388-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2388-106">Parameters</span></span>

 <span data-ttu-id="e2388-107">_cvalues_</span><span class="sxs-lookup"><span data-stu-id="e2388-107">_cValues_</span></span>
  
> <span data-ttu-id="e2388-108">順番新規または変更された状態テーブルの行に含まれるプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="e2388-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="e2388-109">_lpcolumnvals_</span><span class="sxs-lookup"><span data-stu-id="e2388-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="e2388-110">順番新規または変更された状態テーブルの行に列として含まれるプロパティを示すプロパティ値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2388-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="e2388-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2388-111">_ulFlags_</span></span>
  
> <span data-ttu-id="e2388-112">順番状態テーブルの行を定義する情報を処理する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e2388-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="e2388-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e2388-113">The following flag can be set:</span></span>
    
<span data-ttu-id="e2388-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="e2388-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="e2388-115">_lpcolumnvals_で参照されている配列に含まれるプロパティを、新しい行ではなく既存の状態テーブルの行で結合するように MAPI に指示します。</span><span class="sxs-lookup"><span data-stu-id="e2388-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e2388-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="e2388-116">Return value</span></span>

<span data-ttu-id="e2388-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2388-117">S_OK</span></span> 
  
> <span data-ttu-id="e2388-118">状態テーブルが正常に更新されました。</span><span class="sxs-lookup"><span data-stu-id="e2388-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2388-119">解説</span><span class="sxs-lookup"><span data-stu-id="e2388-119">Remarks</span></span>

<span data-ttu-id="e2388-120">**imapisupport:: modifystatusrow**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="e2388-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="e2388-121">サービスプロバイダーは、ログオン時に**modifystatusrow**を呼び出して、状態テーブルに行を追加します。また、その他の場合は、セッション中に行を更新します。</span><span class="sxs-lookup"><span data-stu-id="e2388-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="e2388-122">**modifystatusrow**は、状態テーブルを構築するために必要な情報を MAPI に提供します。</span><span class="sxs-lookup"><span data-stu-id="e2388-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2388-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e2388-123">Notes to callers</span></span>

<span data-ttu-id="e2388-124">**modifystatusrow**を呼び出して、既存の [状態] テーブル行のプロパティを変更する場合は、STATUSROW_UPDATE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="e2388-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="e2388-125">これにより、変更された列だけが_lpcolumnvals_パラメーターに渡されることが MAPI に通知されます。</span><span class="sxs-lookup"><span data-stu-id="e2388-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="e2388-126">クライアントは、状態の表の情報を使用して、状態オブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e2388-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="e2388-127">[状態テーブル] 行に含める必要のある列の完全な一覧については、「 [status Tables](status-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2388-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2388-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2388-128">See also</span></span>



[<span data-ttu-id="e2388-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2388-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

