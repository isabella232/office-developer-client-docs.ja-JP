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
ms.openlocfilehash: a7bb1aca501e24843950114bb76b6a09b20f2467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801250"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**適用対象**: Outlook 
  
トランスポート プロバイダーを処理する受信者の種類を返します。
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [out]返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 関数が返す文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _lpcAdrType_
  
> [out]_LpppszAdrTypeArray_パラメーターが指す配列内のエントリの数へのポインターです。 
    
 _lpppszAdrTypeArray_
  
> [out]受信者の種類を識別する文字列の配列へのポインターへのポインター。
    
 _lpcMAPIUID_
  
> [out]_LpppUIDArray_パラメーターが指す配列内のエントリの数へのポインターです。 
    
 _lpppUIDArray_
  
> [out]受信者の種類を識別する[MAPIUID](mapiuid.md)構造体へのポインターの配列へのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> トランスポート プロバイダーに処理可能な受信者の種類を正常に表示されます。
    
## <a name="notes-to-implementers"></a>実装者へのメモ

MAPI スプーラーは、トランスポート プロバイダーは処理の受信者の種類を示すことができますので、 [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドの呼び出しからトランスポート プロバイダーを返します後すぐに、 **IXPLogon::AddressTypes**メソッドを呼び出します。 これを示すには、トランスポート プロバイダーは、または必要とするには、文字列へのポインターの配列を_lpppszAdrTypeArray_パラメーター内でポインターを渡すポインターを渡す、 _lpppUIDArray_パラメーター内で**MAPIUID**へのポインターの配列構造体、または両方のパラメーターの値です。 
  
異なる id のプロセスでは、これら 2 つの配列が使用されます。 MAPI および MAPI スプーラー、 _lpppUIDArray_配列の[MAPIUID](mapiuid.md)構造体を使用して、トランスポート プロバイダーによって、またはトランスポート プロバイダーが接続先のメッセージング システムで直接処理されるこれらの受信者のエントリ id を識別するには. MAPI も MAPI スプーラーは、 **MAPIUID**構造体のいずれかに含まれているエントリの識別子を使用してアドレスを展開します。これらの構造体は、受信者の種類の識別にのみ使用されます。 
  
MAPI スプーラーを使用して、文字列の_lpppszAdrTypeArray_パラメーターで比較テストのトランスポート プロバイダーは、送信メッセージの受信者を処理する必要がありますを決めるとき。 メッセージの受信者の**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のプロパティには、トランスポート プロバイダーが提供するメッセージングのアドレスの種類のいずれかを識別する文字列が完全に一致する、プロバイダーはその受信者にメッセージを配信できます。
  
複数のトランスポート プロバイダーは、同じ種類の受信者を処理できる、MAPI は、クライアント アプリケーションのプロファイルで指定されているトランスポートの優先順位に基づくトランスポート プロバイダーを選択します。 を使用するトランスポート プロバイダーを確認するのには、MAPI スプーラーは、優先順位に従って、すべてのプロバイダーが指定した**MAPIUID**構造とし、プロバイダーが指定したアドレスの種類のすべての値の優先順位をスキャンします。 このスキャンの特定の受信者に一致する最初のトランスポート プロバイダーは、この受信者を処理する最初の機会を取得します。 そのプロバイダーが、受信者を処理しない場合、MAPI スプーラーは処理されていない任意の受信者、トランスポート プロバイダーを検索するのにはスキャンを継続します。 さらに一致するものが見つからなくなるまで、処理されなかったすべての受信者に配信不能レポートを生成した時点で、スキャンが続行されます。 
  
プロバイダーは、常に特定の受信者の種類のセットをサポートする場合、アドレスの種類とトランスポート プロバイダーは、渡された**MAPIUID**の配列が静的にします。 トランスポート プロバイダーは、これらの配列を動的に構築はその必要はありませんが、 **TransportLogon**への呼び出しで渡された以前のサポート オブジェクトを使用してメモリを割り当てることができます。
  
アドレスの種類と**MAPIUID**の配列に使用されるメモリの最後の呼び出し時にどのトランスポート プロバイダーは、メモリを解放、必要な場合、 [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)メソッドになるまで割り当てられたままです。 トランスポート プロバイダーは、 **TransportLogoff**の呼び出しから返されると、これらの配列の内容を変更できません。 
  
受信者の任意の型を処理できるトランスポート プロバイダーは、 _lpppszAdrTypeArray_パラメーターに NULL を返すことです。 通常、さまざまなメッセージを外部システムに送信メッセージを配信するのには中央のサーバーを使用している LAN ベースのメッセージング システムのトランスポート プロバイダーは、これを行います。 MAPI および MAPI の最後はこの種類のトランスポート プロバイダーをインストールする必要があります、プロファイル内のトランスポート プロバイダーのスプーラーの優先順位です。 
  
アドレスの種類を基に送出された送信メッセージをサポートしていないトランスポート プロバイダーは、 _lpppszAdrTypeArray_で、長さ 0 の文字列を 1 つを返す必要があります。 トランスポート プロバイダーに受信者の種類がサポートしていない場合は、 **MAPIUID**構造体とアドレスの種類の空の文字列の NULL を渡す必要があること。 この種類のトランスポート プロバイダーは、メッセージのプリプロセッサをインストールするのには最も一般的に使用します。 
  
## <a name="see-also"></a>関連項目



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

