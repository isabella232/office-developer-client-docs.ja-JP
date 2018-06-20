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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: edabb9a0f55cb34b4e144672e91ea50b8e9193b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801228"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="10c0d-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="10c0d-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="10c0d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10c0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10c0d-105">メッセージのトランスポート ニュートラル カプセル化形式 (TNEF) データ ストリーム内のメッセージの受信者テーブルのビューをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="10c0d-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="10c0d-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="10c0d-106">Parameters</span></span>

 <span data-ttu-id="10c0d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="10c0d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="10c0d-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="10c0d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="10c0d-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="10c0d-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="10c0d-110">[in]ビューがエンコードされている受信者テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="10c0d-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="10c0d-111">_LpRecipientTable_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="10c0d-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="10c0d-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="10c0d-112">Return value</span></span>

<span data-ttu-id="10c0d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="10c0d-113">S_OK</span></span> 
  
> <span data-ttu-id="10c0d-114">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="10c0d-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10c0d-115">備考</span><span class="sxs-lookup"><span data-stu-id="10c0d-115">Remarks</span></span>

<span data-ttu-id="10c0d-116">プロバイダー、メッセージ ストア プロバイダーでは、TNEF エンコード受信者テーブルの特定のビューを実行するのにはゲートウェイの呼び出し、 **ITnef::EncodeRecips**メソッドを転送します。</span><span class="sxs-lookup"><span data-stu-id="10c0d-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="10c0d-117">TNEF エンコードは便利ですが、たとえば、プロバイダーまたはゲートウェイが必要な場合、特定の列のセット、並べ替え順、または制限、受信者テーブルのです。</span><span class="sxs-lookup"><span data-stu-id="10c0d-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="10c0d-118">プロバイダーまたはゲートウェイは、 _lpRecipientTable_パラメーターでエンコードするテーブルのビューに渡されます。</span><span class="sxs-lookup"><span data-stu-id="10c0d-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="10c0d-119">TNEF の実装では、指定したビューを指定した列のセット、並べ替え順、制限、および位置を使用して受信者テーブルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="10c0d-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="10c0d-120">場合は、プロバイダーまたはゲートウェイ_lpRecipientTable_に NULL を渡すと、TNEF は、 [IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを使用してエンコードされているメッセージの受信者テーブルを取得し、TNEF ストリームを使用して、テーブルのすべての行を処理しますテーブルの現在の設定です。</span><span class="sxs-lookup"><span data-stu-id="10c0d-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="10c0d-121">_LpRecipientTable_に NULL を使用して**EncodeRecips**を呼び出す、すべてのメッセージ受信者をエンコードし、 _ulFlags_パラメーターと**PR_ に TNEF_PROP_INCLUDE フラグを指定して[ITnef::AddProps](itnef-addprops.md)メソッドを呼び出すことと同じです。MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティの_lpPropList_パラメーターにします。</span><span class="sxs-lookup"><span data-stu-id="10c0d-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="10c0d-122">受信者テーブルの特定のビューをエンコードする必要がない限り、 **EncodeRecips**を呼び出すことはほとんど必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="10c0d-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="10c0d-123">外部のメッセージング システムが受信者リストをエンコードの一般的なニーズを処理するのに十分では受信者の一覧を処理するための機能をほぼ常にあります。したがって、これらのシステムでは、この目的のための TNEF ほとんどありませんが必要です。</span><span class="sxs-lookup"><span data-stu-id="10c0d-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10c0d-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="10c0d-124">See also</span></span>



[<span data-ttu-id="10c0d-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="10c0d-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="10c0d-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="10c0d-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="10c0d-127">PidTagMessageRecipients の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="10c0d-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="10c0d-128">ITnef: IUnknown</span><span class="sxs-lookup"><span data-stu-id="10c0d-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

