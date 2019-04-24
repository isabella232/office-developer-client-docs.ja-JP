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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357212"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="3e028-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="3e028-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="3e028-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e028-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e028-105">トランスポートプロバイダーが処理する受信者の種類を返します。</span><span class="sxs-lookup"><span data-stu-id="3e028-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="3e028-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3e028-106">Parameters</span></span>

 <span data-ttu-id="3e028-107">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="3e028-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="3e028-108">読み上げ返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="3e028-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="3e028-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3e028-109">The following flag can be set:</span></span>
    
<span data-ttu-id="3e028-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3e028-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3e028-111">返される文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="3e028-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="3e028-112">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="3e028-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3e028-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="3e028-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="3e028-114">読み上げ_lpppszadrtypearray_パラメーターによって指定された配列内のエントリの数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3e028-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="3e028-115">_lpppszadrtypearray_</span><span class="sxs-lookup"><span data-stu-id="3e028-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="3e028-116">読み上げ受信者の種類を識別する文字列の配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3e028-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="3e028-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="3e028-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="3e028-118">読み上げ_lpppuidarray_パラメーターによって指定された配列内のエントリの数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3e028-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="3e028-119">_lpppuidarray_</span><span class="sxs-lookup"><span data-stu-id="3e028-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="3e028-120">読み上げ受信者の種類を識別する[MAPIUID](mapiuid.md)構造体へのポインターの配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3e028-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3e028-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="3e028-121">Return value</span></span>

<span data-ttu-id="3e028-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e028-122">S_OK</span></span> 
  
> <span data-ttu-id="3e028-123">トランスポートプロバイダーは、処理できる受信者の種類を正常に指定しました。</span><span class="sxs-lookup"><span data-stu-id="3e028-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="3e028-124">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="3e028-124">Notes to implementers</span></span>

<span data-ttu-id="3e028-125">MAPI スプーラーは、トランスポートプロバイダーが、トランスポートプロバイダーが処理する受信者の種類を示すことができるように、トランスポートプロバイダーが[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)メソッドへの呼び出しから戻るときに、 **IXPLogon:: AddressTypes**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3e028-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="3e028-126">これを示すために、トランスポートプロバイダーは_lpppszadrtypearray_パラメーターに戻り、文字列へのポインターの配列へのポインターを渡すか、 _lpppuidarray_パラメーターで**MAPIUID**へのポインターの配列へのポインターを返す必要があります。構造体、または両方のパラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="3e028-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="3e028-127">これら2つの配列は、さまざまな識別プロセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e028-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="3e028-128">mapi および mapi スプーラーは、 _lpppuidarray_配列の[MAPIUID](mapiuid.md)構造体を使用して、トランスポートプロバイダーまたはトランスポートプロバイダーが接続するメッセージングシステムによって直接処理される受信者エントリ識別子を識別します。.</span><span class="sxs-lookup"><span data-stu-id="3e028-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="3e028-129">mapi または mapi スプーラーは、これらの**MAPIUID**構造に含まれるエントリ識別子を使用してアドレスを展開しません。これらの構造体は、受信者の種類の識別にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e028-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="3e028-130">MAPI スプーラーは、出力メッセージの受信者を処理する必要があるトランスポートプロバイダーを決定するときに、 _lpppszadrtypearray_パラメーターの各文字列を使用して比較テストを行います。</span><span class="sxs-lookup"><span data-stu-id="3e028-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="3e028-131">メッセージ受信者の**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティが、トランスポートプロバイダーが提供するメッセージングアドレスの種類のいずれかを識別する文字列と正確に一致する場合、プロバイダーはその受信者にメッセージを配信できます。</span><span class="sxs-lookup"><span data-stu-id="3e028-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="3e028-132">複数のトランスポートプロバイダーが同じ種類の受信者を処理できる場合、MAPI はクライアントアプリケーションのプロファイルに示されているトランスポート優先順位に基づいてトランスポートプロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="3e028-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="3e028-133">使用するトランスポートプロバイダーを決定するために、MAPI スプーラーは、プロバイダーによって指定されたすべての**MAPIUID**構造を優先順位に従ってスキャンし、次に、プロバイダー指定のすべてのアドレスの種類の値を優先順にスキャンします。</span><span class="sxs-lookup"><span data-stu-id="3e028-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="3e028-134">このスキャンの特定の受信者に一致する最初のトランスポートプロバイダーは、この受信者を最初に処理する機会を取得します。</span><span class="sxs-lookup"><span data-stu-id="3e028-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="3e028-135">そのプロバイダーが受信者を処理しない場合、MAPI スプーラーはスキャンを続行して、まだ処理されていない受信者のトランスポートプロバイダーを検索します。</span><span class="sxs-lookup"><span data-stu-id="3e028-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="3e028-136">スキャンは、それ以上一致が見つからない限り続行され、その時点で、処理されていない受信者に対して配信不能レポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="3e028-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="3e028-137">プロバイダーが常に特定の受信者の種類のセットをサポートしている場合、トランスポートプロバイダーが渡されたアドレスの種類と**MAPIUID**配列は静的になることができます。</span><span class="sxs-lookup"><span data-stu-id="3e028-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="3e028-138">トランスポートプロバイダーが動的にこれらの配列を構築する場合は、以前は**transportlogon**への呼び出しで渡された support オブジェクトを使用してメモリを割り当てることができますが、これは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="3e028-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="3e028-139">アドレスの種類と**MAPIUID**の配列に使用されるメモリは、 [IXPLogon:: transportlogoff](ixplogon-transportlogoff.md)メソッドへの最後の呼び出しまで割り当てられたままになります。その時点で、トランスポートプロバイダーは必要に応じてメモリを解放できます。</span><span class="sxs-lookup"><span data-stu-id="3e028-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="3e028-140">トランスポートプロバイダーは、 **transportlogoff**呼び出しから戻った後、これらの配列の内容を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="3e028-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="3e028-141">任意の種類の受信者を処理できるトランスポートプロバイダーは、 _lpppszadrtypearray_パラメーターで NULL を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="3e028-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="3e028-142">中央サーバーを使用して、さまざまな外部メッセージシステムに送信メッセージを配信する、LAN ベースのメッセージングシステムのトランスポートプロバイダーは、一般的にこれを行います。</span><span class="sxs-lookup"><span data-stu-id="3e028-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="3e028-143">この種類のトランスポートプロバイダーは、プロファイルのトランスポートプロバイダーの mapi および mapi スプーラーの優先順位に従って、最後にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e028-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="3e028-144">アドレスの種類に基づいて送信される送信メッセージをサポートしていないトランスポートプロバイダーは、 _lpppszadrtypearray_に1つの長さ0の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="3e028-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="3e028-145">トランスポートプロバイダーが受信者の種類をサポートしていない場合は、 **MAPIUID**構造体に NULL を渡す必要があります。また、アドレスの種類には空の文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="3e028-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="3e028-146">この種類のトランスポートプロバイダーは、メッセージプリプロセッサをインストールするために最もよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e028-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e028-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e028-147">See also</span></span>



[<span data-ttu-id="3e028-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="3e028-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="3e028-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="3e028-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="3e028-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3e028-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3e028-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e028-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

