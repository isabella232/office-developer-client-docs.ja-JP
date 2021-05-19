---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421369"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**OpenEntry** メソッドが、予想されるアドレス帳プロバイダーによって開Exchange確認します。 この関数は [IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが _、pEmsmdbUID_ パラメーターで識別される Exchange アドレス帳を使用して **entryID** を開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> ログオンしている **IMAPISession**。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> エントリ識別子を開く関数で使用される Exchange アドレス帳プロバイダーを含む Exchange Service を識別する **emsmdbUID** へのポインター。 受信エントリ識別子がアドレス帳プロバイダー Exchange識別子ではない場合、このパラメーターは無視され、関数は[IAddrBook::OpenEntry のように動作します](iaddrbook-openentry.md)。 このパラメーターが NULL または 0 **の MAPIUID** の場合、この関数は [IAddrBook::OpenEntry とまったく同じ動作をします](iaddrbook-openentry.md)。 
    
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
    

