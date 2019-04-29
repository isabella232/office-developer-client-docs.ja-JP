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
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーが処理する受信者の種類を返します。
  
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

 _lアウトフラグ_
  
> 読み上げ返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _lpcAdrType_
  
> 読み上げ_lpppszadrtypearray_パラメーターによって指定された配列内のエントリの数へのポインター。 
    
 _lpppszadrtypearray_
  
> 読み上げ受信者の種類を識別する文字列の配列へのポインターへのポインター。
    
 _lpcMAPIUID_
  
> 読み上げ_lpppuidarray_パラメーターによって指定された配列内のエントリの数へのポインター。 
    
 _lpppuidarray_
  
> 読み上げ受信者の種類を識別する[MAPIUID](mapiuid.md)構造体へのポインターの配列へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> トランスポートプロバイダーは、処理できる受信者の種類を正常に指定しました。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI スプーラーは、トランスポートプロバイダーが、トランスポートプロバイダーが処理する受信者の種類を示すことができるように、トランスポートプロバイダーが[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)メソッドへの呼び出しから戻るときに、 **IXPLogon:: AddressTypes**メソッドを呼び出します。 これを示すために、トランスポートプロバイダーは_lpppszadrtypearray_パラメーターに戻り、文字列へのポインターの配列へのポインターを渡すか、 _lpppuidarray_パラメーターで**MAPIUID**へのポインターの配列へのポインターを返す必要があります。構造体、または両方のパラメーターの値を渡します。 
  
これら2つの配列は、さまざまな識別プロセスに使用されます。 mapi および mapi スプーラーは、 _lpppuidarray_配列の[MAPIUID](mapiuid.md)構造体を使用して、トランスポートプロバイダーまたはトランスポートプロバイダーが接続するメッセージングシステムによって直接処理される受信者エントリ識別子を識別します。. mapi または mapi スプーラーは、これらの**MAPIUID**構造に含まれるエントリ識別子を使用してアドレスを展開しません。これらの構造体は、受信者の種類の識別にのみ使用されます。 
  
MAPI スプーラーは、出力メッセージの受信者を処理する必要があるトランスポートプロバイダーを決定するときに、 _lpppszadrtypearray_パラメーターの各文字列を使用して比較テストを行います。 メッセージ受信者の**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティが、トランスポートプロバイダーが提供するメッセージングアドレスの種類のいずれかを識別する文字列と正確に一致する場合、プロバイダーはその受信者にメッセージを配信できます。
  
複数のトランスポートプロバイダーが同じ種類の受信者を処理できる場合、MAPI はクライアントアプリケーションのプロファイルに示されているトランスポート優先順位に基づいてトランスポートプロバイダーを選択します。 使用するトランスポートプロバイダーを決定するために、MAPI スプーラーは、プロバイダーによって指定されたすべての**MAPIUID**構造を優先順位に従ってスキャンし、次に、プロバイダー指定のすべてのアドレスの種類の値を優先順にスキャンします。 このスキャンの特定の受信者に一致する最初のトランスポートプロバイダーは、この受信者を最初に処理する機会を取得します。 そのプロバイダーが受信者を処理しない場合、MAPI スプーラーはスキャンを続行して、まだ処理されていない受信者のトランスポートプロバイダーを検索します。 スキャンは、それ以上一致が見つからない限り続行され、その時点で、処理されていない受信者に対して配信不能レポートが生成されます。 
  
プロバイダーが常に特定の受信者の種類のセットをサポートしている場合、トランスポートプロバイダーが渡されたアドレスの種類と**MAPIUID**配列は静的になることができます。 トランスポートプロバイダーが動的にこれらの配列を構築する場合は、以前は**transportlogon**への呼び出しで渡された support オブジェクトを使用してメモリを割り当てることができますが、これは必須ではありません。
  
アドレスの種類と**MAPIUID**の配列に使用されるメモリは、 [IXPLogon:: transportlogoff](ixplogon-transportlogoff.md)メソッドへの最後の呼び出しまで割り当てられたままになります。その時点で、トランスポートプロバイダーは必要に応じてメモリを解放できます。 トランスポートプロバイダーは、 **transportlogoff**呼び出しから戻った後、これらの配列の内容を変更しないでください。 
  
任意の種類の受信者を処理できるトランスポートプロバイダーは、 _lpppszadrtypearray_パラメーターで NULL を返すことができます。 中央サーバーを使用して、さまざまな外部メッセージシステムに送信メッセージを配信する、LAN ベースのメッセージングシステムのトランスポートプロバイダーは、一般的にこれを行います。 この種類のトランスポートプロバイダーは、プロファイルのトランスポートプロバイダーの mapi および mapi スプーラーの優先順位に従って、最後にインストールする必要があります。 
  
アドレスの種類に基づいて送信される送信メッセージをサポートしていないトランスポートプロバイダーは、 _lpppszadrtypearray_に1つの長さ0の文字列を返します。 トランスポートプロバイダーが受信者の種類をサポートしていない場合は、 **MAPIUID**構造体に NULL を渡す必要があります。また、アドレスの種類には空の文字列を渡します。 この種類のトランスポートプロバイダーは、メッセージプリプロセッサをインストールするために最もよく使用されます。 
  
## <a name="see-also"></a>関連項目



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

