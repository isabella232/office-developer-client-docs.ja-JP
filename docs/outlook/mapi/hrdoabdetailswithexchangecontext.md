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
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347853"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
必要な Exchange アドレス帳プロバイダーが**openentry**メソッドを開いていることを確認します。 この関数は[IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが、 _pEmsmdbUID_パラメーターによって識別される Exchange アドレス帳を使用して**entryID**を開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp .h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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
  
> ログオンしている**imapisession**。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> エントリ id を開くために関数によって使用される exchange アドレス帳プロバイダーを含む exchange サービスを識別する**emsmdbUID**へのポインター。 受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数は[IAddrBook:: openentry](iaddrbook-openentry.md)と同様に動作します。 このパラメーターが NULL またはゼロ**MAPIUID**の場合は、この関数も[IAddrBook:: openentry](iaddrbook-openentry.md)と同じように動作します。 
    
 _pAddrBook_
  
> 順番エントリ識別子を開くために使用されるアドレス帳。 NULL にすることはできません。
    
 _l出 uiparam_
  
> 読み上げダイアログボックスの親ウィンドウへのハンドル。
    
 _lpfnDismiss_
  
> 順番**DISMISSMODELESS**プロトタイプに基づく関数へのポインター、または NULL。 このメンバーは、DIALOG_SDI フラグが設定されている場合のように、ダイアログボックスのモードレスバージョンにのみ適用されます。 MAPI は、ユーザーがモードレスアドレスダイアログボックスを閉じたときに、そのダイアログボックスがアクティブでなくなったことを示す詳細を呼び出していることをクライアントに通知する**DISMISSMODELESS**関数を呼び出します。 
    
 _lpvDismissContext_
  
> 順番_lpfnDismiss_パラメーターが指す**DISMISSMODELESS**関数に渡すコンテキスト情報へのポインター。 このパラメーターは、 **DIALOG_SDI**フラグを_ulflags_パラメーターに含めることによって、ダイアログボックスのモードレスバージョンにのみ適用されます。 
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。 
    
 _lて tryid_
  
> 順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。
    
 _lpfbuttoncallback_
  
> 順番**LPFNBUTTON**関数プロトタイプに基づく関数へのポインター。 **LPFNBUTTON**関数は、[詳細] ダイアログボックスにボタンを追加します。 
    
 _lpvbuttoncontext_
  
> 順番_lpfbuttoncallback_パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。 
    
 _lpszbuttontext_
  
> 順番追加されたボタンに適用されるテキストを含む文字列へのポインター。ボタンが拡張可能な場合です。 拡張ボタンを必要としない場合は、 _lpszbuttontext_パラメーターを NULL に設定する必要があります。 
    
 _ulFlags_
  
> 順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
AB_TELL_DETAILS_CHANGE
  
> 住所に変更が実際に加えられた場合に、詳細が TRUE を返すことを示します。それ以外の場合、詳細は FALSE を返します。
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。 このフラグは、DIALOG_SDI とは相互に排他的です。
    
DIALOG_SDI
  
> [共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。 このフラグは、DIALOG_MODAL とは相互に排他的です。
    
MAPI_UNICODE
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    

