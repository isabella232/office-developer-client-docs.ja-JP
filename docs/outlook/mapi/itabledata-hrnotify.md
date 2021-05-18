---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413270"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="65765-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="65765-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="65765-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65765-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65765-105">テーブル行の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="65765-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="65765-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="65765-106">Parameters</span></span>

 <span data-ttu-id="65765-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="65765-107">_ulFlags_</span></span>
  
> <span data-ttu-id="65765-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="65765-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="65765-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="65765-109">_cValues_</span></span>
  
> <span data-ttu-id="65765-110">[in]_lpSPropValue_ パラメーターが指す [SPropValue](spropvalue.md)構造体のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="65765-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="65765-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="65765-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="65765-112">[in]ターゲット行の列の値を記述する **SPropValue** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="65765-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="65765-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="65765-113">Return value</span></span>

<span data-ttu-id="65765-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="65765-114">S_OK</span></span> 
  
> <span data-ttu-id="65765-115">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="65765-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65765-116">注釈</span><span class="sxs-lookup"><span data-stu-id="65765-116">Remarks</span></span>

<span data-ttu-id="65765-117">**ITableData::HrNotify** メソッドは _、lpSPropValue_ パラメーターが示すプロパティで説明されている行に一致する行に対して TABLE_ROW_MODIFIED 通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="65765-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="65765-118">**HrNotify は** 、行に変更が発生したかどうかに関係なく通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="65765-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="65765-119">テーブルのビューを持ち [、IMAPITable::Advise](imapitable-advise.md) を呼び出しているすべてのクライアントとサービス プロバイダーは、ビューに関する通知を登録するためにこの通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="65765-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65765-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="65765-120">See also</span></span>



[<span data-ttu-id="65765-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="65765-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="65765-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65765-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="65765-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65765-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

