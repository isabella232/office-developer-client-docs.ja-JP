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
ms.openlocfilehash: 20831901567f177ada70a6cea94db0537786db94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571438"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="1efe3-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="1efe3-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="1efe3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1efe3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1efe3-105">テーブルの行の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="1efe3-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="1efe3-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="1efe3-106">Parameters</span></span>

 <span data-ttu-id="1efe3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1efe3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1efe3-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="1efe3-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1efe3-109">_あう_</span><span class="sxs-lookup"><span data-stu-id="1efe3-109">_cValues_</span></span>
  
> <span data-ttu-id="1efe3-110">[in]_LpSPropValue_パラメーターが指す[SPropValue](spropvalue.md)構造体のプロパティ値の数です。</span><span class="sxs-lookup"><span data-stu-id="1efe3-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="1efe3-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="1efe3-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="1efe3-112">[in]対象行の列の値を記述する**SPropValue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1efe3-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1efe3-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1efe3-113">Return value</span></span>

<span data-ttu-id="1efe3-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="1efe3-114">S_OK</span></span> 
  
> <span data-ttu-id="1efe3-115">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="1efe3-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1efe3-116">����</span><span class="sxs-lookup"><span data-stu-id="1efe3-116">Remarks</span></span>

<span data-ttu-id="1efe3-117">**ITableData::HrNotify**メソッドは、 _lpSPropValue_パラメーターで指定されたプロパティで示される行に一致する行の TABLE_ROW_MODIFIED の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="1efe3-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="1efe3-118">**HrNotify**は、行に変更があったかどうかに関係なく通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="1efe3-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="1efe3-119">すべてのクライアントやテーブルのビューがあり、そのビューに通知を登録するのには[IMAPITable::Advise](imapitable-advise.md)としているサービス プロバイダーは、この通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="1efe3-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1efe3-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="1efe3-120">See also</span></span>



[<span data-ttu-id="1efe3-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1efe3-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="1efe3-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1efe3-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="1efe3-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1efe3-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

