---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cb4f38615ac6cacb3acbaa456f0992bf55c3653d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568624"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**OpenEntry**メソッドが必要な Exchange のアドレス帳プロバイダーで開かれているようにします。 この関数は、 [IAddrBook::Details](iaddrbook-details.md)と同様に動作しますが、 _pEmsabpUID_で識別される、Exchange アドレス帳を使用して**エントリ Id**を表示します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _pEmsabpUID_
  
> [in]Exchange アドレス帳プロバイダーを識別する_emsabpUID_へのポインターのエントリ id の詳細を表示するのにはこの関数を使用する必要があります。 受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子ではない場合は、このパラメーターは無視され、 [IAddrBook::Details](iaddrbook-details.md)関数の呼び出しの動作とまったく同じです。 このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数はまた[IAddrBook::Details](iaddrbook-details.md)と同様に機能します。
    
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
    

