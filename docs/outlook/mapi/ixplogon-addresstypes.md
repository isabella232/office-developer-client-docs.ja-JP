---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435377"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="a26fe-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="a26fe-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="a26fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a26fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a26fe-105">トランスポート プロバイダーが処理する受信者の種類を返します。</span><span class="sxs-lookup"><span data-stu-id="a26fe-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="a26fe-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a26fe-106">Parameters</span></span>

 <span data-ttu-id="a26fe-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a26fe-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a26fe-108">[out]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a26fe-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="a26fe-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a26fe-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a26fe-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a26fe-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a26fe-111">返される文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="a26fe-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="a26fe-112">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="a26fe-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a26fe-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="a26fe-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="a26fe-114">[out]  _lpppszAdrTypeArray_ パラメーターが指す配列内のエントリ数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a26fe-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="a26fe-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="a26fe-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="a26fe-116">[out]受信者の種類を識別する文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a26fe-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="a26fe-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="a26fe-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="a26fe-118">[out]  _lpppUIDArray_ パラメーターが指す配列内のエントリ数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a26fe-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="a26fe-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="a26fe-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="a26fe-120">[out]受信者の種類を識別する [MAPIUID](mapiuid.md) 構造体へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a26fe-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a26fe-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="a26fe-121">Return value</span></span>

<span data-ttu-id="a26fe-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a26fe-122">S_OK</span></span> 
  
> <span data-ttu-id="a26fe-123">トランスポート プロバイダーは、処理できる受信者の種類を正常に示しました。</span><span class="sxs-lookup"><span data-stu-id="a26fe-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="a26fe-124">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="a26fe-124">Notes to implementers</span></span>

<span data-ttu-id="a26fe-125">MAPI スプーラーは、トランスポート プロバイダーが [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドへの呼び出しから返された直後に **IXPLogon::AddressTypes** メソッドを呼び出し、トランスポート プロバイダーが処理する受信者の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="a26fe-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="a26fe-126">これを示すために、トランスポート プロバイダーは  _、lpppszAdrTypeArray_ パラメーターに文字列へのポインターの配列へのポインターを渡す必要があります。または  _、lpppUIDArray_ パラメーターに **MAPIUID** 構造体へのポインターの配列へのポインターを渡すか、両方のパラメーターの値を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a26fe-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="a26fe-127">これら 2 つの配列は、異なる識別プロセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a26fe-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="a26fe-128">MAPI と MAPI スプーラーは _、lpppUIDArray_ 配列の [MAPIUID](mapiuid.md)構造体を使用して、トランスポート プロバイダーまたはトランスポート プロバイダーが接続するメッセージング システムによって直接処理される受信者エントリ識別子を識別します。</span><span class="sxs-lookup"><span data-stu-id="a26fe-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="a26fe-129">MAPI スプーラーも MAPI スプーラーも、これらの **MAPIUID** 構造体に含まれるエントリ識別子を使用してアドレスを展開しません。これらの構造は、受信者の種類の識別にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a26fe-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="a26fe-130">MAPI スプーラーは、送信メッセージの受信者を処理するトランスポート プロバイダーを決定するときに、比較テストに  _lpppszAdrTypeArray_ パラメーター内の各文字列を使用します。</span><span class="sxs-lookup"><span data-stu-id="a26fe-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="a26fe-131">メッセージ受信者の PR_ADDRTYPE ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティが、トランスポート プロバイダーが提供するメッセージング アドレスの種類のいずれかを識別する文字列と完全に一致する場合、プロバイダーはメッセージをその受信者に配信できます。 </span><span class="sxs-lookup"><span data-stu-id="a26fe-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="a26fe-132">複数のトランスポート プロバイダーが同じ種類の受信者を処理できる場合、MAPI は、クライアント アプリケーションのプロファイルに示されているトランスポート優先度の順序に基づいてトランスポート プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="a26fe-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="a26fe-133">使用するトランスポート プロバイダーを決定するために、MAPI スプーラーは、プロバイダー指定のすべての **MAPIUID** 構造体を優先度順にスキャンし、その後、プロバイダーが指定したアドレスの種類の値をすべて優先度順にスキャンします。</span><span class="sxs-lookup"><span data-stu-id="a26fe-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="a26fe-134">このスキャンで特定の受信者に一致する最初のトランスポート プロバイダーは、この受信者を処理する最初の機会を取得します。</span><span class="sxs-lookup"><span data-stu-id="a26fe-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="a26fe-135">そのプロバイダーが受信者を処理しない場合、MAPI スプーラーはスキャンを続行して、まだ処理されていない受信者のトランスポート プロバイダーを検索します。</span><span class="sxs-lookup"><span data-stu-id="a26fe-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="a26fe-136">スキャンは、それ以上一致が見つからないまで続きます。その時点で、処理されていない受信者に対して配信されないレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="a26fe-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="a26fe-137">プロバイダーが常に特定の受信者の種類のセットをサポートしている場合、トランスポート プロバイダーが渡したアドレスの種類と **MAPIUID** 配列は静的になります。</span><span class="sxs-lookup"><span data-stu-id="a26fe-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="a26fe-138">トランスポート プロバイダーは、これらの配列を動的に構築する場合 **、TransportLogon** の呼び出しで以前に渡されたサポート オブジェクトを使用してメモリを割り当て可能ですが、これは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a26fe-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="a26fe-139">アドレスの種類と **MAPIUID** 配列に使用されるメモリは [、IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) メソッドを最後に呼び出すまで割り当てられたままにし、その時点でトランスポート プロバイダーは必要に応じてメモリを解放できます。</span><span class="sxs-lookup"><span data-stu-id="a26fe-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="a26fe-140">トランスポート プロバイダーは、TransportLogoff 呼び出しから返された後に、これらの配列の内容 **を変更する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="a26fe-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="a26fe-141">任意の種類の受信者を処理できるトランスポート プロバイダーは  _、lpppszAdrTypeArray_ パラメーターで NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="a26fe-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="a26fe-142">中央サーバーを使用してさまざまな外部メッセージ システムに送信メッセージを配信する LAN ベースのメッセージング システムのトランスポート プロバイダーは、一般的にこれを行います。</span><span class="sxs-lookup"><span data-stu-id="a26fe-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="a26fe-143">この種類のトランスポート プロバイダーは、プロファイル内のトランスポート プロバイダーの MAPI および MAPI スプーラーの優先順位で最後にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a26fe-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="a26fe-144">アドレスの種類に基づいて送信される送信メッセージをサポートしないトランスポート プロバイダーは  _、lpppszAdrTypeArray_ の 1 つの長さ 0 の文字列を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a26fe-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="a26fe-145">トランスポート プロバイダーが受信者の種類をサポートしている場合は **、MAPIUID** 構造体に NULL を渡し、アドレスの種類に空の文字列を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a26fe-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="a26fe-146">この種類のトランスポート プロバイダーは、メッセージ プリプロセッサのインストールに最も一般的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a26fe-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a26fe-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="a26fe-147">See also</span></span>



[<span data-ttu-id="a26fe-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="a26fe-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="a26fe-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="a26fe-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="a26fe-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a26fe-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a26fe-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a26fe-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

