---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426682"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**OpenEntry** メソッドが、予想されるアドレス帳プロバイダーによって開Exchange確認します。 この関数は [IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが _、pEmsabpUID_ で識別される Exchange アドレス帳を使用して **entryID** を開きます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]この関数は、エントリ識別子の詳細を表示するためにExchangeアドレス帳プロバイダーを識別する _emsabpUID_ へのポインターです。 受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D](iaddrbook-details.md)とまったく同じ動作をします。 このパラメーターが NULL または 0 の MAPIUID の場合、この関数は [IAddrBook::D同様に動作します](iaddrbook-details.md)。
    
 _pAddrBook_
  
> [in]エントリ識別子を開くのに使用するアドレス帳。 NULL にすることはできません。
    
 _lpulUIParam_
  
> [out]ダイアログ ボックスの親ウィンドウへのハンドル。
    
 _lpfnDismiss_
  
> [in] **DISMISSMODELESS** プロトタイプまたは NULL に基づく関数へのポインター。 このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。 MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ、ダイアログ ボックスがアクティブでなくなった詳細を呼び出しているクライアントに通知するときに **DISMISSMODELESS** 関数を呼び出します。 
    
 _lpvDismissContext_
  
> [in]_lpfnDismiss_ パラメーターが指す **DISMISSMODELESS** 関数に渡すコンテキスト情報へのポインター。 このパラメーターは _、ulFlags_ パラメーターに DIALOG_SDIを含めて、ダイアログ ボックス **のモードレス** バージョンにのみ適用されます。 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。 
    
 _lpEntryID_
  
> [in]開くアドレス帳エントリを表すエントリ識別子へのポインター。
    
 _lpfButtonCallback_
  
> [in] **LPFNBUTTON 関数プロトタイプに基づく関数への** ポインター。 **LPFNBUTTON 関数は**、詳細ダイアログ ボックスにボタンを追加します。 
    
 _lpvButtonContext_
  
> [in]  _lpfButtonCallback_ パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。 
    
 _lpszButtonText_
  
> [in]追加されたボタンに適用するテキストを含む文字列へのポインター (そのボタンが拡張可能な場合)。 _拡張可能ボタンが不要な場合、lpszButtonText_ パラメーターは NULL である必要があります。 
    
 _ulFlags_
  
> [in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
AB_TELL_DETAILS_CHANGE
  
> アドレスに実際に変更が加えた場合、Details は TRUE を返します。それ以外の場合、Details は FALSE を返します。
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。 このフラグは、このフラグと相互にDIALOG_SDI。
    
DIALOG_SDI
  
> [共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。 このフラグは、他のフラグと相互DIALOG_MODAL。
    
MAPI_UNICODE
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    

