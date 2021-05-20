---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437652"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="2ff33-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="2ff33-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="2ff33-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ff33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ff33-105">メッセージのカプセル化形式 (TNEF) データ ストリームで、Transport-Neutralの受信者テーブルのビューをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2ff33-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="2ff33-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ff33-106">Parameters</span></span>

 <span data-ttu-id="2ff33-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ff33-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2ff33-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="2ff33-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2ff33-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="2ff33-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="2ff33-110">[in]ビューがエンコードされる受信者テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ff33-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="2ff33-111">_lpRecipientTable パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="2ff33-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ff33-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ff33-112">Return value</span></span>

<span data-ttu-id="2ff33-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ff33-113">S_OK</span></span> 
  
> <span data-ttu-id="2ff33-114">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="2ff33-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ff33-115">注釈</span><span class="sxs-lookup"><span data-stu-id="2ff33-115">Remarks</span></span>

<span data-ttu-id="2ff33-116">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::EncodingRecips** メソッドを呼び出して、特定の受信者テーブル ビューに対して TNEF エンコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2ff33-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="2ff33-117">TNEF エンコードは、たとえば、プロバイダーまたはゲートウェイが受信者テーブルの特定の列セット、並べ替え順序、または制限を必要とする場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2ff33-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="2ff33-118">プロバイダーまたはゲートウェイは  _、lpRecipientTable_ パラメーターでエンコードされるテーブル ビューを渡します。</span><span class="sxs-lookup"><span data-stu-id="2ff33-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="2ff33-119">TNEF 実装では、指定された列セット、並べ替え順序、制限、および位置を使用して、受信者テーブルを指定したビューでエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2ff33-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="2ff33-120">プロバイダーまたはゲートウェイが  _lpRecipientTable_ で NULL を渡した場合、TNEF は [IMessage::GetRecipientTable](imessage-getrecipienttable.md) メソッドを使用してエンコードされているメッセージから受信者テーブルを取得し、テーブルのすべての行をテーブルの現在の設定を使用して TNEF ストリームに処理します。</span><span class="sxs-lookup"><span data-stu-id="2ff33-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="2ff33-121">_lpRecipientTable_ で NULL を使用して **EncodeRecips** を呼び出すのは、すべてのメッセージ受信者をエンコードするため、ulFlags パラメーターに TNEF_PROP_INCLUDE フラグを指定して [ITnef::AddProps](itnef-addprops.md)メソッドを呼び出し _、lpPropList_ パラメーターで PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを呼び出すのと同じです。 </span><span class="sxs-lookup"><span data-stu-id="2ff33-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="2ff33-122">特定の受信者テーブル ビューをエンコードする必要がない限り **、EncodeRecips** を呼び出す必要はほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="2ff33-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="2ff33-123">外部メッセージング システムには、受信者リストのエンコードに関する一般的なニーズを処理するのに十分な強力な受信者リストを処理する機能がほとんど常に備わっています。したがって、これらのシステムは、この目的のために TNEF をほとんど必要としません。</span><span class="sxs-lookup"><span data-stu-id="2ff33-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ff33-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ff33-124">See also</span></span>



[<span data-ttu-id="2ff33-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="2ff33-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="2ff33-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="2ff33-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="2ff33-127">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ff33-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="2ff33-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ff33-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

