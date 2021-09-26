---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b3803a416f81a47f01532ac865df93135cc6420
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610798"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Exchange 2007 サーバーの自動検出サービスから取得された情報を表す拡張可能マークアップ言語 (XML) ストリームを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |olmapi32.dll  <br/> |
|呼び出し元:  <br/> |Client  <br/> |
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
  
> [in]自動検出情報を取得するアカウントの NULL 終端の簡易メール転送プロトコル (SMTP) 電子メール アドレス。
    
 _pwzPassword_
  
> [in]  _pwzAddress_ で指定されたアカウントのオプションのパスワードです。 _pwzAddress_ で指定されたアカウントにパスワードが必要ない場合、パスワードを渡しても効果はありません。 
    
 _hCancelEvent_
  
> [in]オプションであり、操作をキャンセルするために使用できる、設定されていない Win32 イベント ハンドル。 操作をキャンセルするには、イベントを設定し、イベント ハンドルを  _hCancelEvent として渡します_。操作 **をキャンセル** しない場合は null を渡します。 イベント ハンドルを表す値を渡しても効果が無く、関数によって無視されます。 
    
 _ulFlags_
  
> [in]このパラメーターは使用されません。 0 である必要があります。
    
 _ppXmlStream_
  
> [out]自動検出 XML を含む [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) オブジェクトへのポインター。 自動検出 **操作が失敗** した場合は null を返します。 [終了したら、IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを解放する必要があります。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数呼び出しが成功しました。
    
E_INVALIDARG 
  
-  _pwzAddress は_ **null** か、有効な SMTP アドレスではないか _、ppXmlStream_ は [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトへの **null** ポインターです。 
    
MAPI_E_NOT_FOUND 
  
- クライアント コンピューターがネットワークに接続されていない、クライアント コンピューターが Microsoft Exchange 2007 サーバーに接続されていない _、pwzAddress_ が Exchange 2007 サーバー上のアカウントではない、または _pwzAddress_ が Exchange 自動検出サービスをサポートしていないアカウントです。 
    
MAPI_E_USER_CANCEL 
  
- 操作を取り消すイベント ハンドルが  _hCancelEvent_ に渡されています。 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- _pwzAddress_ または _pwzPassword_ に渡される値が長すぎるので、サイズ 256 バイトの内部バッファーがオーバーフローします。 
    

