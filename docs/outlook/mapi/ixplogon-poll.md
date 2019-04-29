---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425275"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="6a5ce-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="6a5ce-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="6a5ce-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a5ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a5ce-105">トランスポートプロバイダーが1つ以上の受信メッセージを受信したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6a5ce-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="6a5ce-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6a5ce-106">Parameters</span></span>

 <span data-ttu-id="6a5ce-107">_lアウト受信_</span><span class="sxs-lookup"><span data-stu-id="6a5ce-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="6a5ce-108">読み上げ受信メッセージの存在を示す値。</span><span class="sxs-lookup"><span data-stu-id="6a5ce-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="6a5ce-109">0以外の値は、受信メッセージがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="6a5ce-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a5ce-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="6a5ce-110">Return value</span></span>

<span data-ttu-id="6a5ce-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a5ce-111">S_OK</span></span> 
  
> <span data-ttu-id="6a5ce-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a5ce-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a5ce-113">注釈</span><span class="sxs-lookup"><span data-stu-id="6a5ce-113">Remarks</span></span>

<span data-ttu-id="6a5ce-114">次に示すように、MAPI スプーラーは**IXPLogon::P oll**メソッドを定期的に呼び出します。これは、トランスポートプロバイダーが新しいメッセージをポーリングする必要があることを示している場合、プロバイダーは、LOGON_SP_POLL フラグを[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)への呼び出しに渡すことによって行われます。メソッドは、セッションの開始時に行います。</span><span class="sxs-lookup"><span data-stu-id="6a5ce-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="6a5ce-115">トランスポートプロバイダーが**ポーリング**呼び出しに応答して、1つまたは複数の受信メッセージを処理できることを示している場合、MAPI スプーラーは[IXPLogon:: startmessage](ixplogon-startmessage.md)メソッドを呼び出して、プロバイダーが最初の受信を処理できるようにします。メッセージ。</span><span class="sxs-lookup"><span data-stu-id="6a5ce-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="6a5ce-116">トランスポートプロバイダーは、 _lな着信_パラメーターの値を0以外の値に設定することにより、受信メッセージを示します。</span><span class="sxs-lookup"><span data-stu-id="6a5ce-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a5ce-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a5ce-117">See also</span></span>



[<span data-ttu-id="6a5ce-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="6a5ce-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="6a5ce-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="6a5ce-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="6a5ce-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a5ce-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

