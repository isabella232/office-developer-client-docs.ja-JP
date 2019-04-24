---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347804"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Exchange 2007 サーバーの自動検出サービスから取得された情報を表す、拡張マークアップ言語 (XML) ストリームを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|エクスポート対象:  <br/> |olmapi32  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>パラメーター

 _pwzAddress_
  
> 順番自動検出情報を取得するアカウントの、null で終了する簡易メール転送プロトコル (SMTP) 電子メールアドレス。
    
 _pwzPassword_
  
> 順番_pwzAddress_によって指定されたアカウントのパスワード (省略可能)。 _pwzAddress_で指定されたアカウントがパスワードを必要としない場合、任意のパスワードを渡しても効果はありません。 
    
 _hcancelevent_
  
> 順番省略可能で、操作を取り消すために使用できる、未設定の Win32 イベントハンドル。 操作を取り消すには、イベントを設定し、イベントハンドルを_hcancelevent_として渡します。操作をキャンセルしない場合は、 **null**を渡します。 イベントハンドルを表さない値を渡すと、無効になり、関数は無視されます。 
    
 _ulFlags_
  
> 順番このパラメーターは使用されません。 0である必要があります。
    
 _ppxmlstream_
  
> 読み上げautodiscovery XML を含む[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトへのポインター。 autodiscovery 操作が失敗した場合は**null**を返します。 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトの使用が終了したら解放する必要があります。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数呼び出しが成功しました。
    
E_INVALIDARG 
  
-  _pwzAddress_が**null**であるか、有効な SMTP アドレスではありません。または、 _ppxmlstream_は[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトへの**null**ポインターです。 
    
MAPI_E_NOT_FOUND 
  
- クライアントコンピューターがネットワークに接続されていない、クライアントコンピューターが Microsoft exchange 2007 サーバーに接続されていない、 _pwzAddress_が exchange 2007 サーバーのアカウントではない、または exchange をサポートしていないアカウントである_pwzAddress_自動検出サービス。 
    
MAPI_E_USER_CANCEL 
  
- 操作をキャンセルするため、 _hcancelevent_にイベントハンドルが渡されました。 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- _pwzAddress_または_pwzPassword_に渡された値が長すぎるため、サイズ256バイトの内部バッファーがオーバーフローしています。 
    

