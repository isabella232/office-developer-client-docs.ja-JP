---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cb6138072cd5dedc528168d4056041661c40fd06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800298"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**適用対象**: Outlook 
  
**OpenEntry**メソッドが必要な Exchange のアドレス帳プロバイダーで開かれているようにします。 この関数は、 [IAddrBook::Details](iaddrbook-details.md)と同様に動作しますが、 _pEmsmdbUID_パラメーターで指定された Exchange のアドレス帳を使用して**エントリ Id**を表示します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a>パラメーター

 _pmsess_
  
> **IMAPISession**にログオンします。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> 開くには、エントリの識別子、関数で使用される Exchange アドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。 受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数は、[アドレス帳コンテナー](iaddrbook-openentry.md)のように動作します。 このパラメーターが NULL またはゼロの**MAPIUID**の場合は、この関数は、[アドレス帳コンテナー](iaddrbook-openentry.md)と同じようにも機能します。 
    
 _pAddrBook_
  
> [in]アドレス帳のエントリ id を開くために使用します。 NULL にすることはできません。
    
 _lpulUIParam_
  
> [out]ダイアログ ボックスの親ウィンドウへのハンドル。
    
 _lpfnDismiss_
  
> [in]**DISMISSMODELESS**のプロトタイプでは関数へのポインター。 このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。 MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じるときの詳細] ダイアログ ボックスがアクティブではないことを呼び出しているクライアントに通知します。 
    
 _lpvDismissContext_
  
> [in]_LpfnDismiss_パラメーターが指す、 **DISMISSMODELESS**関数に渡すコンテキスト情報へのポインターです。 このパラメーターは、 _ulFlags_パラメーターに**DIALOG_SDI**フラグを含めることで、モードレス ダイアログ ボックスのバージョンにのみ適用されます。 
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。
    
 _lpfButtonCallback_
  
> [in]**LPFNBUTTON**関数のプロトタイプでは関数へのポインター。 **LPFNBUTTON**関数では、[詳細情報] ダイアログ ボックスにボタンを追加します。 
    
 _lpvButtonContext_
  
> [in]_LpfButtonCallback_パラメーターで指定された関数のパラメーターとして使用されていたデータへのポインター。 
    
 _lpszButtonText_
  
> [in]そのボタンは拡張可能な場合、[追加] ボタンに適用するテキストを含む文字列へのポインター。 拡張ボタンが不要な場合、 _lpszButtonText_パラメーターは NULL である必要があります。 
    
 _ulFlags_
  
> [in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
AB_TELL_DETAILS_CHANGE
  
> 詳細は TRUE を返す場合は、アドレスに変更を加えた実際にことを示します。それ以外の場合、詳細は、FALSE を返します。
    
DIALOG_MODAL
  
> 共通のアドレス] ダイアログ ボックスのモーダル バージョンが表示されます。 このフラグは、DIALOG_SDI と相互に排他的です。
    
DIALOG_SDI
  
> モードレスのバージョンの共通のアドレス] ダイアログ ボックスが表示されます。 このフラグは、DIALOG_MODAL と相互に排他的です。
    
MAPI_UNICODE
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    

