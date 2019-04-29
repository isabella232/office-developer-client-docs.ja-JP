---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409546"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
hropenabentrywithprovideruid 関数と同じ機能を実行します。ただし、 **hroentryabentrywithprovideruidsupport**関数は、セッションとアドレス帳を使用するのではなく、指定されたサポートオブジェクトを使用してエントリを開きます。 [](hropenabentrywithprovideruid.md) 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp .h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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
  
> 順番この関数がエントリ識別子の詳細を表示するために使用する Exchange アドレス帳プロバイダーを識別する_emsabpUID_パラメーターへのポインター。 入力されたエントリ識別子が Exchange アドレス帳プロバイダーのエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D etails](iaddrbook-details.md)と同じように動作します。 このパラメーターが NULL またはゼロ MAPIUID の場合は、この関数も[IAddrBook::D etails](iaddrbook-details.md)と同じように動作します。
    
 _lpsup_
  
> 
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。 
    
 _lて tryid_
  
> 順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。
    
 _lpinterface_
  
> 順番開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイスが返されます。 メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。 配布リストの場合、これは[idistlist: IMAPIContainer](idistlistimapicontainer.md)で、コンテナーの場合は[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)です。 呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。 
    
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
    
 _lpulobjtype_
  
> 読み上げ開かれた項目の種類へのポインター。
    
 _lppunk_
  
> 読み上げ開かれたエントリのポインターへのポインター。
    

