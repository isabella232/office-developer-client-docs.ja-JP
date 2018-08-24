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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 65d633f0c2b0ce56793eaa55a417b5d6a816d449
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589848"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="17a85-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="17a85-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="17a85-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17a85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17a85-105">トランスポート プロバイダーを処理する受信者の種類を返します。</span><span class="sxs-lookup"><span data-stu-id="17a85-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="17a85-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="17a85-106">Parameters</span></span>

 <span data-ttu-id="17a85-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="17a85-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="17a85-108">[out]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="17a85-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="17a85-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="17a85-109">The following flag can be set:</span></span>
    
<span data-ttu-id="17a85-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="17a85-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="17a85-111">関数が返す文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="17a85-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="17a85-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="17a85-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="17a85-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="17a85-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="17a85-114">[out]_LpppszAdrTypeArray_パラメーターが指す配列内のエントリの数へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="17a85-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="17a85-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="17a85-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="17a85-116">[out]受信者の種類を識別する文字列の配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="17a85-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="17a85-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="17a85-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="17a85-118">[out]_LpppUIDArray_パラメーターが指す配列内のエントリの数へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="17a85-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="17a85-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="17a85-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="17a85-120">[out]受信者の種類を識別する[MAPIUID](mapiuid.md)構造体へのポインターの配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="17a85-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="17a85-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="17a85-121">Return value</span></span>

<span data-ttu-id="17a85-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="17a85-122">S_OK</span></span> 
  
> <span data-ttu-id="17a85-123">トランスポート プロバイダーに処理可能な受信者の種類を正常に表示されます。</span><span class="sxs-lookup"><span data-stu-id="17a85-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="17a85-124">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="17a85-124">Notes to implementers</span></span>

<span data-ttu-id="17a85-125">MAPI スプーラーは、トランスポート プロバイダーは処理の受信者の種類を示すことができますので、 [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドの呼び出しからトランスポート プロバイダーを返します後すぐに、 **IXPLogon::AddressTypes**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="17a85-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="17a85-126">これを示すには、トランスポート プロバイダーは、または必要とするには、文字列へのポインターの配列を_lpppszAdrTypeArray_パラメーター内でポインターを渡すポインターを渡す、 _lpppUIDArray_パラメーター内で**MAPIUID**へのポインターの配列構造体、または両方のパラメーターの値です。</span><span class="sxs-lookup"><span data-stu-id="17a85-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="17a85-127">異なる id のプロセスでは、これら 2 つの配列が使用されます。</span><span class="sxs-lookup"><span data-stu-id="17a85-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="17a85-128">MAPI および MAPI スプーラー、 _lpppUIDArray_配列の[MAPIUID](mapiuid.md)構造体を使用して、トランスポート プロバイダーによって、またはトランスポート プロバイダーが接続先のメッセージング システムで直接処理されるこれらの受信者のエントリ id を識別するには.</span><span class="sxs-lookup"><span data-stu-id="17a85-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="17a85-129">MAPI も MAPI スプーラーは、 **MAPIUID**構造体のいずれかに含まれているエントリの識別子を使用してアドレスを展開します。これらの構造体は、受信者の種類の識別にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="17a85-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="17a85-130">MAPI スプーラーを使用して、文字列の_lpppszAdrTypeArray_パラメーターで比較テストのトランスポート プロバイダーは、送信メッセージの受信者を処理する必要がありますを決めるとき。</span><span class="sxs-lookup"><span data-stu-id="17a85-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="17a85-131">メッセージの受信者の**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のプロパティには、トランスポート プロバイダーが提供するメッセージングのアドレスの種類のいずれかを識別する文字列が完全に一致する、プロバイダーはその受信者にメッセージを配信できます。</span><span class="sxs-lookup"><span data-stu-id="17a85-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="17a85-132">複数のトランスポート プロバイダーは、同じ種類の受信者を処理できる、MAPI は、クライアント アプリケーションのプロファイルで指定されているトランスポートの優先順位に基づくトランスポート プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="17a85-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="17a85-133">を使用するトランスポート プロバイダーを確認するのには、MAPI スプーラーは、優先順位に従って、すべてのプロバイダーが指定した**MAPIUID**構造とし、プロバイダーが指定したアドレスの種類のすべての値の優先順位をスキャンします。</span><span class="sxs-lookup"><span data-stu-id="17a85-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="17a85-134">このスキャンの特定の受信者に一致する最初のトランスポート プロバイダーは、この受信者を処理する最初の機会を取得します。</span><span class="sxs-lookup"><span data-stu-id="17a85-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="17a85-135">そのプロバイダーが、受信者を処理しない場合、MAPI スプーラーは処理されていない任意の受信者、トランスポート プロバイダーを検索するのにはスキャンを継続します。</span><span class="sxs-lookup"><span data-stu-id="17a85-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="17a85-136">さらに一致するものが見つからなくなるまで、処理されなかったすべての受信者に配信不能レポートを生成した時点で、スキャンが続行されます。</span><span class="sxs-lookup"><span data-stu-id="17a85-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="17a85-137">プロバイダーは、常に特定の受信者の種類のセットをサポートする場合、アドレスの種類とトランスポート プロバイダーは、渡された**MAPIUID**の配列が静的にします。</span><span class="sxs-lookup"><span data-stu-id="17a85-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="17a85-138">トランスポート プロバイダーは、これらの配列を動的に構築はその必要はありませんが、 **TransportLogon**への呼び出しで渡された以前のサポート オブジェクトを使用してメモリを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="17a85-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="17a85-139">アドレスの種類と**MAPIUID**の配列に使用されるメモリの最後の呼び出し時にどのトランスポート プロバイダーは、メモリを解放、必要な場合、 [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)メソッドになるまで割り当てられたままです。</span><span class="sxs-lookup"><span data-stu-id="17a85-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="17a85-140">トランスポート プロバイダーは、 **TransportLogoff**の呼び出しから返されると、これらの配列の内容を変更できません。</span><span class="sxs-lookup"><span data-stu-id="17a85-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="17a85-141">受信者の任意の型を処理できるトランスポート プロバイダーは、 _lpppszAdrTypeArray_パラメーターに NULL を返すことです。</span><span class="sxs-lookup"><span data-stu-id="17a85-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="17a85-142">通常、さまざまなメッセージを外部システムに送信メッセージを配信するのには中央のサーバーを使用している LAN ベースのメッセージング システムのトランスポート プロバイダーは、これを行います。</span><span class="sxs-lookup"><span data-stu-id="17a85-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="17a85-143">MAPI および MAPI の最後はこの種類のトランスポート プロバイダーをインストールする必要があります、プロファイル内のトランスポート プロバイダーのスプーラーの優先順位です。</span><span class="sxs-lookup"><span data-stu-id="17a85-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="17a85-144">アドレスの種類を基に送出された送信メッセージをサポートしていないトランスポート プロバイダーは、 _lpppszAdrTypeArray_で、長さ 0 の文字列を 1 つを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="17a85-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="17a85-145">トランスポート プロバイダーに受信者の種類がサポートしていない場合は、 **MAPIUID**構造体とアドレスの種類の空の文字列の NULL を渡す必要があること。</span><span class="sxs-lookup"><span data-stu-id="17a85-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="17a85-146">この種類のトランスポート プロバイダーは、メッセージのプリプロセッサをインストールするのには最も一般的に使用します。</span><span class="sxs-lookup"><span data-stu-id="17a85-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17a85-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="17a85-147">See also</span></span>



[<span data-ttu-id="17a85-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="17a85-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="17a85-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="17a85-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="17a85-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="17a85-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="17a85-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17a85-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

