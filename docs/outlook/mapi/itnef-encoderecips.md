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
# <a name="itnefencoderecips"></a><span data-ttu-id="2ac23-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="2ac23-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="2ac23-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ac23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ac23-105">メッセージのトランスポート中立カプセル化形式 (TNEF) データストリームで、メッセージの受信者テーブルのビューをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2ac23-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="2ac23-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ac23-106">Parameters</span></span>

 <span data-ttu-id="2ac23-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ac23-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2ac23-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="2ac23-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2ac23-109">_lp受信者テーブル_</span><span class="sxs-lookup"><span data-stu-id="2ac23-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="2ac23-110">順番ビューがエンコードされている受信者テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ac23-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="2ac23-111">_lp受信者テーブル_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2ac23-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ac23-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ac23-112">Return value</span></span>

<span data-ttu-id="2ac23-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ac23-113">S_OK</span></span> 
  
> <span data-ttu-id="2ac23-114">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="2ac23-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ac23-115">注釈</span><span class="sxs-lookup"><span data-stu-id="2ac23-115">Remarks</span></span>

<span data-ttu-id="2ac23-116">トランスポートプロバイダー、メッセージストアプロバイダー、およびゲートウェイは、 **ITnef:: EncodeRecips**メソッドを呼び出して、特定の受信者テーブルビューの TNEF エンコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2ac23-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="2ac23-117">TNEF エンコードは、たとえばプロバイダーまたはゲートウェイで、特定の列セット、並べ替え順序、または受信者テーブルの制限が必要な場合などに便利です。</span><span class="sxs-lookup"><span data-stu-id="2ac23-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="2ac23-118">プロバイダーまたはゲートウェイは、 _lp受信者テーブル_パラメーターでエンコードされるテーブルビューを渡します。</span><span class="sxs-lookup"><span data-stu-id="2ac23-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="2ac23-119">TNEF 実装は、指定された列セット、並べ替え順序、制限、および位置を使用して、指定されたビューで受信者テーブルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2ac23-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="2ac23-120">_lprecipient テーブル_でプロバイダーまたはゲートウェイが NULL になると、tnef は[IMessage:: get table](imessage-getrecipienttable.md)メソッドを使用してエンコードされているメッセージから受信者テーブルを取得し、次のコードを使用して、テーブルの各行をすべて TNEF ストリームに処理します。表の現在の設定。</span><span class="sxs-lookup"><span data-stu-id="2ac23-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="2ac23-121">_lprecipienttable_で NULL で**EncodeRecips**を呼び出すと、すべてのメッセージの受信者がエンコードされ、 _ulflags_パラメーターと PR_ で TNEF_PROP_INCLUDE フラグを使用して[ITnef:: addprops](itnef-addprops.md)メソッドを呼び出すことと同じになります。 \*\*\*\* _lpproplist_パラメーターの MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="2ac23-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="2ac23-122">特定の受信者テーブルビューをエンコードする必要がある場合を除き、 **EncodeRecips**を呼び出す必要はほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="2ac23-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="2ac23-123">外部メッセージングシステムには、受信者の一覧をエンコードする一般的な要件を十分に処理できる、多くの場合、受信者の一覧を処理する機能が用意されています。そのため、これらのシステムは、この目的のために TNEF を必要としません。</span><span class="sxs-lookup"><span data-stu-id="2ac23-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ac23-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ac23-124">See also</span></span>



[<span data-ttu-id="2ac23-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="2ac23-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="2ac23-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="2ac23-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="2ac23-127">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ac23-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="2ac23-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ac23-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

