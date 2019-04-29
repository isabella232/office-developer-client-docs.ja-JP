---
title: itabledatahrnotify
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
# <a name="itabledatahrnotify"></a><span data-ttu-id="2ae8c-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="2ae8c-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="2ae8c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ae8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ae8c-105">表の行の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="2ae8c-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="2ae8c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ae8c-106">Parameters</span></span>

 <span data-ttu-id="2ae8c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ae8c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2ae8c-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="2ae8c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2ae8c-109">_cvalues_</span><span class="sxs-lookup"><span data-stu-id="2ae8c-109">_cValues_</span></span>
  
> <span data-ttu-id="2ae8c-110">順番_lpspropvalue_パラメーターによってポイントされている[spropvalue](spropvalue.md)構造のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="2ae8c-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="2ae8c-111">_lpspropvalue_</span><span class="sxs-lookup"><span data-stu-id="2ae8c-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="2ae8c-112">順番ターゲット行の列の値を記述する**spropvalue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ae8c-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ae8c-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ae8c-113">Return value</span></span>

<span data-ttu-id="2ae8c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ae8c-114">S_OK</span></span> 
  
> <span data-ttu-id="2ae8c-115">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2ae8c-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ae8c-116">注釈</span><span class="sxs-lookup"><span data-stu-id="2ae8c-116">Remarks</span></span>

<span data-ttu-id="2ae8c-117">**itabledata:: hrnotify**メソッドは、 _lpspropvalue_パラメーターで指定されたプロパティによって示される行に一致する行に対して TABLE_ROW_MODIFIED 通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="2ae8c-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="2ae8c-118">**hrnotify**は、変更が行に対して発生したかどうかにかかわらず通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="2ae8c-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="2ae8c-119">表のビューを持つすべてのクライアントおよびサービスプロバイダーは、 [「IMAPITable:: アドバイス](imapitable-advise.md)」を参照して、この通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="2ae8c-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ae8c-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ae8c-120">See also</span></span>



[<span data-ttu-id="2ae8c-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2ae8c-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="2ae8c-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2ae8c-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="2ae8c-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ae8c-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

