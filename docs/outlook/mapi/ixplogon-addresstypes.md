---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3423391ce6744f7a21bed337778fd8a76aa15d4c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587812"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーが処理する受信者の種類を返します。
  
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
  
> [out]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _lpcAdrType_
  
> [out]  _lpppszAdrTypeArray_ パラメーターが指す配列内のエントリ数へのポインター。 
    
 _lpppszAdrTypeArray_
  
> [out]受信者の種類を識別する文字列の配列へのポインター。
    
 _lpcMAPIUID_
  
> [out]  _lpppUIDArray_ パラメーターが指す配列内のエントリ数へのポインター。 
    
 _lpppUIDArray_
  
> [out]受信者の種類を識別する [MAPIUID](mapiuid.md) 構造体へのポインターの配列へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> トランスポート プロバイダーは、処理できる受信者の種類を正常に示しました。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI スプーラーは、トランスポート プロバイダーが [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドへの呼び出しから返された直後に **IXPLogon::AddressTypes** メソッドを呼び出し、トランスポート プロバイダーが処理する受信者の種類を示します。 これを示すために、トランスポート プロバイダーは  _、lpppszAdrTypeArray_ パラメーターに文字列へのポインターの配列へのポインターを渡す必要があります。または  _、lpppUIDArray_ パラメーターに **MAPIUID** 構造体へのポインターの配列へのポインターを渡すか、両方のパラメーターの値を渡す必要があります。 
  
これら 2 つの配列は、異なる識別プロセスに使用されます。 MAPI と MAPI スプーラーは _、lpppUIDArray_ 配列の [MAPIUID](mapiuid.md)構造体を使用して、トランスポート プロバイダーまたはトランスポート プロバイダーが接続するメッセージング システムによって直接処理される受信者エントリ識別子を識別します。 MAPI スプーラーも MAPI スプーラーも、これらの **MAPIUID** 構造体に含まれるエントリ識別子を使用してアドレスを展開しません。これらの構造は、受信者の種類の識別にのみ使用されます。 
  
MAPI スプーラーは、送信メッセージの受信者を処理するトランスポート プロバイダーを決定するときに、比較テストに  _lpppszAdrTypeArray_ パラメーター内の各文字列を使用します。 メッセージ受信者の PR_ADDRTYPE ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティが、トランスポート プロバイダーが提供するメッセージング アドレスの種類のいずれかを識別する文字列と完全に一致する場合、プロバイダーはメッセージをその受信者に配信できます。 
  
複数のトランスポート プロバイダーが同じ種類の受信者を処理できる場合、MAPI は、クライアント アプリケーションのプロファイルに示されているトランスポート優先度の順序に基づいてトランスポート プロバイダーを選択します。 使用するトランスポート プロバイダーを決定するために、MAPI スプーラーは、プロバイダー指定のすべての **MAPIUID** 構造体を優先度順にスキャンし、その後、プロバイダーが指定したアドレスの種類の値をすべて優先度順にスキャンします。 このスキャンで特定の受信者に一致する最初のトランスポート プロバイダーは、この受信者を処理する最初の機会を取得します。 そのプロバイダーが受信者を処理しない場合、MAPI スプーラーはスキャンを続行して、まだ処理されていない受信者のトランスポート プロバイダーを検索します。 スキャンは、それ以上一致が見つからないまで続きます。その時点で、処理されていない受信者に対して配信されないレポートが生成されます。 
  
プロバイダーが常に特定の受信者の種類のセットをサポートしている場合、トランスポート プロバイダーが渡したアドレスの種類と **MAPIUID** 配列は静的になります。 トランスポート プロバイダーは、これらの配列を動的に構築する場合 **、TransportLogon** の呼び出しで以前に渡されたサポート オブジェクトを使用してメモリを割り当て可能ですが、これは必要ありません。
  
アドレスの種類と **MAPIUID** 配列に使用されるメモリは [、IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) メソッドを最後に呼び出すまで割り当てられたままにし、その時点でトランスポート プロバイダーは必要に応じてメモリを解放できます。 トランスポート プロバイダーは、TransportLogoff 呼び出しから返された後に、これらの配列の内容 **を変更する必要** があります。 
  
任意の種類の受信者を処理できるトランスポート プロバイダーは  _、lpppszAdrTypeArray_ パラメーターで NULL を返します。 中央サーバーを使用してさまざまな外部メッセージ システムに送信メッセージを配信する LAN ベースのメッセージング システムのトランスポート プロバイダーは、一般的にこれを行います。 この種類のトランスポート プロバイダーは、プロファイル内のトランスポート プロバイダーの MAPI および MAPI スプーラーの優先順位で最後にインストールする必要があります。 
  
アドレスの種類に基づいて送信される送信メッセージをサポートしないトランスポート プロバイダーは  _、lpppszAdrTypeArray_ の 1 つの長さ 0 の文字列を返す必要があります。 トランスポート プロバイダーが受信者の種類をサポートしている場合は **、MAPIUID** 構造体に NULL を渡し、アドレスの種類に空の文字列を渡す必要があります。 この種類のトランスポート プロバイダーは、メッセージ プリプロセッサのインストールに最も一般的に使用されます。 
  
## <a name="see-also"></a>関連項目



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

