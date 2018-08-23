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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1be4fd95d29859c542fe553bdc3728ea23444694
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801234"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="e23ff-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="e23ff-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="e23ff-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e23ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e23ff-105">テーブルの行の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="e23ff-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="e23ff-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="e23ff-106">Parameters</span></span>

 <span data-ttu-id="e23ff-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e23ff-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e23ff-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="e23ff-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e23ff-109">_あう_</span><span class="sxs-lookup"><span data-stu-id="e23ff-109">_cValues_</span></span>
  
> <span data-ttu-id="e23ff-110">[in]_LpSPropValue_パラメーターが指す[SPropValue](spropvalue.md)構造体のプロパティ値の数です。</span><span class="sxs-lookup"><span data-stu-id="e23ff-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="e23ff-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="e23ff-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="e23ff-112">[in]対象行の列の値を記述する**SPropValue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e23ff-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e23ff-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e23ff-113">Return value</span></span>

<span data-ttu-id="e23ff-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e23ff-114">S_OK</span></span> 
  
> <span data-ttu-id="e23ff-115">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e23ff-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e23ff-116">����</span><span class="sxs-lookup"><span data-stu-id="e23ff-116">Remarks</span></span>

<span data-ttu-id="e23ff-117">**ITableData::HrNotify**メソッドは、 _lpSPropValue_パラメーターで指定されたプロパティで示される行に一致する行の TABLE_ROW_MODIFIED の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="e23ff-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="e23ff-118">**HrNotify**は、行に変更があったかどうかに関係なく通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="e23ff-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="e23ff-119">すべてのクライアントやテーブルのビューがあり、そのビューに通知を登録するのには[IMAPITable::Advise](imapitable-advise.md)としているサービス プロバイダーは、この通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="e23ff-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e23ff-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="e23ff-120">See also</span></span>



[<span data-ttu-id="e23ff-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e23ff-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="e23ff-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e23ff-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="e23ff-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e23ff-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

