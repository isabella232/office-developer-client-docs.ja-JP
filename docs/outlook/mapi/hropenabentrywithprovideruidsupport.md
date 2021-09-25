---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ebf63e283d332fce73b13d4a12f071349f523f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576164"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)関数と同じ関数を実行しますが **、HrOpenABEntryWithProviderUIDSupport** 関数は、セッションとアドレス帳を使用する代わりに、指定されたサポート オブジェクトを使用してエントリを開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _pEmsabpUID_
  
> [in]この関数がエントリ識別子の詳細を表示するために使用するExchangeアドレス帳プロバイダーを識別する _emsabpUID_ パラメーターへのポインター。 受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D](iaddrbook-details.md)とまったく同じ動作をします。 このパラメーターが NULL または 0 の MAPIUID の場合、この関数は [IAddrBook::D同様に動作します](iaddrbook-details.md)。
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。 
    
 _lpEntryID_
  
> [in]開くアドレス帳エントリを表すエントリ識別子へのポインター。
    
 _lpInterface_
  
> [in]開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合は、オブジェクトの標準インターフェイスを返します。 メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。 配布リストの場合は [、IDistList : IMAPIContainer](idistlistimapicontainer.md)であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。 呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。 
    
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
    
 _lpulObjType_
  
> [out]開いたエントリの種類へのポインター。
    
 _lppUnk_
  
> [out]開いたエントリのポインターへのポインター。
    

