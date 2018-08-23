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
ms.openlocfilehash: 490c834ee63c158b3f9c0e34f8de7f582c650bc4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584066"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
Microsoft Exchange 2007 サーバーの自動検出サービスから取得した情報を表す拡張マークアップ言語 (XML) のストリームを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |olmapi32.dll  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
   
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
  
> [in]Null で終わる簡易メール転送プロトコル (SMTP) メール アドレスの自動検出情報を取得するアカウントです。
    
 _pwzPassword_
  
> [in]オプションの_pwzAddress_で指定されたアカウントのパスワードです。 任意のパスワードを渡す意味を持ちません_pwzAddress_によって指定されたアカウントにパスワードが必要ない場合に注意してください。 
    
 _hCancelEvent_
  
> [in]設定されていない Win32 イベント ハンドルをオプションで、操作をキャンセルするために使用します。 操作をキャンセルするには、イベントを設定し、イベント ハンドルを渡すと_hCancelEvent_。操作をキャンセルしたくない場合は**null**を渡します。 メモがある値を渡すことはありません、イベント ハンドルは、影響を与えません、関数では無視されます。 
    
 _ulFlags_
  
> [in]このパラメーターは使用されません。 0 である必要があります。
    
 _ppXmlStream_
  
> [out]自動検出の XML を含む[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)オブジェクトへのポインター。 自動検出が失敗した場合は**null**を返します。 操作を終了したら、 [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)オブジェクトを解放する必要があります。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数の呼び出しが成功します。
    
E_INVALIDARG 
  
-  _pwzAddress_が**null**か、有効な SMTP アドレスではありませんか_ppXmlStream_ [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)オブジェクトへの**null**ポインター。 
    
MAPI_E_NOT_FOUND 
  
- クライアント コンピューターがネットワークに接続されていない、Microsoft Exchange 2007 サーバーにクライアント コンピューターが接続されていない、 _pwzAddress_は、Exchange 2007 サーバー上のアカウントではありません、または_pwzAddress_は、Exchange でサポートされていないアカウント自動検出サービスです。 
    
MAPI_E_USER_CANCEL 
  
- イベント ハンドルは、操作をキャンセルするのには_hCancelEvent_に渡されました。 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- _PwzAddress_または_pwzPassword_に渡される値が長すぎます、256 バイトのサイズの内部バッファーがオーバーフローしたことなどです。 
    

